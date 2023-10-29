# VSCode Extensions

Extensions installed outside of a container cannot be used inside a container. They must be installed again. This may seem inconvenient at first glance, but extensions to be used in a container can be specified in a configuration file to simplify setup.

List of extensions available in this project inside the container:

**Ruby / Ruby On Rails • environment**

-   [Ruby extension pack](https://marketplace.visualstudio.com/items?itemName=walkme.Ruby-extension-pack) (`walkme.Ruby-extension-pack`): The most common extensions for Ruby in one pack.

    This extension pack includes:

    -   [Ruby Solargraph](https://marketplace.visualstudio.com/items?itemName=castwide.solargraph): Solargraph is a language server that provides intellisense, code completion, and inline documentation for Ruby.
    -   [ruby-rubocop](https://marketplace.visualstudio.com/items?itemName=misogi.ruby-rubocop): rubocop is a code analyzer for ruby.
    -   [Ruby Language Colorization](https://marketplace.visualstudio.com/items?itemName=groksrc.ruby): Adds support for Ruby colorization
    -   [Ruby Haml](https://marketplace.visualstudio.com/items?itemName=vayan.haml): Syntax highlighting for Ruby Haml files
    -   [Simple Ruby ERB](https://marketplace.visualstudio.com/items?itemName=vortizhe.simple-ruby-erb): Ruby and ERB Syntax Highlighting
    -   [ruby-linter](https://marketplace.visualstudio.com/items?itemName=hoovercj.ruby-linter)
    -   [ruby-symbols](https://marketplace.visualstudio.com/items?itemName=miguel-savignano.ruby-symbols): Search modules, class and methos in ruby files
    -   ~~Ruby~~ [DEPRECATED]: Ruby language and debugging support for Visual Studio Code. -> REPLACED by Ruby LSP

-   [Ruby LSP](https://marketplace.visualstudio.com/items?itemName=Shopify.ruby-lsp) (`Shopify.ruby-lsp`): Analyze Ruby code and enhance the user experience
-   [VSCode Ruby rdbg Debugger](https://marketplace.visualstudio.com/items?itemName=KoichiSasada.vscode-rdbg) (`KoichiSasada.vscode-rdbg`): Ruby's rdbg debugger • Ruby debugger to connect [debug](https://github.com/ruby/debug) library which utilize recent Ruby's debug support features.
-   [ERB Formatter/Beautify](https://marketplace.visualstudio.com/items?itemName=aliariff.vscode-erb-beautify): Use with `option + shift + F`
-   [Editor config](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig) (`EditorConfig.EditorConfig`): This plugin attempts to override user/workspace settings with settings found in .editorconfig files
-   [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)

**NodeJS / NPM / Vite / React • environment**

-   [Jest "JS Testing"](https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest) (`Orta.vscode-jest`): Jest features in vscode
-   [Jest Runner](https://marketplace.visualstudio.com/items?itemName=firsttris.vscode-jest-runner) (`firsttris.vscode-jest-runner`): Simple way to run or debug a single (or multiple) tests from context-menu

## Devcontainer default gems

**Rails**

**Webdrivers**

Run Selenium tests more easily with automatic installation and updates for all supported webdrivers.

-   https://github.com/titusfortner/webdrivers

**Solargraph**

Solargraph provides a comprehensive suite of tools for Ruby programming: intellisense, diagnostics, inline documentation, and type checking.

-   https://github.com/castwide/solargraph

**Rubocop**

RuboCop is a Ruby static code analyzer (a.k.a. linter) and code formatter.

-   https://github.com/rubocop/rubocop
-   https://github.com/rubocop/rubocop-rails
-   https://github.com/rubocop/rubocop-rspec
-   https://github.com/rubocop/rubocop-performance/

## Confirmation of plugins operation

Please confirm that Rubocop and Solargraph are running by launching the container from VS Code.

**Rubocop**

The familiar Linter for Ruby can be found in the Problems panel.

**Solargraph**

It is a useful tool for auto-completion and jumping to method and class definitions. If you are not using it, please try it.

The combination of Solargraph and VS Code is complicated to set up if you try to run it from outside a container, but using Dev Containers makes it easy to set up.

[Solargraph: A Ruby Language Server](https://solargraph.org/)

## Resources

-   How to use Docker containers for Ruby on Rails development in Visual Studio Code: https://dev.to/konyu/how-to-use-docker-containers-for-ruby-on-rails-development-in-visual-studio-code-23np
