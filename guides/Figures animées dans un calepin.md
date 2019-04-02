♻️ _Attention, ce document est mis à jour régulièrement en fonction des remarques, des questions et de l'évolution des environnements._

## 1. Introduction
En Python, il est facile de créer des figures animées grâce à Matplotlib et sa fonction `animation`. Des programmes Python qui utilisent cette bibliothèque fonctionneront normalement sur des environnements comme Spyder ou PyCharm. Pour avoir le même rendu avec Jupyter, il est nécessaire de convertir cette animation soit en Javascript, soit en vidéo. Ces conversions se font facilement grâce à deux lignes de codes à ajouter dans le programme :

* pour la conversion Javascript
```python
from IPython.display import HTML
HTML(ani.to_jshtml())
```

* pour la conversion video
```python
from IPython.display import HTML
HTML(anim.to_html5_video())
```

A vous choisir le type de conversion que vous voulez utiliser. Les deux ont des avantages et des inconvénients. La conversion Javascript permet d'avoir, sous la figure, des commandes qui permettent de contrôler le défilement de l'animation. La conversion vidéo permet d'avoir une vidéo que l'on peut afficher en plein écran et que l'on peut télécharger au format `.mp4`. Par contre, pour pouvoir utiliser la conversion vidéo, les codecs `ffmpeg` doivent être présents sur la machine. Si ce n'est pas cas, un message d'erreur apparaitra.

💡 Les exemples ci-dessous sont regroupés dans un calpin qui est consultable sur <kbd>Codekodo</kbd> dans le dossier ["Exemples" - "4. Exemples - Figure Animées"](https://www.codekodo.net/course/50). Les options qui sont présentes sous le titre du calepin vous permettent de visualiser ce calepin, de l'ouvrir directement dans Colaboratory ou Azure Notebooks ou de le télécharger. 

👁️ Si vous voulez directement visualiser le calepin, vous pouvez utiliser ce [lien](https://www.codekodo.net/notebook/50/NC4gRXhlbXBsZXMgLSBGaWd1cmUgQW5pbcOpZXMuaXB5bmI=/aHR0cHM6Ly9naXRodWIuY29tL2NvZGVrb2RvL2NhbGVwaW5zL2Jsb2IvbWFzdGVyLzQuJTIwRXhlbXBsZXMlMjAtJTIwRmlndXJlJTIwQW5pbSVDMyVBOWVzLmlweW5i). Attention, le chargement de la page est un peu long.


## 2. Animation des figures en Javascript
### 2.1. Exemple 1 : sinusoide

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import animation
from IPython.display import HTML

# Définition des paramètes de la figure
fig, ax = plt.subplots()
plt.close()
ax.set_xlim(( 0, 2))
ax.set_ylim((-2, 2))
line, = ax.plot([], [], lw=2)

# fonction initialisation
def init():
    line.set_data([], [])
    return (line,)

# fonction animation appelée séquentiellement
def animate(i):
    x = np.linspace(0, 2, 1000)
    y = np.sin(2 * np.pi * (x - 0.01 * i))
    line.set_data(x, y)
    return (line,)
  
anim = animation.FuncAnimation(fig, animate, init_func=init,
                               frames=100, interval=20, 
                               blit=True)

# conversion javascript
HTML(anim.to_jshtml())
```
### 2.2. Exemple 2 : tangente

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import animation
from IPython.display import HTML

# animate over some set of x, y
x = np.linspace(-4, 4, 100)
y = np.sin(x)

# First set up the figure, the axes, and the plot element
fig, ax = plt.subplots()
plt.close()
ax.set_xlim(( -4, 4))
ax.set_ylim((-2, 2))
line1, = ax.plot([], [], lw=2)
line2, = ax.plot([], [], lw=2)

# initialization function: plot the background of each frame
def init():
    line1.set_data(x, y)      
    return (line1,)
  
# animation function: this is called sequentially
def animate(i):
  at_x = x[i]
  
  # gradient_line will have the form m*x + b
  m = np.cos(at_x)
  b = np.sin(at_x) - np.cos(at_x)*at_x
  gradient_line = m*x + b
  
  line2.set_data(x, gradient_line)
  return (line2,)

anim = animation.FuncAnimation(fig, animate, init_func=init, frames=100, interval=100, blit=True)

# conversion javascript
HTML(anim.to_jshtml())
```

## 3. Animation des figures en vidéo
### 3.1. Exemple 1 : sinusoide

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import animation
from IPython.display import HTML

# Définition des paramètes de la figure
fig, ax = plt.subplots()
plt.close()
ax.set_xlim(( 0, 2))
ax.set_ylim((-2, 2))
line, = ax.plot([], [], lw=2)

# fonction initialisation
def init():
    line.set_data([], [])
    return (line,)

# fonction animation appelée séquentiellement
def animate(i):
    x = np.linspace(0, 2, 1000)
    y = np.sin(2 * np.pi * (x - 0.01 * i))
    line.set_data(x, y)
    return (line,)
  
anim = animation.FuncAnimation(fig, animate, init_func=init,
                               frames=100, interval=20, 
                               blit=True)

# conversion video
HTML(anim.to_html5_video())
```

### 2.2. Exemple 2 : tangente

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib import animation
from IPython.display import HTML

# animate over some set of x, y
x = np.linspace(-4, 4, 100)
y = np.sin(x)

# First set up the figure, the axes, and the plot element
fig, ax = plt.subplots()
plt.close()
ax.set_xlim(( -4, 4))
ax.set_ylim((-2, 2))
line1, = ax.plot([], [], lw=2)
line2, = ax.plot([], [], lw=2)

# initialization function: plot the background of each frame
def init():
    line1.set_data(x, y)      
    return (line1,)
  
# animation function: this is called sequentially
def animate(i):
  at_x = x[i]
  
  # gradient_line will have the form m*x + b
  m = np.cos(at_x)
  b = np.sin(at_x) - np.cos(at_x)*at_x
  gradient_line = m*x + b
  
  line2.set_data(x, gradient_line)
  return (line2,)

anim = animation.FuncAnimation(fig, animate, init_func=init, frames=100, interval=100, blit=True)

# conversion video
HTML(anim.to_html5_video())
```
