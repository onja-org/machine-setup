# Machine setup

Instructions for setting up a new computer.

A glossary has been added below, it includes definitions of troublesome terms.

## Operating system

### Get a ready-made drive

We have pre-installed and pre-configured drives available. Use one of those in your machine.

### Restore from an Image

If there are no ready-made drives left, you can restore from an image to a target hard-drive. Check out the [Hard-drive cloning docs](./hard-drive-cloning.md)

### Installing Windows

If for whatever reason you can't clone your disk and you have to resort to installing Windows from scratch, check out our documentation on [Windows installation](./windows-install.md).

## Configuring your machine

Changing your username and password

- Press `Windows Key` + `R` to show the Run dialog
- Enter 'control'
- Select the Users and Accounts option
- Change your current user from 'Student' to your name
- Change the current user's password to your own password

## Software

### Installing necessary software

Take a look in the `C:\Onja Software` folder. It contains some or all of these:

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

## Bash and Git Configuration

[See the docs on Git & Bash configuration](./git-configuration.md)

### Install VS Code extensions

- EditorConfig
- Sass Formatter
- Prettier

### Install npm globals

```
npm install -g create-react-app parcel-bundler
```

This will install:

- create-react-app
- parcel-bundler

## Glossary

Term | Definition
--- | ---
~ | Home directory, usually found in `C:\Users\StudentName`
cloning | Making an exact copy of something, in this case, a hard-drive
git global config | System-wide settings for git, usually stored in `~/.gitconfig`
Home directory | See ~ above
SSH Key |  A file used to identify your computer or account in a secure way
