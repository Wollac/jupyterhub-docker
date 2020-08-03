FROM jupyter/datascience-notebook:latest

# copy the SCIP optimization suite
ENV SCIPOPTDIR=/opt/scip

COPY SCIPOptSuite/lib ${SCIPOPTDIR}/lib
COPY SCIPOptSuite/include ${SCIPOPTDIR}/include

# Install system libraries first as root
USER root

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    libtbb-dev && \
    rm -rf /var/lib/apt/lists/*

USER $NB_UID

RUN /opt/conda/bin/pip install --no-cache-dir \
        pyscipopt
