# Neovim with LSP and tree-sitter

A simple neovim configuration with native LSP and treesitter support. 

You can use this repo either as a base config to build your own neovim configuration on top of, or as an example of how to configure neovim with treesitter and LSP support.

If you're on Ubuntu (or similar) make sure you have the following software installed:

```bash
sudo apt-get install -y software-properties-common build-essential git curl
```

# Installation

The features in this repo requires neovim 0.5.0+

```bash
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt-get update
sudo apt-get install neovim
```

Clone this repo into nvim config location:

```bash 
mkdir -p ~/.config/nvim
git clone https://github.com/michaeldegli/nvim-lsp-config/ ~/.config/nvim
```

Install vim-plug:

```bash 
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

Install plugins: 

```shell
nvim '+PlugInstall | qa'
```

Start neovim: `nvim`

Install LSPs for the languages you care about, i.e `:LspInstall elixir`.
You can use tab completion after typing `:LspInstall ` to see which language servers are available

Add/customize your keybindings to `~/.config/nvim/init.vim`.
