```
// shell change to zsh
$ apt -y install open-vm-tools
$ apt install zsh
$ chsh -s $(which zsh)
$ echo $SHELL

// ubuntu server settings >> oh-my-zsh theme : eastwood
$ sudo apt install fontconfig

// nanum font
$ sudo apt install fonts-nanum fonts-nanum-coding fonts-nanum-extra

// nerd font install
wget -P ~/.local/share/fonts https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/JetBrainsMono.zip \
&& cd ~/.local/share/fonts \
&& unzip JetBrainsMono.zip \
&& rm JetBrainsMono.zip \
&& fc-cache -fv

// oh-my-zh
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

// zsh-syntax-highlighting
$ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

// zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

// fzf (fuzzy file finding)
$ git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install

// zsh-z >> auto directory movement
$ git clone https://github.com/agkozak/zsh-z ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-z

// .zshrc setting

plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
  fzf
  zsh-z
)

// powerlevel10k
$ git clone https://github.com/romkatv/powerlevel10k.git ~/.powerlevel10k

$ echo 'source ~/.powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zsrhc

$ p10k configure >> reconfiguration

// NvChad install
$ apt install ripgrep : telescope to gitignore

```

$ git clone https://github.com/NvChad/starter ~/.config/nvim && nvim
// Install Proto Nerd Font for Proper Icon Display

```

// Run :MasonInstallAll after plugins downloading
// Delete .git folder
// Manual :h nvui
// Uninstall
rm -rf ~/.config/nvim
rm -rf ~/.local/state/nvim
rm -rf ~/.local/share/nvim
```
