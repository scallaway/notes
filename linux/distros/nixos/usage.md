# Usage

## Development Environments

This is the way to go when you want to build any sort of software from within
the NixOS. This works in the same way as a Python Virtual Environment, but is
available for _all_ languages.

A simple way to switch between these development environments when you navigate
around your file system is with the tool `direnv`. This hooks into your shell
and prevents you from having to clutter the `.profile` file etc. etc.

For more information on NixOS and `direnv` working together, take a look at
this blog post: https://determinate.systems/posts/nix-direnv/
