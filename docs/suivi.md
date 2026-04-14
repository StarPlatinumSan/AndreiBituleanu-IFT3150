---

## Semaine 14 (13-19 avril)

### Objectifs de la pÃ©riode
- DerniÃ¨re tÃ¢che: AmÃ©liorer et peaufiner le systÃ¨me pour l'utilisateur

### Travail rÃ©alisÃ©

!!! abstract "Avancement"
    - [x] Voici ce que j'ai effectuÃ© et optimisÃ© pour clÃ´turer mon projet informatique.
    - [x] Le systÃ¨me commence par analyser ton texte (avec OpenAI) afin dâ€™identifier les personnages, objets ou lieux importants; pour chaque entitÃ© dÃ©tectÃ©e, il extrait des traits physiques sous forme de labels (ex. : â€œgrandâ€, â€œcheveux longsâ€, â€œarmure rougeâ€).
    - [x] Tu peux ensuite gÃ©nÃ©rer une image IA de chaque entitÃ© Ã  partir de ces labels; cela permet aux auteurÂ·es de visualiser leur univers et de voir ce qui manque dans leurs descriptions : si un dÃ©tail nâ€™est pas prÃ©cisÃ©, lâ€™IA doit lâ€™imaginer, un peu comme un lecteur comble les vides avec sa propre imagination.
    - [x] Tu peux ensuite ouvrir lâ€™Ã©diteur de dessin pour modifier directement une image en esquissant des changements (ex. : ajouter des cornes bleus, yeux rouges, changer la couleur des cheveux, les habits, la peau etc.), avec ou sans texte comme support pour aider l'IA Ã  mieux comprendre et dÃ©duire tes sketchs.
    - [x] Lâ€™IA analyse ton sketch et ton Ã©ventuel prompt, dÃ©duit les nouveaux traits Ã  ajouter ou retirer, puis rÃ©gÃ©nÃ¨re lâ€™image uniquement Ã  partir de ces nouveaux labels; le processus reste simple : ce sont toujours les traits visuels en labels qui pilotent la gÃ©nÃ©ration finale.
    - [x] Enfin, tu peux demander Ã  lâ€™IA de rÃ©Ã©crire ton texte pour quâ€™il reste cohÃ©rent avec les nouvelles caractÃ©ristiques visuelles des entitÃ©s; lâ€™outil propose une variante du rÃ©cit oÃ¹ les descriptions physiques sont ajustÃ©es pour reflÃ©ter les changements que tu as faits sur les images, sans modifier le reste de lâ€™histoire, que tu peux accepter ou refuser.
    - [x] Il est fortement conseillÃ© d'effectuer des changements physiques par petites itÃ©rations pour Ã©viter que la boite noire de l'IA hallucine et assurer une cohÃ©rence dans les traits des entitÃ©s de l'auteur.

### DÃ©cisions et ajustements

!!! info "DÃ©cisions"
    - Conserver les labels de traits comme source de vÃ©ritÃ© pour la gÃ©nÃ©ration finale et la rÃ©Ã©criture

### DifficultÃ©s rencontrÃ©es

!!! warning "DifficultÃ©s"
    - Aucune difficultÃ© majeure cette semaine

---
title: Suivi du projet
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Suivi de projet

Ce suivi résume les avancées tirées de ma documentation en format PDF lors du développement de l'outil de Visual Story-Writing. Vous pouvez trouver ma documentation sur le repo de ce site web.

---

## Semaine 1 (12-18 janvier)

### Objectifs de la période
- Définir l’architecture pour une IA locale en proxy
- Préparer le socle serveur

### Travail réalisé

!!! abstract "Avancement"
    - [x] Architecture définie: React → `/api/llm` et `/api/image` → Proxy local
    - [x] Choix des IA locales: LM Studio (LLM) et ComfyAI (images)
    - [x] Création du dossier `server/` et initialisation Express + CORS + TypeScript
    - [x] Installation de `nodemon` et validation des versions Node.js v22.12.0 / npm 10.9.0

### Décisions et ajustements

!!! info "Décisions"
    - Centraliser tous les appels IA via un proxy Node.js/Express

### Difficultés rencontrées

!!! warning "Difficultés"
    - Aucune difficulté majeure cette semaine

---

## Semaine 2 (19-25 janvier)

### Objectifs de la période
- Activer le LLM local via LM Studio

### Travail réalisé

!!! abstract "Avancement"
    - [x] Mise en place des endpoints `/api/llm` et `/api/image` dans `server/index.ts`
    - [x] Connexion de `/api/llm` à LM Studio (format OpenAI-compatible)
    - [x] Modèle local utilisé: `mistral-7b-instruct`

### Décisions et ajustements

!!! info "Décisions"
    - Laisser LM Studio gérer l’essentiel du set-up LLM local

### Difficultés rencontrées

