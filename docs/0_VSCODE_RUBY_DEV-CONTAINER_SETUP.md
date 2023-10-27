# VSCode Ruby Devcontainer setup

## Initial project configuration

Getting an initial Ruby container configured was rather easy as templates exist for many common development environments.

1. Ensure you have [Docker Desktop](https://www.docker.com/products/docker-desktop/) or [OrbStack](https://orbstack.dev) installed and running
2. Ensure you also have [Visual Studio Code](https://code.visualstudio.com/) installed and running
3. In a terminal, generate a new folder for your project:
4. Create a project directory: `mkdir ruby-dev-container`
5. Navigate into the directory: `cd ruby-dev-container`
6. Open the folder in Visual Studio Code: `code .`
7. Install the [Dev Containers Extension](vscode:extension/ms-vscode-remote.remote-containers)
8. Open the Command Palette: `COMMAND + SHIFT + P`
9. Execute Dev Containers: `Add Dev Container Configuration Files`
10. Select `Show all Definitions...`
11. Search for "Ruby"
12. Select `Ruby`
13. Select `3.2-bullseye`
14. Select `Ok`. Don't add features here yet.
15. Wait for the Dev Container to start
16. Open `.devcontainer/devcontainer.json`

From there you should be up and running with a terminal and Ruby pre-installed.
