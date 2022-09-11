# These are the notes from lesson 3.

Lesson 3 is about git, which we are going to use from now on.


## GIT

First we have to configure git on the computer we are using.

```sh
git config --global user.name "MJ Marks"
git config --global user.email "mjmarks09@icloud.com"
```

## Set up SSH keys

We are using SSH to authenticate on `github.com`.  So, we have to set up SSH keys

```sh
ssh-keygen
```

Accept the default settings, then copy the public key from `$HOME/.ssh/id_rsa.pub`

## Initialize the git repository

Now we will initialize the git repsoitory on the local machine.

```sh
cd $HOME/Documents/computer_class
git init
git add -A
git commit -m "Initial commit"
git branch -M main
```

## Create the remote repository on Github.com

Next we logged in to github and created a new repostory.  After we did that, it gave us instructions on pushing our local repository to the remote.

```sh
git remote add origin git@github.com:margaretmarks/computer_class.git
git push -u origin main
```

Now our local repository has been pushed to [Github](https://www.github.com).

## Make a new copy

To make a new copy of the repository on a new computer (or even on the same computer) we can `clone` it.

```sh
git clone git@github.com:margaretmarks/computer_class
```

Note: we need to have our private ssh key on the computer to authenticate SSH.

## To push updates

After each class, we have to commit our changes, and push to [Github](https://www.github.com).

```sh
git add -A
git commit -m "[Commit message]"
git push
```

## To pull updates

At the beginning of each lesson we will pull our repo.

```sh
git pull
```

