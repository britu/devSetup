# Dev Setup
```
1. xcode-select --install
2. Homebrew/terminal/bash : From the Homebrew website
3. OSX Productivity - Window Management/Quick Launcher/Hyperswitch
4. OSX Settings - Dock/Finder
5. Web Browser - Extensions - UBlock Origin, AdBlock, Privacy Badger, OneTab, JSONViewer, Stylus(Github dark); tampermonkey, Vue Devtools, React Devtools
```
# NVM install
```
6. Node.js - nvm : https://tecadmin.net/install-nvm-macos-with-homebrew/
 - brew update 
 - brew install nvm 
 ```
 Next, create a directory for NVM in home.
 ```
 - mkdir ~/.nvm 
 ```
 Now, configure the required environment variables. Edit the following configuration file in your home directory
 ```
 - vim ~/.bash_profile 
 ```
 and, add below lines to ~/.bash_profile ( or ~/.zshrc for macOS Catalina or later)
 
 ```
 export NVM_DIR=~/.nvm
 source $(brew --prefix nvm)/nvm.sh
 
 Press ESC + :wq to save and close your file.
 ```
 - 
7. Code Editor - vs code
8. Code Editor Extensions
9. Break timer and Flux
10. iStat Menus
11. for more info: https://www.youtube.com/watch?v=tMNOpaQrfAE
```

# Turn off mac setting
````
User & Group -> Login items

unnessery app tracking 
Security and privacy -> privacy -> 
turn off unnesseery services
privacy -> location Services -> system Services and turn it off all check
Turn off Analytics
Turn off advertiser
Turn off unnecessary notification
Turn off unnecessary extentions
````

# Node
```
To Clean the chase node
 npm cache clean --force
 rm -rf node_modules package-lock.json
 npm install
 npm start
 killall node
```

# xcode-select --install
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew update
brew cask install iterm2
# update iterm2 settings -> colors, keep directory open new shell, keyboard shortcuts
brew install bash # latest version of bash
# set brew bash as default shell
brew install fortune
brew install cowsay 
brew install git
brew install vcprompt
# update bash_profile
brew cask install spectacle
brew cask install alfred
# set CMD+space to launch alfred
brew cask install firefox
# install nvm/node
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
nvm install stable
mkdir ~/workspace
npm install -g lite-server eslint
brew cask install visual-studio-code
# update vscode settings
# install vscode extensions 


-----------------------------------
alexcvzz.vscode-sqlite
andys8.jest-snippets
apollographql.vscode-apollo
austincummings.razor-plus
bobsparadox.seti-black
BriteSnow.vscode-toggle-quotes
christian-kohler.npm-intellisense
christian-kohler.path-intellisense
CoenraadS.bracket-pair-colorizer
dbaeumer.vscode-eslint
esbenp.prettier-vscode
formulahendry.auto-close-tag
formulahendry.auto-rename-tag
fosshaas.fontsize-shortcuts
ginfuru.ginfuru-onedark-raincoat-theme
glitch.glitch
HookyQR.beautify
JamesBirtles.svelte-vscode
JCsoftIA.jcsoftia
joelday.docthis
johnpapa.vscode-cloak
ms-azuretools.vscode-docker
MS-CEINTL.vscode-language-pack-es
ms-mssql.mssql
ms-vscode-remote.remote-ssh
ms-vscode-remote.remote-ssh-edit
ms-vscode.azure-account
ms-vsliveshare.vsliveshare
msjsdiag.debugger-for-chrome
Nimda.deepdark-material
Nur.just-black
octref.vetur
Orta.vscode-jest
patbenatar.advanced-new-file
PKief.material-icon-theme
ritwickdey.LiveServer
SmukkeKim.theme-setimonokai
streetsidesoftware.code-spell-checker
vscode-icons-team.vscode-icons
WallabyJs.quokka-vscode
WallabyJs.wallaby-vscode
whatwedo.twig
Zignd.html-css-class-completion

------------------------------------------------------------

$extensions =
      "alexcvzz.vscode-sqlite",
      "andys8.jest-snippets",
      "apollographql.vscode-apollo",
      "austincummings.razor-plus",
      "bobsparadox.seti-black",
      "BriteSnow.vscode-toggle-quotes",
      "christian-kohler.npm-intellisense",
      "christian-kohler.path-intellisense",
      "CoenraadS.bracket-pair-colorizer",
      "dbaeumer.vscode-eslint",
      "esbenp.prettier-vscode",
      "formulahendry.auto-close-tag",
      "formulahendry.auto-rename-tag",
      "fosshaas.fontsize-shortcuts",
      "ginfuru.ginfuru-onedark-raincoat-theme",
      "glitch.glitch",
      "HookyQR.beautify",
      "JamesBirtles.svelte-vscode",
      "JCsoftIA.jcsoftia",
      "joelday.docthis",
      "johnpapa.vscode-cloak",
      "ms-azuretools.vscode-docker",
      "MS-CEINTL.vscode-language-pack-es",
      "ms-mssql.mssql",
      "ms-vscode-remote.remote-ssh",
      "ms-vscode-remote.remote-ssh-edit",
      "ms-vscode.azure-account",
      "ms-vsliveshare.vsliveshare",
      "msjsdiag.debugger-for-chrome",
      "Nimda.deepdark-material",
      "Nur.just-black",
      "octref.vetur",
      "Orta.vscode-jest",
      "patbenatar.advanced-new-file",
      "PKief.material-icon-theme",
      "ritwickdey.LiveServer",
      "SmukkeKim.theme-setimonokai",
      "streetsidesoftware.code-spell-checker",
      "vscode-icons-team.vscode-icons",
      "WallabyJs.quokka-vscode",
      "WallabyJs.wallaby-vscode",
      "whatwedo.twig",
      "Zignd.html-css-class-completion"

$cmd = "code --list-extensions"
Invoke-Expression $cmd -OutVariable output | Out-Null
$installed = $output -split "\s"

foreach ($ext in $extensions) {
    if ($installed.Contains($ext)) {
        Write-Host $ext "already installed." -ForegroundColor Gray
    } else {
        Write-Host "Installing" $ext "..." -ForegroundColor White
        code --install-extension $ext
    }
}
