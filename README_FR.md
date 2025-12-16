# Olist:Du Constat Alarmant aux Solutions Data-Driven
## 🌍 Langues disponibles
- 🇬🇧 [English version](README_EN.md)
- 🇫🇷 Français (ce fichier)

## 📊 Introduction

Ce projet a été réalisé dans le cadre du projet de fin de formation (capstone) du bootcamp Data Analytics de Le Wagon, mené sur une période de trois semaines.

L’objectif principal de ce projet est d’analyser le jeu de données e‑commerce Olist afin de :

Explorer le comportement des clients

Comprendre les problématiques de rétention client

Générer des insights pertinents et exploitables

Le projet combine analyse de données, NLP, prévision de séries temporelles et business intelligence, notamment :

Analyse de sentiments des avis clients à l’aide du NLP

Prévision du volume de commandes avec Prophet

Création de tableaux de bord interactifs avec Power BI

🎯 Objectifs du projet

Les principaux objectifs de ce projet sont :

Nettoyer et préparer les données pour l’analyse

Utiliser des techniques de NLP afin de comprendre les causes de la faible rétention client

Appliquer Prophet pour prévoir le volume des commandes sur les cinq prochaines années

Concevoir des tableaux de bord interactifs et pertinents avec Power BI

Fournir des recommandations claires et data‑driven pour améliorer la performance globale d’Olist

## 🗂️ Données Utilisées

Le dataset Olist est composé de neuf fichiers CSV, chacun représentant un aspect différent de la plateforme e‑commerce :

olist_order_items_dataset

olist_orders_dataset

olist_order_payments_dataset

olist_order_reviews_dataset

olist_products_dataset

olist_customers_dataset

olist_sellers_dataset

olist_geolocation_dataset

olist_category_dataset

📘 Dictionnaire de données

Olist fournit un dictionnaire de données clair et bien structuré, décrivant chaque variable présente dans les différentes tables.

Cette documentation [Data dictionary PDF](Data/Data%20dictionary.pdf)


Explique le rôle et la signification de chaque variable

Garantit une interprétation correcte des données

Facilite la compréhension des relations entre les tables

Le dictionnaire de données est essentiel pour réaliser des analyses fiables et cohérentes.

❓ Questions métier
📈 Performance globale

Quel est le chiffre d’affaires total et comment évolue‑t‑il dans le temps ?

Combien de commandes sont reçues et comment ce volume évolue‑t‑il mois par mois ?

Combien de clients et de vendeurs sont actifs sur la plateforme ?

Les commandes sont‑elles livrées à temps ou observe‑t‑on un taux élevé de retards ?

Quel est le niveau de satisfaction client (clients satisfaits vs insatisfaits) ?

Où sont localisés géographiquement les clients ?

🛒 Performance des produits

Quelles catégories de produits génèrent le plus de chiffre d’affaires ?

Combien de produits sont vendus et sur combien de catégories ?

Comment évoluent les volumes de commandes mensuels (2017 vs 2018) ?

Quelle est la valeur moyenne des commandes (AOV) ?

Quels sont les moyens de paiement les plus utilisés par les clients ?

Comment le chiffre d’affaires se compare‑t‑il au nombre de commandes par catégorie de produit ?

🚚 Performance logistique

Quel est le délai moyen de livraison (ADT) et est‑il satisfaisant ?

Quel pourcentage des commandes est livré à temps (OTD) ?

Quel est le coût moyen du transport et quels facteurs l’influencent ?

Comment se répartissent les temps opérationnels (validation, préparation, transport) ?

Existe‑t‑il une corrélation entre le poids des produits et le coût du transport ?

Quels sont les États avec les délais de livraison les plus longs et les plus courts ?

💬 Analyse des sentiments clients (NLP)

Après l’analyse exploratoire et la création des tableaux de bord, nous avons constaté que le taux de rétention client était relativement faible.

Afin d’en comprendre les causes, nous avons mené une analyse de sentiments sur les avis clients, présentée dans le dernier tableau de bord.

Cette analyse met en évidence les principales sources d’insatisfaction, notamment :

Les problèmes de qualité des produits

Les retards de livraison

Les difficultés liées au service client

🔍 Questions clés analysées

Quelles catégories de produits reçoivent le plus d’avis négatifs ?

Quelles sont les principales causes de l’insatisfaction client ?

Quels thèmes dominent dans les avis négatifs (qualité produit, livraison, service client) ?

Quelles catégories sont les plus impactées par les avis négatifs ?

📦 Livrables

Jeux de données nettoyés et structurés

Notebooks d’analyse exploratoire et avancée

Analyse NLP des avis clients

Modèle de prévision des commandes (séries temporelles)

Tableaux de bord interactifs Power BI


## 👥 Équipe Projet

Ce projet a été réalisé dans le cadre du Bootcamp Data Analytics & AI par :

- **Kawtar Jawda**  
- **Khadija Ait ouali**
- **Younes Oubella**
- **Mohammed Amine Regragui**



## 🛠️ Tech Stack

