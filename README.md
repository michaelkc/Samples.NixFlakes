Remember to
- install nix
- modify WSL `/etc/nix/nix.conf` to look like

```
# see https://nixos.org/nix/manual/#sec-conf-file

# So far the sandbox feature does not seem to work on Debian:
# https://github.com/NixOS/nixpkgs/pull/47794#issuecomment-429575989
sandbox = false
experimental-features = nix-command flakes
```
Then go into the shell with

`nix develop`