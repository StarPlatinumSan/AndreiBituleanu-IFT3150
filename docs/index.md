---
title: Vue d'ensemble du projet
---

<style>
    @media screen and (min-width: 76em) {
        .md-sidebar--primary {
            display: none !important;
        }
    }
</style>

# Vue d'ensemble du projet

!!! info "Informations générales"
    **Session**: Hiver 2026  
    **Auteur(s)**: Andrei Bituleanu (20275298)<!-- Nom de chaque membre (matricule)  -->  
    **Thème(s)**: Application Web React/TS/Express, Intégration IA, Outil d'écriture visuelle <!-- Thèmes principaux abordés dans le projet  -->  
    **Superviseur(s)**: Damien Masson <!-- Nom du superviseur (affiliation)  -->  
    **Collaborateur(s):** Andrei Bituleanu <!-- Nom de(s) collaborateur(s) et partenaire(s)` -->  

## Description du projet

L’outil implémente une API d’IA qui a comme instruction d’analyser un texte narratif soumis par
l'utilisateur et de générer des représentations visuelles telles que des graphes structurels et
éventuellement des images de personnages, objets et paysages issus de la description
textuelle afin d’offrir à l’écrivain un retour visuel sur son propre récit. La manipulation de ces
représentations permet également de modifier le texte à l'aide de génération IA et vice-versa.

### Contexte

Ce projet informatique s’inscrit dans le domaine de l’interaction humain-machine (HCI), de la visualisation appliquée à l’écriture narrative et de l’utilisation de l’intelligence artificielle comme outil à intelligence étroite (Artificial Narrow Intelligence).
Il s’insère dans un contexte de recherche visant à explorer de nouvelles formes d’assistance à la créativité humaine, en particulier dans les pratiques contemporaines d’écriture et de narration.

Les travaux récents en HCI et en interaction humain-IA cherchent à concevoir des outils où l’intelligence artificielle agit comme un support cognitif et créatif, plutôt que comme un substitut à l’humain. Dans cette perspective, l’IA est envisagée comme un moyen d’offrir des retours, des visualisations et des aides à la réflexion, tout en laissant le contrôle créatif à l’utilisateur.

Le projet est supervisé par Damien Masson, professeur adjoint et chercheur dont les travaux portent principalement sur l’interaction humain-ordinateur, l’interaction humain-IA et la visualisation de l’information, et s’inscrit dans un cadre universitaire et expérimental.

### Problématique

Les auteurs et écrivains disposent aujourd’hui de peu d’outils capables de leur offrir un soutien concret durant le processus d’écriture narrative. En particulier, il n’existe pas d’outil permettant de visualiser de manière explicite la structure d’un récit, la cohérence des descriptions, l’évolution des personnages, des lieux ou des objets, ni leurs interactions au fil du texte.

Cette absence de retour visuel rend difficile l’identification de problèmes narratifs, stylistiques ou structurels, tels que des incohérences, des descriptions incomplètes ou des éléments narratifs sous-exploités. Le processus d’écriture repose alors essentiellement sur une relecture linéaire du texte, ce qui peut ralentir la création et limiter la qualité du résultat final.

Ainsi, le manque d’outils offrant une représentation visuelle et interactive du récit constitue un frein à l’exploration, à la compréhension et à l’amélioration des textes narratifs, soulevant la question de la manière dont des technologies interactives et intelligentes pourraient soutenir plus efficacement les auteurs dans leur démarche créative.

### Proposition et objectifs

Ce projet informatique vise à poursuivre le développement d’un outil d’écriture de récits assisté par intelligence artificielle qui a pour objectif de soutenir le processus créatif des auteurs. Cette approche vise à répondre à la problématique identifiée, soit l’absence d’outils offrant un retour visuel et interactif sur la structure, la cohérence et l’évolution d’un récit narratif.

Plusieurs tâches ont été établies et l’étudiant sur le projet fera de son mieux pour en compléter un maximum à la hauteur du possible. En cas d’impossibilité d’obtenir un résultat satisfaisant, une tâche peut être altérée, voire retirée. De nouvelles tâches sont susceptibles d’être ajoutées de façon spontanée au cours du semestre sans qu’elles ne figurent nécessairement dans ce document.

Les objectifs du projet sont définis à travers les fonctionnalités suivantes, chacune correspondant à une étape concrète et mesurable du développement de l’outil :

1. Ajouter une fonctionnalité capable d’extraire automatiquement le contenu du texte narratif, tel que des descriptions de personnages, de lieux ou d’objets, et de générer une image par IA servant de brouillons visuels. Ces images ont pour but d’aider l’auteur à mieux visualiser et améliorer les détails décrits dans son récit.

2. Ajouter un mode de génération d’images IA strict, visant à empêcher l’IA d’auto-compléter les parties d’un élément dépourvues de description, en appliquant un fond de texture neutre indiquant une description absente ou incomplète. Cette fonctionnalité permet de signaler visuellement à l’auteur les éléments nécessitant davantage de détails.

3. Permettre à l’auteur de sélectionner une région précise d’une image générée par IA à l’aide d’un outil de découpe et de décrire les changements souhaités pour cette zone, modifiant ainsi la section correspondante de l’image et la description associée dans le texte.

4. Offrir la possibilité de sélectionner une zone d’une image générée par l’IA et de la faire glisser (drag and drop) à un endroit précis du texte afin que l’IA ajoute automatiquement la description correspondante à cet emplacement.

5. Permettre à l’utilisateur d’utiliser une seconde API d’IA, telle que Gemini, en complément de l’API OpenAI actuellement utilisée.

6. Permettre à l’utilisateur d’intégrer sa propre IA locale installée sur sa machine, rendant possible une utilisation hors ligne et sans coût de l’outil.

7. Améliorer l’interface utilisateur afin d’optimiser l’expérience lors de l’édition du texte, de l’exploration des graphes d’interactions narratives et de la manipulation des images générées par IA.

Ces objectifs sont conçus pour être atteignables dans le cadre du semestre et évaluables par la présence de prototypes fonctionnels démontrant les fonctionnalités décrites.

### Méthodologie

La méthodologie du projet repose sur une approche progressive et simple. Le développement est effectué en avançant une tâche à la fois, en cherchant d’abord à faire fonctionner chaque fonctionnalité de manière élémentaire avant de la spécialiser.

Chaque tâche est d’abord implémentée de façon isolée, par exemple en validant la génération d’images par intelligence artificielle sans lien direct avec le récit. Une fois ce fonctionnement de base obtenu, la fonctionnalité est ensuite adaptée afin de fonctionner à partir d’un texte narratif fourni par l’utilisateur.

Cette démarche permet d’avancer par itérations successives, de limiter la complexité à chaque étape et de valider régulièrement le bon fonctionnement des différentes parties de l’outil. Les validations sont principalement fonctionnelles et reposent sur des scénarios d’utilisation simples et concrets.

### Validation et Évaluation

La validation du projet sera réalisée principalement à travers des tests manuels et des scénarios d’usage. L’outil sera utilisé sur des exemples de récits personnels afin de vérifier le bon fonctionnement des fonctionnalités développées et leur capacité à soutenir le processus d’écriture.

L’outil sera également testé par le superviseur du projet ainsi que par d’autres étudiants ne connaissant pas l’application. Ces tests permettront d’obtenir des retours qualitatifs sur la compréhension de l’interface, la pertinence des visualisations générées et l’utilité générale de l’outil dans un contexte de création narrative.

L’évaluation reposera donc principalement sur des indicateurs qualitatifs, tels que la facilité d’utilisation, la cohérence des résultats produits et la perception de l’apport de l’outil par les utilisateurs testeurs.

## Équipe

<b>Andrei Bituleanu</b> : Le développeur et concepteur en relève pour poursuivre l'application. <br>
<b>Damien Masson</b> : Actuellement superviseur pour s'assurer du bon avancement du projet.

## Échéancier

!!! info
    Le suivi complet est disponible dans la page [Suivi de projet](suivi.md).

| Activités                      | Début   |   Fin   | Livrable                            | Statut      |
|--------------------------------|---------|---------|-------------------------------------|-------------|
| Ouverture de projet            | 12 jan. | 12 jan. | Proposition de projet               | ✅ Terminé  |
| Études préliminaires           | 12 jan. | 23 jan. | Document d'analyse                  | 🔄 En cours |
| Présentation + Rapport         | 17 avr. | 30 avr. | Présentation + Rapport              | ⏳ À venir  |
