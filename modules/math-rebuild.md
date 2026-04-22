# Math Rebuild

Module spécial pour rattraper les maths : diagnostic des trous + carte de dépendances + parcours ordonné avec validation à chaque étape.

## Quand l'utiliser

- L'utilisateur dit *"je veux rattraper les maths"*, *"j'ai des trous"*, *"je dois apprendre les maths pour ML/finance/data"*
- Il a du mal avec un sujet avancé qui repose sur des fondations manquantes
- Il a plusieurs fois essayé des cours mais abandonne — signe que le niveau d'entrée est mal calibré

## Philosophie

Les maths sont un **graphe de dépendances** (A → B → C). Si A est faible, tenter B est inutile — tu vas tourner en rond. La plupart des gens échouent en maths non parce qu'ils sont "mauvais", mais parce qu'ils attaquent B sans avoir solidifié A.

Ce module fait une chose : **cartographier tes trous et définir le point d'entrée réel**, pas le point d'entrée fantasmé.

## Procédure

### Phase 1 — Cadrer l'objectif (3 min)

1. **Demander** : *"Pourquoi tu veux rattraper les maths ? Pour faire quoi concrètement ?"*
2. Les objectifs typiques et leurs pré-requis réels :

| Objectif | Vrais pré-requis |
|---|---|
| Lire des papiers ML | Algèbre linéaire + calcul + probabilités de base |
| Trader en options | Probabilités + stats + un peu de calcul différentiel |
| Comprendre la crypto / chiffrement | Arithmétique modulaire + théorie des groupes (base) |
| Passer un concours / diplôme | Programme officiel — variable |
| Maths "générales" pour culture | Lycée solide suffit souvent |

3. **Nommer les pré-requis** réels de l'objectif.
4. Si l'objectif est flou → creuser avant de planifier.

### Phase 2 — Diagnostic en 4 niveaux (10 min)

La skill propose **des questions de test** par niveau, de plus en plus difficile. L'utilisateur répond. La skill identifie le niveau exact de trou.

#### Niveau 1 — Fondations collège
- *"Résous : 2x + 5 = 13"*
- *"Combien font 3/4 + 1/6 ?"*
- *"Quelle est l'aire d'un cercle de rayon 5 ?"*

Si trou ici → remonter ici avant de continuer. C'est critique mais pas honteux.

#### Niveau 2 — Lycée (seconde/première)
- *"Dérive f(x) = 3x² + 2x - 1"*
- *"Résous x² - 5x + 6 = 0"*
- *"Qu'est-ce qu'une fonction exponentielle, concrètement ?"*

#### Niveau 3 — Lycée avancé (terminale)
- *"Calcule l'intégrale de x² entre 0 et 2"*
- *"Qu'est-ce qu'une variable aléatoire ?"*
- *"Multiplie les matrices [[1,2],[3,4]] et [[5,6],[7,8]]"*

#### Niveau 4 — Post-bac
- *"Qu'est-ce qu'une valeur propre ? Comment la calculer ?"*
- *"Différence entre dérivée partielle et gradient ?"*
- *"Qu'est-ce que l'espérance conditionnelle ?"*

### Phase 3 — Cartographier les trous

5. **Identifier le niveau maîtrisé** vs **premier niveau en galère**.
6. **Nommer les concepts spécifiques** qui manquent, pas juste "niveau X".
7. Si l'utilisateur maîtrise 70% d'un niveau → pas besoin de tout refaire, juste combler les trous ciblés.

### Phase 4 — Proposer un parcours ordonné

8. **Parcours séquentiel obligatoire** : on ne saute pas une étape.
9. Pour chaque étape :
   - Concepts à maîtriser
   - Ressources recommandées (voir plus bas)
   - Exercices de validation
   - Temps estimé réaliste
10. **Validation avant passage** : on ne passe à l'étape N+1 que si on a validé N avec un test d'exercices.

### Phase 5 — Ressources recommandées (par niveau)

