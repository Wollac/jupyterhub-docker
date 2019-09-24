FROM jupyterhub/jupyterhub:latest

COPY jupyterhub_config.py .

RUN wget https://raw.githubusercontent.com/jupyterhub/jupyterhub/1.0.0/examples/cull-idle/cull_idle_servers.py
RUN pip install dockerspawner
