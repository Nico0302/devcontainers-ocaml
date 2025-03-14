FROM ocaml/opam:debian-12-ocaml-5.0

# Ensure we're running as root
USER root

# Install common utilities and debugging tools
RUN apt-get update && apt-get install -y \
    curl \
    git \
    build-essential \
    gdb \
    && rm -rf /var/lib/apt/lists/*

# Switch to opam user for OPAM operations
USER opam

# Move utop-config file into .config/utop/init.ml
RUN mkdir -p /home/opam/.config/utop
COPY utop-config /home/opam/.config/utop/init.ml

RUN opam update && opam install -y \
    dune \
    ocaml-lsp-server \
    earlybird \
    ocamlformat \
    utop

# SHELL ["/bin/bash", "-c"]
WORKDIR /home/opam/workspace