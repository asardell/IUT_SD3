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

Toutes les questions de cette exercice sont à réaliser dans l'invite de commandes. Attention, les commandes peuvent-être différentes si vous n'êtes pas sur un environnement Windows.

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


6. Commencer par un peu de lecture pour comprendre l'utilité des environnements virtuels : [cliquez-ici](https://www.docstring.fr/glossaire/environnement-virtuel)

7. Installer la librairie *`virtualenv`* sur votre environnement Python par défaut avec la commande suivante : 
```
pip install virtualenv
```

8. Vérifier que la librairie est correctement installée  avec la commande suivante : 
```
pip list
```

9. Créer un environnement virtuel avec la commande suivante : 
```
py -m venv virtual-environment-name
```
`-m` est une option qui indique à l'interpréteur Python d'exécuter un module en tant que script.

![](media/warning.gif)

Il faut bien penser à changer de chemin et vous positionner dans le dossier où vous souhaitez créer votre environnement virtuel. Voici un exemple : 
```
cd C:\Users\Anthony\Documents\asardell\my_virtual_envs
```

Pour rappel, la commande `cd` pour *change directory" permet de se déplacer de dossier en dossier en changeant le chemin du répertoire courant.
Une fois dans le bon fichier vous pouvez créer votre environnement.