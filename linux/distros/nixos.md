# Neovim

## Treesitter

Due to way that NixOS works, in that you can only install build tools at the
shell-level and not at the user-level, you need to first be in a shell that
contains the `gcc` compiler before being able to install the Treesitter
languages:

```nix
nix-shell -p gcc
```

Once you're in there, open up an instance of Neovim and Treesitter should carry
on as normal (without any errors).
