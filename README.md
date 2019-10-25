# jupyterhub-docker

jupyterhub-docker provides a simple deployment of [JupyterHub](https://github.com/jupyter/jupyterhub), a multi-user [Jupyter Notebook](http://jupyter.org/) environment, on a single host using [Docker Compose](https://docs.docker.com/compose/).

## Installation

### Configuration

-   Configure Docker Compose: Create the file `.env` in the base folder with the following content:
    ```
    # name of Docker network
    DOCKER_NETWORK_NAME=jupyterhub-network

    # name of the traefik docker network
    TRAEFIK_NETWORK=traefik

    # host under which traefik should make jupyter available
    TRAEFIK_HOST=<myhost.mydomain>
    ```

-  Configure `userlist`: Create a `userlist` file in the `jupyter-hub` folder.
   This file contains the list of authorized JupyterHub users specified by their GitHub usernames, and this file should designate at least one `admin` user.
   For example:
   ```
   unrealsoon admin
   kittypuree
   flangefile
   ```

-   Configure GitHub OAuth: You must pass the GitHub OAuth Client ID, Client Secret and OAuth callback url JupyterHub's runtime.
    To do this, add them to an `oauth.env` file in the `secrets` directory of this repository.
    You may need to create both the `secrets` directory and the `oauth.env` file.
    For example, add the following lines in the `oauth.env` file:
    ```
    GITHUB_CLIENT_ID=<github_client_id>
    GITHUB_CLIENT_SECRET=<github_client_secret>
    OAUTH_CALLBACK_URL=https://<myhost.mydomain>/hub/oauth_callback
    ```

### SCIP

The jupyter-notebook requires a local copy of the [SCIP Optimization Suite](http://scip.zib.de).
Follow the installation instructions [here](jupyter-notebook/README.md) to copy the SCIP Optimization Suite files into the `jupyter-nodebook` folder.

### Docker

Run the following command to update the images and start the hub:
```
docker-compose up -d --build
```
