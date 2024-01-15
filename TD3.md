# Introduction à Azure et Databricks

## OBJECTIFS

Voici les objectifs de ce cours :
- [x] Créer une souscription étudiante sur Azure
- [x] Comprendre l'intérêt du cloud dans le secteur data
- [x] Connaître les fonctionnalités de base de Databricks
- [x] Créer des modèles de data science dans Databricks

## TD3

### Get Started

1. Créer un cluster avec les configurations ci-dessous :
- Name : SD3_cluster
- Policy : Unrestricted
- Single node
- Access mode : No isolation shared
- Databricks Runtime Version : 14.2 ML (Spark 3.5.0, Scala 2.12)
- Ne pas utiliser Photon Acceleration
- Node type : Standard DS3 v2 14GB Memory, 4 Cores
- Terminate after 30 min of inactivity
   
2. Importer et utiliser le notebook databricks pour tester des modèles de data science (knn et arbre) sur les données iris
- Sauvegarder un modèle de KNN et un modèle d'arbre de décision

### Accidents de la route

1. Tester le notebook avec les commandes utiles

2. Importer les 4 fichiers csv d'accidents en tant que table dans un notebook databricks

3. Merger les 4 fichiers dans un autre notebook databricks et exporter la table de résultat dans une nouvelle table

4. S'aider du [tutoriel d'Ilyes Talbi de la revue IA](https://larevueia.fr/xgboost-vs-random-forest-predire-la-gravite-dun-accident-de-la-route/) pour tester des modèles de prédictions avec les méthodes de KNN, Arbre de décision, Régression logistique et Ramdom Forest.

5.  Pour les méthodes de KNN et arbre de décision, utilisez la méthode GridSearch de scikit-learn pour trouver les meilleurs paramètres de chaque type de modèle.

6.  Construire dans un seul graphique, une courbe ROC pour chaque type de modèle

7.  Inscrire le modèle retenu dans databricks

## LIENS UTILES

- [Tutoriel d'Ilyes Talbi de la revue IA](https://larevueia.fr/xgboost-vs-random-forest-predire-la-gravite-dun-accident-de-la-route/)
- [Qu’est-ce que l’écosystème Hadoop ?](https://www.databricks.com/fr/glossary/hadoop-ecosystem)
- [Qu'est-ce qu'un cluster Hadoop ?](https://www.databricks.com/fr/glossary/hadoop-cluster)
- [Qu'est-ce qu'Apache Spark ?](https://www.databricks.com/fr/glossary/what-is-apache-spark)
