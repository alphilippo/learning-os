# Contributing to learning-os

Merci de vouloir contribuer. `learning-os` est une skill Claude open-source — les contributions bienvenues améliorent les modules existants ou ajoutent de nouveaux mécanismes pédagogiques rigoureusement définis.

## Les 3 types de contributions bienvenues

### 1. Amélioration des modules existants

Si tu constates que :
- Le `learning-path-planner` accepte des objectifs flous
- Le `concept-explainer` produit des explications sans question-test
- Le `study-session-designer` laisse passer des sessions sans active recall
- Le `knowledge-synthesizer` fait de la fausse symétrie
- Le `math-rebuild` ignore un signal d'anxiété

Ouvre une issue avec le prompt exact + la sortie obtenue + ta proposition d'amélioration.

### 2. Nouveaux modules

Critères pour ajouter un module :
- **Unique** — pas de doublon avec les 5 existants
- **Vérifiable** — produit une sortie avec mécanisme de test
- **Actionnable** — livrable observable, pas conceptuel
- **Testable** — on peut écrire 5+ cas de test

Candidats bienvenus :
- **Spaced Repetition Helper** (génération de flashcards Anki)
- **Research Mode** (deep-reading d'un papier de recherche)
- **Language Learning** (apprentissage langues)
- **Teach-back Recorder** (assistant pour enregistrer ses explications à voix haute)

Candidats **refusés** :
- "Motivational coach" ou quoi que ce soit de style gamifié
- Résumé simple sans vérification
- Module trop spécifique à un domaine (ex: "apprendre SQL") — préférer un module générique applicable à plusieurs domaines

### 3. Ressources à jour

Les URLs et références de livres peuvent dater. Si tu constates qu'une ressource est :
- Devenue payante
- Plus disponible
- Remplacée par une meilleure alternative

→ Ouvre une PR qui met à jour le module concerné.

## Ce qu'on refuse

- Pédagogie qui encourage la consommation passive ("lis ces 20 livres")
- Promesses irréalistes ("maîtrise les maths en 1 mois")
- Sources uniquement payantes ou inaccessibles
- Analogies sans leurs limites
- Ton condescendant ou culpabilisant

## Style

- **Ton direct, pas condescendant** — l'apprenant est intelligent, juste inexpérimenté
- **Vérité sur les ordres de grandeur** — pas de sugar-coating sur les durées
- **Sources précises** — titre/auteur/plateforme, pas "un bon livre"
- **Livrables observables** — pas d'intentions vagues

## Process

1. Fork le repo
2. Branche `feat/<module>` ou `fix/<problème>`
3. Si nouveau module : ajouter au moins 3 cas de test dans `tests/test-cases.md`
4. Si nouveau template : ajouter dans `templates/`
5. Commit clair : `feat: add spaced-repetition-helper module`
6. PR avec description + sortie d'exemple

## Code de conduite

Rigueur avec les idées, gentillesse avec les personnes. Les débats sur la pédagogie sont bienvenus, les attaques personnelles non.
