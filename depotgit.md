# Premier dépôt sur Github
[Retour à l'énoncé](README.md)

## Récupération des fichiers de l'exercice
Pour récupérer les fichiers fournis pour réaliser l'exercice demandé vous devrez utiliser la commande suivante :
```
git clone URL_de_votre_repository_git
```
`git clone` : Cette commande est utilisée pour créer une copie locale d'un dépôt Git distant. Par exemple, si vous trouvez un projet sur GitHub auquel vous aimeriez contribuer ou que vous voudriez étudier en détail sur votre propre ordinateur, vous pouvez utiliser git clone pour le télécharger.

La commande s'utilise en fournissant l'URL du dépôt que vous souhaitez cloner, comme suit :

```bash
git clone https://github.com/user/repo.git
```
Dans cet exemple, `https://github.com/user/repo.git` serait l'URL du dépôt que vous souhaitez cloner. Git va alors créer une copie locale de ce dépôt dans un sous-répertoire du répertoire courant. Ce sous-répertoire aura par défaut le même nom que le dépôt cloné.

Par exemple, si vous exécutez `git clone https://github.com/user/repo.git` dans votre répertoire personnel, Git créera une copie du dépôt dans un répertoire appelé `repo`.

### Contenu du répertoire
Vous retrouvez dans ce projet les répertoires :  
- le répertoire `.github` : **Répertoire à ne pas utiliser**. C'est un répertoire où se trouvent certains fichiers spécifiques à GitHub.
- le répertoire `__TEST__` : **Répertoire à utiliser plus tard**. Ce répertoire contient les fichiers permettant de réaliser des tests unitaires dans le contexte du développement de projet.
- le répertoire `doc` : **Répertoire à utiliser plus tard**. Ce répertoire contient la documentation sur le code produit.
- le répertoire `dist` : **Répertoire à utiliser**. C'est le répertoire qui contiendra votre projet. L'essentiel de votre production sera dans ce répertoire.
---
et les fichiers suivants :
- `.gitignore` : **Fichier à ne pas éditer**. Ce fichier permet de spécifier quels fichiers ou répertoires le système de contrôle de version Git doit ignorer.
- `package-lock.json` : **Fichier à ne pas éditer**. Ce fichier est généré automatiquement lors de l'installation de vos dépendances npm. Il contient des informations détaillées sur les versions précises de chaque dépendance installée pour votre projet.
- `package.json` : **Fichier à ne pas éditer**. Ce fichier décrit votre projet et ses dépendances.
- `README.md` : **Fichier à ne pas éditer**. Ce fichier permet de documenter le projet. Ici il est utilisé pour fournir l'énoncé. 
- `.eslint.json` : **Fichier à ne pas éditer**. Ce fichier décrit les vérifications qui seront effectuées sur la syntaxe de votre code Javascript.

## Dépôt des fichiers sur GitHub
Une fois les modifications réalisées, le projet peut être déposé sur Github. Voici la séquence de commandes à réaliser.
```
git add .
git commit -m "Intitulé du commit"
git push
```

`git add .` : Cette commande ajoute tous les fichiers modifiés dans le répertoire courant et ses sous-répertoires à l'index de Git. C'est une étape préparatoire pour faire un commit. L'index est l'endroit où Git stocke les fichiers que vous voulez inclure dans votre prochain commit. Le point (.) signifie "le répertoire courant et ses sous-répertoires". Vous pouvez aussi spécifier des fichiers ou répertoires spécifiques au lieu d'un point.

`git commit -m "Intitulé du commit"` : Cette commande crée un nouveau commit avec les modifications que vous avez ajoutées à l'index avec la commande git add. Le commit représente une "photo" de votre projet à un moment donné. L'option -m permet de fournir un message de commit, qui est une brève description des modifications que vous avez apportées. En pratique, "Intitulé du commit" serait remplacé par votre message de commit réel.

`git push` : Cette commande envoie vos commits locaux à un dépôt distant, comme un dépôt sur GitHub.

## Vérification des résultats des tests
Une fois que vous aurez soumis votre travail sur GitHub, des tests automatiques seront déclenchés grâce à un système appelé GitHub Actions. Ces tests sont notamment réalisés par Jest, un framework de test en JavaScript.

Pour vérifier les résultats de ces tests, suivez les étapes ci-dessous :

1. Allez sur la page principale du dépôt sur GitHub.
2. Cliquez sur l'onglet "Actions" situé en haut de la page. Cet onglet donne accès à l'historique des workflows exécutés par GitHub Actions pour ce dépôt.
3. Dans la liste des workflows exécutés, recherchez celui qui correspond à votre dernier commit. Le nom du workflow sera généralement le même que votre message de commit.
4. Cliquez sur le nom du workflow pour voir les détails.
5. Vous verrez une liste des jobs qui ont été exécutés dans le cadre de ce workflow. Si les tests ont réussi, vous verrez une coche verte à côté du job de test. Si les tests ont échoué, vous verrez une croix rouge.
6. Pour plus de détails sur les échecs de test, cliquez sur le job de test échoué. Vous serez alors capable de voir la sortie de console de Jest, qui comprendra des informations sur quels tests ont échoué et pourquoi.

N'oubliez pas que votre but est de faire en sorte que tous les tests réussissent. Si un test échoue, examinez l'erreur, faites les corrections nécessaires dans votre code, et soumettez à nouveau votre travail sur GitHub.
