```
// shell change to zsh
$ apt -y install open-vm-tools
$ apt install zsh
$ chsh -s $(which zsh)
$ echo $SHELL

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

$ source ~/.powerlevel10k/powerlevel10k.zsh-theme

$ p10k configure >> reconfiguration

```
