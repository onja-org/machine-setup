# Git & Bash configuration 

## SSH keys

1. [Create a new `id_rsa` SSH Key](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) in your `~/.ssh/` folder using your Onja email address
2. [Upload your SSH key to your Github account](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

## Bash profile

3. Add a `.bash_profile` file to your home directory (`~`) including the following:

```sh
echo "~/.bash_profile loading…"
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
```

## Git Global configuration

4. Add your name and onja email to your git global config

```
git config --global user.name "YOUR_NAME_HERE"
git config --global user.email "YOUR_ONJA_EMAIL_ADDRESS_HERE"
```

5. Make Git automatically add tracking branches for new branches with the same name

```
git config --global push.default current
```


### Optional Git configuration

See: [First time Git setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

6. Set your primary git branch names to `main`

```
git config --global init.defaultBranch main
```

7. Change your default editor for Git to something like VS Code?
