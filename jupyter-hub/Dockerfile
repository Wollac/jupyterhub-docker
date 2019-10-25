FROM jupyterhub/jupyterhub:latest

COPY jupyterhub_config.py .

# stop idle servers as a service
RUN wget https://raw.githubusercontent.com/jupyterhub/jupyterhub/1.0.0/examples/cull-idle/cull_idle_servers.py

# install dockerspawner and oauth
RUN /opt/conda/bin/pip install --no-cache-dir \
        dockerspawner \
        oauthenticator

# copy user white list
COPY ./userlist /srv/jupyterhub/userlist
