# 📊 Sales Analytics Dashboard

Dashboard interactif d'analyse des ventes construit avec **Streamlit** et **Plotly**, permettant d'explorer les performances commerciales d'un réseau de magasins : évolution des ventes, effet des promotions, comparaison par type de magasin/assortiment, et impact de la concurrence.

## 🎯 Objectif

Fournir un outil de pilotage self-service pour explorer des données de ventes multi-magasins et en tirer des insights exploitables : quels magasins performent, quel est l'effet des promotions et jours fériés, et comment la proximité de la concurrence influence les ventes.

## 🗂️ Données

Le dashboard fusionne deux jeux de données :
- **Ventes journalières** par magasin (ventes, nombre de clients, date, promotions, jours fériés)
- **Caractéristiques des magasins** (type de magasin, niveau d'assortiment, distance à la concurrence, historique des promotions)

## ⚙️ Traitement des données

- Nettoyage et conversion des types (dates, valeurs numériques)
- Traitement des valeurs manquantes (ex. distance à la concurrence imputée par la médiane)
- Création de variables temporelles : année, mois, jour de la semaine, semaine de l'année, indicateur week-end
- Création de variables de décalage (lag) des ventes par magasin, pour analyser les tendances

## 📈 Fonctionnalités du dashboard

Le dashboard est organisé en 8 onglets :

1. **Vue d'ensemble** — KPIs clés (total des ventes, vente moyenne, total et moyenne de clients) + export des données filtrées en CSV
2. **Ventes au fil du temps** — évolution des ventes quotidiennes et mensuelles
3. **Analyse par type & assortiment** — ventes agrégées par type de magasin et par niveau d'assortiment
4. **Promotions & jours fériés** — impact des promotions et des jours fériés sur les ventes
5. **Distance à la compétition** — distribution de la distance des magasins à la concurrence
6. **Analyse des clients** — évolution du nombre de clients dans le temps et par magasin
7. **Corrélations** — matrice de corrélation entre ventes, clients, distance à la concurrence, promotions et week-end
8. **Aperçu des données** — visualisation brute des données filtrées

### Filtres dynamiques (barre latérale)
- Magasin(s)
- Plage de dates
- Type de magasin
- Niveau d'assortiment

## 🛠️ Stack technique

- **Python** (Pandas)
- **Streamlit** — interface web interactive
- **Plotly Express** — visualisations dynamiques

## 🚀 Lancer le projet en local

```bash
git clone https://github.com/nazif96/Sales-Analytics-dashboard.git
cd Sales-Analytics-dashboard
pip install -r requirements.txt
streamlit run Dashboard.py
```

L'application s'ouvre automatiquement dans le navigateur à l'adresse `http://localhost:8501`.

> ℹ️ Les fichiers de données (`data/train.csv` et `data/store.csv`) doivent être présents dans le dossier `data/` à la racine du projet.

## 👤 Auteur

**Nazifou Afolabi** — Data Analyst / BI Analyst Junior
[LinkedIn](#) · [GitHub](https://github.com/nazif96)
