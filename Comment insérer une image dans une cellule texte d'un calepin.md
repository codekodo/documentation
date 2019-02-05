♻️ Attention, ce document est mis à jour reglierement en fonction des remarques et de l'evolution des environements.

Lorsque l'on souhaite insérer une image dans une cellule texte d'un calepin, il n'est pas possible de le faire commen on le ferait avec un docuement Word, LibreOffice ou Google Doc. Les images ne peuvent pas etre imcorporee à la cellule elle-meme. Elles doivent etre placees en dehors du calepin. Le plus smiple est de les conservees dans un espace accessible depuis internet. Plusieurs solutions existent. A vous choisir celle qui vous convient le lieux.

# 1. Syntaxe
Soit une image prsente a l'adresse suivante : https://www.exemple.com/images/image.png
Pour inserer cette image dans une cellule texte d'une calepins, deux syntaxe sont possibles :
- `[description de l'image](https://www.exemple.com/images/image.png)`<br />
Le texte entre crochets est optionel, il ne sert qu'a decrire l'image si jamais l'image ne s'affiche pas. Pour en [savoir plus](https://fr.wikipedia.org/wiki/Alternative_textuelle).
avec cette syntaxe, il n'est pas possible de modifier la taille l'image. Elle s'affichera dans sa taille originale.
- `<img src="https://www.exemple.com/images/image.png" alt="description de l'image" width="50" />`<br />
La balise `alt` est optionelle.
Il est possible de spécifier la largeur de l'image. Le chifree correspond au nombre de pixels. A la place de `width`, il est possible d'utiliser `height` pour definir la hauteur de l'image. Il est aussi possible d'utiliser `width` et `height` en meme temps.

# 2. Conserver les images sur Google Drive
Si vous conservez vos calepins dans un Google Drive, vous pouvez aussi y conserver les images que vous vous voulez utiliser dans les cellules texte de vos calepins. Imaginons que les images sonversees dans le repertoire `Mon Drive > calepins > images`.Et que dans dossier, il y a une image `monimage.png`. L'adresse qui permettra d'inserer cette image dans la cellule texte d'un calepin sera de la forme :<br />
`https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP`

`1OfiLs18cI_omYZ22SjervuaLZeUP` est le code unique d'identication de l'image.

Pour recuper ce code, il suffit :
- d'aller sur le Drive et de naviger jusqu'au répertoire qui contient l'image. Ex. : `Mon Drive > calepins > images`
- faire un clic droit sur l'iamge et de choisir `partager`
- de cliquer en haut à droite de la fenetre qui vient de s'ouvrir sur `Obtenir le lien de partage`.
- de chjsois `Visible : utilisateurs avec le lien`
- de copier ce lien qui est de la forme `https://drive.google.com/file/d/1OfiLs18cI_omYZ22SjervuaLZeUP/view?usp=sharing`
- de coller ce lien, de ne garder que `1OfiLs18cI_omYZ22SjervuaLZeUP`

Ainsi, il sera possible de finir de construire la syntaxe voulue : `[description de l'image](https://drive.google.com/uc?export=view&id=1OfiLs18cI_omYZ22SjervuaLZeUP)`. En collant ce code dans la cellule texte d'un calepin, l'iame apparaitra lorsque vous executerez la cellule.


# 3. Conserver les image sur Imgur
Il est aussi possible d'heberger les images sur des services internet. Il en existe de nombreux. Le plus connu est [Imgur](https://imgur.com/). C'est un site tres populaire auptes des utilisateurs de [Reddit](https://www.reddit.com/). Il n'est pas necessaire de creer un compte sur Imgur pour y heberger des images. Cependant, en creant un compte, vous pourrez mieux organiser vos images.
Etapes pour placer une image sur Imgur et l'inserer dans une ceklue texte d'un calepin :
- 



🔎 Si vous voulez en savoir plus à propos de la syntaxe `markdown` utilisee dans les celleules texte d'un calepin, vous pouvez consulter cette [page](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/Working%20With%20Markdown%20Cells.html).

