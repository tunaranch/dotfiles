# @tunaranch's Dotfiles

Dotfiles and system configuration to get a MacOS system the way tunaranch likes it.

Including:

  ✅ A basic, sensible zsh config.  
  ✅ Homebrew, and essential packages,  
  ❌ macOS user and system preferences (todo),  
  ❌ Themes. Can't manage themes neatly until Ansible's
       `osx_defaults` supports dicts.  
  ❌ macOS application settings (probably won't bother with this.

## A Fresh macOS Setup

Run these commands:

```shell script
chsh -s /bin/zsh
git clone https://github.com/tunaranch/dotfiles .dotfiles
git clone https://github.com/Tarrasch/antigen-hs.git ~/.zsh/antigen-hs/
~/.dotfiles/install.sh
```

This will bootstrap enough Homebrew to run ansible, and will use ansible
to set up the rest. See [the setup playbook](./ansible/setup.playbook.yml).  

### Setting up your Mac

After bove you may now follow these install instructions to set up a new Mac.

1. Update macOS to the latest version with the App Store
2. Install macOS Command Line Tools by running `xcode-select --install`
3. [Generate a new public and private SSH key](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) and add them to Github
4. Clone this repo to `~/.dotfiles`
5. Run `install.sh` to start the installation
6. Install antigen-hs


Your Mac is now ready to use!

## Thanks To...

This repo is a fork of [driesvints/dotfiles](https://github.com/driesvints/dotfiles), but
the guts have been replaced with ansible.
