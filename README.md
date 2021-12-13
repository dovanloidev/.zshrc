# .zshrc

```sh
export ZSH="/Users/loi.do/.oh-my-zsh"
export PATH=/opt/homebrew/bin:$PATH
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
export NVM_DIR=~/.nvm

ZSH_THEME="agnoster"

plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
    web-search
    yarn
    react-native
)

source $(brew --prefix nvm)/nvm.sh
source $ZSH/oh-my-zsh.sh

# run new tab
fortune | cowsay -f tux

# react native alias
alias installios='cd ios && arch -x86_64 pod install && cd ..'
alias rnios13pm='npx react-native run-ios --simulator "iPhone 13 Pro Max"'
alias rniPad125='npx react-native run-ios --simulator "iPad Pro (12.9-inch) (5th generation)"'
```
