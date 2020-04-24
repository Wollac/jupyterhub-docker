FROM jupyterhub/jupyterhub:latest

COPY jupyterhub_config.py .

# stop idle servers as a service
ADD https://raw.githubusercontent.com/jupyterhub/jupyterhub/master/examples/cull-idle/cull_idle_servers.py .

# Install dockerspawner and oauth
RUN pip install --no-cache-dir \
        oauthenticator \
        dockerspawner

# copy user white list
COPY ./userlist /srv/jupyterhub/userlist
