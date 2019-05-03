## Install
```
rpm --import https://packages.microsoft.com/keys/microsoft.asc
sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
yum install -y code
```

# Extensions
```
code --install-extension austenc.laravel-blade-spacer
code --install-extension bmewburn.vscode-intelephense-client
code --install-extension cjhowe7.laravel-blade
code --install-extension cmstead.jsrefactor
code --install-extension dbaeumer.vscode-eslint
code --install-extension eamodio.gitlens
code --install-extension fayras.simple-new-file
code --install-extension felixfbecker.php-intellisense
code --install-extension hollowtree.vue-snippets
code --install-extension HookyQR.beautify
code --install-extension makao.phpcsfixer
code --install-extension MehediDracula.php-namespace-resolver
code --install-extension octref.vetur
code --install-extension onecentlin.laravel5-snippets
code --install-extension PKief.material-icon-theme
code --install-extension sleistner.vscode-fileutils
code --install-extension Tyriar.sort-lines
code --install-extension vuetifyjs.vuetify-vscode
code --install-extension xabikos.JavaScriptSnippets
code --install-extension ylw1694.removeEmptyLines
code --install-extension Zignd.html-css-class-completion
```

# Themes
```
code --install-extension azemoh.one-monokai
```

# PHP formatter
```
wget https://cs.sensiolabs.org/download/php-cs-fixer-v2.phar -O php-cs-fixer
chmod a+x php-cs-fixer
mv php-cs-fixer /usr/local/bin/php-cs-fixer
```

# Large workspace
```
printf "fs.inotify.max_user_watches=524288" >> /etc/sysctl.conf
sysctl -p
```

# Settings
```
{
    "beautify.language": {
        "html": ["html", "blade", "vue"]
    },
    "breadcrumbs.enabled": true,
    "diffEditor.ignoreTrimWhitespace": true,
    "diffEditor.renderSideBySide": true,
    "editor.fontSize": 22,
    "editor.formatOnPaste": true,
    "editor.formatOnSave": true,
    "editor.formatOnType": false,
    "editor.lineHeight": 35,
    "editor.minimap.enabled": false,
    "editor.quickSuggestions": true,
    "editor.wrappingIndent": "none",
    "emmet.syntaxProfiles": {
        "javascript": "jsx",
        "xml": {
            "attr_quotes": "single"
        }
    },
    "emmet.includeLanguages": {
        "blade": "html",
        "vue": "html"
    },
    "eslint.autoFixOnSave": true,
    "explorer.confirmDelete": false,
    "explorer.openEditors.visible": 0,
    "files.associations": {
        ".blade.php": "html",
        ".vue": "html"
    },
    "files.autoSave": "afterDelay",
    "files.trimFinalNewlines": true,
    "files.trimTrailingWhitespace": true,
    "git.autofetch": true,
    "git.confirmSync": false,
    "git.enableSmartCommit": true,
    "gitlens.keymap": "alternate",
    "html.format.wrapLineLength": 0,
    "phpcsfixer.executablePath": "/usr/local/bin/php-cs-fixer",
    "scss.lint.emptyRules": "ignore",
    "telemetry.enableCrashReporter": false,
    "telemetry.enableTelemetry": false,
    "window.menuBarVisibility": "toggle",
    "window.title": "${dirty}${activeEditorMedium}${separator}${rootName}${separator}${appName}",
    "workbench.colorCustomizations": {
        "statusBar.background": "#272727",
        "titleBar.activeBackground": "#272727",
        "activityBar.background": "#272727"
    },
    "workbench.iconTheme": "material-icon-theme",
    "workbench.startupEditor": "none",
    "workbench.statusBar.visible": true,
    "workbench.colorTheme": "Monokai Dimmed",
    "window.titleBarStyle": "custom",
    "[javascript]": {
        "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[jsonc]": {
        "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[scss]": {
        "editor.defaultFormatter": "HookyQR.beautify"
    },
    "[vue]": {
        "editor.defaultFormatter": "HookyQR.beautify"
    }
}
```

# Keybindings
```
[
    {
        "key": "ctrl+u",
        "command": "editor.action.transformToUppercase"
    },
    {
        "key": "ctrl+l",
        "command": "editor.action.transformToLowercase"
    },
    {
        "key": "ctrl+,",
        "command": "workbench.action.openSettingsJson"
    },
    {
        "key": "ctrl+alt+g",
        "command": "git.push"
    }
]
```
