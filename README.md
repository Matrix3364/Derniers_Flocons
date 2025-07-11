Application web interactive pour l'analyse des derniers épisodes neigeux dans les Alpes

L'application sera accessible : [Lien du site](ttps://huggingface.co/spaces/matrix3364/Derniers_Flocons)
**[► LANCER L'APPLICATION](https://huggingface.co/spaces/matrix3364/Derniers_Flocons)**

***Description***
Le projet « Les Derniers Flocons » vise à anticiper l’impact du changement climatique sur l’activité des stations de ski.
En s’appuyant sur des données météorologiques historiques (depuis 1970) et des modèles de prévision,
l’application estime l’évolution future de la neige et de la température afin de prédire les risques de fermeture des stations à une date donnée.
Cette plateforme, développée sous Streamlit, s’adresse principalement aux professionnels de la montagne (gestionnaires de stations, exploitants touristiques)
ainsi qu’aux décideurs publics

***Technologies utilisées***
•	Python - Pandas - Prophète
•	Streamlit 
•	Plotly - Matplotlib
•	NumPy 

***Structure du projet***
Derniers_Flocons/
• app.py                 # Application Streamlit principale
• requirements.txt       # Dépendances Python
• README.md              # Documentation du projet
• images                

***Données***
Les données proviennent de l’API open-meteo.com et couvrent 148 stations de ski situées dans les Alpes françaises.
Elles intègrent des mesures journalières agrégées:
- Température moyenne de l’air,
- Température du sol (de 0 à -100 cm),
- Somme des chutes de neige,
- Équivalent en eau des chutes de neige,
- Somme des précipitations pluvieuses,
- Durée d’ensoleillement,
- Vitesse moyenne du vent,
- Couverture nuageuse,
Des informations sur les stations déjà fermées (incluant leur date de fermeture) ont également été collectées afin d’entraîner un modèle prédictif.

***Méthodologie***
- Collecte & nettoyage des données.
- Scraping des stations de ski (Savoie, Haute-Savoie, Isère).
- Récupération des coordonnées GPS et de l’altitude.
- Extraction via API des données météorologiques historiques (1970–2024).
- Intégration des dates de fermeture pour les stations déjà inactives.
- Détection et correction des valeurs aberrantes.
  
***Analyse exploratoire***
- Étude des tendances saisonnières et climatiques.
- Comparaisons par altitude et région.

***Modélisation & prévision***
- Visualisation de l’évolution climatique station par station.
- Modélisation des séries temporelles avec Prophet (températures, neige).
- Analyse de survie (survival analysis) pour estimer le risque de fermeture dans le temps.




