# 🐪 OCaml DevContainer

Run OCaml inside a VSCode Development Container.

## Getting Started

To get started with this project, you'll need Docker installed on your machine. The project uses a development container to provide a consistent environment with OCaml-LSP (for editor integration) and debugger support.

### Prerequisites

- Docker
- Visual Studio Code with the Remote - Containers extension

### Setting Up the Development Container

1. Run `>Dev Containers: Clone repository in container volume...` using `CMD+Shift+P` in VS Code
2. Enter `nico0302/devcontainers-ocaml`

### Executing OCaml Code

The repository provides an example `notebook.ml` file which can be run using the following methods:

1. Debug the file using the VS Code `OCaml Debug notebook.ml` configuration.
2. Run the file using `ocaml notebook.ml` in the terminal.

> [!IMPORTANT]
> The debugger is only configured for the `notebook.ml` file. You either need to copy your code into this file to debug it (for testing code snippets) or reconfigure the [dune](https://dune.readthedocs.io/en/stable/quick-start.html) project and `.vscode/launch.json`.

If you want to run small code snippets in your terminal, you can use the [utop](https://github.com/ocaml-community/utop) command:

```bash
utop
```

This is a improved version of the default `ocaml` shell.