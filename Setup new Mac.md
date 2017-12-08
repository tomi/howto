# Dev software

## Terminal

* [iTerm2](https://iterm2.com/)
* [oh-my-zsh](http://ohmyz.sh/)

* [HomeBrew](https://brew.sh/)

## JS development

* [nvm](https://github.com/creationix/nvm#install-script)

## [Generate new SSH key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) and add it to GitHub

```bash
# Generate key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
# Start ssh-agent
eval "$(ssh-agent -s)"
```

Modify `~/.ssh/config` to automatically load keys into the ssh-agent and store passphrases in your keychain.

```bash
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```

Add SSH private key to the SSH agent

```bash
ssh-add -K ~/.ssh/id_rsa
```

[Add the public key to GitHub](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

```bash
pbcopy < ~/.ssh/id_rsa.pub
```

Goto https://github.com/settings/keys

## Postgres

* [Postico](https://eggerapps.at/postico/)
