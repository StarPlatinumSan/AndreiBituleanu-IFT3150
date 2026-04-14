# Implémentation

## Stack technique
- Frontend en React + TypeScript.
- Backend Node.js/Express en TypeScript servant de proxy IA.
- LLM via OpenAI, avec option de LLM local via LM Studio.
- Génération et édition d'images via ComfyUI.

## Backend
Le serveur expose des endpoints dédiés:
- `/api/llm` pour l'extraction d'entités et la réécriture du texte.
- `/api/image` pour la génération d'images à partir des traits.
- `/api/image/edit` pour les éditions à partir d'un sketch et d'un prompt.

La pipeline ComfyUI comprend l'upload, le workflow, le polling d'historique et un retour en base64 pour plus de stabilité côté frontend.

## Frontend
L'interface propose:
- un éditeur de texte et le choix du fournisseur IA,
- une liste d'entités avec gestion des labels,
- des cartes d'images avec un bouton d'édition,
- un éditeur de dessin (pinceau, gomme, masque, taille, couleurs),
- une file d'attente pour gérer plusieurs générations.

## Fonctionnalités livrées
- Extraction automatique des entités et traits physiques.
- Génération d'images guidées par labels.
- Édition par sketch avec régénération globale cohérente.
- Réécriture du texte alignée sur l'apparence visuelle.
- Mesure de performance (`durationMs`) pour suivre les temps de traitement.