**Niveau 1-2 (fondations)** :
- [Khan Academy en français](https://fr.khanacademy.org) — gratuit, exercices illimités
- Livre : *Maths tout-en-un 2de* / *1re* (Hachette ou Nathan, collection "tout-en-un")

**Niveau 3 (terminale)** :
- [Khan Academy](https://fr.khanacademy.org) — chapitres terminale
- Chaîne YouTube : [Yvan Monka](https://www.youtube.com/@yvan_monka) — excellente pédagogie
- Livre : *Maths Terminale Spécialité* (collection tout-en-un)

**Niveau 4+ (post-bac pour ML/finance)** :
- [3Blue1Brown — Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) — intuition visuelle
- [3Blue1Brown — Essence of Calculus](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
- Livre : *Mathematics for Machine Learning* (Deisenroth, Faisal, Ong) — gratuit PDF sur mml-book.github.io
- Livre : *Think Stats* (Allen Downey) — gratuit, orienté pratique

**Note** : vérifier que les ressources sont encore accessibles et à jour — les liens peuvent changer.

### Phase 6 — Définir la cadence réaliste

11. **Ordres de grandeur honnêtes** :
    - Lycée solidifié (niveau 1+2+3) partant de trous : ~3-6 mois à 4h/semaine
    - Maths pour ML niveau intermédiaire : ~6-12 mois à 4h/semaine
    - Niveau prépa : 2-3 ans à temps plein
12. **Pas de fausse promesse.** Dire la vérité sur les durées, même si ça pique.

## Format de sortie

```markdown
# Math Rebuild — <ton nom / date>

## 🎯 Objectif réel
<pourquoi tu rattrapes les maths, formulé en capacité observable>

**Pré-requis mathématiques réels** : <liste des domaines nécessaires>

## 📊 Diagnostic (niveau détecté)

| Niveau | Status | Concepts OK | Concepts à revoir |
|---|---|---|---|
| 1 — Collège | ✅ / 🟡 / ❌ | <liste> | <liste> |
| 2 — 2de/1re | ✅ / 🟡 / ❌ | <liste> | <liste> |
| 3 — Terminale | ✅ / 🟡 / ❌ | <liste> | <liste> |
| 4 — Post-bac | ✅ / 🟡 / ❌ | <liste> | <liste> |

**Point d'entrée recommandé** : Niveau <N>, sujet <X>.

## 📍 Parcours ordonné

### Étape 1 — <nom> (~<N> semaines)
**Concepts** :
- <concept 1>
- <concept 2>

**Ressources** :
- <ressource précise 1>
- <ressource précise 2>

**Validation avant passage à l'étape 2** :
- [ ] Résoudre <N> exercices sur <sujet> sans regarder la correction
- [ ] Expliquer par écrit <concept clé> en 10 lignes

### Étape 2 — ...
...

## ⏱️ Cadence proposée
- <X>h / semaine
- Total estimé : <Y> semaines
- Date de revue : <date>

## ⚠️ Vérités honnêtes
- <ordre de grandeur réaliste — pas de sugar coating>
- <risque principal, ex: abandonner après 3 semaines si pas de feedback>
- <conseil : trouver un partenaire d'étude ou un tuteur humain pour les blocages profonds>

## 🔁 Checkpoint à mi-parcours
Date : <...>
Auto-test : pouvoir résoudre 5 exercices de niveau <N> en <durée>.

---

**Première action concrète (dans les 48h)** : <micro-action pour démarrer — souvent juste "faire le test de Khan Academy pour se situer">
```

## Règles dures

- **Pas de parcours qui saute des niveaux.** Si niveau 2 est fragile, on ne commence pas par le niveau 4 même si l'objectif y pointe.
- **Validation obligatoire à chaque étape.** Sans validation, l'utilisateur avance sur du sable.
- **Pas de ressources gratuites = pas de plan.** La skill ne recommande que des ressources accessibles (gratuites ou ouvrages disponibles), pas des cours à 500€ introuvables.
- **Vérité sur la durée.** Rattraper 10 ans de maths en 3 mois est impossible. Le dire.
- **Partenariat humain recommandé.** Les maths s'apprennent mieux avec quelqu'un à qui parler. Suggérer un tuteur, un pair, un groupe d'étude — la skill n'est pas un substitut.

## Piège classique

L'utilisateur refuse de faire le diagnostic parce que *"je sais déjà ce que je connais"*. Insister. Le point de blocage est presque toujours un niveau en dessous de celui qu'on croit.

Autre piège : l'utilisateur veut aller vite et saute les exercices. Résultat : il lit sans intégrer, abandonne au bout de 3 semaines. Les maths ne s'apprennent pas en lisant, elles s'apprennent en faisant — c'est non négociable.

## Signal rouge

Si pendant le diagnostic l'utilisateur montre :
- Forte anxiété autour des maths
- Histoire de "je suis nul en maths depuis toujours"
- Blocage émotionnel évident

→ Ne pas ignorer. L'anxiété mathématique est réelle et documentée. Recommander de chercher un accompagnement humain (tuteur, thérapeute spécialisé si vraiment fort), pas juste un plan.
