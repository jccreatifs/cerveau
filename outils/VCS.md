# Version Control Systems

*Version control* is a system that records changes to a file(s) you are working on so that you can recall specific versions later, like a time machine scale of **undo button**.

**Git** is the version control we'll be using for local "snapshots" (the versions you choose to save as your options later in case you want to undo at some specific points during your project development) and **Github** is a celestial place of data heaven where you can save your *version controlled* projects, or better called "repositories".

## Installing git

```shell
sudo apt install git
```

After installing git, you can set your name and email address with the following command.

For setting up your git user name:
```shell
git config --global user.name "Charles Sanders Peirce"
```

For setting up you git user email address:
```shell
git config --global user.email "mail@address.com"
```

## ssh and Github

To be able to upload or '*push*' your projects to a remote place like Github, you need to set up a ssh key pair. *Pushing* to Github is making a copy of your local repository to Github's server. This is an important step because it allows collaboration, and some more benefits, like ultimate backup file sharing options.

### Generating an ssh Key

1. On the terminal, enter the text below, but change the `mail@address.com` with your own:
```shell
ssh-keygen -t ed25519 -C "mail@address.com"
```

2. Add your ssh key to ssh-agent:
```shell
eval "$(ssh-agent -s)"
```

3. Then add your SSH private key too:
```shell
ssh-add ~/.ssh/id_ed25519
```

Source: [Github Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=linux)

### Adding ssh to Github

1. Copy the public key to the clipboard:
```shell
cat ~/.ssh/id_ed25519.pub
```

2. Navigate to your [Github account >> Settings >> Access >> SSH and GPG keys](https://github.com/settings/keys).
3. Create a new key with your public key you just copied.
4. Now, you can access your Github repositories with your machine via ssh. You may need to do this procedure on every device that you use to code.

Source: [Github Docs](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)


