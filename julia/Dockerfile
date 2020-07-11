ARG JULIA_VERSION

FROM jupyter/datascience-notebook:${JULIA_VERSION}

RUN pip install jupyterthemes \
 && jt -cellw 95%

COPY packages.jl /home/jovyan/
RUN julia /home/jovyan/packages.jl

