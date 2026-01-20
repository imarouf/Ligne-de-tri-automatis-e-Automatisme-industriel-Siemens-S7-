# ⏱️ Temps nécessaire pour le projet – Ligne de tri automatisée

👉 **Réponse courte**  
➡️ Entre **20 et 40 heures**, selon le niveau de finition souhaité.

Ce projet a été conçu comme un **projet d’automatisme industriel simple de A à Z**, avec une approche réaliste proche des pratiques en entreprise.

---

## 🧩 Découpage réaliste (automaticien junior)

---

## 1️⃣ Définition du besoin & architecture  
⏱️ **2–3 h**

### 🎯 Objectif
Définir clairement le besoin fonctionnel et poser les bases du système avant toute programmation.

Le but est de développer une **ligne de tri automatisée** capable de :
- détecter des pièces
- les classer selon un critère défini
- les orienter vers différentes sorties

---

### 🔄 Fonctionnement global
Le fonctionnement du système est le suivant :

Un convoyeur transporte des pièces →  
Un capteur détecte la présence d’une pièce →  
Un critère de tri est analysé →  
La pièce est dirigée vers la sortie correspondante →  
Le système revient à l’état initial et attend la pièce suivante  

Ce cycle est répété de manière automatique.

---

### 📥 Liste des entrées / capteurs (simulés)

| Référence | Désignation | Rôle |
|---------|------------|------|
| S1 | Capteur de présence (type infrarouge) | Détecter l’arrivée d’une pièce sur le convoyeur |
| S2 | Capteur de type | Déterminer la catégorie de la pièce (A ou B) |

---

### 📤 Liste des sorties / actionneurs (simulés)

| Référence | Désignation | Rôle |
|---------|------------|------|
| M1 | Moteur de convoyeur | Assurer le déplacement des pièces |
| Y1 | Vérin de déviation | Orienter la pièce vers la sortie appropriée |

---

### ⚙️ Modes de fonctionnement

- **Arrêt**  
  Permet l’arrêt complet et immédiat du système.

- **Automatique**  
  Le système exécute le cycle de tri de manière autonome.

- **Mode défaut / alarme**  
  Déclenché en cas de comportement anormal (capteur bloqué, incohérence de séquence, arrêt d’urgence).

> Le mode manuel n’est pas implémenté dans cette version afin de conserver un projet simple et ciblé automatisme.

---

## 2️⃣ Logique de commande & GRAFCET  
⏱️ **4–6 h**

### 🎯 Objectif
Définir une logique séquentielle claire, robuste et compréhensible, typique d’un système automatisé industriel.

---

### 🔁 Description du cycle automatique

Le cycle automatique se déroule selon les étapes suivantes :

1. Le système attend l’arrivée d’une pièce
2. Le convoyeur est mis en marche
3. La pièce est détectée par le capteur de présence
4. Le type de la pièce est analysé
5. La décision de tri est prise
6. Le vérin dévie la pièce vers la sortie correspondante
7. Le système revient à l’état initial

---

### 🧠 Principe de la logique de commande
La logique repose sur :
- une **séquence d’états bien définie**
- des **conditions de transition claires**
- des **temporisations** pour éviter les comportements incohérents
- une gestion des défauts intégrée

---

### 📊 GRAFCET
Un GRAFCET a été défini afin de représenter le cycle automatique :

- Étape d’attente
- Étape convoyeur en marche
- Étape analyse du type de pièce
- Étape déviation
- Étape retour à l’état initial

Des transitions prioritaires permettent :
- le passage en **arrêt sécurisé**
- la détection et la gestion des défauts

Le GRAFCET constitue la base de la programmation PLC.

---

## 3️⃣ Programmation PLC (TIA Portal)  
⏱️ **8–12 h**

- Organisation claire du programme
- Utilisation des blocs **OB / FC / FB**
- Gestion des entrées / sorties
- Temporisations et compteurs
- Tests unitaires du programme

👉 **Partie centrale du projet.**

---

## 4️⃣ Supervision WinCC  
⏱️ **4–6 h**

- Écrans principaux de commande
- Boutons de contrôle et voyants d’état
- Gestion des alarmes
- Compteurs de pièces triées

---

## 5️⃣ Simulation & tests (PLCSim)  
⏱️ **3–5 h**

- Tests en fonctionnement nominal
- Tests de défauts capteurs
- Test de l’arrêt d’urgence
- Test du redémarrage après défaut

---

## 6️⃣ Documentation & GitHub  
⏱️ **3–4 h**

- README clair et structuré
- Screenshots du projet
- Explication de l’architecture
- Description des cas de tests

👉 **Ce point fait la différence sur un CV.**

---

## 📊 Récapitulatif

| Niveau de projet | Temps estimé | Impact CV |
|-----------------|------------|-----------|
| Minimal propre | ~20 h | ✅ Suffisant |
| Solide industriel | ~30 h | 🔥 Très bon |
| Très poussé | ~40 h | 🚀 Excellent |

👉 **30 h est le sweet spot.**

---

## 🧠 Conseil stratégique
Mieux vaut :
- **1 projet bien fini**

plutôt que :
- **3 projets à moitié faits**

Un recruteur préférera toujours :
> *« Il a un projet clair, testé et documenté »*

---

## 🗓️ Exemple de planning simple

- **Semaine 1** : logique + PLC  
- **Semaine 2** : IHM + tests + GitHub  

➡️ Projet faisable en **2 semaines tranquilles**, même avec une alternance.

---

## 👤 Auteur
Projet personnel réalisé par **Ilyes Marouf**  
Projet orienté **automatisme industriel – Siemens S7**
