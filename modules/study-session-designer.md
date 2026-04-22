# Study Session Designer

Structure une session d'étude de 30-90 min avec objectif observable, méthode active, et livrable en fin de session.

## Quand l'utiliser

- L'utilisateur dit *"j'ai 1h pour étudier"*, *"session sur X aujourd'hui"*, *"je veux progresser cette semaine sur Y"*
- Il a du temps bloqué mais ne sait pas comment l'utiliser efficacement
- Il a tendance à lire passivement sans retenir

## Procédure

### Phase 1 — Cadrer l'objectif de session (2 min)

1. **Demander** : *"En fin de session, qu'est-ce que tu pourras faire que tu ne peux pas faire maintenant ?"*
2. Forcer un **livrable observable** :
   - ❌ *"Comprendre le chapitre 3"*
   - ✅ *"Résoudre les 5 exercices du chapitre 3 sans regarder les corrigés"*
   - ✅ *"Écrire une explication de 200 mots du théorème X qu'un étudiant de mon niveau pourrait suivre"*
   - ✅ *"Implémenter en Python la fonction X et tester sur 3 cas"*
3. Si le livrable est trop gros pour 30-90 min → couper.

### Phase 2 — Diagnostic du type d'apprentissage (2 min)

4. **Identifier la nature** de ce qu'il y a à apprendre :
   - **Concepts** (comprendre le pourquoi) → méthode : exposition + reformulation + test
   - **Procédures** (savoir-faire reproductible) → méthode : observation + pratique + feedback
   - **Mémorisation** (faits, formules, vocabulaire) → méthode : spaced repetition + active recall
   - **Intégration** (plusieurs concepts liés) → méthode : synthèse + schéma + cas pratique
5. **Adapter la structure** de la session selon ce type.

### Phase 3 — Découper la session (3 min)

6. **Structure type pour 60 min** :
   - **Setup (3 min)** : préparer le matériel, ouvrir les sources, définir la question de sortie
   - **Bloc 1 Exposition (15-20 min)** : lire / regarder / observer le contenu
   - **Bloc 2 Active recall (15-20 min)** : refermer les sources, reproduire de mémoire, repérer les trous
   - **Bloc 3 Application (15-20 min)** : exercices, code, explication écrite
   - **Wrap-up (3-5 min)** : note de ce qui est clair, ce qui reste flou, prochaine session
7. **Adapter** selon durée : 30 min → 1 bloc d'exposition + 1 bloc d'application ; 90 min → ajouter une pause 10 min au milieu.

### Phase 4 — Définir la méthode d'active recall

8. **Technique obligatoire** : au moins UNE méthode active dans la session.
   - **Teach-back** : expliquer le concept à voix haute (ou par écrit) comme à quelqu'un qui ne connaît pas
   - **Blank page** : fermer tous les supports, écrire tout ce qu'on sait sur le sujet, comparer avec les sources
   - **Practice problems** : exercices sans regarder les corrigés en premier
   - **Prediction** : avant de lire une explication, deviner la réponse ; comparer après
   - **Elaboration** : pour chaque fait appris, répondre à *"pourquoi c'est vrai ?"* et *"quand ce serait faux ?"*

### Phase 5 — Setup environnement (3 min)

9. Conditions non-négociables :
   - Téléphone mode avion ou autre pièce
   - Onglets fermés sauf supports de travail + ce doc de session
   - Prévoir l'eau/café avant
   - Règle d'interruption : *"je reviens dans <N> min"*

### Phase 6 — Protocol de fin de session

10. **Wrap-up sacré** : ne pas déborder sur le bloc 3.
11. Écrire 3 lignes :
    - Ce qui est maintenant clair (factuel)
    - Ce qui reste flou ou confus
    - Prochaine question à attaquer

## Format de sortie

```markdown
# Study Session — <sujet> (<durée>)

## 🎯 Livrable observable en fin de session
<en 1 phrase, vérifiable>

## 📊 Type d'apprentissage
<concept / procédure / mémorisation / intégration>

**Méthode prioritaire** : <teach-back / blank page / practice / prediction / elaboration>

## ⏱️ Structure

| Bloc | Durée | Action | Output intermédiaire |
|---|---|---|---|
| Setup | 3 min | <setup spécifique> | Matériel prêt |
| Exposition | <N> min | <lire/regarder/observer quoi> | Notes brutes |
| Active recall | <N> min | <méthode> | Ce que je sais, ce que j'ai oublié |
| Application | <N> min | <exercices/code/explication> | Livrable observable |
| Wrap-up | 5 min | Note de fin | 3 lignes |

## 🔒 Environnement non-négociable
- [ ] Téléphone en mode avion
- [ ] Onglets fermés sauf <liste>
- [ ] Boisson préparée
- [ ] Règle interruption : "je reviens à <heure>"

## ❓ Question-test à la fin (auto-évaluation)
<question que tu dois pouvoir répondre sans aide si tu as vraiment compris>

## 📝 Note de fin de session (à remplir au wrap-up)
- Clair maintenant :
- Reste flou :
- Prochaine question :
- Auto-évaluation /5 :
  - Concentration : /5
  - Qualité du livrable : /5
  - Conditions respectées : /5

---

**Démarre à <heure>.** Setup maintenant. Chrono sur <durée>.
```

## Règles dures

- **Pas de session sans livrable observable.** "Étudier le chapitre 3" n'est pas un livrable, c'est une intention.
- **Active recall obligatoire.** Une session qui n'a que de l'exposition (lecture, vidéo) ne compte pas comme étude — c'est de la consommation.
- **Pas de session > 90 min sans pause longue.** Au-delà, la rétention chute fortement.
- **Wrap-up non négociable.** Sans la note de fin, la session suivante perd 20 min à retrouver le fil.
- **Téléphone séparé.** Pas d'exception, même *"juste pour écouter de la musique"* — 95% des gens finissent par checker les notifs.

## Piège classique

L'utilisateur dit *"je vais juste lire X, c'est suffisant"*. Non. La lecture seule = 10-20% de rétention à J+7. Avec active recall, on monte à 60-80%. Refuser une session sans active recall.

Autre piège : l'utilisateur veut *"réviser plein de choses"* en 1h. Résultat : il survole tout, ne retient rien. Forcer à choisir **UN** sujet ou **UN** chapitre maximum pour une session de 60 min.
