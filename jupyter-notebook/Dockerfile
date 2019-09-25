FROM jupyter/datascience-notebook:latest

# install pyscipopt
ENV SCIPOPTDIR=/opt/scip

COPY SCIPOptSuite/lib ${SCIPOPTDIR}/lib
COPY SCIPOptSuite/include/scip ${SCIPOPTDIR}/include/scip

RUN pip install pyscipopt
