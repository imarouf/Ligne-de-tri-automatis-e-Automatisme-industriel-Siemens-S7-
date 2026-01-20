# Ligne de tri automatisée – Automatisme industriel (Siemens S7)

## Présentation du projet
Ce projet consiste à concevoir et simuler une **ligne de tri automatisée** pilotée par un **automate Siemens S7**, avec une **supervision opérateur via WinCC**.  
L’objectif est de reproduire un cas industriel réaliste mettant en œuvre une logique séquentielle, la gestion de capteurs/actionneurs, des sécurités et des défauts.

Le projet a été réalisé **en autonomie**, avec une approche orientée **automatisme industriel et mise en service**.

---

## Objectifs techniques
- Analyser un besoin fonctionnel industriel
- Concevoir une logique de commande fiable et sécurisée
- Programmer un automate Siemens sous **TIA Portal**
- Mettre en place une **supervision opérateur (IHM)**
- Tester et valider le fonctionnement via simulation

---

## Description du fonctionnement
Une pièce est transportée par un convoyeur motorisé.  
Lorsqu’elle est détectée par un capteur de présence, un critère de tri (simulé) permet de décider si la pièce doit être orientée vers la **sortie A** ou la **sortie B** à l’aide d’un déviateur.

Le système fonctionne selon plusieurs modes :
- **Arrêt**
- **Manuel**
- **Automatique**
- **Défaut / Arrêt d’urgence**

---

## Architecture du système

### Capteurs (simulés)
- Capteur de présence pièce
- Capteur de type pièce (A / B)

### Actionneurs (simulés)
- Moteur de convoyeur
- Vérin / déviateur de tri

---

## Logique de commande
La logique de commande est basée sur :
- Un **cycle séquentiel** (type GRAFCET)
- Des temporisations et conditions de transition
- Une gestion des modes de fonctionnement
- Des sécurités intégrées

---

## Sécurités intégrées
Le projet intègre plusieurs mécanismes de sécurité :
- **Arrêt d’urgence** prioritaire (arrêt immédiat des actionneurs)
- **Détection de défaut capteur** (présence active trop longtemps)
- **Sécurité de séquence** (actions autorisées uniquement dans les états cohérents)
- **Redémarrage sécurisé** avec acquittement opérateur après défaut

---

## Supervision (WinCC)
L’IHM permet à l’opérateur de :
- Commander la machine (Marche / Arrêt / Auto / Manuel)
- Visualiser l’état du système
- Consulter les défauts et alarmes
- Suivre les compteurs de pièces triées (A / B)
- Acquitter les défauts

---

## Tests & validation
Le système a été validé par simulation à l’aide de **PLCSim** :
- Tests en fonctionnement nominal
- Tests de défauts capteurs
- Tests d’arrêt d’urgence
- Tests de redémarrage après défaut

Les résultats des tests confirment un comportement conforme au cahier des charges.

---

## Technologies utilisées
- Automate : **Siemens S7**
- Environnement de développement : **TIA Portal**
- Simulation : **PLCSim**
- Supervision : **WinCC**
- Langages : LAD / FBD

---

## 📁 Structure du dépôt
