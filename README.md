# jjui.nvim

A Neovim plugin that provides a floating window interface for
[jjui](https://github.com/idursun/jjui).

## Requirements

- Neovim >= 0.5.0
- [plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [jjui](https://github.com/idursun/jjui) installed and available in your PATH.

## Installation

Using [packer.nvim]():

```lua
use {
    'sgremm/jjui.nvim',
    requires = 'nvim-lua/plenary.nvim',
    config = function()
        require('jjui').setup()
    end
}
```

Using [lazy.nvim](https://github.com/folke/lazy.nvim):


```lua
{
    'sgremm/jjui.nvim',
    dependencies = 'nvim-lua/plenary.nvim',
    opts = {}
}
```

## Configuration

The plugin can be configured by passing options to the setup function:

```lua
require('jjui').setup({
    mapping = '<leader>jj'  -- Change the default keymap
})
```

Or when using [lazy.nvim](https://github.com/folke/lazy.nvim):

```lua
{
    'sgremm/jjui.nvim',
    dependencies = 'nvim-lua/plenary.nvim',
    opts = {
      mapping = '<leader>jj'
    }
}
```

## Usage

- Use the configured keymap (default: `<leader>jj`) to open `lazyjj` in a floating
  window
- Or use the `:JJui` command
- Press `q` or lose focus to close the window
- The window will automatically return focus to your previous window when
  closing `jjui`

## License

This plugin is licensed under the [MIT license](LICENSE).
The Code based on [lazyjj.nvim] (https://github.com/swaits/lazyjj.nvim)
