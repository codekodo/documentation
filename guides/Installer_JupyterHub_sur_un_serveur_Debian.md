Executer les commandes suivantes dans une console avec les droits administrateur afin d'installer, sur un serveur Debian, JupyterHub avec une interface JupyterLab.

## Curl

<kbd>apt-get install curl</kbd>

## Nodejs & npm

<kbd>curl -sL https://deb.nodesource.com/setup_12.x | bash</kbd>

<kbd>apt-get install -y nodejs</kbd>

## PIP

<kbd>apt-get install python3-pip</kbd>

## JupyterHub

<kbd>python3 -m pip install jupyterhub</kbd>

<kbd>npm install -g configurable-http-proxy</kbd>

<kbd>python3 -m pip install notebook</kbd>

## Configuration

<kbd>jupyterhub --generate-config</kbd>

<kbd>jupyterhub -f /etc/jupyterhub/jupyterhub_config.py</kbd>

## Interface Jupyter Lab

<kbd>pip3 install jupyterlab</kbd>

<kbd>jupyter labextension install @jupyterlab/hub-extension</kbd>

Dans `jupyterhub_config.py`, ajouter :
```
c.Spawner.cmd = ['jupyter-labhub']
c.Spawner.default_url = '/lab'
```

## Service JupyterHub

A jouter dans `/lib/systemd/system/jupyterhub.service` :
```
[Unit]
Description=Jupyterhub
[Service]
User=root
ExecStart=/usr/local/bin/jupyterhub -f /etc/jupyterhub/jupyterhub_config.py
[Install]
WantedBy=multi-user.target
```

**Démarrer le service**

<kbd>systemctl start jupyterhub</kbd>

**Redémarrer le service**

<kbd>systemctl daemon-reload</kbd>

*Documentation officielle* : https://jupyterhub.readthedocs.io/en/latest/quickstart.html
