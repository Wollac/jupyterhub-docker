FROM jupyterhub/jupyterhub:1.0.0

COPY jupyterhub_config.py .

# stop idle servers as a service
ADD https://raw.githubusercontent.com/jupyterhub/jupyterhub/1.0.0/examples/cull-idle/cull_idle_servers.py .

# Install dockerspawner and oauth
RUN pip install --no-cache-dir \
        oauthenticator \
        dockerspawner

# copy user white list
COPY ./userlist /srv/jupyterhub/userlist
