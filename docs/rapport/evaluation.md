# Évaluation & Tests

## Validation réalisée
- Tests manuels sur récits courts et moyens pour vérifier l'extraction d'entités.
- Génération d'images pour chaque entité et comparaison avec les traits.
- Édition par sketch puis validation que les nouveaux traits sont pris en compte.
- Réécriture du texte et vérification de la cohérence avec les images.

## Observations
- Les LLM locaux sont plus lents et moins fiables sur des prompts longs.
- OpenAI fournit des extractions et réécritures plus stables.
- La régénération globale via ComfyUI réduit les artefacts du sketch, au prix d'un temps de rendu plus long.

## Limites
- Absence d'étude utilisateur formelle ou de métriques quantitatives.
- Dépendance à la qualité des descriptions initiales.
- Coût et latence variables selon l'infrastructure IA utilisée.

Une évaluation plus formelle pourrait être menée avec des auteurs externes et des scénarios d'écriture comparatifs.
