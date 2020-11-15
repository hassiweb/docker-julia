ARG JULIA_VERSION

FROM jupyter/datascience-notebook:${JULIA_VERSION}

ENV DEBIAN_FRONTEND=noninteractive

# Install Jupyter theme
RUN pip install jupyterthemes \
 && jt -t monokai -T -N -ofs 11 -f inconsolata -tfs 11 -cellw 95%  # use dark mode with monokai theme

# Install Qt5 to display graphs
USER root
RUN apt-get update \
 && apt-get install -yq qt5-default

# Install Julia packages
USER jovyan
WORKDIR /home/jovyan
COPY packages.jl /home/jovyan/
RUN julia /home/jovyan/packages.jl
