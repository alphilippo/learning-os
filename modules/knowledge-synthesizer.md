# Knowledge Synthesizer

Synthétise 3-10 sources sur un sujet en une structure claire, avec positions comparées, points de consensus, et question-test.

## Quand l'utiliser

- L'utilisateur dit *"j'ai lu 5 articles sur X, aide-moi à structurer"*, *"synthétise ces sources"*, *"vue d'ensemble de X"*
- Il a consommé plusieurs contenus mais n'arrive pas à en extraire une compréhension unifiée
- Il veut comprendre un domaine où les experts ne sont pas d'accord

## Procédure

### Phase 1 — Cadrer la question centrale (3 min)

1. **Demander** : *"À quelle question précise cette synthèse doit-elle te permettre de répondre ?"*
2. Si pas de question claire → la synthèse risque de partir dans tous les sens. Forcer une formulation.
   - ❌ *"Comprendre le ML"*
   - ✅ *"Quand utiliser un random forest vs un réseau de neurones pour mon cas ?"*
3. La question centrale devient l'**ancrage** de toute la synthèse.

### Phase 2 — Inventorier les sources (3 min)

4. **Lister les sources** fournies ou à fournir. Pour chacune :
   - Titre / auteur
   - Type (article scientifique, blog, livre, vidéo, podcast)
   - Niveau de fiabilité (primaire / secondaire / vulgarisation)
   - Date (certaines sources datent)
5. **Flag des sources douteuses** : si une source est anonyme, promotionnelle, ou contradictoire avec 3 autres → à traiter avec précaution ou exclure.

### Phase 3 — Extraire les positions (10 min)

6. Pour chaque source, extraire :
   - **Thèse principale** en 1 phrase
   - **Arguments clés** (2-3)
   - **Exemples / preuves** fournis
   - **Hypothèses implicites** (ce que l'auteur tient pour acquis sans le démontrer)

### Phase 4 — Cartographier consensus et désaccords (5 min)

7. **Points de consensus** : qu'est-ce que TOUTES les sources disent ou impliquent ?
8. **Points de désaccord** : où les sources divergent ? Pourquoi (données différentes, cadre théorique différent, intérêts différents) ?
9. **Blind spots** : quelles questions importantes aucune source ne traite ?

### Phase 5 — Construire la synthèse

10. Structure imposée :
    - **Ce qui fait consensus** (base solide)
    - **Où les experts divergent** + explications des divergences
    - **Ce qu'aucune source ne dit** (les trous)
    - **Réponse provisoire** à la question centrale, avec niveau de confiance
    - **Ce qui reste à creuser**

### Phase 6 — Question-test

11. Poser une question à laquelle la synthèse permet de répondre si elle est bien comprise.
12. Bonus : une question à laquelle la synthèse ne permet PAS de répondre — pour marquer les limites honnêtement.

## Format de sortie

```markdown
# Synthèse — <sujet> (<N> sources)

## 🎯 Question centrale
<la question précise à laquelle cette synthèse répond>

## 📚 Sources analysées

| # | Source | Type | Fiabilité | Date | Thèse en 1 phrase |
|---|---|---|---|---|---|
| 1 | <titre/auteur> | <type> | <primaire/secondaire/vulgarisation> | <date> | <thèse> |
| 2 | ... | ... | ... | ... | ... |
| 3 | ... | ... | ... | ... | ... |

## ✅ Ce qui fait consensus

<3-5 points que toutes les sources affirment ou impliquent>

1. <point 1> — confirmé par sources <#>
2. <point 2> — confirmé par sources <#>
3. <point 3> — confirmé par sources <#>

## ⚔️ Où les experts divergent

### Divergence 1 : <sujet précis>
- **Position A** (sources <#>) : <thèse>
  - Arguments : <...>
- **Position B** (sources <#>) : <thèse>
  - Arguments : <...>
- **Pourquoi ils ne sont pas d'accord** : <data différente / cadre différent / intérêts différents>

### Divergence 2 : ...

## 🕳️ Ce qu'aucune source ne traite

- <question importante non couverte 1>
- <question importante non couverte 2>

Ces angles morts sont peut-être dus à : <ancienneté des sources / biais du corpus / question trop pointue pour les sources grand public>.

## 💡 Réponse provisoire à la question centrale

<réponse synthétique de 3-5 lignes>

**Niveau de confiance** : <faible / modéré / élevé> — justification : <...>

## 🔬 Ce qui reste à creuser

Pour avoir une réponse plus ferme, il faudrait :
- <source additionnelle à chercher>
- <expérience ou donnée manquante>
- <expert à consulter>

## ❓ Question-test

<question à laquelle cette synthèse permet de répondre>

**Et une question à laquelle elle ne permet PAS de répondre** : <question précise>

---

**Export** : cette synthèse est un artefact markdown, tu peux la sauvegarder et la ré-injecter dans une future session pour approfondir.
```

## Règles dures

- **Pas de synthèse sans question centrale.** Une synthèse sans ancrage devient un résumé de résumés — inutile.
- **Pas de fausse symétrie.** Si 9 sources sur 10 disent X et qu'une source marginale dit non-X, ne pas les présenter comme "deux camps égaux". La divergence se rapporte proportionnellement.
- **Fiabilité nommée.** Ne pas mettre un blog promotionnel au même niveau qu'un papier peer-reviewed.
- **Trous assumés.** La synthèse est honnête sur ce qu'elle ne sait pas.
- **Pas de synthèse > 2 pages.** Si ça déborde, c'est un livre, pas une synthèse.

## Piège classique

L'utilisateur veut une synthèse "objective". Il n'existe pas de synthèse objective — il existe des synthèses honnêtes sur leurs biais. **Nommer explicitement** :
- Le biais de sélection des sources (toutes anglophones ? tous du même domaine ?)
- Le cadre implicite adopté
- Les positions non représentées

Autre piège : citer tout ce que chaque source dit, sans hiérarchie. Non. La skill hiérarchise : 3-5 points par source maximum, ceux qui servent la question centrale.
