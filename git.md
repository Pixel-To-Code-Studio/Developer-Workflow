# Overview

Your projects will be hosted in Github. Each developer will be using different git branches for feature work. That work will be pushed into a main branch. It's going to be important that you know how to traverse git branches and work with git history.

## Setting up Git

### Introduction

Git is a very popular version control system. You’ll become very familiar with this piece of software throughout TOP, so don’t worry too much about understanding it at this point. There are many lessons focused on Git later in the curriculum.

GitHub is a service that allows you to upload your code using Git and to manage your code with a nice web interface. GitHub and Git are not the same thing or even the same company.

> Step 1: Install Git

[Install GIT](https://github.com/git-guides/install-git)

> Step 2: Configure Git and Github

Step 2.1: Create a Github Account

<a href="http://www.youtube.com/watch?feature=player_embedded&v=w3jLJU7DT5E" target="_blank"><img src="./../assets/github-logo.png" alt="GitHub Video" /></a>

GitHub is a place where you can put your code online. Why? To safely store your code in case something bad happens to your computer (computer crash, virus, faulty files). You'll always be able to access this code from GitHub, using any other computer.

- [Register](https://github.com/join) for an account
- Put the URL for your account in the class trello board

During the account setup, it will ask you for an email address. This needs to be a real email, and will be used by default to identify your contributions. If you are privacy conscious, or just don’t want your email address to be publicly available, make sure you tick the following two boxes on the [Email Settings](https://github.com/settings/emails) page after you have signed in:

![Email Settings](./../assets/email_setting.png)

Having these two options enabled will prevent you accidentally exposing your personal email address when working with Git and GitHub.

You may also notice an email address under the Keep my email addresses private option, this is your private GitHub email address. If you plan to use this, make note of it now as you will need it when setting up Git in the next step.

Step 2.2: Setup Git
For Git to work properly, we need to let it know who we are so that it can link a local Git user (you) to GitHub. When working on a team, this allows people to see what you have committed and who committed each line of code.

The commands below will configure Git. Be sure to enter your own information inside the quotes (but include the quotation marks)!

```
git config --global user.name "Your Name"
```
```
git config --global user.email "yourname@example.com"
```

If you opted to use the private GitHub email address, the second command will look something like this:

```
git config --global user.email "61502370+pixel2code@users.noreply.github.com" # Remember to use your own private GitHub email here.
```

To enable colorful output with git, type

```
git config --global color.ui auto
```

To verify that things are working properly, enter these commands and verify whether the output matches your name and email address.

```
git config --get user.name
```
```
git config --get user.email
```

**macOS Users**: Run these two commands to tell git to ignore .DS_Store files, which are automatically created when you use Finder to look into a folder. .DS_Store files are invisible to the user and hold custom attributes or metadata (like thumbnails) for the folder, and if you don’t configure Git to ignore them, pesky .DS_Store files will show up in your commits.

```
echo .DS_Store >> ~/.gitignore_global
```
```
git config --global core.excludesfile ~/.gitignore_global
```

Step 2.3: Create an SSH Key
An SSH key is a cryptographically secure identifier. It’s like a really long password used to identify your machine. GitHub uses SSH keys to allow you to upload to your repository without having to type in your username and password every time.

First, we need to see if you have an Ed25519 algorithm SSH key already installed. Type this into the terminal and check the output with the information below:

```
ls ~/.ssh/id_ed25519.pub
```

If a message appears in the console containing the text “No such file or directory”, then you do not yet have an Ed25519 SSH key, and you will need to create one. If no such message has appeared in the console output, you can proceed to step 2.4.

To create a new SSH key, run the following command inside your terminal. The -C flag followed by your email address ensures that GitHub knows who you are.

Note: The angle brackets (< >) in the code snippet below indicate that you should replace that part of the command with the appropriate information. Do not include the brackets themselves in your command. For example, if your email address is luke@example.com, then you would type ssh-keygen -t ed25519 -C luke@example.com. You will see this convention of using angle brackets to indicate placeholder text used throughout The Odin Project’s curriculum and other coding websites, so it’s good to be familiar with what it means.

```
ssh-keygen -t ed25519 -C <youremail>
```

- When it prompts you for a location to save the generated key, just push ```Enter```.

- Next, it will ask you for a password; enter one if you wish, but it’s not required.

Step 2.4: Link Your SSH Key with GitHub

Now, you need to tell GitHub what your SSH key is so that you can push your code without typing in a password every time.

First, you’ll navigate to where GitHub receives our SSH key. Log into GitHub and click on your profile picture in the top right corner. Then, click on ```Settings``` in the drop-down menu.

Next, on the left-hand side, click ```SSH and GPG keys```. Then, click the green button in the top right corner that says ```New SSH Key```. Name your key something that is descriptive enough for you to remember where it came from. Leave this window open while you do the next steps.

Now you need to copy your public SSH key. To do this, we’re going to use a command called [cat](http://www.linfo.org/cat.html) to read the file to the console. (Note that the .pub file extension is important in this case.)

```
cat ~/.ssh/id_ed25519.pub
```

Highlight and copy the output, which starts with ssh-ed25519 and ends with your email address.

Now, go back to GitHub in your browser window and paste the key you copied into the key field. Then, click ```Add SSH key```. You’re done! You’ve successfully added your SSH key!

Step 2.5 Testing your key

Follow the directions in [this article from GitHub](https://help.github.com/en/articles/testing-your-ssh-connection) to verify your SSH connection ***(Don’t forget to omit the*** $ ***when you copy and paste the code!)***. You should see this response in your terminal: ***Hi username! You’ve successfully authenticated, but GitHub does not provide shell access***. Don’t let GitHub’s lack of providing shell access trouble you. If you see this message, you’ve successfully added your SSH key and you can move on. If the output doesn’t correctly match up, then try going through these steps again.

Step 3: Let us know how it went!
You’ve completed the basic installations section, good job! As you progress through the Paths there will be other tools to install, so keep an eye out!

You probably felt like you were way in over your head, and you probably didn’t understand much of what you were doing. That’s 100% normal. Hang in there. You can do this! And we’ve got your back.

## Activity

- Go to this [repository](#) and follow along.

## Additional Resources

This section contains helpful links to related content. It isn’t required, so consider it supplemental.

[Understanding SSH Key Pairs](https://winscp.net/eng/docs/ssh_keys) SSH is a secure network protocol that uses an implementation of public-key cryptography, also known as asymmetric cryptography. Having a basic understanding of how it works can help you understand what an SSH key is all about.

[Asymmetric Encryption - Simply explained](https://www.youtube.com/watch?v=AQDCe585Lnc) a short video explaining Asymmetric Encryption.


## Commands

Undo unstaged changes : 

`git restore <FILE NAME>`

`git restore . `

Undo staged changes:

`git reset <FILE NAME>`

`git reset . `

Followed by : 

Undo unstaged changes : 

`git restore <FILE NAME>`

`git restore . `

Undo complete commits :

`git reset HEAD~<NUMBER OF COMMITS  BACK>`

Undo unstaged changes : 

`git restore <FILE NAME>`

`git restore . `

Or

A hard reset :
`git reset --hard HEAD~<NUMBER OF COMMITS BACK>`
