# Termux-ZSH

\
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/d6ded24b90164566a98e32c4343e543e)](https://app.codacy.com/gh/Sohil876/Termux-zsh?utm_source=github.com&utm_medium=referral&utm_content=Sohil876/Termux-zsh&utm_campaign=Badge_Grade_Settings)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/3a469a271f6b4a37b73288cc9929d0e1)](https://www.codacy.com/gh/Sohil876/Termux-zsh/dashboard?utm_source=github.com&utm_medium=referral&utm_content=Sohil876/Termux-zsh&utm_campaign=Badge_Grade)

##

![Termux-zsh-SS](Termux-zsh-SS.png)

### What it does

-   Installs zsh and sets it as default shell.
-   Installs [OhMyZsh](https://github.com/ohmyzsh/ohmyzsh) framework for plugins and themes. (Dropped prezto, zinit)
-   Installs customized Powerlevel10k theme and JetBrains Mono Nerd font as default.
-   Added color scheme and font changer scripts in ~/.termux/ directory to change color schemes and fonts in termux easily.
-   Installs syntax highlighter and autosuggestion plugins (from zsh users).
-   Enabled plugins by default `alias-finder command-not-found git node npm zsh-autosuggestions zsh-syntax-highlighting`, to check their usage and more available plugins [Go Here](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)
-   Installs lf (Terminal file manager), press CTRL+O to execute lf in current directory.
-   Added command edit function, press CTRL+E to edit any command in micro text editor (you can change it to whatever text editor you prefer in `~/.zshrc` file here `export VISUAL=micro`.

### Notes

-   Termux from playstore [is no longer updated](https://wiki.termux.com/wiki/Termux_Google_Play), install termux from [f-droid](https://f-droid.org/en/packages/com.termux) or from their [github releases](https://github.com/termux/termux-app/releases) instead.
-   To run commands in termux from other apps or open it in a directory with a filemanager ([Mixplorer](https://forum.xda-developers.com/t/app-2-2-mixplorer-v6-x-released-fully-featured-file-manager.1523691/) for example) give it App on top or draw over other apps permission and uncomment `allow-external-apps` and make sure it's set to `true` in `~/.termux/termux.properties`, However keep in mind that any app that supports this functionality can then automatically execute commands in termux so its very unsafe and should be only set to true when necessary.
-   You can set custom aliases or override any alias you want by setting them in `OhMyZsh/custom_aliases.zsh` before installing termux-zsh, or in `~/.oh-my-zsh/custom/custom_aliases.zsh` after installing it.
-   By default all `commit` aliases of git plugin now use verbose flags for some reason, that ends up inserting huge verbose diff in commit message, if you don't want that behaviour for any git commit aliases you can re set them as specified in above note in the `custom_aliases.zsh` file, im overriding `gc` alias in there by default to remove the verbose flag, you can use that as example and set yours in that file, you need to reload (`omz reload`) or restart termux after setting them.
-   You can use `color-changer` alias to change color scheme and `font-changer` alias to change font easily.
-   Checkout [OhMyZsh Cheatsheet](https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet) for some quick usefull tricks.
-   Checkout [OhMyZsh Wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Home) to see how to customize it, add plugins and themes.

### Installation

-   Clone this repo `git clone https://github.com/Sohil876/Termux-zsh`
-   Run setup.sh file `bash setup.sh`
-   Restart termux
-   On first start it will fetch and setup some things in background, leave it for a minute and its done.

### Update

-   You can use `omz update` command in termux to update OhMyZsh framework/plugins manually to latest versions, by default it will prompt you automatically if it finds any update available.
-   You can use `p10k-update` command in termux to check and update powerlevel10k theme to latest version, this has to be done manually.
