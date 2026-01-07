# Planning Analytics — Power BI

## Contexte
Projet réalisé dans un contexte de **suivi du planning opérationnel**, visant à fiabiliser les indicateurs liés au **temps de travail**, aux **règles RH** et à la **conformité réglementaire**.

Les données provenaient de plusieurs extractions CSV, difficiles à exploiter et à maintenir dans le temps.

---

## Objectifs
- Centraliser et fiabiliser les données RH  
- Faciliter l’analyse du temps de travail et des écarts  
- Fournir des indicateurs clairs et exploitables aux équipes métier  

---

## Approche data
Architecture analytique inspirée des environnements professionnels :

 SharePoint (CSV) → PostgreSQL (raw) → dbt (analytics) → Power BI

- Séparation données brutes / données analytiques  
- Logique métier centralisée hors de Power BI  
- Modèle réutilisable et maintenable  

---

## Réalisations
- Intégration des données dans PostgreSQL  
- Mise en place d’une couche analytique avec dbt  
- Modélisation et mesures DAX sous Power BI  
- Création de dashboards orientés décision  

---

## Technologies
- Power BI  
- PostgreSQL  
- dbt  
- SQL  

---

📌 *Données anonymisées et adaptées à des fins de démonstration.*
