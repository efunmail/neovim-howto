## TODO

- [.] LOCAL
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
# // https://stackoverflow.com/questions/4774054/reliable-w
ay-for-a-bash-script-to-get-the-full-path-to-itself
SCRIPT_DIR=$(dirname $(realpath $0))

# ** Run nvim - with init.vim
#VIMRUNTIME=${SCRIPT_DIR}/share/nvim/runtime ${SCRIPT_DIR}/
bin/nvim  -u ${SCRIPT_DIR}/init.vim  $@
VIMRUNTIME=${SCRIPT_DIR}/share/nvim/runtime ${SCRIPT_DIR}/b
in/nvim  -u  $@
```

### CLI Tools
 
 - `Node`, `Yarn` - (in `$PATH` - e.g. under `/usr/local/bin/`)

### Node - YARN

- `package.json`

```json
```

- .yarnrc.yml

```yaml

### PROJECT - `nvim-init`

