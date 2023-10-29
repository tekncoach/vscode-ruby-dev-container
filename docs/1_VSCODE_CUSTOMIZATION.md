# VSCode customization

Add the following configuration if you want to personalize your VSCode experience

1. Add extensions
    - [Atom One Dark Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)
    - [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
2. Set Keyboad shortcuts
   In `Settings > Keyboards Shortcuts`
   Look for `format document`: `option + shift + F`
3. Set ERB Formatting
    - Add [ERB Formatter/Beautify](https://marketplace.visualstudio.com/items?itemName=aliariff.vscode-erb-beautify)
    - Install `gem 'htmlbeautifier'`
4. Edit editor settings in `Settings > Settings`
    - search:
        - `files.trimTrailingWhitespace`: true
        - `editor.formatOnPaste`: true
    - search `settings` and finally click on any blue link to `Edit in settings.json`
        - Enable [Emmet](https://code.visualstudio.com/docs/editor/emmet#_emmet-when-quicksuggestions-are-disabled) for ERB "emmet.includeLanguages": { "ruby": "html", "erb": "html" }

## Ressources

-   [Lesson 3 - Configure VSCode for Rails Development](https://www.youtube.com/watch?v=WHVqcN3S_jI&list=PLBnuWio6_OZD3pMycSjzDK5BvW3m28_IL&index=3)
