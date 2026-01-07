# Data Analytics Platform Portfolio

## Technologies & plateformes

- **Cloud data platforms** :  
  GCP BigQuery ![Cloud](https://img.shields.io/badge/Cloud-AWS-FF9900), Azure *(Azure Data Factory, Microsoft Fabric )* ![Cloud](https://img.shields.io/badge/Cloud-Azure-0078D4),  AWS ![Cloud](https://img.shields.io/badge/Cloud-GCP-4285F4)

- **Databases** : PostgreSQL, Snowflake  
  ![Database](https://img.shields.io/badge/Database-PostgreSQL-336791)
  ![Database](https://img.shields.io/badge/Database-Snowflake-56B9EB)

- **Data Transformation** : dbt *(SQL, modélisation analytique, couche analytics)*  
  ![Transformation](https://img.shields.io/badge/Data%20Transformation-dbt-F26C50)

- **Data Visualization** : Power BI, Looker Studio, QlikView / Qlik Sense  
  ![DataViz](https://img.shields.io/badge/DataViz-Power%20BI-F2C811)
  ![DataViz](https://img.shields.io/badge/DataViz-Looker%20Studio-34A853)
  ![DataViz](https://img.shields.io/badge/DataViz-Qlik-00B140)

- **SQL** : analyse, agrégations, modélisation analytique  
  ![SQL](https://img.shields.io/badge/SQL-Analytics-F39C12)


---

## Overview
Ce dépôt regroupe mes projets **Data Analyst** et **BI**, structurés par plateformes et technologies.  
Il présente des cas d’usage proches de missions réelles, depuis l’ingestion de données brutes jusqu’à leur restitution dans des outils de data visualisation.

Une attention particulière est portée à :
- la structuration des données,
- la séparation entre données brutes et données analytiques,
- la centralisation de la logique métier,
- la maintenabilité et l’évolutivité des solutions.

---

## Architecture data (approche entreprise)

Les projets suivent une architecture inspirée des environnements professionnels :
  Sources métier (CSV / exports applicatifs)
  ↓
  PostgreSQL — schéma raw (données brutes)
  ↓
  dbt — transformations & logique métier
  ↓
  PostgreSQL — schéma analytics (données analytiques)
  ↓
  Outils de Data Visualization (Power BI, Looker Studio, Qlik)


Principes clés :
- Les données brutes sont stockées **sans modification** dans un schéma `raw`
- Les transformations sont réalisées **exclusivement via dbt**
- Les données analytiques sont exposées dans un schéma `analytics`
- Les outils de visualisation consomment uniquement la couche analytique

Cette approche garantit traçabilité, sécurité des données sources et évolutivité.

---

## Projets

### 🔹 PostgreSQL / dbt / Data Visualization  
**RH & Planning Analytics (CSV → SQL → BI)**

Mise en place d’une chaîne analytique complète à partir de fichiers CSV RH, avec exposition finale dans un outil de data visualisation.

**Travaux réalisés :**
- Ingestion de données CSV dans PostgreSQL (schéma `raw`)
- Mise en place d’une couche analytique avec dbt (schéma `analytics`)
- Utilisation de dbt en mode *pass-through* pour remplacer les sources CSV dans les dashboards sans refonte des visuels
- Séparation claire entre données brutes et données analytiques
- Centralisation de la logique data hors des outils de visualisation

**Objectif principal :**
- Sécuriser les données sources
- Rendre les dashboards indépendants des fichiers CSV
- Préparer une architecture scalable et réutilisable

📁 Dossier :  
`/postgresql/dbt/powerbi-rh-analytics`

---

### 🔹 Cloud / SQL / Data Visualization  
**E-commerce Customer Analytics**

Analyse d’un dataset e-commerce afin de mesurer la performance business et le comportement client.

**Travaux réalisés :**
- KPI mensuels (chiffre d’affaires, commandes, clients actifs, panier moyen)
- Analyse de cohortes clients
- Étude de la rétention dans le temps
- Visualisations interactives

📁 Dossier :  
`/gcp/bigquery/ecommerce-customer-analytics`

---

### 🔹 Data Visualization *(à venir)*
- Dashboards KPI
- Modélisation BI
- DAX
- Bonnes pratiques de visualisation

---

### 🔹 Databases / Cloud *(à venir)*
- SQL analytique
- Préparation de datasets pour la BI

---

## Structure du dépôt
Le repository est organisé par **plateformes**, puis par **technologies**, afin de refléter une vision globale et cohérente de l’écosystème data moderne.

---

## À propos
Ce portfolio est conçu comme un support de démonstration de compétences en **Data Analytics**, avec une approche orientée métier, qualité des données et clarté de restitution.

📫 Contact :  
- LinkedIn : https://www.linkedin.com/in/jalal-hilal/
- Email : jalal.hilal@hotmail.fr