!!! warning "Difficultés"
    - Aucune difficulté majeure cette semaine

---

## Semaine 3 (26 janvier-1 février)

### Objectifs de la période
- Brancher la génération d’images IA côté proxy

### Travail réalisé

!!! abstract "Avancement"
    - [x] Tentative d’intégration d’Automatic1111 pour `/api/image`
    - [x] Recherche d’un modèle Stable Diffusion alternatif
    - [x] Téléchargement du modèle `sd_xl_base_0.9.safetensors`

### Décisions et ajustements

!!! info "Décisions"
    - Préparer une solution alternative si Automatic1111 échoue

### Difficultés rencontrées

!!! warning "Difficultés"
    - Automatic1111 tente de télécharger un moteur Stable Diffusion obsolète et ne démarre pas

---

## Semaine 4 (2-8 février)

### Objectifs de la période
- Migrer vers ComfyAI pour la génération d’images

### Travail réalisé

!!! abstract "Avancement"
    - [x] Installation de ComfyAI et de son API
    - [x] Ajout du modèle `sd_xl_base_0.9.safetensors` dans `ComfyUI/models/checkpoints/`
    - [x] Démarrage local de ComfyAI et validation par requêtes `curl`
    - [x] Intégration de `payload.json` pour piloter le workflow
    - [x] Génération d’images IA locale validée via GPU

### Décisions et ajustements

!!! info "Décisions"
    - Abandon définitif d’Automatic1111 au profit de ComfyAI

### Difficultés rencontrées

!!! warning "Difficultés"
    - Configuration initiale plus longue que prévu, mais résolue

---

## Semaine 5 (9-15 février)

### Objectifs de la période
- Afficher une image IA sur le frontend à partir d’un prompt

### Travail réalisé

!!! abstract "Avancement"
    - [x] Génération d’images depuis un prompt simple côté frontend
    - [x] Mise en place du boilerplate pour transformer un prompt en JSON

### Décisions et ajustements

!!! info "Décisions"
    - Valider ce flux simple avant l’extraction d’éléments narratifs complexes

### Difficultés rencontrées

!!! warning "Difficultés"
    - Aucune difficulté majeure cette semaine

---

## Semaine 6 (16-22 février)

### Objectifs de la période
- Préparer le LLM local pour l’extraction d’entités et de traits

### Travail réalisé

!!! abstract "Avancement"
    - [x] Setup détaillé de `mistral-7b-instruct-v0.2` dans LM Studio
    - [x] Test du proxy `/api/llm` par requête PowerShell
    - [x] Ajout de `aiProvider` dans `Model.tsx` pour distinguer IA locale vs OpenAI
    - [x] Tests avec prompts à descriptions riches et pauvres

### Décisions et ajustements

!!! info "Décisions"
    - Appeler le mode local “Mistral” pour uniformiser l’interface

### Difficultés rencontrées

!!! warning "Difficultés"
    - Les LLM locaux montrent des limites de performance sur de longs prompts

---

## Semaine 7 (23 février-1 mars)

### Objectifs de la période
- Évaluer la viabilité du mode IA locale

### Travail réalisé

!!! abstract "Avancement"
    - [x] Analyse des performances de `mistral-7b-instruct-v0.2`
    - [x] Identification des limites: temps d’inférence long et manque de rigueur
    - [x] Décision de recommander OpenAI pour un usage fluide

### Décisions et ajustements

!!! info "Décisions"
    - Limiter certaines fonctionnalités en mode IA locale

### Difficultés rencontrées

!!! warning "Difficultés"
    - Qualité inégale des modifications de texte par le LLM local

---

## Semaine 8 (2-8 mars)

### Objectifs de la période
- Implémenter l’extraction et l’édition des traits pour la génération d’images
- Consolider la génération d’entités et d’images

### Travail réalisé

!!! abstract "Avancement"
    - [x] Système d’extraction des traits pour enrichir les entités (traits physiques)
    - [x] Ajout, suppression et modification des traits pour piloter l’apparence
    - [x] V1 de régénération d’images à partir des traits modifiés
    - [x] Ajustements des prompts dans `ImageEntitiesExtractor.ts`
    - [x] Validation des JSON via `JSONPrompt.tsx` et `ImagesEditor.tsx`
    - [x] Prompt de réécriture via `RewriteFromImageTraits`
    - [x] Ajout d’une file d’attente pour générations multiples d’images
    - [x] Correctif: la voiture est maintenant reconnue comme entité
    - [x] Ajout d’un bouton pour supprimer toutes les images

### Décisions et ajustements

!!! info "Décisions"
    - Réouverture partielle de fonctionnalités locales malgré des limites

### Difficultés rencontrées

!!! warning "Difficultés"
    - Reste à confirmer l’efficacité d’OpenAI face à Mistral sur la réécriture

---

## Semaine 9 (9-15 mars)

