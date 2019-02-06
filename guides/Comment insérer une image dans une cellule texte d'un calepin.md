♻️ Attention, ce document est mis à jour régulièrement en fonction des remarques et de l'évolution des environnements.

Lorsque l'on souhaite insérer une image dans une cellule texte d'un calepin, il n'est pas possible de le faire comment on le ferait avec un document Word, LibreOffice ou Google Doc. Les images ne peuvent pas être incorporées à la cellule elle-même. Elles doivent être placées en dehors du calepin. Le plus simple est de les conserver dans un espace accessible depuis internet. Plusieurs solutions existent. A vous choisir celle qui vous convient le mieux.

## 1. Syntaxe
Soit une image présente à l'adresse suivante  : `https://www.exemple.com/images/monimage.png`.

Pour insérer cette image dans une cellule texte d'un calepin, deux syntaxes sont possibles :
- `![description de l'image](https://www.exemple.com/images/monimage.png)`<br />
Le texte entre crochets est optionnel, il ne sert qu'à décrire l'image si jamais l'image ne s'affiche pas. C'est ce que l'on appelle une [alternative textuelle](https://fr.wikipedia.org/wiki/Alternative_textuelle).<br />
Avec cette syntaxe, il n'est pas possible de modifier la taille l'image. Elle s'affichera dans sa taille originale.

- `<img src="https://www.exemple.com/images/monimage.png" alt="description de l'image" width="50" />`<br />
L'alternative textuelle <kbd>alt</kbd> est optionnelle.<br />
Avec cette syntaxe, on peut spécifier la largeur de l'image grâce à la déclaration <kbd>width</kbd>. Le chiffre indiqué est exprimé en pixels. A la place de <kbd>width</kbd>, il est possible d'utiliser <kbd>height</kbd> pour définir la hauteur de l'image. Il est aussi possible d'utiliser <kbd>width</kbd> et <kbd>height</kbd> en même temps.

## 2. Conserver les images sur Google Drive
Si vous conservez vos calepins dans un Google Drive, vous pouvez aussi y conserver les images que vous vous voulez utiliser dans les cellules texte de vos calepins. Imaginons que les images soient conservées dans le dossier <kbd>Mon Drive > calepins > images</kbd>. Et que dans ce dossier, il y a une image <kbd>monimage.png</kbd>. L'adresse qui permet d'utiliser cette image est de la forme :<br />
`https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP`<br />
avec `1OfiLs18cI_omYZ22SjervuaLZeUP`, l'identifiant unique de l'image.

Pour récupérer cet identifiant, il faut :
- aller sur le Drive et naviguer jusqu'au répertoire qui contient l'image. Ex. : <kbd>Mon Drive > calepins > images</kbd>
- faire un clic droit sur <kbd>monimage.png</kbd> et choisir <kbd>partager</kbd>
- cliquer, en haut à droite de la fenêtre qui vient de s'ouvrir, sur <kbd>Obtenir le lien de partage</kbd>.
- choisir <kbd>Visible : utilisateurs avec le lien</kbd>
- copier ce lien qui est de la forme `https://drive.google.com/file/d/1OfiLs18cI_omYZ22SjervuaLZeUP/view?usp=sharing`
- coller ce lien et ne garder que `1OfiLs18cI_omYZ22SjervuaLZeUP`

Ainsi, il sera possible de finir de construire la syntaxe souhaitée :

`![description de l'image](https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP)`<br />
ou<br />
`<img src="https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP" alt="description de l'image" width="50" />`

Dernière étape : coller ce code à l'endroit voulu dans la cellule texte d'un calepin et exécutez la cellule. Le code sera remplacé par l'image.

## 3. Conserver les images sur Imgur
Il est aussi possible d'héberger les images sur des services internet. Il en existe de nombreux. Le plus connu est [Imgur](https://imgur.com/). C'est un site très populaire auprès des utilisateurs de [Reddit](https://www.reddit.com/). Il n'est pas nécessaire de créer un compte sur Imgur pour y héberger des images. Cependant, en créant un compte, vous pourrez mieux organiser vos images.
Etapes pour placer une image sur Imgur et l'insérer dans une cellule texte d'un calepin :
- aller sur [Imgur](https://imgur.com/)
- cliquer en haut à gauche de la page d'accueil sur <kbd>+ new post</kbd>
- cliquer sur <kbd>browse</kbd> ou faire un glisser-déposer
- attention : ne pas copier le lien qui est présente à droite de l'image
- placer la souris au-dessus l'image, cliquer sur le menu déroulant (<i class="material-icons align-middle">keyboard_arrow_down</i>) qui est proposé à côté du lien et cliquer sur <kbd>Get share links</kbd>
- une fenêtre apparait avec quatre propositions de lien ; copier le lien <kbd>Markdown (Reddit)</kbd>, il est de la forme :<br />
`[Imgur](https://i.imgur.com/eZdopx.png)`

En remplaçant <kbd>Imgur</kbd> par le texte que vous voulez (ou rien) et en ajoutant un point d'exclamation devant, vous obtiendrez le code à insérer dans votre cellule texte :

`![description de l'image](https://i.imgur.com/eZdopx.png)`<br />

Et vous pouvez aussi contruire le code : <br />
`<img src="https://i.imgur.com/eZdopx.png" alt="description de l'image" width="50" />`

Dernière étape : coller le code à l'endroit voulu dans la cellule texte d'un calepin et exécutez la cellule. Le code sera remplacé par l'image.

🔎 Si vous voulez en savoir plus à propos de la syntaxe <kbd>markdown</kbd> utilisée dans les cellules texte d'un calepin, vous pouvez consulter cette [page](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Working%20With%20Markdown%20Cells.html).
