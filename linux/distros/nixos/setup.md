# home-manager
This appears to be _the_ way to handle user environments in the Nix ecosystem, and allows some very clean user-defined package management etc. I can see this being very good for having privileged and non-privileged accounts and defining the bounds in which they can work nice and easily.
## Using unstable for certain packages
This was a nightmare to get working but I got there in the end.  
It involved setting up a variable called `nixpkgs` that contained both the "stable" and "unstable" URLs that you would then pass down to the home-manager modules themselves.  
From there, you can reference the unstable package that you need through `nixpkgs.from.unstable.{package_name}`.
# Fonts

Still not sure that the problem with fonts are, at least in Alacritty. I can get `CaskaydiaCove Nerd Font` to install fine, although `CommitMono` doesn't seem to have an associated package.

I think for the latter I'm going to have to open an issue on the Github pointing this out, since I really like the font!