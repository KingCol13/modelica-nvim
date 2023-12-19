# Installation

## Requirements

- [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter) for syntax highlighting

Using vim-plug:

```vim
Plug 'KingCol13/modelica-nvim'
```

# Tree-sitter configuration

Add to your tree-sitter configuration lua:

```lua
-- Set the treesitter parser for modelica filetype
local parser_config = require "nvim-treesitter.parsers".get_parser_configs()
parser_config.modelica = {
  install_info = {
    url = "https://github.com/OpenModelica/tree-sitter-modelica",
    files = {"src/parser.c"},
    branch = "master",
    generate_requires_npm = false,
    requires_generate_from_grammar = false,
  },
}
```

Then run:

```vim
:TSInstall modelica
```

# Features

- modelica filetype detection
- syntax highlighting [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
