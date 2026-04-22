# Exemple 1 — Math Rebuild pour ML

**Prompt utilisateur** :
> *"Je veux rattraper les maths pour comprendre les papiers de ML. J'ai fait un bac S il y a 15 ans, j'ai tout oublié. Par où je commence ?"*

---

## Ce que la skill fait

**Détection** : *"rattraper les maths"* + objectif ML → module `math-rebuild` immédiat.

**Signal à relever** : "bac S il y a 15 ans" + "j'ai tout oublié" → très probable que le niveau 2 (lycée) soit fragile, pas juste le niveau 4.

---

## Sortie

📚 **Module : Math Rebuild**

Avant de te proposer un plan, il faut faire un diagnostic rapide. Tu sous-estimes probablement tes trous ou tu les surestimes — dans les deux cas, on perd du temps si on ne vérifie pas.

## Objectif réel

Lire et comprendre des papiers de ML. Les pré-requis réels :
- **Algèbre linéaire** : vecteurs, matrices, produit matriciel, valeurs propres, décompositions
- **Calcul différentiel** : dérivées, dérivées partielles, gradient, règle de la chaîne
- **Probabilités & stats** : variables aléatoires, espérance, variance, distributions courantes, théorème de Bayes
- **Calcul** (un peu) : intégrales simples, séries

**Bonne nouvelle** : pas besoin de maths prépa complètes. Un niveau "post-bac orienté ML" suffit pour 80% des papiers accessibles.

## Diagnostic (réponds honnêtement aux 12 questions)

### Niveau 1 — Collège
1. Résous : 2x + 5 = 13
2. Calcule 3/4 + 1/6 (fraction irréductible)
3. Aire d'un cercle de rayon 5 (valeur exacte) ?

### Niveau 2 — 2de/1re
4. Dérive f(x) = 3x² + 2x - 1
5. Résous x² - 5x + 6 = 0
6. Qu'est-ce qu'une fonction exponentielle ? (1 phrase)

### Niveau 3 — Terminale
7. Calcule l'intégrale de x² entre 0 et 2
8. Qu'est-ce qu'une variable aléatoire ? (1 phrase)
9. Multiplie [[1,2],[3,4]] × [[5,6],[7,8]]

### Niveau 4 — Post-bac
10. Qu'est-ce qu'une valeur propre et comment la calculer ?
11. Différence entre dérivée partielle et gradient ?
12. Qu'est-ce que l'espérance conditionnelle ?

**Réponds par :**
- ✅ si tu connais sans hésiter
- 🟡 si tu devines / te souviens vaguement
- ❌ si tu ne sais plus

Ne triche pas. Ne Google pas. Réponds ce que tu sais *maintenant*.

---

## [L'utilisateur répond]

