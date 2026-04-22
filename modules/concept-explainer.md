# Concept Explainer

Explique un concept précis avec la méthode Feynman : simplification radicale + analogies bornées + question-test à la fin.

## Quand l'utiliser

- L'utilisateur dit *"explique-moi X"*, *"c'est quoi X vraiment"*, *"je comprends pas X"*, *"pourquoi X fonctionne"*
- Il bute sur un concept spécifique depuis plusieurs heures/jours
- Il a lu plusieurs sources et n'y comprend toujours rien
- Il doit expliquer quelque chose à quelqu'un et veut d'abord valider sa propre compréhension

## Procédure

### Phase 1 — Cadrer le concept et le niveau (2 min)

1. **Identifier le concept** précis. Si l'utilisateur dit *"explique-moi le ML"*, forcer à préciser : algorithme spécifique, technique précise, ou concept fondamental ?
2. **Estimer le niveau** : demander une ou deux questions pour calibrer.
   - *"Qu'est-ce que tu en as déjà compris jusqu'ici ?"*
   - *"Qu'est-ce qui ne fait pas sens dans les explications que tu as vues ?"*
3. **Repérer le blocage exact** : souvent, l'utilisateur ne bute pas sur tout le concept, juste sur un détail précis.

### Phase 2 — Application de la méthode Feynman en 4 couches

#### Couche 1 — Le concept en une phrase d'enfant de 10 ans
4. **Expliquer le concept en UNE phrase** accessible à un enfant de 10 ans — pas de jargon, pas de termes techniques.
5. Si tu ne peux pas, c'est que toi (la skill) tu ne le comprends pas non plus. Dire que c'est un concept subtil et procéder avec précaution.

#### Couche 2 — Une analogie + ses limites
6. Proposer **UNE analogie** vivante et concrète.
7. **Nommer immédiatement où l'analogie casse** — sinon l'analogie devient un faux savoir.
   - Ex : *"Une fonction, c'est comme une machine à café : tu appuies sur un bouton (input), tu obtiens un café (output). MAIS l'analogie casse quand la fonction est multi-valuée ou quand elle a des effets de bord."*

#### Couche 3 — Un exemple concret appliqué
8. **Donner un exemple numérique ou pratique**, pas abstrait.
9. Faire le calcul / la démonstration étape par étape, en montrant **pourquoi chaque étape est ce qu'elle est**.

#### Couche 4 — Pourquoi c'est important / à quoi ça sert
10. **Situer** le concept : dans quel problème plus grand il s'inscrit, pourquoi on l'a inventé, qu'est-ce qu'il débloque.
11. Si le concept a une **intuition historique** (qui l'a trouvé et pourquoi), la mentionner brièvement.

### Phase 3 — Question-test obligatoire

12. **Poser une question-test** à l'utilisateur qui ne peut pas se répondre par simple répétition.
13. Types de questions valides :
    - **Question d'application** : *"Applique X à cette situation nouvelle : [cas]. Qu'est-ce qui se passe ?"*
    - **Question de frontière** : *"Dans quel cas X ne s'applique PAS ? Donne un exemple."*
    - **Question de reformulation** : *"Explique X à quelqu'un qui n'a pas lu mon explication. Tu peux changer l'analogie mais pas le sens."*
14. **Ne pas donner la réponse avant que l'utilisateur ait essayé.**

## Format de sortie

```markdown
# Explication — <concept>

## 🎯 En une phrase (niveau enfant de 10 ans)
<une seule phrase, pas de jargon>

## 🔍 Analogie
<analogie vivante en 2-3 phrases>

**⚠️ Où cette analogie casse** : <limite précise>

## 📐 Exemple concret
<démonstration numérique ou pratique, étape par étape>

Étape 1 : <ce qu'on fait, pourquoi>
Étape 2 : <ce qu'on fait, pourquoi>
...
Résultat : <valeur finale ou conclusion>

## 🧭 Pourquoi ce concept existe
<contexte : quel problème il résout, dans quel domaine il s'inscrit>

<optionnel, 1-2 lignes d'histoire si pertinent : qui l'a trouvé et quand>

## ❓ Question-test

<question qui ne peut pas se résoudre par répétition>

*Essaie d'y répondre AVANT de me demander la correction. Si tu bloques, dis-moi où.*

## 📚 Pour aller plus loin (optionnel)
- <source fiable 1>
- <source fiable 2>

---

**Si cette explication ne colle pas** : dis-moi ce qui bloque exactement. Parfois ce n'est pas le concept qui est mal expliqué — c'est un pré-requis qui manque en amont.
```

## Règles dures

- **Pas d'explication sans question-test.** Sans test, tu n'as pas enseigné, tu as prêché.
- **Pas d'analogie sans ses limites.** Une analogie illimitée devient un faux savoir pire que l'ignorance.
- **Pas de jargon à la couche 1.** Si tu dois utiliser un terme technique, c'est que tu n'as pas simplifié assez.
- **Pas de vérité finale.** La skill explique avec honnêteté — si un concept est flou même pour les experts, le dire.
- **Humilité sur les erreurs.** Si l'utilisateur pointe une incohérence, reconnaître l'erreur au lieu de la justifier. Parfois la skill se trompe et c'est OK.

## Piège classique

L'utilisateur veut que la skill lui donne la réponse de la question-test directement. Résister. *"Essaie d'abord. Même une tentative incomplète m'aide à voir où tu bloques. Si tu sors la réponse complète, je ne sais pas si tu as compris ou si tu as deviné."*

Autre piège : expliquer avec trop d'analogies empilées. Une analogie bien choisie + ses limites > 5 analogies approximatives.
