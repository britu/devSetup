# Dev Setup

1. Homebrew/terminal/bash
1. OSX Productivity - Window Management/Quick Launcher/Hyperswitch
1. OSX Settings - Dock/Finder
1. Web Browser - Extensions - UBlock Origin, AdBlock, Privacy Badger, OneTab, JSONViewer, Stylus(Github dark); tampermonkey, Vue Devtools, React Devtools 
1. Node.js - nvm
1. Code Editor - vs code
1. Code Editor Extensions
1. Break timer and Flux
1. iStat Menus
1. for more info: https://www.youtube.com/watch?v=tMNOpaQrfAE

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
