# Ligne de tri automatisée – Projet d’automatisme industriel

## Présentation du projet
Ce projet a pour objectif de concevoir et simuler une **ligne de tri automatisée** pilotée par un **automate Siemens S7**, avec une **supervision via WinCC**.

Il s’agit d’un projet d’automatisme réalisé de bout en bout, depuis la définition du besoin jusqu’à la simulation et la documentation, dans une approche proche d’un cas industriel réel.

---

## Objectif du système
Le système doit être capable de :
- détecter des pièces sur un convoyeur
- les classer selon un critère défini
- les orienter vers différentes sorties
- fonctionner de manière automatique et sécurisée

---

## Description du fonctionnement global
Le fonctionnement général de la ligne de tri est le suivant :

Un convoyeur transporte les pièces.  
Lorsqu’une pièce est détectée par un capteur de présence, le système analyse un critère de tri simulé.  
En fonction de ce critère, la pièce est orientée vers la sortie correspondante à l’aide d’un vérin de déviation.  
Une fois la pièce triée, le système revient à l’état initial et attend la pièce suivante.

Le cycle est répété de manière automatique.

---

## Définition du besoin et architecture

### Capteurs (simulés)
- Capteur de présence de type infrarouge, utilisé pour détecter l’arrivée d’une pièce
- Capteur de type, utilisé pour déterminer la catégorie de la pièce (A ou B)

### Actionneurs (simulés)
- Moteur de convoyeur assurant le déplacement des pièces
- Vérin de déviation permettant d’orienter les pièces vers la bonne sortie

---

## Modes de fonctionnement
Le système intègre les modes suivants :
- **Arrêt** : arrêt complet du système
- **Automatique** : exécution autonome du cycle de tri
- **Défaut / alarme** : mise en sécurité du système en cas de comportement anormal

Le mode manuel n’est pas implémenté dans cette version afin de conserver un projet simple et ciblé automatisme.

---

## Logique de commande et séquence automatique
La logique de commande repose sur une **séquence d’états** décrivant le cycle automatique :

1. Attente de l’arrivée d’une pièce  
2. Mise en marche du convoyeur  
3. Détection de la pièce  
4. Analyse du type de pièce  
5. Décision de tri  
6. Déviation de la pièce vers la sortie correspondante  
7. Retour à l’état initial  

Cette logique est formalisée à l’aide d’un **GRAFCET**, servant de base à la programmation de l’automate.

---

## Sécurités et gestion des défauts
Le projet intègre plusieurs mécanismes de sécurité :
- arrêt immédiat du système via un arrêt d’urgence
- détection de défauts capteurs (capteur actif trop longtemps)
- cohérence de la séquence de fonctionnement
- redémarrage contrôlé après acquittement d’un défaut

Ces sécurités permettent de garantir un comportement fiable et sûr du système.

---

## Programmation automate
La programmation est réalisée sous **TIA Portal** pour automate **Siemens S7**.  
Le programme est structuré de manière claire, avec :
- une séparation des fonctions
- une gestion explicite des entrées et sorties
- l’utilisation de temporisations et de compteurs
- des tests unitaires du comportement du programme

---

## Supervision opérateur
Une interface de supervision a été développée sous **WinCC** afin de permettre :
- le pilotage du système
- la visualisation de l’état de la machine
- l’affichage des défauts et alarmes
- le suivi des pièces triées

---

## Simulation et validation
Le fonctionnement du système a été validé par simulation à l’aide de **PLCSim**.  
Différents scénarios ont été testés :
- fonctionnement nominal
- défauts capteurs
- arrêt d’urgence
- redémarrage après défaut

---

## Documentation et dépôt GitHub
Le projet est documenté et structuré dans ce dépôt GitHub, incluant :
- la description du fonctionnement
- les fichiers de programmation
- des captures d’écran du projet
- la description des tests réalisés

---

## Auteur
Projet personnel réalisé par **Ilyes Marouf**,  
dans le cadre d’un approfondissement en **automatisme industriel**.
