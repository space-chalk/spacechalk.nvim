# 🛸 Space Chalk Theme for NeoVim 🎨
A theme trying to combine a love of neon space colors and pastel chalk board colors.

<img src="./img/nvim_example.png" style="width=800" alt="Screenshot of neovim editing a python file. It's showing off the Space Chalk Color Theme, featuring syntax highlight colors somewhere between pastel and neon on a very dark bluish purple background">

## Supported features

- [barbecue](https://github.com/utilyre/barbecue.nvim)
- [gitsigns](https://github.com/lewis6991/gitsigns.nvim)
- [scrollbar.nvim](https://github.com/petertriho/nvim-scrollbar)
- [Telescope](https://github.com/nvim-telescope/telescope.nvim) - currently working on this
- [barbar](https://github.com/romgrk/barbar.nvim)


## Installation

You should be able to install this fine with any neovim plugin manager. (If you can't, let me know via an Issue or PR)

### vim-plug

```vim
Plug 'space-chalk/spacechalk.nvim'
```

### packer

```lua
use {'space-chalk/spacechalk.nvim'}
```

## Setup

#### neovim (in lua)
You can of course use vimscript instead of lua, but for those new to neovim, this is what you want to do:

```lua
-- you will want this after packer has been loaded
vim.cmd.colorscheme("spacechalk")
```

### tmux
If you are running neovim inside tmux:

```tmux
set-option -g default-terminal "xterm-256color"
set-option -ga terminal-overrides ',xterm-256color:Tc'
```

## Contributing and Troubleshooting

Contributions to get the syntax highlighting working everywhere are absolutely
welcome. If you're new to vim colorschemes, here's some tips!

### Get the current highlighting for a given variable/filetype
If you're already in a file in vim, and the highlighting doesn't look quite right,
but you're not sure what the variable is called, you can run the following command:

```vim
:highlight
```

That will give the exact `highlight` commands for all the variables, but unfortunately in vim, it is not searchable, so you'll have to page through it ;(

### Get the current syntax for a given variable/filetype
Open a python file in vim and then type the following:

```vim
:syntax list
```

That will give you all the syntax variable names and their colors as three `x`s, like:

```vim
pythonInclude  xxx from import
```

It may also be helpful to check out more about syntax/colors with:

```vim
:help syntax
```

Finally, useful tool for learning what highlight variables are called:
[vivify](http://bytefluent.com/vivify/)
