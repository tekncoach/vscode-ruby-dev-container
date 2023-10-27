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
17. Enable the `"forwardPorts"` option by uncommenting the property
18. Open `.devcontainer/Dockerfile`
19. Edit the last line with `RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && nvm install --lts" 2>&1` to install Node LTS
20. Rebuild the dev container: `Dev Containers: Rebuild and Re-Open in Container` (from command palette)

From there I was up and running and ready to generate a new Rails project. With Visual Studio Code still connected to the dev container, I opened a new terminal (inside of vscode) and generated a new rails app:

```bash
rails new . -T -d postgresql
```

…and I customized the database configuration following indications in `docker-compose.yml`:

```yml
# File: ./config/database.yml
default: &default
  adapter: postgresql
  encoding: unicode
  # For details on connection pooling, see Rails configuration guide
  # https://guides.rubyonrails.org/configuring.html#database-pooling
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  host: db
  username: postgres
  password: postgres

development:
  <<: *default
  database: weblog_devc_development

test:
  <<: *default
  database: weblog_devc_test

production:
  <<: *default
  database: weblog_devc_production
  username: weblog_devc
  password: <%= ENV["WEBLOG_DEVC_DATABASE_PASSWORD"] %>
```

```bash
--- a/config/database.yml
+++ b/config/database.yml
@@ -20,6 +20,9 @@ default: &default
   # For details on connection pooling, see Rails configuration guide
   # https://guides.rubyonrails.org/configuring.html#database-pooling
   pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
+  host: db
+  username: postgres
+  password: postgres

 development:
   <<: *default
```

From there I could confirm the server works:

```bash
# this will run a setup script that will also generate a schema.rb
./bin/setup
# this will launch the rails server at localhost:3000
./bin/rails server
```

Resources:

- Create a Ruby dev container: https://www.endpointdev.com/blog/2023/01/developing-rails-apps-in-a-dev-container-with-vs-code/
- Create a Rails dev container (Capybara + System Tests on Apple Silicon): https://bendyworks.com/blog/how-to-get-your-capybara-system-tests-running-in-a-docker-dev-container-on-apple-silicon
