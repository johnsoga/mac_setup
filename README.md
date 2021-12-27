# MacOS

### Homebrew(Cask) GUI Apps:
- [Cyberduck](https://cyberduck.io/)
- [Firefox](https://www.mozilla.org/en-US/firefox/)
- [Google Chrome](https://www.google.com/chrome/)
- [iTerm2](https://www.iterm2.com/)
- [Little Snitch](https://www.obdev.at/products/littlesnitch/index.html)
- [Microsoft Office](https://products.office.com/en-us/mac/microsoft-office-for-mac)
- [Visual Studio Code](https://code.visualstudio.com/)
- [VLC](https://www.videolan.org/vlc/index.html)
- [Wireshark](https://www.wireshark.org/)

### AppStore Apps:
- [Xcode](https://apps.apple.com/us/app/xcode/id497799835)

***

## Prerequisite
1. Install [Xcode](https://itunes.apple.com/us/app/xcode/id497799835) or Xcode Tools (Homebrew Requirement)
    ```
    xcode-select --install
    ```
2. Install [Homebrew](https://docs.brew.sh/Installation)
3. Install [Python3](https://www.python.org/)
    ```
    brew install python3
    ```
4. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
    ```
    python3.9 -m pip install --user ansible
    ```
    Update `$PATH` in `.bashrc` as this is where the Ansible binaries are installed
    
    ```
    export PATH=$PATH:~/Library/Python/3.9/bin
    ```
5. Create a directory to store repositories in and clone the repo
    ```
    mkdir ~/Documents/Code
    cd ~/Documents/Code
    git clone https://github.com/johnsoga/mac_setup.git
    cd mac_setup
    ```

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
