# Neovim

![1](https://user-images.githubusercontent.com/60380217/142715096-078b3cbd-f7a1-4426-a419-dd327bb8ce28.png)![2](https://user-images.githubusercontent.com/60380217/142715098-c8a51323-daa4-47aa-971e-fc3966d3b73f.png)
![3](https://user-images.githubusercontent.com/60380217/142715100-bdb3ca58-bcaa-4640-ae7d-5605f736a432.png)![4](https://user-images.githubusercontent.com/60380217/142715101-b1e54d76-491d-4fe5-a4da-11e559b7c2b7.png)

## Installation

### Neovim

**Debian/Ubuntu:**

Run the following commands:

```jsx
sudo add-apt-repository ppa:neovim-ppa/stable
sudo apt-get update
sudo apt-get install neovim
```

**Arch Linux:**

Neovim can be installed from the community repository:

```jsx
sudo pacman -S neovim
```

### Vim-plug for Neovim

Unix, Linux:

```bash
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

---

## Configuration

Create config folder and config file:

```bash
sudo mkdir ~/.config/nvim
sudo touch ~/.config/nvim/init.vim
sudo chmod 774 ~/.config/nvim/init.vim
```

*For Ubuntu the folder to store all plugins is '~/.config/nvim/plugged'*

**First**, try to install *Dracula* theme for Neovim:

```css
call plug#begin('~/.config/nvim/plugged')

" onedarkthem less contract
Plug 'dracula/vim',

call plug#end()

" syntax on
colorscheme dracula
```

Press `Esc` key to switch to Normal mode, and then type `:w` to overwrite and `:so %` to source this file.

Now, type `:PlugInstall` to install plugins.

If everything is OK, **Next step**

Delete all lines in current file, copy all the lines in the [init.vim](https://raw.githubusercontent.com/VuNgN/Neovim-config/main/init.vim) file above there ☝️☝️☝️ to current file 

And install again: 

Press `Esc` key to switch to Normal mode, and then type `:w` to overwrite and `:so %` to source this file and type `:PlugInstall` to install plugins.

### Noted: 

The fzf plugin has some dependencies: 
- For syntax-highlighted preview, install [bat](https://github.com/sharkdp/bat)
- If [delta](https://github.com/dandavison/delta) is available, `GF?`,
`Commits` and `BCommits` will use it to format `git diff` output.
- `Ag` requires [The Silver Searcher (ag)](https://github.com/ggreer/the_silver_searcher)
- `Rg` requires [ripgrep (rg)](https://github.com/BurntSushi/ripgrep)
- `Tags` and `Helptags` require Perl

If Vim-hexokinase error "needs to updating"  like that
![](https://user-images.githubusercontent.com/5801052/103404265-3ba57500-4b53-11eb-928c-deff22e2b133.png)
- Go to directory where Hexokinase in that like  *~/.config/nvim/plugged/vim-hexokinase* using the `cd` command.
- Run command `make hexokinase` . **DONE !**
