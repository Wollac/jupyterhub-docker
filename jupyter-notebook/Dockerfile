FROM jupyter/datascience-notebook:latest

# install pyscipopt
ENV SCIPOPTDIR=/opt/scip

COPY SCIPOptSuite/lib ${SCIPOPTDIR}/lib
COPY SCIPOptSuite/include ${SCIPOPTDIR}/include

RUN pip install pyscipopt
