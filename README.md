# 🐪 OCaml DevContainer

Run OCaml inside a VSCode Development Container.

## Getting Started

To get started with this project, you'll need Docker installed on your machine. The project uses a development container to provide a consistent environment with OCaml-LSP (for editor integration) and debugger support.

### Prerequisites

- Docker
- Visual Studio Code with the Remote - Containers extension

### Setting Up the Development Container

1. Clone the repository to your local machine.
2. Open the project folder in Visual Studio Code.
3. When prompted, reopen the folder in the container. This will build the Docker image defined in the `.devcontainer/Dockerfile` and set up your environment.

### Executing OCaml Scripts

Each OCaml script file is ready for execution in VS Code with full debugger support and OCaml-LSP integration.

- **Run with the debugger:** Open your OCaml script file in VS Code, then go to the Run and Debug pane and start debugging.
- **Run directly from the terminal:** You can also execute an OCaml script via the integrated terminal:
  ```bash
  ocaml myscript.ml
  ```

### Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue with any suggestions or improvements.

### License

This project is licensed under the MIT License. See the LICENSE file for more details.