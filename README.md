### Nix flakes
A simple hello-worldish demo cobbled together from examples and LLM generation.

Demonstrates the ability to use nix-managed dependencies locally, as well as during a GitHub Actions workflow run.

#### Running it
Start up local env (I use WSL)

Install nix

Modify `/etc/nix/nix.conf` to look like

```
# see https://nixos.org/nix/manual/#sec-conf-file

# So far the sandbox feature does not seem to work on Debian:
# https://github.com/NixOS/nixpkgs/pull/47794#issuecomment-429575989
sandbox = false
experimental-features = nix-command flakes
```
Then go into the nix shell with

`nix develop`

and check versions with

`node --version`
`dotnet --version`

No matter what versions are installed locally, they should read 22 and 8 respectively.
