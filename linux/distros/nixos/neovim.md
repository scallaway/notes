This is, at least for the time being, probably going to be the single biggest point of configuration for my setup.

It's a bit annoying that I'm going to have to move away from the current neovim configuration that I have, since that's very robust and battle-tested, but if I want to go all-in on the NixOS setup then that's the route I need to go down.

I have had a look at this previously, and simply including my current configuration in `./config/nvim` doesn't really work since you need a mutable environment in which to build the packages etc. I think I recall `treesitter` being a bit of a pain, as well as the LSP itself.