# learning-os

![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-Apache%202.0-green) ![Claude](https://img.shields.io/badge/Claude-Skill-purple)

🌍 **Français** · **[English](README.en.md)**

> Système d'apprentissage pour Claude : transforme la curiosité en maîtrise via 5 modules qui insistent sur la vérification plutôt que la consommation.

## Ce que ça fait

La plupart des gens confondent **exposition** et **maîtrise**. Ils lisent un livre, regardent une vidéo, et croient avoir appris. Ils n'ont rien appris — ils ont consommé.

`learning-os` applique 4 principes durs :

1. **Pas de plan sans test de sortie** — chaque plan inclut des checkpoints où tu prouves ce que tu sais
2. **Pas d'explication sans question de contrôle** — chaque concept expliqué se termine par une question-test
3. **Pas de session sans livrable observable** — exercices résolus, concept expliqué par écrit, code qui tourne
4. **Pas d'analogie sans sa limite** — les analogies sont utiles mais dangereuses ; la skill nomme toujours où elles cassent

## Les 5 modules

| Module | Quand l'utiliser |
|---|---|
| **Learning Path Planner** | Démarrer un domaine sur 1-3 mois |
| **Concept Explainer** | Bloquer sur un concept précis |
| **Study Session Designer** | Session 30-90 min avec objectif |
| **Knowledge Synthesizer** | Synthétiser plusieurs sources |
| **Math Rebuild** | Rattrapage maths avec diagnostic |

## Déclencheurs

La skill se déclenche automatiquement quand tu dis :
- *"Je veux apprendre X"*, *"par où commencer"* → Learning Path Planner
- *"Explique-moi X"*, *"je comprends pas X"*, *"c'est quoi X vraiment"* → Concept Explainer
- *"J'ai 1h pour étudier"*, *"session sur X"* → Study Session Designer
- *"Synthétise ces sources"*, *"j'ai lu plusieurs articles sur X"* → Knowledge Synthesizer
- *"Je veux rattraper les maths"*, *"j'ai des trous en maths"* → Math Rebuild

## Skills complémentaires (écosystème complet)

- 🧠 [**thinking-os**](https://github.com/alphilippo/thinking-os) — routeur cognitif
- ⚙️ [**execution-os**](https://github.com/alphilippo/execution-os) — système d'exécution
- 📚 [**learning-os**](https://github.com/alphilippo/learning-os) — système d'apprentissage
- ⚔️ [**strategy-intel**](https://github.com/alphilippo/strategy-intel) — analyse stratégique
- 🧭 [**alignment-os**](https://github.com/alphilippo/alignment-os) — alignement personnel

Les 5 répondent à des questions différentes :
- `thinking-os` — **QUOI** faire (cadre de pensée)
- `execution-os` — **COMMENT** le faire (cadence)
- `learning-os` — **APPRENDRE** à le faire (montée en compétence)
- `strategy-intel` — **OÙ & CONTRE QUI** le faire (positionnement)
- `alignment-os` — **POURQUOI** le faire (cohérence vie/valeurs)

## Installation

### Claude.ai

1. Télécharge le ZIP depuis GitHub (Code → Download ZIP) ou clone le repo
2. Assure-toi que la structure ZIP contient le dossier `learning-os/` à la racine (pas les fichiers directement)
3. Dans Claude.ai : Settings → Skills → "+" → "+ Create skill" → upload le ZIP
4. Toggle la skill ON

### Claude Code

```bash
cp -r learning-os ~/.claude/skills/
```

### API Claude

Package en `.skill` et upload via l'endpoint `/skills`. Voir la [doc officielle](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview).

## Exemples

### Rattrapage maths
> *"Je veux rattraper les maths pour comprendre les papiers de ML. Bac S il y a 15 ans, j'ai tout oublié."*

→ La skill force un **diagnostic 4 niveaux** avant de planifier, identifie le vrai point d'entrée (souvent plus bas que ce que l'utilisateur pense), propose un parcours séquentiel 6 mois avec ressources gratuites précises (Khan Academy, 3Blue1Brown, *Mathematics for Machine Learning*).

### Explication d'un concept flou
> *"Je comprends pas ce que c'est une valeur propre."*

→ La skill **diagnostique le pré-requis manquant** (souvent l'intuition des transformations linéaires), explique avec analogie + exemple numérique + limites, termine par une question-test à laquelle elle ne donne pas la réponse.

### Session bloquée
> *"J'ai 1h30 pour solidifier les dérivées partielles, j'ai lu 2 chapitres mais ça rentre pas."*

→ La skill identifie le **problème de méthode** (exposition sans active recall), structure une session avec blank page recall + exercices précis + livrable observable (document d'1 page).

## Structure

```
learning-os/
├── SKILL.md                         # Métadonnées + routeur
├── README.md                        # Ce fichier (français)
├── README.en.md                     # Version anglaise
├── modules/
│   ├── learning-path-planner.md
│   ├── concept-explainer.md
│   ├── study-session-designer.md
│   ├── knowledge-synthesizer.md
│   └── math-rebuild.md
├── templates/
│   ├── learning-plan-template.md
│   ├── concept-card-template.md
│   ├── study-session-template.md
│   ├── synthesis-template.md
│   └── math-diagnostic-template.md
├── examples/
│   ├── math-rebuild-example.md
│   ├── concept-explainer-example.md
│   └── study-session-example.md
└── tests/
    └── test-cases.md                # 11 cas de validation
```

## Philosophie

- **Progressive disclosure** : le SKILL.md ne contient que le routeur.
- **Pas de consommation passive** : la skill refuse de produire un simple résumé sans test.
- **Sources externes nommées** : pas "un bon livre", toujours un titre/auteur/plateforme précis.
- **Artefacts exportables** : chaque output est un markdown structuré que tu peux sauvegarder.
- **Humilité** : la skill ne remplace pas la pratique réelle (exercices, projets, feedback humain) ni un tuteur humain.

## Limites

- Pas de mémoire entre sessions — il faut ré-injecter tes plans/notes
- Ne remplace pas la pratique (exercices, projets, feedback)
- Les ressources recommandées peuvent dater (à vérifier)
- Certaines ressources clés sont anglophones
- Pour les maths, un tuteur humain reste fortement recommandé en complément sur les blocages profonds

## Roadmap

- **v1.0** (actuel) : 5 modules + 5 templates + routage
- **v1.1** : **Spaced repetition helper** (module pour générer des flashcards Anki à partir des concept cards)
- **v1.2** : **Research mode** (module pour apprendre en profondeur un papier de recherche)
- **v1.3** : **Language learning** (module spécifique apprentissage langues)
- **v2.0** : **Progress tracker** qui se souvient entre sessions via un fichier status exporté

## Licence

Apache 2.0 — fork, adapte, republie.

## Crédits

Conçu avec Claude comme Skill Architect. Inspiré par la méthode Feynman, Anders Ericsson (deliberate practice), Peter Brown (*Make It Stick*), et 3Blue1Brown (intuition visuelle en maths).
