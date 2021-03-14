# MacOS

### Homebrew(Cask) GUI Apps:
- [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html)
- [Ableton Live](https://www.ableton.com/en/)
- [Firefox](https://www.mozilla.org/en-US/firefox/)
- [Google Chrome](https://www.google.com/chrome/)
- [iTerm2](https://www.iterm2.com/)
- [Atom](https://atom.io/)
- [Etcher](https://www.balena.io/etcher/)
- [Wireshark](https://www.wireshark.org/)
- [OpenVPN Connect](https://openvpn.net/client-connect-vpn-for-mac-os/)
- [Tunnelblick](https://tunnelblick.net/)
- [GitAhead](https://gitahead.github.io/gitahead.com/)
- [VLC](https://www.videolan.org/vlc/index.html)
- [The Unarchiver](https://theunarchiver.com/)
- [Microsoft Office](https://products.office.com/en-us/mac/microsoft-office-for-mac)
- [Virtualbox](https://www.virtualbox.org/)
- Virtualbox Extension Pack
- [MusicBrainz Picard](https://picard.musicbrainz.org/)
- [VMware Fusion](https://www.vmware.com/products/fusion.html)
- [Fork](https://git-fork.com/)
- [Focusrite Control](https://focusrite.com/en/focusrite-control)
- [Tripmode](https://www.tripmode.ch/)
- [Cyberduck](https://cyberduck.io/)

### AppStore Installed Apps:
- [Xcode](https://apps.apple.com/us/app/xcode/id497799835)

***

## Prerequisite
Install Xcode or Xcode Tools: this is a prereq. of Homebrew

```
$ xcode-select --install
```
Install [Homebrew](https://docs.brew.sh/Installation)

Install [Ansible](https://www.ansible.com/)
```
$ brew install ansible
```

Create the directory you will store your repositories in and go to it
```
$ mkdir ~/Documents/VersionControl
$ cd ~/Documents/VersionControl
```

Clone the repo
```
$ git clone https://github.com/johnsoga/mac_setup.git
$ cd mac_setup
```

_Note: MacOS Catalina & Earlier_

Installing Little Snitch via Homebrew only works for MacOS Big Sur & Newer. For older version check [here](https://www.obdev.at/products/littlesnitch/download-previous-versions.html).

**Recommended** to install Little Snitch and apply rules before installing other software

## SSH Setup
#### SSH Key Generation:
Be Kind, [Rewind](https://www.ssh.com/ssh/keygen)!

```
$ ssh-keygen -t ed25519
Generating public/private ed25519 key pair.
Enter file in which to save the key (/path/to/.ssh/id_ed25519): meaningful_name
Enter passphrase (empty for no passphrase): meaningful_passphrase
Enter same passphrase again: meaningful_passphrase
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
