FROM jupyterhub/jupyterhub:latest

COPY jupyterhub_config.py .

# Install dockerspawner and oauth
RUN pip install --no-cache-dir \
        oauthenticator \
        dockerspawner \
        jupyterhub-idle-culler

# copy user white list
COPY ./userlist /srv/jupyterhub/userlist
