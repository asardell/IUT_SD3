# Examen - Créer et héberger un modèle prédictif

Voici les modalités de l'examen : 

- Durée : 3h
- Documents autorisés et accès internet
- Travail individuel
- Restitution sur un repository GitHub et avec un accès partagé sur Azure
- Les ressources **mal nommées** ne seront pas évaluées.
- L'ensemble du sujet est disponible sur ce repository GitHub.
- Respecter bien les consignes et aider vous des liens utiles
- Penser à documenter votre code avec des titres, sous-titres et commentaires.

Les données de l'examen portent sur les accidents de la route. Le sujet a été abordé dans les premières sessions. L'objectif est d'importer les données dans databricks afin de construire un modèle  hébergé. 

## Azure /3

1. Créer un groupe de ressources nommé `votre-nom-iut-sd3-exam` (exemple : `dupont-iut-sd3-exam`) localisé en `North Europe`.

2. M'assigner un rôle `Owner` sur votre groupe de ressource pour me permettre d'évaluer le projet.  

3. Créer une instance Azure Databricks dans ce groupe de ressource avec les configurations suivantes : 
    - `Workspace name` : *votre-nom-iut-sd3-databricks*
    - `Region` : *North Europe*
    - `Pricing Tier` : *Premium (+ Role-based access controls)*
 
## Databricks /12

1. Créer un cluster avec les configurations ci-dessous :
    - `Name` : iut_sd3_exam
    - `Policy` : Unrestricted
    - `Single` node
    - `Access mode` : No isolation shared
    - `Databricks Runtime Version` : 14.2 **ML** (Spark 3.5.0, Scala 2.12)
    - :warning: Ne pas utiliser Photon Acceleration
    - `Node type` : Standard DS3 v2 14GB Memory, 4 Cores
    - `Terminate after` : 60 min of inactivity

2. Importer les données dans Databricks

3. Créer un notebook nommée `Modelisation` dans le dossier *Shared* du workspace de Databricks

4. Suivre toutes les étapes de *Pre Processing* du [Tutoriel d'Ilyes Talbi de la revue IA](https://larevueia.fr/xgboost-vs-random-forest-predire-la-gravite-dun-accident-de-la-route/).

5. Construire l'échantillon *train* et *test* avec **10%** des données pour l'apprentissage.

6. Construire un modèle de `KNeighborsClassifier`. Pour trouver les meilleurs paramètres d'un modèle, utilisez la commande `GridSearchCV` pour optimiser le paramètre `n_neighbors`.

7. Construire un modèle de `DecisionTreeClassifier`. Utilisez la commande `GridSearchCV` pour optimiser les paramètres :
    - `max_depth`
    - `min_samples_leaf`

8. Construire un modèle de `RandomForestClassifier`. Utilisez la commande `GridSearchCV` pour optimiser les paramètres :
    - `n_estimators`
    - `max_depth`
    - `min_samples_leaf`

9. Calculer les métriques (accuracy, f1-score) du meilleur modèle de chaque méthode pour comparer leur performance en vous aidant du tutoriel.

10. Inscrire un des 3 meilleurs modèles dans Databricks en le nommant `BestModel`.

11. Créer un point de terminaison pour hébérger votre modèle.

12. Créer un token afin de pouvoir consommer l'API de votre modèle. Définir le délai d'expiration à **30 jours**.

13. Créer un deuxième notebook nommée `Test API` dans le dossier *Shared* du workspace de Databricks dans lequel il est possible de tester votre modèle avec des exemples d'accidents.


## Repository /5

Toutes les questions de cette exercice sont à réaliser sur la version GitHub online. 

1. Créer un compte sur GitHub **si vous n'avez pas encore de compte**.

2. Créer un repository GitHub **public** appelé `Databricks-Accidents-Project` en **ajoutant un fichier README.md par défaut**.

3. Uploader les deux notebooks Databricks au format `dbc`

4. Documenter le fichier README.md en présentant : 
    - une présentation du projet
    - les sources des données (cf : Ilyes Talbi )
    - les éléments de votre repository
    - le modèle retenu et ses performances
    - le lien de l'endpoint du modèle

## Restitution du projet

- :warning: M'assigner un rôle `Owner` sur votre groupe de ressource pour me permettre d'évaluer le projet
- :warning: M'envoyer un mail sur `********@hotmail.fr` **avec** comme objet **IUT SD3 - Projet Databricks** et en précisant le lien de votre repository GitHub

## LIENS UTILES

- [Assigner un rôle à un utilisateur](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal?tabs=delegate-condition)
- [Tutoriel d'Ilyes Talbi de la revue IA](https://larevueia.fr/xgboost-vs-random-forest-predire-la-gravite-dun-accident-de-la-route/)
- [Limitation des regions dans Databricks](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/model-serving/model-serving-limits)
- [Création d'un token avec Databricks](https://docs.databricks.com/en/dev-tools/cli/authentication.html)
- [Création d'un endpoint avec Databricks](https://docs.databricks.com/en/machine-learning/model-serving/create-manage-serving-endpoints.html)
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [GitHub Get Started](https://docs.github.com/fr/get-started/quickstart/hello-world)
- [Plus d'info sur la commande GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
