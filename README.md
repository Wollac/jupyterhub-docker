# jupyterhub-docker

jupyterhub-docker provides a simple deployment of [JupyterHub](https://github.com/jupyter/jupyterhub), a multi-user [Jupyter Notebook](http://jupyter.org/) environment, on a single host using [Docker Compose](https://docs.docker.com/compose/).

## Installation

### Configuration

Create the file `.env` in the base folder with the following content:
```
# name for this Docker Compose application, it can be whatever you like
COMPOSE_PROJECT_NAME=jupyter

# user name of the user with admin rights
ADMIN_USER=admin
```
### SCIP

The jupyter-notebook requires a local copy of the [SCIP Optimization Suite](http://scip.zib.de).
Follow the installation instructions [here](jupyter-notebook/README.md) to copy the SCIP Optimization Suite files into the `jupyter-nodebook` folder.

### Docker

Run the following command to update the images and start the hub:
```
docker-compose up -d --build
```
