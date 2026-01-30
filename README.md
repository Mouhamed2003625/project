# 🚀 Lakehouse Data Engineering Platform – Databricks Community

## 📌 Contexte du projet

Ce projet consiste en la conception et l’implémentation d’une **plateforme Data Engineering de type Lakehouse**, développée en **PySpark** et déployée sur **Databricks Community Edition**.  
Il s’inscrit dans un cadre académique / capstone project et vise à mettre en œuvre des **bonnes pratiques industrielles** de traitement de données à grande échelle.

Le pipeline traite **plus de 8 Go de données**, issues de **sources hétérogènes**, et repose sur une architecture **Bronze / Silver / Gold** garantissant :
- la traçabilité des données,
- l’idempotence des traitements,
- la qualité et la standardisation des datasets,
- l’exploitabilité analytique et métier.

---

## 🏗️ Architecture globale

L’architecture du projet suit le **Lakehouse pattern** :


### 🔹 Bronze
- Données brutes ingérées sans transformation majeure
- Conservation maximale de l’information
- Traçabilité par `run_date` / `run_id`

### 🔹 Silver
- Nettoyage et standardisation
- Schémas explicites
- Gestion des valeurs nulles et doublons
- Harmonisation des types et formats
- Écriture optimisée en **Parquet / Delta**

### 🔹 Gold
- Données agrégées et orientées métier
- Tables analytiques prêtes pour la BI et le reporting
- Optimisation pour la performance et la lecture

---

## 📂 Structure du projet


---

## 📊 Jeux de données utilisés

### 1️⃣ Dataset principal – Jane Street (anonymisé)
- Données financières réalistes
- Séries temporelles non stationnaires
- Caractéristiques numériques à haute dimension
- Cas d’étude proche du trading algorithmique réel

### 2️⃣ Dataset utilisateur – Craigslist Cars & Trucks
Source : https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data

- Données semi-structurées
- Problèmes de qualité (nulls, catégories incohérentes)
- Cas idéal pour démontrer le nettoyage et la standardisation

---

## 🔁 Idempotence du pipeline

Le pipeline est **entièrement idempotent** :
- Relancer un job **ne corrompt jamais les résultats**
- Écriture partitionnée par `run_date`
- Possibilité d’overwrite ciblé
- Compatibilité avec exécutions incrémentales

---

## ✅ Qualité des données

Des contrôles systématiques sont appliqués :
- Comptage des valeurs nulles
- Détection des doublons
- Vérification des schémas
- Statistiques descriptives
- Validation des clés de jointure

Des rapports de qualité sont générés dans `reports/data_quality/`.

---

## ⚙️ Technologies utilisées

- **Databricks Community Edition**
- **Apache Spark / PySpark**
- **Delta Lake**
- **Parquet**
- **Python**
- **Git & GitHub**
- **LaTeX** (rapport final)

---

## 🚀 Exécution du projet

1. Cloner le dépôt GitHub dans Databricks (Repos)
2. Lancer les notebooks d’ingestion (Bronze)
3. Exécuter les transformations Silver
4. Générer les tables Gold
5. Consulter les rapports et agrégations finales

---

## 🎯 Objectifs pédagogiques et techniques

- Appliquer une architecture Lakehouse complète
- Manipuler de gros volumes de données
- Garantir la qualité et la fiabilité des pipelines
- Optimiser les performances Spark
- Approcher des cas réels de Data Engineering

---

## 📌 Auteur

**Mohamed Dia**  
**NdiogOU DIADIE DIOUF
Data Engineering / Big Data  
Databricks Community Edition

---

## 📄 Licence

Projet à vocation **académique et pédagogique**.  
Les datasets restent soumis à leurs licences respectives.
