# .zshrc

```sh
# Enable Powerlevel10k instant prompt. Should stay close to the top of ~/.zshrc.
# Initialization code that may require console input (password prompts, [y/n]
# confirmations, etc.) must go above this block; everything else may go below.
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

export ZSH="/Users/loi.do/.oh-my-zsh"
export PATH=/opt/homebrew/bin:$PATH
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
export NVM_DIR=~/.nvm

ZSH_THEME="powerlevel10k/powerlevel10k"

plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
    web-search
    yarn
    react-native
    zsh-completions
)

source $(brew --prefix nvm)/nvm.sh
source $ZSH/oh-my-zsh.sh
source $ZSH/custom/dracula/zsh-syntax-highlighting.sh

# run new tab
fortune | cowsay -f tux
autoload -U compinit && compinit

# my alias
alias cdd='cd dev/'
alias vizsh='vim ~/.zshrc'
alias vivim='vim ~/.vimrc'
alias vip10k='vim ~/.p10k.zsh'

# fzf alias
alias falias='alias | fzf'

# react native alias
alias installios='cd ios && arch -x86_64 pod install && cd ..'
alias rnios13pm='npx react-native run-ios --simulator "iPhone 13 Pro Max"'
alias rniPad125='npx react-native run-ios --simulator "iPad Pro (12.9-inch) (5th generation)"'

# To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh

# zsh-bd
. $HOME/.zsh/plugins/bd/bd.zsh
```
