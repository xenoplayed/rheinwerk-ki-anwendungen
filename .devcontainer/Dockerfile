FROM mcr.microsoft.com/devcontainers/miniconda:1-3

COPY environment.yml* /tmp/conda-tmp/
RUN if [ -f "/tmp/conda-tmp/environment.yml" ]; then umask 0002 && /opt/conda/bin/conda env update -n base -f /tmp/conda-tmp/environment.yml; fi \
    && rm -rf /tmp/conda-tmp

# RUN conda create -m ki_lab -y python=3.11.5 \
#     && conda install -n ki_lab -y numpy pandas matplotlib scikit-learn keras tensorflow jupyter \
#     && conda install -n ki_lab -y ipykernel --update-deps --force-reinstall
