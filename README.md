Application web interactive pour l'analyse des derniers épisodes neigeux dans les Alpes

L'application sera accessible : [Lien du site](ttps://huggingface.co/spaces/matrix3364/Derniers_Flocons)
**[► LANCER L'APPLICATION](https://huggingface.co/spaces/matrix3364/Derniers_Flocons)**

Description :

Le projet « Les Derniers Flocons » vise à anticiper l’impact du changement climatique sur l’activité des stations de ski.
En s’appuyant sur des données météorologiques historiques (depuis 1970) et des modèles de prévision,
l’application estime l’évolution future de la neige et de la température afin de prédire les risques de fermeture des stations à une date donnée.
Cette plateforme, développée sous Streamlit, s’adresse principalement aux professionnels de la montagne (gestionnaires de stations, exploitants touristiques)
ainsi qu’aux décideurs publics

Technologies utilisées
•	Python - Pandas - Prophète
•	Streamlit 
•	Plotly - Matplotlib
•	NumPy 

Structure du projet
Derniers_Flocons/
• app.py                 # Application Streamlit principale
• requirements.txt       # Dépendances Python
• README.md              # Documentation du projet
• images                

Données
Les données proviennent de l’API open-meteo.com et couvrent 148 stations de ski situées dans les Alpes françaises.
Elles intègrent des mesures journalières agrégées:\n
- Température moyenne de l’air,\n
- Température du sol (de 0 à -100 cm),\n
- Somme des chutes de neige,\n
- Équivalent en eau des chutes de neige,\n
- Somme des précipitations pluvieuses,\n
- Durée d’ensoleillement,\n
- Vitesse moyenne du vent,\n
- Couverture nuageuse,\n
Des informations sur les stations déjà fermées (incluant leur date de fermeture) ont également été collectées afin d’entraîner un modèle prédictif.\n

***Méthodologie***\n
- Collecte & nettoyage des données.\n
- Scraping des stations de ski (Savoie, Haute-Savoie, Isère).\n
- Récupération des coordonnées GPS et de l’altitude.\n
- Extraction via API des données météorologiques historiques (1970–2024).\n
- Intégration des dates de fermeture pour les stations déjà inactives.\n
- Détection et correction des valeurs aberrantes.\n
  
***Analyse exploratoire***\n
- Étude des tendances saisonnières et climatiques.\n
- Comparaisons par altitude et région.\n

***Modélisation & prévision***\n
- Visualisation de l’évolution climatique station par station.\n
- Modélisation des séries temporelles avec Prophet (températures, neige).\n
- Analyse de survie (survival analysis) pour estimer le risque de fermeture dans le temps.\n




