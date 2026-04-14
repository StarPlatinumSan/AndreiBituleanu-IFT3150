# Résultats & Discussion

## Résultats obtenus
Le projet a produit un prototype fonctionnel qui:
- analyse un texte narratif et extrait des entités avec leurs traits,
- génère des images à partir de ces traits,
- permet l'édition visuelle par sketch et la régénération,
- propose une réécriture du texte cohérente avec les images,
- offre un choix entre IA locale et IA distante selon le contexte.

## Discussion
L'approche basée sur des labels explicites renforce le contrôle utilisateur et réduit les hallucinations. Le flux texte -> traits -> images -> réécriture crée une boucle itérative utile pour repérer ce qui manque dans une description et l'améliorer progressivement.

## Perspectives
- Ajouter une visualisation des interactions narratives sous forme de graphes.
- Mieux optimiser les temps de génération et la gestion des lots.
- Explorer des métriques d'évaluation automatique de cohérence texte-image.
