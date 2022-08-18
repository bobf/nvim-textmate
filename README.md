# nvim-textmate
A textmate-based syntax highlighter to nvim, compatible with VScode

# install

git clone http://github.com/icedman/nvim-textmate ~/.config/nvim/lua
cd ~/.config/nvim/lua
mkdir build
cd build
cmake ../
make

```lua
-- init.lua
require('textmate')
```

--


```lua
-- init.lua
require('textmate').setup({quick_load = true})
```

* quick_load - defers loading of grammar and theme at the opening of a buffer 

# extensions

Copy vscode theme and grammar extensions to any of these directories:

```sh
~/.config/nvim/lua/nvim-textmate/
~/.editor/extensions/
~/.vscode/extensions/
```

# commands

* TextMateToggle
* TextMateTheme Dracula

# known issues

* a colorscheme must be loaded prior to running nvim-textmate
* cpp - Some grammars take a bit of time to load. cpp, the largest grammar file causes a visible lag on first load; hence the *quick_load* option is available.
* markdown - Other grammars - like markdown will load other grammar languages for inline code and will re-render after the other languages are loaded.
* scrolling and text editing - syntax highlighting is currently done at these events as a debounced (defer_fn) function.

# warning

* This plugin is just a proof of concept - from a novice lua coder, and much worse - from a non neovim user (not yet at least)

