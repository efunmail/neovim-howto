## TODO

- [ ] [WIP:] LOCAL
- [ ] Can put Node-based (LSP) **_language servers_** in a (Alpine? Debian-Slim?) **container**?

## LOCAL - Init

### Neovim

- Dir structure (under `~/neovim/` - ALT: `~/nv/` ??)

```
~/neovim/
         094/
             nvim.sh
             *.*
```

- `nvim.sh`:

```sh
# Get DIR of script
# // https://stackoverflow.com/questions/4774054/reliable-way-for-a-bash-script-to-get-the-full-path-to-itself
SCRIPT_DIR=$(dirname $(realpath $0))

# ** Run nvim - with init.vim
#VIMRUNTIME=${SCRIPT_DIR}/share/nvim/runtime ${SCRIPT_DIR}/bin/nvim  -u ${SCRIPT_DIR}/init.vim  $@
VIMRUNTIME=${SCRIPT_DIR}/share/nvim/runtime ${SCRIPT_DIR}/bin/nvim  -u  $@
```

- [TODO:] `vim-plug`

    - [ ] https://github.com/junegunn/vim-plug/tree/master#neovim

### CLI Tools
 
 - `Node`, `Yarn` - (in `$PATH` - e.g. under `/usr/local/bin/`)

### Node - YARN

- `package.json`:

```json
```

- `.yarnrc.yml`:

```yaml
```

### PROJECT - `nvim-init`

- [ ] **`.nvim-init.lua`**

### PROJECT - PYTHON

- `pyrightconfig.json`:

```json
{
  "pythonVersion": "3.8"
}
```

### PROJECT - NODE

- `tsconfig.json`:

```json
{
  "vueCompilerOptions": {
    "plugins": ["@vue/language-plugin-pug"]
  }
}
```
