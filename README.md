# VSCode Ruby On Rails Devcontainer

Setup a Ruby On Rails Development environment in VSCode with devcontainer

[VS Code](https://code.visualstudio.com/), one of the most popular editors/IDEs today, with help from the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension, makes the task of setting up a container for software development easier than ever.

To demonstrate that, we’re going to walk through setting up such an environment for developing Ruby on Rails applications.

## VSCode .devcontainer

A dev container employs a [Docker Container](https://www.docker.com/) as a development environment. With one you can [mount Visual Studio Code (vscode) to a container for development](https://code.visualstudio.com/docs/devcontainers/containers) through the configuration of a [devcontainer.json](https://code.visualstudio.com/docs/devcontainers/containers#_create-a-devcontainerjson-file) file. Visual Studio Code isn't the only application for dev containers, but it is the one I'll cover here.

Development Containers: https://containers.dev
Use pre-made templates: https://containers.dev/templates
For Ruby On Rails and Postgresql: https://github.com/devcontainers/templates/tree/main/src/ruby-rails-postgres

See: https://code.visualstudio.com/docs/devcontainers/create-dev-container
