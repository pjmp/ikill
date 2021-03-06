ikill [![Crates.io](https://img.shields.io/crates/v/ikill)](https://crates.io/crates/ikill) ![License](https://img.shields.io/crates/l/ikill)
---

> Interactively kill running processes, inspired by [fkill-cli](https://github.com/sindresorhus/fkill-cli).

### Features
- List and fuzzy find running processes.
- Multi select processes (by pressing <kbd>⭾</kbd>)

### Usage
Run `ikill` on terminal, search and press <kbd>↵</kbd>.

### Screenshot

[![A screenshot](./screencast.gif)](./screencast.gif)

### Installation
```
cargo install ikill
```

### Usage
```
ikill - Interactively kill processes

USAGE:
    ikill

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information
```

# Alternatives
```bash
# using `fzf`
pgrep . -l | fzf --reverse -m | awk '{ print $2 }' | xargs -I% -r kill -9 '%'

# using `dmenu`
pgrep . -l | dmenu -l 20 | awk '{ print $2 }' | xargs -I% -r kill -9 '%'
```

### TODO
 - [ ] Kill process by PID/name (without fuzzy finder).
 - [ ] Preview pane with process id?