### Objectifs de la période
- Implémenter l’éditeur de dessin sur image
- Générer un payload d’édition cohérent à partir du canvas

### Travail réalisé

!!! abstract "Avancement"
    - [x] Éditeur de dessin React avec deux canvas superposés (base + draw)
    - [x] Outils ajoutés: pinceau, gomme, sélection de couleur, taille du pinceau
    - [x] Génération du payload: `baseImageDataUrl`, `drawLayerImageDataUrl`, `maskImageDataUrl`, `editPromptText`
    - [x] Masque généré automatiquement avec légère dilatation des traits

### Décisions et ajustements

!!! info "Décisions"
    - Rendre le texte d’édition obligatoire pour améliorer la compréhension côté IA

### Difficultés rencontrées

!!! warning "Difficultés"
    - Aucune difficulté majeure cette semaine

---

## Semaine 10 (16-22 mars)

### Objectifs de la période
- Intégrer l’éditeur dans la vue des images
- Corriger le bug critique d’édition (preview vs image finale)

### Travail réalisé

!!! abstract "Avancement"
    - [x] Intégration de l’éditeur dans `ImagesEditor.tsx` (bouton Edit par carte)
    - [x] Séparation stricte des états: base, calque de dessin, masque, preview locale, image finale
    - [x] Ajout d’undo/redo et d’un bouton pour effacer le dessin
    - [x] L’image affichée ne change qu’après réponse IA, sinon elle reste intacte

### Décisions et ajustements

!!! info "Décisions"
    - Garantir que le dessin reste un calque temporaire, jamais un rendu final

### Difficultés rencontrées

!!! warning "Difficultés"
    - Confusion initiale entre preview fusionnée et image finale (résolue)

---

## Semaine 11 (23-29 mars)

### Objectifs de la période
- Valider la voie OpenAI pour l’édition d’image
- Préparer une migration complète vers ComfyAI si nécessaire

### Travail réalisé

!!! abstract "Avancement"
    - [x] Tentative OpenAI (édition via base + masque + guide + prompt)
    - [x] Analyse des échecs: clé API, vieux process sur 3001, contraintes DALL‑E
    - [x] Constat: DALL‑E 3 ne supporte pas les edits, DALL‑E 2 trop strict
    - [x] Migration vers ComfyAI avec un endpoint dédié: `POST /api/image/edit`
    - [x] Pipeline ComfyAI: upload → workflow → polling `/history` → récupération `/view`
    - [x] Retour en base64 (data URL) pour plus de fiabilité côté frontend

### Décisions et ajustements

!!! info "Décisions"
    - Abandonner OpenAI pour l’édition d’images au profit de ComfyAI

### Difficultés rencontrées

!!! warning "Difficultés"
    - OpenAI trop instable dans ce contexte (API, environnement, contraintes modèle)

---

## Semaine 12 (30 mars-5 avril)

### Objectifs de la période
- Obtenir une fidélité visuelle forte avec ComfyAI
- Réactiver les labels de traits et reconnecter l’édition au texte

### Travail réalisé

!!! abstract "Avancement"
    - [x] Passage en mode global regénération: re-rendu complet fidèle à l’image d’origine
    - [x] Renforcement du prompt système (style lock, anti-traces/anti-doodle)
    - [x] Re-rendu plus cohérent (ex: “cheveux rouges bouclés” sans traces de doodle)
    - [x] Réintégration des labels dans `ImagesEditor.tsx` (édition inline, ajout, suppression)
    - [x] Synchronisation automatique entre dessin et labels
    - [x] Reconnexion avec le système d’édition du texte via IA
    - [x] Télémetrie `durationMs` ajoutée pour suivre les performances

### Décisions et ajustements

!!! info "Décisions"
    - Favoriser un re-rendu global cohérent plutôt qu’une retouche locale par masque
    - OpenAI définitivement écarté pour cette feature

### Difficultés rencontrées

!!! warning "Difficultés"
    - Problèmes d’optimisation toujours majeurs (temps de génération élevé)
    - Risque d’hallucinations ou de dérive visuelle malgré le mode global redraw

---

## Semaine 13 (6-12 avril)

### Objectifs de la période
- Réintégrer le système de traits dans le flux principal
- Reconnecter la modification de texte avec l’IA selon l’apparence des entités
- Mettre à jour la documentation du projet

### Travail réalisé

!!! abstract "Avancement"
    - [x] Réintégration du système de traits (labels) temporairement retiré
    - [x] Modification du texte par l’IA en fonction de la nouvelle apparence des entités
    - [x] Rapport rempli depuis Obsidian et ajout d’un bouton de téléchargement du PDF de documentation

### Décisions et ajustements

!!! info "Décisions"
    - Maintenir les labels comme source principale d’édition des traits

### Difficultés rencontrées

!!! warning "Difficultés"
    - Aucune difficulté majeure cette semaine

---
