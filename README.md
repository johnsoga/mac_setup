# MacOS

### Homebrew(Cask) GUI Apps:
- [VLC](https://www.videolan.org/vlc/index.html)
- [The Unarchiver](https://theunarchiver.com/)
- [Microsoft Office](https://products.office.com/en-us/mac/microsoft-office-for-mac)
- [Firefox](https://www.mozilla.org/en-US/firefox/)
- [Virtualbox](https://www.virtualbox.org/)
- Virtualbox Extension Pack
- [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html)
- [iTerm2](https://www.iterm2.com/)
- [Ableton Live](https://www.ableton.com/en/)
- [Atom](https://atom.io/)
- [MusicBrainz Picard](https://picard.musicbrainz.org/)
- [VMware Fusion](https://www.vmware.com/products/fusion.html)
- [Fork](https://git-fork.com/)
- [Focusrite Control](https://focusrite.com/en/focusrite-control)
- [Etcher](https://www.balena.io/etcher/)
- [Tripmode](https://www.tripmode.ch/)
- [Wireshark](https://www.wireshark.org/)

### AppStore Installed Apps:
- [Xcode](https://apps.apple.com/us/app/xcode/id497799835)
- [Brother iPrint&Scan](https://apps.apple.com/us/app/brother-iprint-scan/id1193539993)

***
## SSH Setup
#### SSH Key Generation:
Be Kind, [Rewind](https://www.ssh.com/ssh/keygen)!

```
$ ssh-keygen -t ed25519
Generating public/private ed25519 key pair.
Enter file in which to save the key (/path/to/.ssh/id_ed25519): meaningful_name
Enter passphrase (empty for no passphrase): meaninful_passphrase
Enter same passphrase again: meaninful_passphrase
Your identification has been saved in meaningful_name.
Your public key has been saved in meaningful_name.pub.
```

#### Setup SSH config
Append the following to your `/path/to/.ssh/confg` file
```
Host host.to.use.ssh.key.to.remote.to
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/meaningful_name
```

#### Add Key/Passcode to Keychain
```
$ ssh-add -K ~/.ssh/meaningful_name
Enter passphrase for meaningful_name:
Identity added: meaningful_name (user@machine_name)
```

### Trackpad Options:
