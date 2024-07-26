# Naive-Bayes-Classifier
Projet Classification Naïve Bayésienne (IRIS)

## Objectifs du Projet

L'objectif de ce projet est de mettre en œuvre un classificateur Naïve Bayes pour classifier les données du célèbre dataset Iris. Ce projet vise à démontrer comment le modèle Naïve Bayes peut être utilisé pour des tâches de classification en exploitant les caractéristiques des données et les probabilités conditionnelles. Les étapes du projet comprennent une étude mathématique préalable et l'implémentation pratique du modèle.

## Études Mathématiques

Avant d'implémenter le classificateur Naïve Bayes, une étude approfondie des concepts mathématiques est réalisée pour comprendre le théorème de Bayes et les probabilités conditionnelles. Cette section couvre :

- **Rappel de Probabilités** : Propriétés, indépendance des événements, conditionnement, formule de probabilités totales.
- **Variables Aléatoires** : Définition, types de variables aléatoires (discrètes et continues), exemples concrets.
- **Probabilités Conditionnelles** : Définition, théorème de Bayes, indépendance des événements.
- **Classification Naïve de Bayes** : Hypothèse naïve de Bayes, Vraisemblance, application

## Implémentation Pratique

### 1. Chargement et Exploration des Données

Le projet commence par le chargement du dataset Iris à l'aide de la bibliothèque `sklearn`. Le dataset contient des informations sur trois types de fleurs d'iris, décrites par quatre caractéristiques : longueur et largeur des sépales, longueur et largeur des pétales. Les données sont ensuite séparées en ensembles d'entraînement et de test en utilisant la méthode `train_test_split` de `sklearn`. Une stratification est utilisée pour s'assurer que chaque classe est proportionnellement représentée dans les deux ensembles.

### 2. Méthode Manuelle

#### 2.1 Calcul des Probabilités A Priori et Statistiques des Attributs

Les probabilités a priori pour chaque classe sont calculées à partir des données d'entraînement. Ces probabilités représentent la proportion de chaque classe dans l'ensemble d'entraînement. Ensuite, les moyennes et variances des attributs pour chaque classe sont calculées. Ces statistiques sont nécessaires pour modéliser les distributions gaussiennes des caractéristiques continues.

#### 2.2 Implémentation de la Densité de Probabilité Gaussienne

La fonction de densité de probabilité gaussienne est implémentée pour calculer la probabilité d'une caractéristique donnée une classe, en utilisant les moyennes et variances précédemment calculées. La probabilité conditionnelle de chaque classe donnée les valeurs des caractéristiques d'une nouvelle instance est alors calculée. La classe avec la plus haute probabilité conditionnelle est choisie comme prédiction.

#### 2.3 Évaluation des Performances et Prédiction pour de Nouvelles Instances

Les performances du modèle sont évaluées en comparant les prédictions avec les classes réelles des données de test. La précision du modèle est calculée pour mesurer son efficacité. Le projet inclut également une fonctionnalité permettant de saisir les valeurs des caractéristiques pour une nouvelle instance et de prédire sa classe. Les probabilités conditionnelles et les densités de probabilité sont également affichées pour cette nouvelle instance.

### 3. Méthode d'entraînement du modèle avec Scikit-Learn

Scikit-Learn offre une implémentation simple et efficace du classificateur Naïve Bayes. En utilisant la classe `GaussianNB`, nous pouvons entraîner notre modèle avec quelques lignes de code.

