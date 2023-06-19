# AstroNvim with GitHub Copilot integration

## Installing
### [AstroNvim](https://github.com/AstroNvim/AstroNvim)

#### Make a backup of your current nvim and shared folder
```shell
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/share/nvim.bak
```

#### Clone the repository
```shell
git clone --depth 1 https://github.com/AstroNvim/AstroNvim ~/.config/nvim
nvim
```

### [Copilot](https://github.com/zbirenbaum/copilot.lua)

Paste in ~/.config/nvim/lua/plugins/copilot.lua:
```lua
return {
	"zbirenbaum/copilot.lua",
	cmd = "Copilot",
	event = "User AstroFile",
	opts = { suggestion = { auto_trigger = true, debounce = 150 } },
}
```

Restart nvim, then enter commands:

>:Copilot setup
>:Copilot enable

### Using
Use `Alt` + `l` for accept
