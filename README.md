# VLC for Eufonia Client

This Flatpak extension adds VLC and LibVLC to Eufonia Client.

## Build and install

Install Eufonia Client and Flatpak Builder, then run:

```sh
flatpak run --command=flatpak-builder org.flatpak.Builder \
  --user --install --install-deps-from=flathub --force-clean build-dir \
  studio.eufonia.EufoniaClient.Extension.VLC.yml
```
