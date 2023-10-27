FROM mcr.microsoft.com/devcontainers/ruby:1-3.2-bullseye

# Install Rails
RUN su vscode -c "gem install rails webdrivers --no-document"
RUN su vscode -c "/usr/local/rvm/bin/rvm fix-permissions"

# Add some aliases to the Docker image
COPY --chown=vscode:vscode .devcontainer/.bash_aliases /home/vscode/.bash_aliases

# Default value to allow debug server to serve content over GitHub Codespace's port forwarding service
# The value is a comma-separated list of allowed domains 
ENV RAILS_DEVELOPMENT_HOSTS=".githubpreview.dev,.preview.app.github.dev,.app.github.dev"

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment this line to install additional gems.
# RUN su vscode -c "gem install <your-gem-names-here>"
RUN su vscode -c "gem install solargraph rubocop rubocop-rails rubocop-rspec rubocop-performance --no-document"

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1
RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && nvm install --lts" 2>&1