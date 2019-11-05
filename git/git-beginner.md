

# Intro


## Intro 1/2

Git is something called a DVCS which stands for decentralized version control
system. At a simple level it allows you to store file versions with it. The
decentralized part means that every single &ldquo;repo&rdquo; of files can be used
standalone without interacting with another computer. Some other versions
control systems are SVN, CVS, Mercurial and TFS.


## Intro 2/2

Git has the idea of a remote place to store your git repos. One of these remote
places is github. While github uses git, git does not use github.

To get started we need to install git. Run this command to see if git is
installed already. If not follow the instructions according to your operating
system below (in windows search for the program git for bash to get the prompt).

    git --version

    git version 2.24.0


# Installation


## Windows

go to <https://github.com/git-for-windows/git/releases/tag/v2.23.0.windows.1> and
scroll down to where it says Assets. Click on the dropdown and download the 64
bit exe which says Git-2.23.0-64-bit.exe.
@TODO(Renzix): go through install


## macOS

for macOS you have 2 options. You can either install xcode and it will
automatically install it or install it directly from git-scm.


### Xcode

Install xcode via the app store. To test it run

    git --version


### git-scm

go to <https://git-scm.com/download/mac> and install it.


## Linux

This depends on your distro. Nearly all distros have git in their repository so
you can just use your package manager.

-   Debian based `sudo apt install git`
-   Redhat based `sudo dnf install git`
-   Arch Based `sudo pacman -S git`


# Creating the Repo


## Git Init

To get started run the command

    git init myProject

This will give you a empty git repo called myProject. A repo is actually just a
folder for a project. You can now go into this folder and make a file called
readme.md. You can put in `Hello World` in the file as plain text.


## Git Add

After you make this file you can &ldquo;add&rdquo; it to your repository by running the
command `git add`. If you had multiple files then you would run `git add
filename` on each file.

    git add readme.md


## Git Commit part 1

`git add` doesn&rsquo;t actually tell git to save the current version of the file.
What it does is tell git that this files exists and you want to track it
possibly in the future. In order to tell git that this is a final change you
want to commit then run `git commit`.

    git commit


## Git Commit part 2

It will then pop up a tui text editor based on what you choose. Nano is probably
the default as it is the most simple so you can just write you commit message
then control o to save and quit(write o).

Make sure to write a helpful message as others will see it!!!


## Congrats

Congrats you have a repo with `readme.md`. You can git add and git commit every
time you change any files to save the changes in git.


## Recap

-   To make a repo `git init reponame`
-   To add a file (stage) `git add filename`
-   To commit changes `git commit`


# Using a remote


## Creating your account

Now you can setup github as a remote repository for your code. Keep in mind
there are alternatives the big two being bitbucket and gitlab.


## Create a repo

Once you create a account you have to do 2 things. First you create a empty
repository on the website. `DO NOT ADD A LICNESE OR README YET` as it will mess
up the history of the remote.


## Adding the remote

You can then tell your git repo (on your machine) where the remote place to
store it is. Change the url below to have your username instead of Renzix and
change test to the name of your repo you setup.

    git remote add origin https://github.com/Renzix/test.git


## First push

Now that you told it WHERE its going you can tell it to send the code.

To send the code you just and type in your username/password for github.

    git push -u origin master


## Congrats

If you refresh the page it will now show you whatever you typed inside
readme.md!!!

after you run this command you can just run `git push` and it will remember the
other options.


## Recap

-   To setup
    -   `git remote add origin https://github.com/USERNAME/REPONAME.git=`
    -   `git push -u origin master`
-   Afterwords you can just `git push`


# Misc


## Pulling changes

To pull down changes from a repo you can run the comand

    git pull


## Cloning repos

To get a local copy of a repository online you can run. Note that the remote
normally has a link you can copy when you visit the repo online.

    git clone https://github.com/Renzix/test.git


## Using ssh

Passwords are not a very good way to securely login. The better way is via ssh
keys. In order to do this you have to add a ssh key to your account then when
you set the remote you can give it the ssh url.

    git remote add origin git@github.com:Renzix/test.git


## Removing files

If you would like to stop tracking a file through git you can run the command

    git rm filename


## git status

One useful command to see what you have or have not commited yet is git status.
This shows you which files were modified, commit, untracked and more.


## Flags

Every git command has associated flags with them. These flags change what that
command can do.


## git commit -m

One example is git commit -m which allows you to specify a message from the
commandline instead of going into the editor to write said message. Generally
its better to go into the editor because it shows you what files were changed.

    git commit -m "My first commit!!!"


## Recap

-   To pull down changes from the remote `git pull`
-   To get someone elses repo `git clone`
-   You can also use ssh keys instead of a login
-   You can tell git to stop tracking a file with `git rm filename`
-   git status lets you see which files are being tracked and how
-   Every git options has optional flags associated to it


# Learning

To learn more about git there is a ton of information about it online for free.
Also the man pages for git include a ton of information on it offline. You
cannot see the man pages on windows however you can through WSL(windows
subsystem for Linux).


# Closing

The slides will be up on github <https://github.com/Renzix/Lectures.git>

Any Questions? (made with emacs and org mode)

