# 1. Install linux using a bootable external source.
   * **Download ISO Image** - https://ubuntu.com/download/desktop
   * **Download RUFUS for making a drive bootable** - https://rufus.ie/en/#
   * **Open Rufus and Create Bootable Installation Media** - https://softwarekeep.com/help-center/how-to-create-a-bootable-usb-using-rufus
   * **Boot System with Bootable Installation Media and try to install** - https://ubuntu.com/tutorials/install-ubuntu-desktop#5-installation-setup

# 2. Install required packages
   * `sudo apt update`
   * `sudo apt install git curl jq`
   * **Docker**
      - Installation - https://docs.docker.com/engine/install/ubuntu/   
      - Post Installation - https://docs.docker.com/engine/install/linux-postinstall/
   * **Google-cloud-cli** - https://cloud.google.com/sdk/docs/install#deb
   * **Stack** - `curl -sSL https://get.haskellstack.org/ | sh`
   * **Ghci, Cabal** - `sudo apt install ghc cabal-install`
   * **Slack** - `sudo snap install slack --classic`
   * **Ghcid** - `stack install ghcid`
   * `export PATH=/home/$USER/.local/bin:$PATH`
   * **Docker Compose** - `sudo apt install docker-compose`
   * **Microsoft Teams**
      - download teams .deb file from https://www.microsoft.com/en-in/microsoft-teams/download-app
      - open .deb file with software installer and click install.
   * **Zoom**
      - download zoom .deb file from https://zoom.us/download
      - open .deb file with software installer and click install.
   * **Visual Studio**
      - `sudo apt-get install wget gpg`
      - `wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg`
      - `sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings`
      - `sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'`
      - `rm -f packages.microsoft.gpg`
      - `sudo apt install apt-transport-https`
      - `sudo apt update`
      - `sudo apt install code`

# 3. Terminal Customization.
   * **install ZSH** - `sudo apt install zsh`
   * **Follow below One time steps.**
      - `zsh`  - *you should be able to see a prompt.*
      - *Enter* `2` *on Prompt and press* `ENTER`
   * **install OH-MY-ZSH** - `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
   * **Download plug-ins for auto-suggestions and zsh-syntax-highlighting**
      - `git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
      - `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`
   * **Add these plug-ins to zshrc file**
      - `nano ~/.zshrc`
      - You can see plugins in that file. Edit to make it like this. `plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`
      - Close and open your terminal to see magic.

# 4. Copy Paste Utilities
   * `sudo apt-get install xclip -y`
   * **add below lines to ~/.zshrc file**
      - `alias pbcopy='xclip -selection clipboard'`
      - `alias pbpaste='xclip -selection clipboard -o'`