> *"Niveau 1 : ✅✅✅ (trop facile)*
> *Niveau 2 : ✅✅🟡 (dérivée OK, second degré OK, exponentielle je sais plus trop c'est quoi vraiment)*
> *Niveau 3 : 🟡❌❌ (intégrale je me souviens du principe mais hésite, variable aléatoire aucune idée, produit matriciel j'ai oublié)*
> *Niveau 4 : ❌❌❌ (rien)"*

---

## Diagnostic final et parcours

# Math Rebuild — <utilisateur> — 21 avril 2026

## 🎯 Objectif réel
Lire et comprendre des papiers de ML de niveau intermédiaire.
**Pré-requis** : algèbre linéaire, calcul, probabilités & stats (niveau post-bac).

## 📊 Diagnostic

| Niveau | Status | Concepts OK | Concepts à revoir |
|---|---|---|---|
| 1 — Collège | ✅ | Tout | Rien |
| 2 — 2de/1re | 🟡 | Dérivée simple, second degré | **Exponentielle et logarithme** |
| 3 — Terminale | ❌ | — | **Intégrales, variables aléatoires, matrices** |
| 4 — Post-bac | ❌ | — | Tout |

**Point d'entrée réel** : Niveau 2, sujet "exponentielle et logarithme", puis TOUT le niveau 3 avant de toucher au niveau 4.

**Vérité qui pique** : tu vises niveau 4, mais ton point d'entrée réel est niveau 2. **Ignorer ce gap = abandonner dans 6 semaines.** Beaucoup de gens s'en vont direct sur "Mathematics for Machine Learning" et n'y comprennent rien parce qu'ils n'ont pas niveau 3.

## 📍 Parcours ordonné (6 mois à 4h/semaine)

### Étape 1 — Refonder niveau 2 (2 semaines)
**Concepts** : exponentielle, logarithme, suites (bases), trigonométrie rafraîchie.

**Ressources** :
- Khan Academy FR — section "exponentielle" et "logarithme" (niveau 1re)
- Yvan Monka sur YouTube — playlists correspondantes

**Validation** :
- [ ] Dériver `f(x) = e^(2x) × x`
- [ ] Résoudre `ln(x) + ln(x-1) = ln(6)`
- [ ] Expliquer en 5 lignes pourquoi on utilise la fonction exponentielle pour modéliser la croissance

### Étape 2 — Niveau 3 complet (6 semaines)
**Concepts** : intégrales (primitives, calcul d'aires), variables aléatoires (discrètes + continues), espérance/variance, loi normale, matrices (opérations de base, déterminant).

**Ressources** :
- Khan Academy FR — chapitres Terminale Spé
- *Maths Terminale Spécialité* (collection tout-en-un Hachette ou Nathan)
- 3Blue1Brown *Essence of Calculus* (anglais mais visuel) pour l'intuition des intégrales

**Validation** :
- [ ] Calculer `∫ (x² + 2x) dx` de 0 à 3
- [ ] Expliquer ce qu'est une variable aléatoire avec un exemple concret
- [ ] Multiplier 2 matrices 3x3 sans erreur
- [ ] Calculer l'espérance d'une VA discrète

### Étape 3 — Algèbre linéaire (8 semaines)
**Concepts** : espaces vectoriels (intuition), transformations linéaires, valeurs propres / vecteurs propres, produit scalaire, décompositions (SVD au moins conceptuellement).

**Ressources** :
- 3Blue1Brown *Essence of Linear Algebra* (priorité absolue — intuition visuelle irremplaçable)
- *Mathematics for Machine Learning* (Deisenroth et al.) — gratuit PDF sur mml-book.github.io — chapitres 2-4

**Validation** :
- [ ] Calculer les valeurs propres d'une matrice 2x2
- [ ] Expliquer en 10 lignes ce que fait géométriquement une transformation linéaire
- [ ] Décomposer une matrice 3x3 simple en valeurs singulières à la main

### Étape 4 — Calcul multivariable + optimisation (4 semaines)
**Concepts** : dérivées partielles, gradient, matrice jacobienne, chain rule multivariable, descente de gradient (intuition).

**Ressources** :
- *Mathematics for Machine Learning* chapitres 5-7
- 3Blue1Brown *Neural Networks* série (intuition backprop + gradient)

**Validation** :
- [ ] Calculer le gradient de `f(x,y) = x² + 3xy + y²`
- [ ] Expliquer la règle de la chaîne multivariable sur un exemple
- [ ] Implémenter une descente de gradient simple en Python

### Étape 5 — Probabilités avancées (4 semaines)
**Concepts** : probabilités conditionnelles, Bayes, distributions courantes (gaussienne multivariée), information mutuelle (bases).

**Ressources** :
- *Think Stats* (Allen Downey) — gratuit, orienté pratique Python
- *Mathematics for Machine Learning* chapitre 6

**Validation** :
- [ ] Appliquer Bayes à un problème non trivial
- [ ] Expliquer pourquoi la gaussienne multivariée est omniprésente en ML

## ⏱️ Cadence proposée

- 4h / semaine (2 × 2h en sessions deep work — voir `execution-os/deep-work-designer`)
- Total : **24 semaines ≈ 6 mois**
- Check-in à mi-parcours : **semaine 12** — tu dois valider la fin de l'étape 3

## ⚠️ Vérités honnêtes

1. **6 mois c'est l'optimiste.** Si tu rates 2-3 semaines, compte 7-8 mois. C'est normal.
2. **Les 2 premières étapes sont les plus ingrates.** Re-faire du lycée à 35+ ans, ça pique l'ego. Accepte-le ou tu abandonnes.
3. **Seul, c'est dur.** Cherche :
   - Un pair qui apprend aussi (Discord, Reddit r/learnmachinelearning)
   - Optionnel : tuteur humain 1h/semaine pour débloquer (forte valeur si budget)
4. **Pas de papier ML avant l'étape 3 finie.** Tu vas être frustré de ne pas lire les papiers tout de suite. Tiens bon — sinon tu gaspilles de l'énergie à lire sans comprendre.

## 🔁 Checkpoint mi-parcours (semaine 12)

Tu dois pouvoir sans aide :
- Calculer une intégrale simple
- Expliquer ce qu'est une valeur propre géométriquement
- Multiplier des matrices 3x3
- Expliquer la loi normale

Si ❌ à plus de 2/4 → tu avances trop vite, repasser sur les étapes faibles.

---

**Première action concrète (48h)** : fais le test de positionnement Khan Academy "Mathématiques au lycée" pour confirmer le diagnostic. ~30 min.

**Prochaine conversation** : partage-moi cette carte en début de session et dis-moi où tu en es. Je peux charger `concept-explainer` si tu bloques sur un concept précis, ou `study-session-designer` quand tu as une plage de temps.

---

## Commentaires sur la sortie

Ce qui fait que cet exemple fonctionne :

1. **Diagnostic avant plan** — la skill refuse de planifier sans avoir vérifié le niveau réel.
2. **Vérité sur le gap** — la skill dit clairement que l'utilisateur vise niveau 4 mais doit commencer niveau 2.
3. **Parcours séquentiel strict** — pas de shortcut, validation avant passage.
4. **Ressources nommées précisément** — Khan Academy, Yvan Monka, 3Blue1Brown, mml-book.github.io, pas de "un bon cours de maths".
5. **Cadence réaliste** — 6 mois à 4h/sem, et la skill dit que ça peut déborder à 7-8.
6. **Reconnaissance des aspects humains** — anxiété maths, ego, besoin de pairs, option tuteur.
7. **Composition avec autres skills** — renvoi explicite à `execution-os/deep-work-designer`.
8. **Prochaine action concrète en 48h** — pas de procrastination possible.
