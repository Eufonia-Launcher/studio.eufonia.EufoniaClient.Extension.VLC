# VLC for Eufonia Client

This Flatpak extension adds VLC and LibVLC to Eufonia Client.

## Build and install

The build requires the `stable` Eufonia Client parent runtime. You also need the flatpak-builder, here are instructions for Fedora, adapt the command to your own distro.

```sh
# Install flatpak-builder
sudo dnf install -y flatpak flatpak-builder

# Build the extension
flatpak-builder --user --force-clean --disable-rofiles-fuse \
  --state-dir=.flatpak-builder --repo=repo build-dir \
  studio.eufonia.EufoniaClient.Extension.VLC.yml

# Then add the local flatpak repo and install
flatpak remote-add --user --if-not-exists --no-gpg-verify \
  eufonia-vlc-local "$PWD/repo"
flatpak install --user --reinstall eufonia-vlc-local \
  runtime/studio.eufonia.EufoniaClient.Extension.VLC/x86_64/50
```
