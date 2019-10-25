FROM jupyter/datascience-notebook:latest

# copy the SCIP optimization suite
ENV SCIPOPTDIR=/opt/scip

COPY SCIPOptSuite/lib ${SCIPOPTDIR}/lib
COPY SCIPOptSuite/include ${SCIPOPTDIR}/include

RUN /opt/conda/bin/pip install --no-cache-dir \
        pyscipopt
