# VSCode Ruby On Rails Devcontainer setup

## Initial project configuration

Getting the initial container configured was rather easy as templates exist for many common development environments.
For my purposes, I started with the [Ruby On Rails template](https://github.com/devcontainers/templates/tree/main/src/ruby-rails-postgres):

1. Ensure you have [Docker Desktop](https://www.docker.com/products/docker-desktop/) or [OrbStack](https://orbstack.dev) installed and running
2. Ensure you also have [Visual Studio Code](https://code.visualstudio.com/) installed and running
3. In a terminal, generate a new folder for your project:
4. Create a project directory: `mkdir rails-dev-container`
5. Navigate into the directory: `cd rails-dev-container`
6. Open the folder in Visual Studio Code: `code .`
7. Install the [Dev Containers Extension](vscode:extension/ms-vscode-remote.remote-containers)
8. Open the Command Palette: `COMMAND + SHIFT + P`
9. Execute Dev Containers: `Add Dev Container Configuration Files`
10. Select `Show all Definitions...`
11. Search for "Rails"
12. Select `Ruby on Rails & Postgres` • [Setup README.md](https://github.com/devcontainers/templates/tree/main/src/ruby-rails-postgres)
13. Select `3.2-bullseye`
14. Select `Ok`. Don't add features here yet.
15. Wait for the Dev Container to start
16. Open `.devcontainer/devcontainer.json`
