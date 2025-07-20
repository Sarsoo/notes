---
tags:
  - linux
  - infra
title: Nix
---
# nix.shell
- Declaratively define shell including packages
```nix
let
  nixpkgs = fetchTarball "https://github.com/NixOS/nixpkgs/tarball/nixos-23.11";
  pkgs = import nixpkgs { config = {}; overlays = []; };
in

pkgs.mkShell {
  packages = with pkgs; [
    git
    neovim
    nodejs
  ];
  
  GIT_EDITOR = "${pkgs.neovim}/bin/nvim";

  shellHook = ''
    git status
  ''
}
```
- Run `nix-shell` in same folder as `nix.shell`
- Packages defined in the `packages` attribute will be available in `$PATH`
- Any attributes that aren't special are used as env variables