Voici les technologies utilisées pour l'analyse, le nettoyage, la modélisation et la visualisation des données du projet Olist :

### ☁️ **Environnement & Stockage**
- **Google BigQuery** – Stockage des données et exécution des requêtes SQL à grande échelle  
- **Google Colab** – Environnement d’exécution Python pour analyses, visualisations et Machine Learning

### 🗄️ **Langages & Requêtes**
- **SQL** – Exploration, transformations, agrégations, vérification des duplicatas et cohérence des tables

### 📊 **Visualisation & Reporting**
- **Power BI** – Construction de dashboards interactifs (performance produits, logistique, satisfaction client)
- **Matplotlib / Seaborn** – Visualisations analytiques Python

### 🐍 **Python & Data Science**
- **Python** – Analyse exploratoire, visualisations, ML, NLP
- **NumPy** – Manipulations numériques & calculs vectorisés
- **Pandas** – Nettoyage, transformation et analyse des datasets
- **Scikit-learn** – Machine Learning (classification, régression, clustering, LDA)
- **NLTK / spaCy** – NLP, tokenisation, nettoyage textuel
- **Gensim** – Topic Modeling (LDA)

### 🤖 **Modèles**
- **Prophet** – Prévision des commandes  
- **LDA (Latent Dirichlet Allocation)** – Détection des 3 thèmes principaux des clients insatisfaits  
- **Algorithmes ML** – Analyse prédictive et segmentation produit/client  

## 🔍 Analyse effectuée

### ✅ 1. Vérification des valeurs nulles  
Pour chaque table :
- Comptage des valeurs manquantes  
- Visualisation du pourcentage de nulls  
- Décision de nettoyage (drop, imputation, ou correction)

Tables étudiées :
- `orders`
- `order_items`
- `customers`
- `products`
- `sellers`
- `geolocation`
- `Reviews`
- `payement`


### ✅ 2. Vérification des types de colonnes  
Conversion des colonnes au bon format :
- Dates → `datetime`
- Identifiants → `string`
- Montants → `float`
- Catégories → `category`

Objectif : éviter les erreurs d’analyse et permettre des transformations fiables.

  
### ✅ 3. Détection des outliers  

Colonnes sensibles :
- `payment_value`
- `price`
- `freight_value`
- délais de livraison calculés

---
### ✅ 3. Vérification des doublons (duplicates)  
Pour chaque table :  
- Recherche des enregistrements **dupliqués** (par exemple, mêmes `order_id`, `customer_id`, etc.)  
- Comptage du nombre de doublons  
- Suppression ou consolidation des doublons pour garantir l’unicité des enregistrements  

**Tables concernées :**  
`orders`, `order_items`, `customers`, `products`, `sellers`, `geolocation`, `reviews`, `payment`


### ✅ 4. Analyse des dates de la table Orders  
Calcul de la différence entre :
- `order_purchase_timestamp`
- `order_approved_at`
- `order_delivered_carrier_date`
- `order_delivered_customer_date`
- `order_estimated_delivery_date`

Objectif :
➡️ comprendre les retards logistiques  
➡️ détecter les commandes problématiques  
➡️ analyser la satisfaction client potentielle


### ❗ 5. Détection des commandes absentes dans `order_items`
Nous avons identifié :
- commandes présentes dans `orders` mais **sans aucun article**  
→ problème de data entry ou annulation non marquée  
→ distorsion dans les KPIs logistiques et financiers


### ✅  Analyse statistique & Corrélations entre colonnes

Dans la phase de découverte des données, nous avons réalisé une analyse statistique descriptive afin de mieux comprendre les relations entre les variables :

- Calcul des statistiques de base : moyenne, médiane, variance, quantiles.
- Analyse de la distribution des variables numériques (price, freight_value, payment_value, délais…).
- Vérification des corrélations entre colonnes grâce à :
  - une **matrice de corrélation (Heatmap)**,
  - des scatterplots pour visualiser les relations entre variables clés.
- Identification des variables fortement corrélées afin d’éviter la redondance et d’améliorer les modèles prédictifs.

**Objectif :**  
➡️ détecter les relations importantes entre les variables  
➡️ mieux comprendre les facteurs influençant le prix, les délais, la satisfaction client  
➡️ préparer le terrain pour la modélisation (Prophet, ML, etc.)


## 📊 Dashboards & Analyses Avancées

Après le nettoyage complet des tables et la vérification de l’intégrité des données, nous avons construit plusieurs dashboards afin de transformer les observations en insights exploitables pour l’entreprise.

### 🟦 1. Dashboard Global
Ce tableau de bord donne une vision 360° de l’activité Olist :
- volume de commandes par période  
- évolution des revenus  
- répartition géographique  
- performance de livraison  
- taux de satisfaction global  

Objectif : offrir une vue consolidée pour la direction.

---

### 🟩 2. Dashboard Performance Produit
Analyse détaillée des produits :
- Top 5 catégorie vendus  
- Saisonnalité des Commandes
- Répartition des moyens de paiement  
 

