# Exemple 2 — Concept Explainer : "Valeur propre"

**Prompt utilisateur** :
> *"Je comprends pas ce que c'est une valeur propre. J'ai lu 3 articles et regardé 2 vidéos, c'est toujours flou."*

---

## Ce que la skill fait

**Détection** : *"Je comprends pas"* + concept technique précis → `concept-explainer` immédiat.

**Signal** : l'utilisateur a déjà consommé plusieurs sources → ce n'est probablement pas un manque d'exposition, c'est un manque de **point d'entrée intuitif**. Les explications formelles ne collent pas parce que le pré-requis intuitif manque.

---

## Sortie

📚 **Module : Concept Explainer — "Valeur propre"**

Avant d'expliquer, une question : est-ce que tu comprends ce qu'est une **transformation linéaire** (géométriquement, ce que fait une matrice sur un vecteur) ?

- Si **oui** → on peut attaquer les valeurs propres directement.
- Si **non** → c'est le pré-requis manquant. Impossible de comprendre les valeurs propres sans ça. On commence par là.

*[L'utilisateur répond : "Je sais qu'une matrice multiplie un vecteur mais je visualise pas géométriquement ce qu'elle fait."]*

Exact. Voilà pourquoi les valeurs propres restent floues — tu n'as pas l'intuition géométrique des matrices. Je vais te donner cette intuition d'abord, puis les valeurs propres couleront.

---

# Explication — Transformation linéaire (pré-requis) + Valeur propre

## 🎯 En une phrase (niveau enfant de 10 ans)

Une matrice, c'est une **machine qui étire, écrase ou fait tourner l'espace**. Une valeur propre, c'est un **facteur d'étirement dans une direction qui ne change pas**.

## 🔍 Analogie

Imagine une feuille de papier que tu peux **étirer**, **compresser**, ou **faire pivoter**. Une matrice, c'est l'action que tu fais sur la feuille.

Maintenant, dessine quelques flèches sur cette feuille avant de la transformer. Après transformation :
- La plupart des flèches vont **changer de direction ET de taille**
- **Mais certaines flèches gardent leur direction** (elles pointent dans le même sens qu'avant, juste plus longues ou plus courtes)

Ces flèches "qui ne tournent pas" → ce sont les **vecteurs propres**.
Le facteur de combien elles sont étirées ou rétrécies → c'est la **valeur propre**.

**⚠️ Où cette analogie casse** : dans un vrai espace 3D ou plus, "faire tourner" et "étirer" se mélangent de façon non intuitive. Certaines matrices font des transformations qui n'ont pas d'équivalent papier simple (rotations complexes, projections). L'analogie marche parfaitement en 2D, devient imparfaite au-delà.

## 📐 Exemple concret

Prends la matrice :
```
A = [[3, 0],
     [0, 2]]
```

Cette matrice **étire par 3 horizontalement** et **par 2 verticalement**.

**Question** : quels vecteurs gardent leur direction quand on les multiplie par A ?

- Le vecteur `(1, 0)` (horizontal pur) → après transformation : `(3, 0)` → même direction, juste 3 fois plus long. ✅ **Vecteur propre, valeur propre = 3.**
- Le vecteur `(0, 1)` (vertical pur) → après : `(0, 2)` → même direction, 2 fois plus long. ✅ **Vecteur propre, valeur propre = 2.**
- Le vecteur `(1, 1)` (diagonal) → après : `(3, 2)` → **direction différente**. ❌ Pas un vecteur propre.

Donc pour cette matrice, il y a **2 valeurs propres (3 et 2)** avec chacune leur direction propre (horizontale et verticale).

**Calcul général** : pour trouver les valeurs propres d'une matrice `A`, tu résous :
```
det(A - λI) = 0
```
où `λ` (lambda) est l'inconnue. Les solutions sont les valeurs propres.

## 🧭 Pourquoi ce concept existe

Les valeurs propres sont partout où on veut comprendre **comment une transformation se comporte "dans le fond"**.

Exemples concrets :
- **En ML** : l'**ACP (Analyse en Composantes Principales)** trouve les directions dans lesquelles les données varient le plus — ce sont littéralement les vecteurs propres de la matrice de covariance.
- **En physique** : les modes de vibration d'une structure (pont, molécule) sont ses vecteurs propres — les fréquences propres sont les valeurs propres.
- **Google PageRank** : le classement des pages web est un problème de vecteur propre d'une matrice géante de liens.
- **En stats** : décomposer une matrice en valeurs propres simplifie énormément les calculs.

Historiquement, le concept a émergé au XIXe siècle avec Cauchy et d'autres, pour résoudre des systèmes d'équations différentielles. Le nom "eigenvalue" vient de l'allemand *eigen* = "propre, caractéristique".

## ❓ Question-test

Soit la matrice :
```
B = [[4, 0],
     [1, 3]]
```

**Question 1** : Le vecteur `(1, 0)` est-il un vecteur propre de B ? Si oui, quelle est la valeur propre associée ?

**Question 2** : Le vecteur `(1, 1)` est-il un vecteur propre de B ? (Essaie de calculer `B × (1,1)` et compare la direction du résultat avec `(1,1)`.)

*Essaie de répondre AVANT de me demander la correction. Si tu bloques, dis-moi où.*

## 📚 Pour aller plus loin

Les meilleures ressources pour **l'intuition** des valeurs propres :
- 3Blue1Brown — *Essence of Linear Algebra, chapitre 14 "Eigenvectors and eigenvalues"* (15 min, anglais sous-titré) — la meilleure explication visuelle existante
- *Mathematics for Machine Learning*, chapitre 4 — formalisme propre

Si tu veux la manipulation :
- Khan Academy — section "Vecteurs et valeurs propres"
- Exercices : toute feuille d'algèbre linéaire de L1/L2 universitaire

---

**Si cette explication ne colle pas** : dis-moi où exactement tu bloques. Souvent ce n'est pas le concept lui-même, c'est un mot (ex: "déterminant") qu'on n'a pas revu. Je peux charger un `concept-explainer` sur ce pré-requis.

---

## Commentaires sur la sortie

Ce qui fait que cet exemple fonctionne :

1. **Diagnostic du pré-requis avant explication** — la skill détecte que le vrai blocage est l'absence d'intuition géométrique, pas la valeur propre elle-même.
2. **Analogie vivante (feuille de papier)** + limite explicite de l'analogie.
3. **Exemple numérique concret** avec calculs à la main.
4. **Contextualisation** — pourquoi ce concept existe, où on le trouve en ML / physique / web.
5. **Question-test** qui demande de l'application, pas de la récitation.
6. **Pas de réponse donnée tout de suite.**
7. **Ressources nommées précisément** — pas "une bonne vidéo" mais "3Blue1Brown chapitre 14".
8. **Porte ouverte pour continuer** — si ça ne colle pas, on peut creuser un sous-concept.
