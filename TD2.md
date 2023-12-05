# Création d'environnement virtuel et Data Science

## OBJECTIFS

Voici les objectifs de ce cours :
- [x] Comprendre l'importance des environnements virtuels
- [x] Créer des environnements virtuels
- [x] Installer des librairies python
- [x] Exporter et importer un environnement
- [x] Utiliser des librairies de data science

## TD2

Dans ce TD, vous utiliserez le même repository  `iut_sd3_accidents` de la séance précédente. Pour simplifier le versionnement de votre projet, vous pouvez utiliser GitHub Desktop à la place des commandes Git Bash si vous le souhaitez.

### Exercice 1 - Création d'environnement virtuel

Toutes les questions de cet exercice sont à réaliser dans l'invite de commandes. Attention, les commandes peuvent-être différentes si vous n'êtes pas sur un environnement Windows.

1. Ouvrer une fenêtre d'invite de commandes.

2. Vérifier que Python 3 est bien installé sur votre machine avec la commande suivante :
```
python --version
```
ou
```
python -V
```
Si ce n'est pas le cas, installez Python 3

3. Vérifier le chemin d'installation de Python sur votre système avec la commande suivante :
```
where python
```

4. Lister les librairies Python actuellement installées sur votre système avec la commande suivante : 
```
pip list
```

5. Avant d'aller plus loin, un peu de lecture sur l'intérêt de créer en environnement virtuel : [cliquez-ici](https://www.docstring.fr/glossaire/environnement-virtuel)

6. Installer la librairie *`virtualenv`* sur votre environnement Python par défaut avec la commande suivante : 
```
pip install virtualenv
```

7. Vérifier que la librairie est correctement installée  avec la commande suivante : 
```
pip list
```

8. Créer un environnement virtuel appelé `env-accident` avec la commande suivante : 
```
py -m venv env-accident
```
`-m` est une option qui indique à l'interpréteur Python d'exécuter un module en tant que script.

![](media/warning.gif)

Il faut bien penser à changer de chemin et vous positionner dans le dossier où vous souhaitez créer votre environnement virtuel. Voici un exemple : 
```
cd C:\Users\Anthony\Documents\asardell\my_virtual_envs
```

Pour rappel, la commande `cd` pour *change directory* permet de se déplacer de dossier en dossier en changeant le chemin du répertoire courant.
Une fois dans le bon dossier vous pouvez créer votre environnement.
:warning: Ne pas utiliser créer votre environnement virtuel dans votre dossier projet.

### Exercice 2 - Activer son environnement virtuel

Toutes les questions de cet exercice sont à réaliser dans l'invite de commandes. Attention, les commandes peuvent-être différentes si vous n'êtes pas sur un environnement Windows.

1. Avant d'aller plus loin, lire attentivement cette partie du cours de l'exercice 1 : [cliquez-ici](https://www.docstring.fr/glossaire/environnement-virtuel/#comment-activer-un-environnement-virtuel-python)

2. Se déplacer jusqu'au fichier d'activation `activate.bat` de l'environnement avec les commandes suivantes : 
```
cd ./env-accident/Scripts
```
```
activate.bat
```
`./` permet d'éviter de récrire tous le chemin relatif.

3. Vérifier sur votre terminal que l'environnement est bien activé.

![](media/env_activate.PNG)

4. Désactiver votre environnement avec la commande suivante : 
```
deactivate
```
On remarque que l'environnement est désactivé.

5. Activer de nouveau votre environnement et afficher la liste des librairies actuellement installées avec la commande suivante :
```
pip list
```

6. Il y a très peu de librairies, installez les librairies `numpy` et `pandas`. Vérifier avec la commande `pip list`.

7. Exporter votre environnement virtuel dans un fichier appelé *requirements.txt* avec la commande suivante : 
```
pip freeze > requirements.txt
```

Cette commande capture la liste des packages installés avec leurs versions exactes et les enregistre dans un fichier *requirements.txt* qui sera créé dans le **répertoire actuel**.

![](media/warning.gif)

Dans cette question on souhaite enregistrer le fichier *requirements.txt* à la racine de votre repository local.

8. Désactiver votre environnement et fermer le terminal de commande.

9. Créer un autre environnement virtuel appelé `test-env` pour faire un test uniquement dans le cadre de cet exercice.

10. Le fichier *requirements.txt* généré dans la question précédente peut ensuite être partagé avec d'autres personnes ou utilisé pour recréer un environnement Python. Pour installer les dépendances à partir de ce fichier, vous pouvez utiliser la commande suivante :
```
pip install -r requirements.txt
```
:warning: Il faut se placer dans le répértoire où le fichier est présent sinon il sera introuvable.

11. Vérifier que les librairies du fichier *requirements.txt* ont bien été installées sur l'environnement `test-env`.

### Exercice 3 - Utiliser son environnement virtuel dans Visual Studio Code