# Learning Path Planner

Construit un plan d'apprentissage 1-3 mois pour un domaine, avec checkpoints testables et sources externes nommées.

## Quand l'utiliser

- L'utilisateur démarre un nouveau domaine (ML, droit, finance, langue, instrument, autre)
- Il dit *"je veux apprendre X"*, *"par où commencer"*, *"je veux maîtriser Y d'ici 3 mois"*
- Il a plusieurs ressources disponibles mais ne sait pas dans quel ordre les aborder
- Il sent qu'il tourne en rond depuis plusieurs semaines sur un sujet

## Procédure

### Phase 1 — Cadrer l'objectif (5 min)

1. **Demander** : *"Concrètement, dans 3 mois, qu'est-ce que tu veux POUVOIR faire que tu ne peux pas faire aujourd'hui ?"*
2. Forcer une réponse **observable** :
   - ❌ *"Mieux comprendre le ML"*
   - ✅ *"Construire et entraîner un modèle de classification depuis zéro sur un dataset que j'ai choisi"*
3. Si l'objectif est trop flou → l'utilisateur n'est pas prêt à faire un plan, il doit d'abord clarifier pourquoi il apprend ce sujet.

### Phase 2 — Estimer le niveau de départ (5 min)

4. **Demander** : *"Qu'est-ce que tu connais déjà sur le sujet ? Qu'est-ce qui te manque clairement ?"*
5. **Test de calibration** : proposer 2-3 questions fondamentales du domaine et demander les réponses.
   - Si l'utilisateur répond bien → niveau intermédiaire+
   - S'il bute sur les bases → démarrage fondations
   - S'il connaît une partie mais pas une autre → plan asymétrique
6. **Nommer explicitement** les pré-requis manquants.

### Phase 3 — Estimer le budget temps (3 min)

7. **Demander** : *"Combien d'heures par semaine tu peux vraiment allouer ?"*
8. Règle du **70%** : budget réel = heures théoriques × 0.7 (vie qui déborde).
9. Préciser : *"Ces heures seront-elles continues (1 bloc de 5h) ou fragmentées (5 blocs de 1h) ?"* — ça change le plan.

### Phase 4 — Construire le parcours (15 min)

10. **Décomposer** le domaine en 3-6 modules progressifs, par ordre de dépendance.
11. Pour chaque module :
    - **Concepts clés** à maîtriser (3-7)
    - **Ressources recommandées** (livre, cours, vidéo, papier) — nommées précisément, pas "un bon livre de maths"
    - **Exercices/projet** pour valider
    - **Temps estimé** en heures
12. **Checkpoint testable** à la fin de chaque module : qu'est-ce que tu dois POUVOIR faire sans aide ?
13. **Vérifier la cohérence** : somme des temps modules = budget total disponible ? Si > 100%, couper le scope.

### Phase 5 — Définir les checkpoints de sortie (5 min)

14. **Projet final** observable qui prouve la maîtrise à la fin du plan.
15. **Signal d'alerte** : si à 50% du plan tu ne peux pas répondre à 3 questions de niveau intermédiaire, le plan dérive → replanifier.

## Format de sortie

```markdown
# Plan d'apprentissage — <domaine> (<date début> → <date fin>)

## 🎯 Objectif dans <N> mois
<ce que tu pourras faire concrètement, formulé en "être capable de...">

## 📊 Niveau de départ estimé
- Ce que tu maîtrises déjà : <liste>
- Pré-requis manquants : <liste>
- Niveau global : <débutant / intermédiaire / avancé sur X>

## ⏱️ Budget
- Heures théoriques : <X>h/semaine × <N> semaines = <Y>h
- Heures réelles (70%) : <Z>h
- Format : <blocs continus / fragmenté>

## 📍 Modules

### Module 1 — <nom> (~<N>h)
**Concepts clés** :
- <concept 1>
- <concept 2>

**Ressources recommandées** :
- 📚 <livre précis> — chapitres <X-Y>
- 🎥 <cours/vidéo précis> — URL si connue
- 📝 <exercices>

**Checkpoint** : à la fin du module, tu dois pouvoir :
- [ ] <action observable 1>
- [ ] <action observable 2>

### Module 2 — ...
...

## 🏁 Projet final
<description précise du livrable qui prouve la maîtrise>

## 🚦 Signal d'alerte à mi-parcours
À S+<N>/2, tu dois pouvoir répondre à ces 3 questions :
1. <question niveau intermédiaire>
2. <question niveau intermédiaire>
3. <question niveau intermédiaire>

Si non → replanifier, pas continuer en espérant.

## ⚠️ Limites de ce plan
- <risque 1, ex: sans pratique quotidienne, les concepts abstraits ne rentrent pas>
- <risque 2, ex: certaines ressources sont anglophones>
- <risque 3, ex: le domaine évolue vite, certaines sources dateront>

---

**Prochaine action concrète (dans les 48h)** : <première micro-action qui lance le plan>

**Date de check-in à mi-parcours** : <date>
```

## Règles dures

- **Pas de "tour d'horizon" générique.** Si l'objectif n'est pas observable, forcer à le reformuler ou refuser de planifier.
- **Sources nommées précisément.** Jamais *"un bon cours"*. Toujours *"le cours X de Y sur la plateforme Z"*, ou si pas sûr, dire *"cherche un cours de niveau intermédiaire sur X, critères : A, B, C"*.
- **Checkpoints obligatoires à chaque module.** Pas de module sans test de sortie.
- **Vérité sur les ordres de grandeur.** Si l'utilisateur veut apprendre les maths prépa en 1 mois, dire que c'est irréaliste et proposer soit un objectif plus réaliste soit un scope plus restreint.
- **Humilité sur les sources.** Si le domaine bouge vite (IA, finance, droit), dire que certaines ressources peuvent être datées et indiquer comment vérifier la fraîcheur.

## Piège classique

L'utilisateur veut un plan "parfait" avec 20 livres et 10 cours. Il ne fera rien. **Règle** : un bon plan < un plan parfait. 3-5 ressources par module maximum, pas 15. Le plan doit tenir sur 2 pages.

Autre piège : l'utilisateur veut *"être expert en X en 3 mois"* alors que X demande 3 ans. **Ne pas acquiescer.** Proposer un objectif réaliste à 3 mois (compétent sur un sous-domaine) plutôt qu'un fantasme d'expertise.
