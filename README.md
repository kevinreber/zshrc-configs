# zshrc-configs

Installing zshrc

On mac(homebrew)
```bash
brew install zsh
```

On linux
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Configs inside `~.zshrc` file
```bash
# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="/Users/kreber/.oh-my-zsh"

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="agnoster"

# Set list of themes to pick from when loading at random
# Setting this variable when ZSH_THEME=random will cause zsh to load
# a theme from this variable instead of looking in $ZSH/themes/
# If set to an empty array, this variable will have no effect.
# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )


# Which plugins would you like to load?
# Standard plugins can be found in $ZSH/plugins/
# Custom plugins may be added to $ZSH_CUSTOM/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(
   git
   zsh-syntax-highlighting
   zsh-autosuggestions
)

source $ZSH/oh-my-zsh.sh

# LunarVim
export PATH="$HOME/.local/bin":$PATH

# User configuration

# Configs
alias zshconfig="nvim ~/.zshrc"
alias tmuxconfig="nvim ~/.tmux.conf"

# yarn aliases
alias y="yarn"
alias yi="yarn install"
alias yst="yarn start"

# Git Aliases
alias g="git"
alias ga="git add"
alias gst="git status"
alias gb="git branch"
alias gco="git checkout"
alias gc="git commit"
alias gpl="git pull"
alias gps="git push"
alias gfo="git fetch origin"
alias gl="git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset) %C(bold cyan)(committed: %cD)%C(reset) %C(auto)%d%C(reset)%n''          %C(white)%s%C(reset)%n''          %C(dim white)- %an <%ae> %C(reset) %C(dim white)(committer: %cn <%ce>)%C(reset)'"
alias glo="git log --oneline"

# TMux Aliases
alias tmns="tmux new-session -s"
alias tma="tmux attach-session -t"
alias tml="tmux list-sessions"
alias tmk="tmux kill-session -t"
alias tmd="tmux detach"
alias tmrename="tmux rename-window"
alias tmv="tmux split-window -v"
alias tmh="tmux split-window -h"
alias tmnw="tmux new-window"
alias tmnext="tmux next-window"
alias tmprev="tmux previous-window"
alias tmsw="tmux select-window -t"
alias tmresize="tmux resize-pane"
alias tmsync="tmux setw synchronize-panes on"
alias tmunsync="tmux setw synchronize-panes off"
alias tmsend="tmux send-keys"
alias tmcapture="tmux capture-pane -S -"
alias tmsave="tmux save-buffer -b"
alias tmconf="tmux show-options -g"

# Playwright Aliases
alias codegen="npx playwright codegen localhost:3000"

# MAC Aliases
alias ports="sudo lsof -i -n -P | grep TCP"

# VM Login Alias
alias login="ssh <REMOTE_HOST>"
```


# Installing plugins
```bash
# Install zsh-syntax-highlighting plugin
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

# Install zsh-autosuggestions plugin
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

# Source the updated .zshrc file to apply changes
source ~/.zshrc
```
