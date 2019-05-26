https://jupyterhub.readthedocs.io/en/latest/quickstart.html
* Curl
apt-get install curl
* Nodejs & npm
curl -sL https://deb.nodesource.com/setup_10.x | bash
apt-get install -y nodejs
* pip
apt-get install python3-pip
* Jupyter
python3 -m pip install jupyterhub
npm install -g configurable-http-proxy
python3 -m pip install notebook
* config file
jupyterhub --generate-config
jupyterhub -f /etc/jupyterhub/jupyterhub_config.py
Installer JupyterHub service
***
[Unit]
Description=Jupyterhub
[Service]
User=root
ExecStart=/usr/local/bin/jupyterhub -f /etc/jupyterhub/jupyterhub_config.py
[Install]
WantedBy=multi-user.target
***
a mettre dans "/lib/systemd/system/jupyterhub.service"
Reload
> systemctl daemon-reload
Start
> systemctl start jupyterhub
