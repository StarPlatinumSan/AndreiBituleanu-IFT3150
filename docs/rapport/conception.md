# Conception

## Principe directeur
L'IA est utilisée comme un outil d'assistance à la créativité. L'utilisateur conserve le contrôle, et les traits visuels en labels servent de source de vérité pour la génération et la réécriture.

## Pipeline fonctionnel
1. Analyse du texte narratif pour extraire les entités et leurs traits physiques.
2. Génération d'images à partir des traits sous forme de labels.
3. Édition visuelle par sketch, puis déduction des nouveaux traits.
4. Régénération d'image et proposition de réécriture du texte alignée.

## Modèle de données
- Une entité est décrite par un nom, un type et une liste de traits physiques.
- Une image est associée à une entité et à une version des traits.
- Toute modification d'image met à jour les traits, puis relance la génération.

## Interface
La conception vise une interface qui facilite:
- l'édition du texte narratif,
- la visualisation des entités et de leurs traits,
- la génération et l'édition d'images par un canvas,
- la validation ou le rejet des réécritures proposées.
