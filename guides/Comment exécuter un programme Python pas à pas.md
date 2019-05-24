♻️ *Attention, ce document est mis à jour régulièrement en fonction des remarques, des questions et de l'évolution des environnements.*


Pour expliquer aux élèves comment du code Python s'exécute ligne par ligne, il existe un outil très pratique : Python Tutor (http://pythontutor.com).


> "Python Tutor (created by Philip Guo) helps people overcome a fundamental barrier to learning programming: understanding what happens as the computer runs each line of code."

Python Tutor peut être utilisé en ligne à l’adresse suivante : `http://pythontutor.com/visualize.html#mode=edit`.
Mais aussi directement dans un calepin comme expliqué ci-dessous.


## Python Tutor dans un calepin

Pour pouvoir utiliser Python Tutor dans un calepin, il faut tout d'abord importer les bibliothèques. Pour cela on doit créer une première cellule code quand laquelle on place les lignes suivantes : 

```python
!pip install metakernel
from metakernel import register_ipython_magics
register_ipython_magics();
```

Exécutez cette cellule. La liste des bibliothèques s'affiche alors sous la cellule. Une fois que le chargement des bibliothèques est terminé (`Successfully installed metakernel-0.23.0`), pour plus de clarté, vous pouvez effacer le contenu de la console en cliquant sur la croix en haut à gauche (`Clear ouput`).

Dans une seconde cellule, vous pouvez écrite votre code Python en le faisant précéder de la déclaration `%%tutor`.

Exemple :

```python
%%tutor

# code Python
liste = []
for i in range(10):
    liste.append(i ** 2)
```

Une fois la cellule exécutée, une interface de contrôle s'affiche. Cette interface vous permet de visualiser le code, de l'exécuter ligne par ligne, de repérer la ligne qui vient d'être exécutée et la ligne qui sera exécutée lors du pas suivant ainsi que de suivre le remplissage des listes et l'évolution des variables.


## Python Tutor en action

Démo interactive (*attention, le chargement peut être long*) : [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/codekodo/documentation/master?filepath=Comment%2520ex%25C3%25A9cuter%2520un%2520programme%2520Python%2520pas%2520%25C3%25A0%2520pas.ipynb)

<br />
<br />
