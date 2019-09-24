FROM jupyter/datascience-notebook:latest

# Install pyscipopt
ENV SCIPOPTDIR=/opt/scip

COPY scip-opt/lib ${SCIPOPTDIR}/lib
COPY scip-opt/include ${SCIPOPTDIR}/include

RUN pip install pyscipopt

