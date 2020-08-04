# My Setup

> This repo contains all the programs (and their extensions) I use in a daily basis and how to configure them.

## Manjaro

### Programs

<!-- > Check out my `setup.sh` file in `manjaro` folter to install the programs listed below -->

> Format: <**program_name**> - <*manjaro_source*>

- [ ] **Android Studio** - *Flatpak*
- [x] **DBeaver** - *Snap*
- [x] **Discord** - *Official*
- [x] **Fira Code (tff, woff, woff2)** - *Official*
- [ ] **Flutter** - *AUR*
- [x] **Git** - *Official*
- [x] **Google Chrome** - *AUR*
- [x] **Insomnia** - *Snap*
- [x] **Mousepad** - *Official*
- [x] **NVM** - *Official*
- [ ] **OBS** - *Official*
- [x] **Vim** - *AUR*
- [x] **VSCode** - *AUR*
- [x] **Vysor** - *AUR*

> Unchecked ones are optional (I don't install them right away because I don't use them all the time)

### Troubleshooting

If, even after setting Chrome as the default browser in `System Setting -> Application -> Default Applications -> Web Browser`, it doesn't recognise itself as such, replace all `firefox.desktop` to `google-chrome.desktop` in `~/.config/mimeapps.list` file, and run the following command:

```bash
sudo xdg-settings set default-web-browser google-chrome.desktop
```

If you have problems to run Flutter after installing it (`flutter doctor -v` is returning "Unable to 'pub upgrade'..."), run the following command:

``` bash
sudo chown -hRf kaisen:kaisen /opt/flutter # Note that kaisen:kaisen and /opt/flutter are specific to my environment
```

## Oh My Zsh

> Check out my `.zshrc` file in `oh-my-zsh` folder (follow the instructions below to make it works properly)

Install Oh My Zsh by running:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Then, download Dracula color theme at [Dracula Theme](https://draculatheme.com) (Manjaro KDE uses Konsole by defaut) and apply it to your terminal. Also, set Fira Code Retina as your terminal font (if you don't have Fira Code fonts installed, [click here](https://github.com/tonsky/FiraCode/releases)).

After that, install Spaceship theme by running the following commands:

```bash
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

Last but not least, run the command below to install ZInit (so you can install plugins to Zsh):

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"
```

## NodeJS

> Make sure you've added NVM configs to your `.zshrc` or `.bashrc` file

Run the following command to install the Node's latest version:

```bash
nvm install node
```

Or run the following command to install the Node's latest LTS version:

```bash
nvm install --lts
```

### Globals

> Format: <**global_name**> - <*npm_source*>

- [ ] **Angular** - *@angular/cli*
- [ ] **Vue** - *@vue/cli*
- [x] **Yarn** - *yarn*
- [x] **Expo** - *expo-cli*

## VSCode

> Check out my `settings.json` and `keybindings.json` files in `vscode` folder

### Extensions

- [x] **Auto Import**
- [x] **Auto Rename Tag**
- [x] **Beaufity**
- [x] **Bracket Pair Colorizer 2**
- [ ] **Dart**
- [x] **Debugger for Chrome**
- [x] **Docker**
- [x] **Dracula Official**
- [x] **EditorConfig for VS Code**
- [x] **ESLint**
- [x] **ES7 React/Redux/GraphQL/React-Native snippets**
- [x] **Excel Viewer**
- [ ] **Flutter**
- [x] **Git History**
- [x] **GitLens - Git supercharged**
- [ ] **GraphQL for VSCode**
- [x] **Live Sass Compiler**
- [x] **Live Server**
- [x] **Live Share**
- [x] **Material Icon Theme**
- [x] **Prettier - Code formatter**
- [x] **Python**
- [x] **React Native Tools**
- [x] **REST Client**
- [x] **SVG Viewer**
- [ ] **Vetur**
- [x] **Vim**
- [x] **Visual Studio IntelliCode**
- [x] **vscode-styled-components**
- [x] **YAML**

> Unchecked ones are optional (I don't install them right away because I don't use them all the time)
