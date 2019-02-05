♻️ Attention, ce document est mis à jour reglierement en fonction des remarques et de l'evolution des environements.

Lorsque l'on souhaite insérer une image dans une cellule texte d'un calepin, il n'est pas possible de le faire commen on le ferait avec un docuement Word, LibreOffice ou Google Doc. Les images ne peuvent pas etre imcorporee à la cellule elle-meme. Elles doivent etre placees en dehors du calepin. Le plus smiple est de les conservees dans un espace accessible depuis internet. Plusieurs solutions existent. A vous choisir celle qui vous convient le lieux.

## 1. Syntaxe
Soit une image prsente a l'adresse suivante : `https://www.exemple.com/images/image.png`.

Pour inserer cette image dans une cellule texte d'une calepins, deux syntaxe sont possibles :
- `![description de l'image](https://www.exemple.com/images/image.png)`<br />
Le texte entre crochets est optionel, il ne sert qu'a decrire l'image si jamais l'image ne s'affiche pas. C'est ce que l'on appelle une [alternative textuelle](https://fr.wikipedia.org/wiki/Alternative_textuelle).<br />
Avec cette syntaxe, il n'est pas possible de modifier la taille l'image. Elle s'affichera dans sa taille originale.

- `<img src="https://www.exemple.com/images/image.png" alt="description de l'image" width="50" />`<br />
L'alternative textuelle <kbd>alt</kbd> est optionelle.<br />
Avec cette syntaxe, on peut spécifier la largeur de l'image grace à la declaration <kbd>width</kbd>. Le chifree indique est exprime en pixels. A la place de <kbd>width</kbd>, il est possible d'utiliser <kbd>height</kbd> pour definir la hauteur de l'image. Il est aussi possible d'utiliser <kbd>width</kbd> et <kbd>height</kbd> en meme temps.

## 2. Conserver les images sur Google Drive
Si vous conservez vos calepins dans un Google Drive, vous pouvez aussi y conserver les images que vous vous voulez utiliser dans les cellules texte de vos calepins. Imaginons que les images sont conservées dans le dossier <kbd>Mon Drive > calepins > images</kbd>. Et que dans ce dossier, il y a une image <kbd>monimage.png</kbd>. L'adresse qui permet d'utiliser cette image est de la forme :<br />
`https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP`<br />
avec `1OfiLs18cI_omYZ22SjervuaLZeUP`, l'identifiant unique de l'image.

Pour recuper cet identifiant, il faut :
- aller sur le Drive et naviger jusqu'au répertoire qui contient l'image. Ex. : <kbd>Mon Drive > calepins > images</kbd>
- faire un clic droit sur <kbd>monimage.png</kbd> et choisir <kbd>partager</kbd>
- cliquer en haut à droite de la fenetre qui vient de s'ouvrir sur <kbd>Obtenir le lien de partage</kbd>.
- choisois <kbd>Visible : utilisateurs avec le lien</kbd>
- copier ce lien qui est de la forme `https://drive.google.com/file/d/1OfiLs18cI_omYZ22SjervuaLZeUP/view?usp=sharing`
- coller ce lien et ne garder que `1OfiLs18cI_omYZ22SjervuaLZeUP`

Ainsi, il sera possible de finir de construire la syntaxe souhaitée :

`![description de l'image](https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP)`<br />
ou<br />
`<img src="https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP" alt="description de l'image" width="50" />`

Dernière etape : coller ce code à l'endroit voulu dans la cellule texte d'un calepin et executerez la cellule. Le code sera remplacé par l'image.

## 3. Conserver les image sur Imgur
Il est aussi possible d'heberger les images sur des services internet. Il en existe de nombreux. Le plus connu est [Imgur](https://imgur.com/). C'est un site tres populaire auptes des utilisateurs de [Reddit](https://www.reddit.com/). Il n'est pas necessaire de creer un compte sur Imgur pour y heberger des images. Cependant, en creant un compte, vous pourrez mieux organiser vos images.
Etapes pour placer une image sur Imgur et l'inserer dans une ceklue texte d'un calepin :
- aller sur [Imgur](https://imgur.com/)
- cliquer en haut à gauche de la page d'accueil sur <kbd>+ new post</kbd>
- cliquer sur <kbd>browse</kbd> ou faire un glisser-déposer
- attention : ne pas copier le lien qui est presente à droite de l'image
- placer la souris au dessus l'image, cliquer sur le menu deroulant (<i class="material-icons align-middle">keyboard_arrow_down</i>) qui est propose à cote du lien et cliquer sur <kbd>Get share links</kbd>
- une fentre apparait avec quatre propositions de lien; copier le lien <kbd>Markdown (Reddit)</kbd>, il est de la forme :<br />
`[Imgur](https://i.imgur.com/eZdopx.png)`

En remplacant <kbd>Imgur</kbd> par le texte que vous voulez (ou rien) et en ajoutant un point d'exclamation devant, vous obtiendrez le code à inserer dans vos cellule texte :

`![description de l'image](https://i.imgur.com/eZdopx.png)`<br />
ou<br />
`<img src="https://i.imgur.com/eZdopx.png" alt="description de l'image" width="50" />`

Dernière étape : coller ce code à l'endroit voulu dans la cellule texte d'un calepin et executerez la cellule. Le code sera remplacé par l'image.



🔎 Si vous voulez en savoir plus à propos de la syntaxe <kbd>markdown</kbd> utilisee dans les celleules texte d'un calepin, vous pouvez consulter cette [page](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Working%20With%20Markdown%20Cells.html).

