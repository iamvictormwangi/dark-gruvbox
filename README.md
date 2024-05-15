<div align="center">
      <h1> <img src="https://i.postimg.cc/WpQzgxVh/plugin-Icon.png" width="80px"><br/>gruvbox.nvim</h1>
     </div>
<p align="center">
      <a href="https://twitter.com/intent/user?screen_name=ellisonleao" target="_blank"><img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/ellisonleao?style=for-the-badge" style="vertical-align:center" ></a>
      <a href="#"><img alt="Made with Lua" src="https://img.shields.io/badge/Made%20with%20Lua-blueviolet.svg?style=for-the-badge&logo=lua" style="vertical-align:center" /></a>
</p>

A port of [gruvbox community](https://github.com/gruvbox-community/gruvbox) theme to lua with [treesitter](https://github.com/nvim-treesitter/nvim-treesitter) and [semantic highlights](https://neovim.io/doc/user/lsp.html#lsp-semantic-highlight) support!

<p align="center">
    <img src="https://i.postimg.cc/fy3tnGFt/gruvbox-themes.png" />
</p>

# Prerequisites

Neovim 0.8.0+

# Installing

## Using `packer`

```lua
use { "iamvictormwangi/dark-gruvbox" }
```

## Using `lazy.nvim`

```lua
{ "iamvictormwangi/dark-gruvbox", priority = 1000 , config = true, opts = ...}
```

## Using `vim-plug`

```vim
Plug 'eiamvictormwangi/dark-gruvbox'
```

# Basic Usage

Inside `init.vim`

```vim
set background=dark " or light if you want light mode
colorscheme dark-gruvbox
```

Inside `init.lua`

```lua
vim.o.background = "dark" -- or "light" for light mode
vim.cmd([[colorscheme dark-gruvbox]])
```

# Configuration

Additional settings for gruvbox are:

```lua
-- Default options:
require("dark-gruvbox").setup({
  terminal_colors = true, -- add neovim terminal colors
  undercurl = true,
  underline = true,
  bold = true,
  italic = {
    strings = true,
    emphasis = true,
    comments = true,
    operators = false,
    folds = true,
  },
  strikethrough = true,
  invert_selection = false,
  invert_signs = false,
  invert_tabline = false,
  invert_intend_guides = false,
  inverse = true, -- invert background for search, diffs, statuslines and errors
  contrast = "", -- can be "hard", "soft" or empty string
  palette_overrides = {},
  overrides = {},
  dim_inactive = false,
  transparent_mode = false,
})
vim.cmd("colorscheme dark-gruvbox")
```

