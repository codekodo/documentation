♻️ _Attention, ce document est mis à jour régulièrement en fonction des remarques, des questions et de l'évolution des environnements._

Ces dernières années, **Python** a fait son apparition dans les programmes de **Mathématiques** et **Physique-Chimie** et, avec la réforme du Lycée, il a une place de choix dans le programme de la spécialité “**Numérique et Science de l’Informatique - NSI**”. Mettre à disposition des élèves et des enseignants un environnement de développement Python dans un établissement scolaire est généralement une tâche compliquée et gourmande en ressources. Par exemple, l’installation de la distribution Anaconda nécessite une installation poste par poste, des machines robustes, un suivi des mises à jour et une maintenance régulière. Et les élèves qui souhaitent développer sur leur ordinateur personnel vont rencontrer les mêmes contraintes sans avoir généralement l’expertise nécessaire pour les surmonter. De plus, les établissement qui ont fait le choix de s’équiper en Chromebook se retrouvent dans une impasse.

La façon la plus simple de contourner toutes ces contraintes est donc d’utiliser un environnement de développement en ligne.

Il existe des services comme [Repl.it](https://repl.it/) ou [Trinket.io](https://trinket.io/) mais ils ont tendance a devenir payants et ils ne répondent pas toujours aux exigences des programmes.

Cependant, une solution existe : **[Jupyter](https://jupyter.org/)**. Non seulement Jupyter répond à toutes les demandes mais cet environnement offre en plus un type de format de fichier qui permet de créer des supports de cours riches et interactifs : le format “**calepin numérique**” (“notebook” en anglais).

Jupyter et les calepins numériques sont les outils parfaits pour les enseignements qui nécessitent l’inutilisation de Python.
Jupyter est, de plus, un **logiciel libre**.

## 1. Qu'est-ce qu'un calepin
### 1.1. Le format calepin
En informatique, tout fichier est lié à un ou plusieurs logiciels. Par exemple, un fichier Word (en .docx) a besoin du logiciel Word pour pouvoir être modifié. Un fichier PDF (en .pdf) a besoin de PDF Reader (ou d'un logiciel équivalent) pour pouvoir être lu. Un fichier texte (en .txt) a besoin de Notepad, ou de WordPad ou de tout autre logiciel qui est capable de lire et modifier un fichier texte.

Ces logiciels qui permettent de manipuler certains types de fichiers peuvent être des logiciels installés sur un ordinateur et / ou des services en ligne que l'on utilise avec un navigateur web (Chrome, Firefox, Internet Explorer...). Par exemple, les fichiers Word peuvent être utilisés avec l'application Word installée sur l’ordinateur, mais aussi avec sa version en ligne (présente sur un serveur) Word Online que l’on utilise via un navigateur. Certains fichiers ne peuvent être manipulés que via un navigateur. C'est le cas des Google Docs.

Pour pouvoir être créé / modifié / sauvegardé, un fichier a donc besoin d’une application qui est soit installée sur ordinateur, soit installée sur un serveur (et qui nécessite donc l’utilisation d’un navigateur). Certaines applications ne fonctionnent qu’en étant installées sur un ordinateur, d’autres ne peuvent être installées que sur un serveur, enfin d’autres peuvent être installées sur un ordinateur ou un serveur.

Pour les calepins, la logique est la même. Un calepin est un autre type de fichier (en .ipynb), et pour pouvoir manipuler ces fichiers, il faut une application particulière qui est Jupyter. Jupyter peut être installé sur un ordinateur ou sur un serveur et s'ouvre à l'aide d’un navigateur.

Pour résumer : un calepin se crée, se modifie et s’enregistre à l'aide de l’application Jupyter que l'on utilise via un navigateur.

Remarque : les termes « application » et « logiciel » peuvent être considérés ici comme équivalents.

### 2.1. Particularités du format calepin
Le format calepin est un format particulier. Ce n'est pas un simple format texte, ce n'est pas un simple format code, c'est les deux à la fois.

Un calepin se décompose en cellules et il existe deux types de cellules : les cellules "texte" et les cellules "code". Ces cellules se placent les unes en dessous des autres et elles peuvent être réarrangées à volonté.

Dans une cellule "texte", on place du texte. Ce texte peut être mis en page (titres, différents niveaux de sous-titres, paragraphes, gras, italique, liens hypertextes, images, tableaux…) grâce au format "Markdown". Et, point important pour les scientifiques, il est aussi possible d'intégrer du code Latex dans ces cellules.

La combinaison des cellules "texte" et "code" permet donc créer des documents riches, faciles à structurer et interactifs.

Ce format calepin est donc un **format idéal pour la création de supports** de cours, d'exercices, de devoirs… Ces calepins peuvent être aussi facilement partagés.

## 2. Qu'est-ce que Jupyter

Jupyter est un logiciel libre qui existe sous plusieurs formes et dont le nom varie selon qu’il est proposé par exemple par Google, Microsoft ou autres. Le cœur est toujours le même (les fonctionnalités sont identiques) mais sa présentation (interface utilisateur) peut varier légèrement :
* le Jupyter classique, appelé **Jupyter Lab**, tel qu'on le retrouve sur une installation classique de Jupyter
* le Jupyter de Google : **Colaboratory**. Le cœur et les fonctionnalités sont les mêmes que pour un Jupyter classique. Mais l'interface graphique est différente.
* le Jupyter de Microsoft : **Azure Notebook**. Le cœur et les fonctionnalités sont les mêmes que pour un Jupyter classique. L'interface reste très proche de la version classique. Seule la gestion générale des fichiers et des projets diffère.

Quelle que soit la version de Jupyter utilisée, les calepins créés, eux, sont tous identiques et fonctionneront de la même manière sur n'importe quelle version de Jupyter. Par exemple, La seule différence peut se situer au niveau des bibliothèques supplémentaires qui sont installées. Cela dit, si une bibliothèque n'est pas présente de façon native sur le Jupyter que vous utilisez, il est toujours possible de l’ajouter depuis un calepin (voir « Comment ajouter une bibliothèque depuis un calepin »).

## 3. Les différentes interfaces de Jupyter
### 3.1. Le Jupyter Classique - Jupyter Lab
Pour installer cette version de Jupyter sur un ordinateur Windows, vous pouvez utiliser : [www.portabledevapps.net](https://www.portabledevapps.net/jupyter-portable.php)

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/mon-premier-calepin-jupyterlab.png" /></p>

### 3.2. Le Jupyter de Google - Colaboratory
Pour utiliser cette version qui n’existe qu’en ligne vous devez posséder un compte Google.
Adresse : [colab.research.google.com](https://colab.research.google.com)
L’interface est assez éloignée de celle de Jupyter Lab mais le mode d’utilisation et les fonctionnalités restent les mêmes.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/mon-premier-calepin-colaboratory.png" /></p>

### 3.3. Le Jupyter de Microsoft - Azure Notebook
Pour utiliser cette version qui n’existe qu’en ligne, vous devez posséder un compte Microsoft.
Adresse : [notebooks.azure.com](https://notebooks.azure.com)
L’interface est assez proche de celle de Jupyter Lab.

<p align="center"><img src="https://raw.githubusercontent.com/codekodo/documentation/master/guides/mon-premier-calepin-azurenotebook.png" /></p>
