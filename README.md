# Data Analytics Platform Portfolio

<!-- Google stack -->
![GCP](https://img.shields.io/badge/GCP-Cloud-4285F4)
![BigQuery](https://img.shields.io/badge/BigQuery-SQL-4285F4)
![Looker](https://img.shields.io/badge/Looker%20Studio-BI-4285F4)

<!-- Microsoft stack -->
![Azure](https://img.shields.io/badge/Azure-Data%20Platform-7B3FE4)
![PowerBI](https://img.shields.io/badge/Power%20BI-Microsoft-7B3FE4)

<!-- Other -->
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791)
![dbt](https://img.shields.io/badge/dbt-Transformations-F26C50)
![Snowflake](https://img.shields.io/badge/Snowflake-Cloud-56B9EB)
![SQL](https://img.shields.io/badge/SQL-Analytics-F39C12)

---

## Overview
Ce dépôt regroupe mes projets **Data Analyst** et **BI**, structurés par plateformes et technologies.  
Il présente des cas d’usage proches de missions réelles, depuis l’ingestion de données brutes jusqu’à leur restitution dans des outils de visualisation.

Une attention particulière est portée à :
- la structuration des données,
- la séparation entre données brutes et données analytiques,
- la centralisation de la logique métier,
- la maintenabilité et l’évolutivité des solutions.

---

## Technologies & plateformes
- **Google Cloud Platform** : BigQuery, Looker Studio  
- **Microsoft** : Power BI, Azure Data Factory *(concepts & architecture)*  
- **PostgreSQL** : base de données analytique  
- **dbt (data build tool)** : transformations SQL et modélisation analytique  
- **Snowflake** *(à venir)*  
- **Qlik** : QlikView / Qlik Sense  
- **SQL** : analyse, agrégations, modélisation analytique

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
  Outils BI (Power BI, Looker Studio, etc.)


- Les données brutes sont stockées **sans modification** dans un schéma `raw`
- Les transformations sont réalisées **exclusivement via dbt**
- Les données analytiques sont exposées dans un schéma `analytics`
- Les outils BI consomment uniquement la couche analytique

Cette approche garantit traçabilité, sécurité des données sources et évolutivité.

---

## Projets

### 🔹 PostgreSQL / dbt / Power BI  
**RH & Planning Analytics (CSV → SQL → BI)**

Mise en place d’une chaîne analytique complète à partir de fichiers CSV RH, avec exposition finale dans Power BI.

**Travaux réalisés :**
- Ingestion de données CSV dans PostgreSQL (schéma `raw`)
- Mise en place d’une couche analytique avec dbt (schéma `analytics`)
- Utilisation de dbt en mode *pass-through* pour remplacer les sources CSV dans Power BI sans refonte des visuels
- Séparation claire entre données brutes et données analytiques
- Centralisation de la logique data hors de Power BI

**Objectif principal :**
- Sécuriser les données sources
- Rendre les dashboards indépendants des fichiers CSV
- Préparer une architecture scalable et réutilisable

📁 Dossier :  
`/postgresql/dbt/powerbi-rh-analytics`

---

### 🔹 GCP — BigQuery / Looker Studio  
**E-commerce Customer Analytics**

Analyse d’un dataset e-commerce afin de mesurer la performance business et le comportement client.

**Travaux réalisés :**
- KPI mensuels (chiffre d’affaires, commandes, clients actifs, panier moyen)
- Analyse de cohortes clients
- Étude de la rétention dans le temps
- Visualisations interactives sous Looker Studio

📁 Dossier :  
`/gcp/bigquery/ecommerce-customer-analytics`

---

### 🔹 Microsoft — Power BI *(à venir)*
- Dashboards KPI
- Modélisation BI
- DAX
- Bonnes pratiques de visualisation

---

### 🔹 Snowflake *(à venir)*
- SQL analytique
- Préparation de datasets pour la BI

---

## Structure du dépôt
Le repository est organisé par **plateformes**, puis par **technologies**, afin de refléter une vision globale et cohérente de l’écosystème data moderne.

---

## À propos
Ce portfolio est conçu comme un support de démonstration de compétences en **Data Analytics**, avec une approche orientée métier, qualité des données et clarté de restitution.

📫 Contact :  
- LinkedIn : *(à ajouter)*  
- Email : *(à ajouter)*

