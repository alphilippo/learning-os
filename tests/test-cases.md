# Cas de test — learning-os

11 prompts pour valider la skill. Pour chacun : bon module routé, mécanisme de vérification inclus, pas de consommation passive encouragée.

## Comment tester

Pose chaque prompt à Claude avec la skill chargée. Vérifie pour chaque :
1. Le bon module est annoncé
2. La réponse inclut un **mécanisme de vérification** (question-test, livrable, checkpoint)
3. Les **sources externes sont nommées** précisément (pas "un bon livre")
4. Pas d'encouragement à la consommation passive

---

## Cas 1 — Démarrer un domaine (plan)

**Prompt** : *"Je veux apprendre le droit des sociétés dans les 3 prochains mois. Par où commencer ?"*

**Module attendu** : `learning-path-planner`
**Doit** : forcer un objectif observable, estimer le niveau de départ, proposer un plan avec checkpoints, nommer des ressources précises, inclure un projet final.

**Red flags** :
- Plan sans objectif observable ("mieux comprendre")
- Ressources génériques ("un bon livre de droit")
- Pas de checkpoints testables
- Promesse irréaliste (maîtrise en 3 mois)

---

## Cas 2 — Concept qui ne colle pas

**Prompt** : *"Je comprends rien aux options financières, j'ai lu 3 livres là-dessus."*

**Module attendu** : `concept-explainer`
**Doit** : diagnostiquer le pré-requis manquant (probablement "dérivée" ou "variable sous-jacente"), expliquer avec Feynman + analogie + limite, finir par question-test non-triviale.

**Red flags** :
- Explique sans diagnostic préalable
- Analogie sans limite
- Pas de question-test
- Donne la réponse de la question-test tout de suite

---

## Cas 3 — Session bloquée

**Prompt** : *"J'ai 1h. Je veux solidifier les probabilités conditionnelles."*

**Module attendu** : `study-session-designer`
**Doit** : livrable observable obligatoire, méthode d'active recall explicite, structure de blocs avec pauses, exercices précis fournis, wrap-up obligatoire.

**Red flags** :
- Session sans livrable observable
- "Juste lire le chapitre"
- Pas d'active recall
- Durée sans pause

---

## Cas 4 — Synthèse de multiples sources

**Prompt** : *"J'ai lu 6 articles sur l'effet Mozart et les bénéfices de la musique pour les bébés. Certains disent que c'est prouvé, d'autres que c'est un mythe. Aide-moi à y voir clair."*

**Module attendu** : `knowledge-synthesizer`
**Doit** : forcer une question centrale, inventorier les sources avec fiabilité nommée, distinguer consensus / divergences / angles morts, répondre avec niveau de confiance.

**Red flags** :
- Synthèse sans question centrale
- Fausse symétrie ("les deux camps ont des arguments")
- Pas de hiérarchie de fiabilité
- Pas de biais assumés

---

## Cas 5 — Rattrapage maths (objectif ML)

**Prompt** : *"Je veux rattraper les maths pour comprendre le deep learning. J'ai fait un bac L il y a 20 ans."*

**Module attendu** : `math-rebuild`
**Doit** : diagnostiquer (4 niveaux), identifier que bac L = très probable début niveau 2, nommer le vrai point d'entrée, parcours séquentiel, vérité sur les durées (6-12 mois minimum).

**Red flags** :
- Saute le diagnostic
- Propose directement un cours de "math for ML"
- Ordre de grandeur irréaliste ("en 3 mois c'est faisable")
- Ressources payantes > 100€ sans alternative gratuite

---

## Cas 6 — Rattrapage maths (avec signaux d'anxiété)

**Prompt** : *"Je veux apprendre les stats mais j'ai toujours été nul en maths. Je bloque à chaque fois, je sais pas pourquoi. Tout le monde y arrive sauf moi."*

**Module attendu** : `math-rebuild` + **signal rouge**
**Doit** : reconnaître les signaux d'anxiété mathématique ("toujours été nul", "tout le monde sauf moi"), ne pas ignorer, recommander un accompagnement humain en complément du plan.

**Red flags** :
- Ignore les signaux émotionnels
- Fait un plan standard sans mention de la dimension émotionnelle
- Sur-promesse rassurante type "tu vas y arriver !"

---

## Cas 7 — Objectif flou

**Prompt** : *"Je veux mieux comprendre l'économie."*

**Module attendu** : `learning-path-planner` mais **avec refus initial**
**Doit** : refuser de planifier tant que l'objectif n'est pas observable, demander *"pour faire quoi concrètement ?"*, proposer des reformulations.

**Red flags** :
- Accepte l'objectif flou et fait un plan
- Balance une liste de 20 livres

---

## Cas 8 — Sous-promesse dangereuse

**Prompt** : *"Je veux être expert en cryptographie en 1 mois, je bosse 2h par semaine."*

**Module attendu** : `learning-path-planner`
**Doit** : dire clairement que c'est impossible, proposer soit un scope plus restreint ("comprendre les bases de X en 1 mois"), soit une durée plus réaliste.

**Red flags** :
- Accepte la demande sans broncher
- Fait un plan ultra-dense qui échouera
- Ne dit pas la vérité sur les ordres de grandeur

---

## Cas 9 — Concept simple

**Prompt** : *"C'est quoi vraiment un logarithme ?"*

**Module attendu** : `concept-explainer`
**Doit** : expliquer avec Feynman (pas "c'est l'inverse de l'exponentielle" version jargon), analogie concrète, exemple numérique, question-test.

**Red flags** :
- Définition circulaire
- Pas d'analogie
- Pas d'exemple numérique
- Pas de question-test

---

## Cas 10 — Après test fait

**Prompt** : *"J'ai passé le test de Khan Academy que tu m'as dit de faire. J'ai eu 65% en terminale mais 30% en 1re. Qu'est-ce que ça veut dire ?"*

**Module attendu** : `math-rebuild` (adaptation)
**Doit** : interpréter le résultat (1re fragile → refonder ce niveau avant terminale), ajuster le parcours en conséquence, ne pas ignorer le paradoxe (30% en 1re mais 65% en terminale = pièces détachées sans base).

**Red flags** :
- Suppose que le niveau est "entre les deux"
- N'ajuste pas le plan
- Ignore la fragilité du niveau 1re

---

## Cas 11 — Composition avec thinking-os

**Prompt** : *"J'hésite entre apprendre le Python ou apprendre le R pour faire de la data science. Je sais pas lequel choisir."*

**Module attendu** : **PAS `learning-os`** — c'est une décision, pas un apprentissage.
**Doit** : reconnaître que c'est une question pour `thinking-os` (`opportunity-cost`), rediriger poliment plutôt que faire un plan sur les deux.

**Red flags** :
- Fait un plan d'apprentissage sur Python
- Ou un plan sur R
- Sans d'abord aider à trancher entre les deux

---

## Critères de validation globaux

La skill est validée si :

- ✅ **9/11** cas routent sur le bon module
- ✅ **100%** des sorties incluent un mécanisme de vérification
- ✅ **100%** des ressources sont nommées précisément
- ✅ **0%** de "consommation passive" encouragée (lecture seule sans active recall)
- ✅ Le cas 6 (anxiété maths) déclenche **bien** le signal rouge
- ✅ Les cas 7, 8 (objectif flou / sous-promesse dangereuse) **refusent** correctement

Si plusieurs échecs :
- Routage → revoir la table dans SKILL.md
- Pas de vérification → durcir section "Règles dures" du module concerné
- Sources vagues → ajouter l'exigence explicite dans le module
