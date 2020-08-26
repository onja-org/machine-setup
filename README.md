# Machine setup

Instructions for setting up a new computer.

A glossary has been added below, it includes definitions of troublesome terms.



## Operating system

### Installing Windows

TBD

## Software

### Installing necessary software

- Antivirus
- Antispyware
- Glasswire
- Google Chrome
- Mozilla Firefox
- Visual Studio Code
- Git for Windows, inlcudes Git Bash
- Paint.net
- Figma, and Figma Font Helper
- Slack
- Node.js
- Bamboo / TinyApp (PNG & JPEG compression)

### Optional software

- Sourcetree

## Configuration

1. [Create a new `id_rsa` SSH Key](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) in your `~/.ssh/` folder using your Onja email address
1. [Upload your SSH key to your Github account](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)
1. Add a `.bash_profile` file to your home directory (`~`) including the following:

```sh
echo "~/.bash_profile loading…"
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa
```

1. Add your name and onja email to your git global config

```
git config --global user.name "YOUR_NAME_HERE"
git config --global user.email "YOUR_ONJA_EMAIL_ADDRESS_HERE"
```

1. Make Git automatically add tracking branches for new branches with the same name

```
git config --global push.default current
```


### Optional configuration

See: [First time Git setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

1. Set your primary git branch names to `main`

```
git config --global init.defaultBranch main
```

1. Change your default editor for Git to something like VS Code?


### Install VS Code extensions

- EditorConfig
- Sass Formatter
- Prettier

### Install npm globals

```
npm install -g create-react-app parcel prettier
```

This will install:

- create-react-app
- parcel
- prettier

## Glossary

Term | Definition
--- | ---
~ | Home directory, usually found in `C:\Users\StudentName`
SSH Key |  A file used to identify your computer or account in a secure way
Home directory | See ~ above
git global config | System-wide settings for git, usually stored in `~/.gitconfig`
