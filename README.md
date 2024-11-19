A sane, batteries-included starter template for running NixOS on WSL forked from LGUG2Z, adjusted by me to run on windows for arm/aarch64

build command:

sudo $(which nix) --extra-experimental-features "nix-command flakes" \
  --option accept-flake-config true \
  --option substitute true \
  --option sandbox false \
  run .#nixosConfigurations.nixos.config.system.build.tarballBuilder
