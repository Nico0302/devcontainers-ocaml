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
RUN opam update && opam install -y ocaml-lsp-server utop

WORKDIR /home/$USERNAME/workspace