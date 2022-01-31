# nixos-configuration

After partitioning, before running `nixos-generate-config`:

```sh
mkdir /mnt/etc
nix-env -i git vim
cd /mnt/etc
git clone https://github.com/arnfinn/nixos-configuration nixos
cd /mnt/etc/nixos
nixos-generate-config --show-hardware-config >>hardware-configuration.nix

vim configuration.nix

nixos-install
reboot
```
