# Utilisation de GitHub et Visual Studio Code

## OBJECTIFS

Voici les objectifs de ce cours :
- [x] Créer un compte GitHub
- [x] Télécharger GitBash
- [x] Configurer la connexion en SSH
- [x] Télécharger Visual Studio Code
- [x] Utiliser les commandes usuelles de Git

## TD1

### Exercice 1 - GitHub Online

Toutes les questions de cette exercice sont à réaliser sur la version GitHub online. 

1. Créer un compte sur GitHub si vous n'avez pas encore de compte
1. Créer un repository GitHub **public** appelé `iut_sd3_accidents`sur le workspace online avec un fichier README.md par défaut ([plus d'info ici](https://docs.github.com/fr/repositories/creating-and-managing-repositories/creating-a-new-repository#creating-a-new-repository-from-the-web-ui)).

Pour personnaliser le fichier README.md, vous pouvez vous aider de [ce lien](https://www.markdownguide.org/cheat-sheet/).

1. Modifier le fichier README.md en ajoutant un titre de niveau 2

```
## Titre 2
```
1. La modification sauvegardée apparaît sous la forme d'un `commit`

1. Créer une branche appelée *`votre_prénom`* depuis la branche principale.

1. Dans la branche *`votre_prénom`*, ajouter un fichier *test.py* avec ce bout de code : 
```
## print("hello")
```

1. Créer une branche appelée *`votre_prénom_DEV`* depuis la branche principale.

1. Dans la branche *`votre_prénom_DEV`* ajouter un fichier *test.py* avec ce bout de code : 
```
## print("Hola")
```
Nous avons donc 3 branches : 

- [x] la branche principale *`main`*
- [x] la branche *`votre_prénom`*
- [x] la branche *`votre_prénom_DEV`*

1. Créer une `pull request` de la branche *`votre_prénom`* sur la branche principale *`main`*

1. Merger la `pull request` pour fusionner les branches sans supprimer la branche *`votre_prénom`*. Aucun conflit n'apparaît entre les deux branches.

1. Créer une `pull request` de la branche *`votre_prénom_DEV`* sur la branche principale *`main`*

1. Merger la `pull request` pour fusionner les branches sans supprimer la branche *`votre_prénom_DEV`*. Un conflit apparaît entre les deux branches. Il faut le résoudre en choisissant une des deux syntaxes du fichier *test.py* qui a été créée dans les deux branches *`votre_prénom`* et *`votre_prénom_DEV`* puis en cliquant sur `mark as resolved`. 

### Exercice 2 - Configurer GitHub en local

Dans cet exercice, nous allons utiliser des commandes Git avec GitBash. 

1. Télécharger Git et GitBash
1. Ouvrir GitBash
1. Créer un dossier *`IUT_SD3_Github`* sur votre bureau
1. Ouvrir GitBash et placer vous sur le dossier créée avec : 
```
cd Desktop/IUT_SD3_Github
```
1. Générer la clé SSH avec :
```
ssh-keygen
```
1. Saisir `id_rsa` comme filename pour sauvegarder la clé ssh
1. Entrer une passphrase qui permettra de se connecter à votre compte GitHub à chaque connexion
1. Ajouter la clé en tant que nouvelle clé dans les paramètres de votre compte GitHub online ([voir lien utile](https://linuxhint.com/clone-repo-with-ssh-key-in-git/))

### Exercice 3

1. Installer Python
1. Installer Visual Studio Code
1. 

## LIENS UTILES

Voici quelques liens utiles qui pourrait vous aider durant ce projet :

- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [GitHub Cheat Sheet](https://training.github.com/downloads/fr/github-git-cheat-sheet.pdf)
- [GitHub Get Started](https://docs.github.com/fr/get-started/quickstart/hello-world)
- [GitHub Set up](https://docs.github.com/fr/get-started/quickstart/set-up-git)
- [Bash Cheat Sheet](https://github.com/RehanSaeed/Bash-Cheat-Sheet)
- [Tutoriel GitHub SSH](https://linuxhint.com/clone-repo-with-ssh-key-in-git/)
