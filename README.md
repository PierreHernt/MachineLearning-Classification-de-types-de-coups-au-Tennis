# Classification des Coups de Tennis avec Machine Learning

Ce projet vise à classifier différents types de coups de tennis à partir de mesures d'accélération et de gyroscope enregistrées avec un accéléromètre positionné sur le manche d'une raquette.
Pour visualiser le rendu, il faut télécharger le dossier complet, l'extraire et lancer le document htlm **'Resultat.html'**.

## Description du Jeu de Données

Les données (training_dataset_normalise.csv) sont issues de mesures d'accélération et de gyroscope pour différents types de coups de tennis. Chaque coup est représenté par 100 frames de données brutes. Pour les rendre exploitables par les algorithmes de Machine Learning, ces données ont été agrégées en caractéristiques globales calculées pour chaque coup.

### Caractéristiques Calculées

Pour chaque axe (`X`, `Y`, `Z`) de l'accéléromètre et du gyroscope, les métriques suivantes ont été calculées :

- **Mean** : Moyenne des valeurs.
- **Min** : Valeur minimale.
- **Max** : Valeur maximale.
- **SD** : Écart-type.
- **Kurtosis** : Applatissement de la courbe.
- **Skew** : Asymétrie de la courbe.

### Variable Cible

La variable cible, `TypeOfShot`, correspond au type de coup réalisé :
- `0` : Service
- `1` : Coup droit fond de court
- `2` : Revers fond de court
- `3` : Coup droit de volée
- `4` : Revers de volée

## Objectif

L'objectif est de prédire le type de coup (`TypeOfShot`) à partir des caractéristiques calculées.

## Étapes du Projet

1. **Prétraitement des Données** :
   - Transformation des données brutes en caractéristiques globales.
   - Normalisation des variables pour assurer une meilleure performance des modèles.

2. **Sélection du Modèle** :
   - Entraînement et validation des différents modèles de Machine Learning.
   - Comparaison des performances à l'aide de métriques comme l'accuracy et la matrice de confusion.

3. **Évaluation** :
   - Identification du modèle offrant les meilleures performances.
   - Analyse des erreurs de classification.

