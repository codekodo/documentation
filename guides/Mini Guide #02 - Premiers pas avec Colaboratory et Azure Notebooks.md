♻️ _Attention, ce document est mis à jour régulièrement en fonction des remarques, des questions et de l'évolution des environnements._

Ces dernières années, **Python** a fait son apparition dans les programmes de **Mathématiques** et **Physique-Chimie** et, avec la réforme du Lycée, il a une place de choix dans le programme de la spécialité “**Numérique et Science de l’Informatique - NSI**”. Mettre à disposition des élèves et des enseignants un environnement de développement Python dans un établissement scolaire est généralement une tâche compliquée et gourmande en ressources. Par exemple, l’installation de la distribution Anaconda nécessite une installation poste par poste, des machines robustes, un suivi des mises à jour et une maintenance régulière. Et les élèves qui souhaitent développer sur leur ordinateur personnel vont rencontrer les mêmes contraintes sans avoir généralement l’expertise nécessaire pour les surmonter. De plus, les établissement qui ont fait le choix de s’équiper en Chromebook se retrouvent dans une impasse.

La façon la plus simple de contourner toutes ces contraintes est donc d’utiliser un environnement de développement en ligne.

Il existe des services comme [Repl.it](https://repl.it/) ou [Trinket.io](https://trinket.io/) mais ils ont tendance a devenir payants et ils ne répondent pas toujours aux exigences des programmes.

Cependant, une solution existe : **[Jupyter](https://jupyter.org/)**. Non seulement Jupyter répond à toutes les demandes mais cet environnement offre en plus un type de format de fichier qui permet de créer des supports de cours riches et interactifs : le format “**calepin numérique**” (“notebook” en anglais).

Jupyter et les calepins numériques sont les outils parfaits pour les enseignements qui nécessitent l’utilisation de Python.
Jupyter est, de plus, un **logiciel libre**.

## 1. Jupyter et ses différentes interfaces

Jupyter est un logiciel libre qui existe sous plusieurs formes et dont le nom varie selon qu’il est proposé par exemple par Google, Microsoft ou autres. Le cœur est toujours le même (les fonctionnalités sont identiques) mais sa présentation (interface utilisateur) peut varier légèrement :
* le Jupyter classique, appelé Jupyter Lab, tel qu’on le retrouve sur une installation classique de Jupyter
* le Jupyter de Google : Colaboratory. Le cœur et les fonctionnalités sont les mêmes que pour un Jupyter classique. Mais l’interface graphique est différente.
* le Jupyter de Microsoft : Azure Notebook. Le cœur et les fonctionnalités sont les mêmes que pour un Jupyter classique. L’interface reste très proche de la version classique. Seule la gestion générale des fichiers et des projets diffère.

Quelle que soit la version de Jupyter utilisée, les calepins créés, eux, sont tous identiques et fonctionneront de la même manière sur n’importe quelle version de Jupyter.

Dans un établissement scolaire, l'idéal serait de pouvoir installer Jupyter sur un serveur afin de conserver un contrôle total sur la plateforme (contrôle des services mais aussi contrôle des utilisateurs). Cependant, l'installation et la maintenance d'un tel environnement demandent une bonne expertise et des ressources humaines. Si les conditions ne sont pas réunies, il est néanmoins possible de se tourner vers les services en ligne de Google et Microsoft : Colaboratory ou Azure Notebooks.

## 2. Pourquoi Colaboratory ou Azure Notebooks?

**Avantages :**
* services en ligne donc pas d'installation (inutile de solliciter le service IT de l'établissement pour mettre en place l'environnement de travail)
* utilisation possible avec des Chromebooks / tablettes (il n'est pas possible d'installer des environnements de développement "classiques" sur un Chromebook)
* uniformité de l'environnement et des formats (enseignants et élèves travaillent avec les mêmes outils – il est donc facile d'aider les élèves, d'encadrer les classes et de partager les ressources)
* outils intégrés à des environnements "Classroom" (possibilité de mettre automatiquement en place des séquences interactives avec création, modification, partage et évaluation des travaux)
* richesse des outils (toutes les bibliothèques sont préinstallées ou s'installent automatiquement)
* pas de connaissance techniques nécessaires (l'environnement se met automatiques à jour et intègre ainsi les versions les plus stables des outils)
* puissance de calcul indépendante de l'ordinateur utilisé (les calculs sont effectués par le serveur, pas par l'ordinateur)

**Inconvénient :**
* connexion internet nécessaire


## 3. Premiers pas avec Colaboratory
1. Ouvrir un navigateur et saisir l'adresse [https://colab.research.google.com](https://colab.research.google.com)
2. Se connecter au service avec une adresse Gmail (`Sign in` au haut à droite de la page d'accueil)

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-01.png" /></p>

3. Cliquer sur `File` et sélectionner `New Python 3 notebook` pour créer votre premier calepin

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-02.png" /></p>

4. Cliquer sur le titre pour le changer (ne pas modifier l'extension ".ipynb")

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-03.png" /></p>

5. Lors de la création du calepin, une première cellule est présente. Il s'agit d'une cellule "code". Vous pouvez donc saisir du code Python dans cette cellule. Par exemple :

```python
# Code Python
print('mon premier code Python')
```

6. Cliquer sur le bouton `Run cell` à gauche de la cellule ou utiliser la combinaison de touches `Ctrl + Enter`. Ainsi, le code s'exécute et le résultat apparait sous la cellule.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-04.png" /></p>

7. Pour créer une cellule "texte", cliquer sur `TEXT`. Le bouton `TEXT` est présent dans le menu du haut à côté du bouton `CODE`, mais aussi sous une cellule déjà créée (placer la souris sous une cellule pour faire apparaitre les boutons `TEXT` et `CODE`)

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-05.png" /></p>

Pour compléter le calepin, il suffit d'ajouter des cellules "code" et des cellules "texte" et de les organiser correctement (les cellules peuvent être déplacées grâce aux flèches "haut" et "bas") afin d'obtenir un document complet et structuré que vous pouvez ensuite partager via `Classroom` avec les élèves ou des collègues.

Les calepins s'enregistrent automatiquement sur votre `Google Drive` dans le dossier `Colab Notebooks`.

## 4. Premiers pas avec Azure Notebooks
1. Ouvrir un navigateur et saisir l'adresse [https://notebooks.azure.com](https://notebooks.azure.com)
2. Se connecter au service avec l'adresse courriel de votre choix (`Sign In` au haut à droite de la page d'accueil).

Remarque : Colaboratory (un service Google) nécessite une adresse courriel Gmail, alors qu’Azure Notebooks (un service Microsoft) accepte n'importe quelle adresse courriel. Azure Notebooks est donc intéressant pour les établissements qui ne fournissent pas d'adresse Gmail aux élèves et enseignants ou qui ne proposent pas un environnement "G Suite for education".

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-an-01.png" /></p>

3. Cliquer sur `My Projects` et sélectionner `+ New Project` pour créer votre premier projet.

Remarque : Colaboratory gère les calepins indépendamment les uns des autres. Alors qu’Azure Notebooks classe les calepins par "Projet". 

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-an-02.png" /></p>

4. Choisir un nom pour le projet et décider si le projet doit être public. Pour ne pas compliquer la démarche, décocher `Initialize this project with a README`.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-an-03.png" /></p>

5. Sur la page suivante, cliquer sur `+` et sélectionner `Notebook` pour créer le premier Notebook du projet. Le menu déroulant indique aussi qu'il est possible de créer des dossiers pour organiser les calepins au sein du projet. Pour l'instant, ne pas tenir compte de `Blank File` et de `Markdown`. Une fenêtre `Create New Notebook` s'ouvre. Saisir le nom de votre calepin, choisir `Python 3.6` et cliquer sur `New`.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-an-04.png" /></p>

6. Le calepin apparait alors au sein du projet. Cliquer sur le nom du calepin pour l'ouvrir.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-an-05.png" /></p>

7. Lorsque le calepin s'ouvre, une première cellule est présente. Il s'agit d'une cellule "code". Vous pouvez donc saisir du code Python dans cette cellule. Par exemple :

```python
# Code Python
print('mon premier code Python')
```

Cliquer sur le bouton `▶` ou utiliser la combinaison de touches `Ctrl + Enter`. Ainsi, le code s'exécute et le résultat apparait sous la cellule.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/premiers-pas-an-06.png" /></p>

8. Pour créer une nouvelle cellule "texte" ou "code", cliquer sur `+`. Cliquer sur la cellule qui vient de se créer et cliquer sur `Code ⊻`. Le menu déroulant propose alors `Code` ou `Markdown` (équivalent de `TEXT`).

Pour compléter le calepin, il suffit d'ajouter des cellules "Code" et des cellules "Markdown" et de les organiser correctement (les cellules peuvent être déplacées en les sélectionnant et en les faisant glisser avec la souris) afin d'obtenir un document complet et structuré.

Pour enregistrer les calepins, cliquer sur l'icône qui représente une disquette.

Dans le menu de gauche, vous pouvez visualiser tous les fichiers et dossiers de votre projet. Vous pouvez, directement depuis ce menu, créer des nouveaux calepins, de nouveaux dossiers et réorganiser les documents.

Pour vous familiariser davantage avec les calepins, vous pouvez ouvrir les calepins des dossiers "[Python pour la Physique-Chimie en seconde](https://www.codekodo.net/course/60)" ou "[Exemples](https://www.codekodo.net/course/60)" directement dans Colaboratory en cliquant sur les icones `Colaboratory` présentes sous les titres des calepins.
