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

- `.yarnrc.yml`:

```yaml
nodeLinker: node-modules
```

#### PYTHON 

- `package.json`: (Can be in a **separate** dir)

```json
{
  "name": "python_tools",
  "packageManager": "yarn@3.5.0",
  "devDependencies": {
    "pyright": "^1.1.332",
  }
}
```

#### NODE Project

- `package.json`: (Best to be in **same**/project dir)

```json
{
  "name": "my_NODE_Project",
  "packageManager": "yarn@3.5.0",
  "devDependencies": {
    "@tailwindcss/language-server": "^0.0.13",
    "@vue/language-plugin-pug": "^1.8.20",
    "@vue/language-server": "^1.8.20",
    "tailwindcss": "^3.3.5",
    "typescript": "^5.2.2",

    "vue": "^3.3.7"
  }
}
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

- **TypeScript**-related config: `tsconfig.json`:

```json
{
  "vueCompilerOptions": {
    "plugins": ["@vue/language-plugin-pug"]
  }
}
```

- **TailwindCSS** config: `tailwind.config.js`: (Can be BLANK)
