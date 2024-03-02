# NixOS

## home-manager

This appears to be _the_ way to handle user environments in the Nix ecosystem,
and allows some very clean user-defined package management etc. I can see this
being very good for having privileged and non-privileged accounts and defining
the bounds in which they can work nice and easily.

## Fonts

Still not sure what the problem with fonts are, at least in Alacritty. I can
get `CaskaydiaCove Nerd Font` to install fine, although `CommitMono` doesn't
seem to have an associated package.

I think for the latter I'm going to have to open an issue on the Github
pointing this out, since I really like the font!

## Neovim

It looks as though I should be using the Nix-way of configuring Neovim, rather
than doing it through Lua. This is a real shame because I want to be able to
use my Neovim configuration on all distributions of Linux, not just NixOS.

I feel this is going to take some more research, given we're very nearly there
(it's just FZF that is being a pain).

### Treesitter

Due to way that NixOS works, in that you can only install build tools at the
shell-level and not at the user-level, you need to first be in a shell that
contains the `gcc` compiler before being able to install the Treesitter
languages:

```nix
nix-shell -p gcc
```

Once you're in there, open up an instance of Neovim and Treesitter should carry
on as normal (without any errors).

---

Another way to do this would be to have a flake that's part of the `nvim`
directory and ensure that it has `gcc` present at the time. So you can clone
the `nvim` repository, load the flake, and then compile Treesitter happily.