Objectif : aider le département commercial & marketing à optimiser l’offre produit.

---

### 🟧 3. Dashboard Logistique
Analyse complète du processus d'expédition :
- Corrélation entre le prix du transport et poids des produits 
-Analyse anomalie du statut des commandes  
- évolution de la répartition des temps opérationnels  
- Carte de délais de livraison selon états / régions du Brésil  

Objectif : identifier les points de friction dans la supply chain.

---

### 🟨 4. Dashboard Satisfaction Client
Dédié à l’expérience client :
- distribution des commandes et satisfaction client
- Top vendeurs selon la note des clients  
- Catégorie produits qui générent l insatisfaction client
-Carte de répartition note des reviews par Région 

Objectif : améliorer la satisfaction client et réduire les plaintes.

---

### 🤖 5. Machine Learning – Modélisation Prédictive
Nous avons développé un modèle de prévision utilisant :
- Prophet   
- variables liées à la saisonnalité  
- retards logistiques  
- valeurs moyennes historiques  

Résultats :
- Prévision des commandes avec projection dans 5 ans.    
- Identification des pics saisonniers  

Objectif : aider l’entreprise à anticiper la demande et ajuster la logistique.

---

## 🎯 Valeur Business du projet
Ce projet fournit à Olist :
- une vision globale de sa performance  
- des insights exploitables pour réduire les retards  
- une amélioration de la satisfaction client  
- une optimisation des produits  
- un modèle prédictif pour la planification  


## 🧠 Analyse NLP – Détection des Thèmes des Clients Insatisfaits (LDA)

Afin de comprendre les principaux motifs d’insatisfaction des clients, une analyse NLP a été réalisée sur les reviews négatives (notes ≤ 3) & le top 5 de catégorie des produits la moins recommandé par les clients.  

Après nettoyage des textes (tokenisation, lemmatisation, suppression des stopwords), un modèle **Latent Dirichlet Allocation (LDA)** a été entraîné.

---
### 🔹 Modèle LDA : Configuration
- **Méthode :** LDA (Latent Dirichlet Allocation) – scikit-learn  
- **Nombre de topics (`n_components`) :** 3  
- **Mesure utilisée :** Probabilités des mots par topic  
- **Objectif :** Identifier les motifs les plus fréquents dans les plaintes clients  

## 🎯 Recommandations Stratégiques

À partir des analyses (qualité produit, délais de livraison, NLP sur les reviews, performance logistique), plusieurs axes d'amélioration ont été identifiés pour améliorer la satisfaction client, réduire les retours et augmenter les ventes.

---

## 🔧 1. Problématique : Mauvaise Qualité & Service Client Faible

Les analyses des reviews négatives et du modèle LDA montrent que **la mauvaise qualité des produits** et **les réponses tardives du service client** et **retards de livraison**  figurent parmi les causes majeures d’insatisfaction.

### ✅ Recommandations

### 📝 **A. Revoir les contrats avec les vendeurs mal classés**
- Identifier les vendeurs avec :
  - taux élevé de retours,
  - produits défectueux,
  - mauvaises évaluations clients.
- Renégocier ou suspendre les partenariats si la qualité n'est pas améliorée.
- Instaurer un score "Seller Quality Index" mis à jour en continu.

### 🤖 **B. Mettre en place un système d’IA pour analyser les feedbacks en temps réel**
- Analyse automatique des commentaires via NLP (LDA, sentiment analysis).
- Détection immédiate des anomalies (augmentation soudaine des plaintes).
- Dashboard en temps réel pour la qualité produit & expérience client.

### 💬 **C. Déployer un Chatbot 24/7 pour les demandes courantes**
- Réponses instantanées pour :
  - Suivi de commande  
  - Politique de retour  
  - Informations produit  
- Réduction de la charge du service client humain.
- Amélioration du temps de résolution (SLA).

---

## 🚚 2. Problématique : Retards de Livraison & Produits Indisponibles

Les données montrent que **les retards de livraison et l’indisponibilité des produits** affectent fortement la satisfaction client et les ventes.

### ✅ Recommandations

### 📦 **A. Court terme : Externalisation partielle de la livraison**
- Utiliser des partenaires logistiques fiables pour les zones à forte demande.
- Réduire les délais et assurer une meilleure traçabilité.

### 🏭 **B. Moyen/Long terme : Créer un Hub Logistique Centralisé**
- Centraliser une partie du stock pour réduire les temps d’acheminement.
- Optimiser l’entreposage et les coûts de transport.
- Meilleur contrôle de la chaîne logistique.

### 📊 **C. Planification intelligente des stocks via Deep Learning**
- Utiliser des modèles (LSTM, Prophet, RNN) pour :
  - Prévoir la demande par catégorie,
  - Anticiper les ruptures,
  - Optimiser les niveaux de stock.
- Réduction des pertes et maximisation de la disponibilité.


➡️ Ces recommandations combinées permettent d'améliorer significativement **la satisfaction client**, **la qualité du service**, et **la performance logistique** d’Olist.


