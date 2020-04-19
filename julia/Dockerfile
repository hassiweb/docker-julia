ARG JULIA_VERSION

FROM jupyter/datascience-notebook:${JULIA_VERSION}

COPY packages.jl /home/jovyan/

RUN julia /home/jovyan/packages.jl

