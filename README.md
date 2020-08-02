
# Git

## What is git?

You should take a look at the
[Wikipedia](https://en.wikipedia.org/wiki/Git) article, but the gist of
it is that git is a piece of software that allows many people to work on
the same code and keep track of each other's changes.

## Why should you use it?

Have you ever tried to work a single project with multiple people?
It can very quickly become a mess. If I'm writing one part of a program
on my laptop, and you're writing another part on yours, what happens
when both of us finish? Now I have to send you my code (or vice versa)
so that you can integrate my changes into the program. Then you have to
take my copy of the program, compare it to your copy of the program, and
manually edit in my changes.

What a lot of repetitious work! Isn't that what we have computers for?
Yes! Software that tries to solve these kinds of problems is
generally called version control, and git is one of the more popular
(and powerful) version control systems currently in use.

## How do I install it?

### Windows

Go to [git-for-windows.github.io](https://git-for-windows.github.io/),
and click "Download". That should take you to a page with some release
notes on it. Scroll down the section marked "Downloads" and find the
appropriate .EXE file file for your machine. This will probably be the
file marked "Git-2.14.2.3-64-bit.exe". If you're lost, here are some
direct
[64-bit](https://github.com/git-for-windows/git/releases/download/v2.14.2.windows.3/Git-2.14.2.3-64-bit.exe)
and
[32-bit](https://github.com/git-for-windows/git/releases/download/v2.14.2.windows.3/Git-2.14.2.3-32-bit.exe)
download links.

Once you've downloaded the installer, follow the on-screen instructions
to finish the installation. If you're not sure what to do, accepting the
defaults should yield reasonable results.

### Macs

If you already have XCode installed you needn't do anything more here.
XCode includes git by default.

If you don't have XCode and would like to have git, download
git-osx-installer from
[SourceForge](https://sourceforge.net/projects/git-osx-installer/files/).
If you follow the SourceForge link, you should be presented with a list
of various versions of git-osx-installer. Most likely you'll want the
latest one ("git-2.14.1-intel-universal-mavericks.dmg"), but this may
depend on your operating system version.

### Linux

Search for "git" in your distribution's package manager, and install it.

## How do I use it?

### Clone a repository

When you want to download and work on someone else's code, the first
thing that you want to do is download the person's source code and
associated change history from their repository (a.k.a. their repo).

Let's try this out; Open your operating system's terminal application,
type the following and press [ENTER]:

`$ git clone https://github.com/FoothillCSClub/git-workshop.git`

This will clone the source code for this workshop into the folder
"git-workshop". (The `$` symbol represents whatever your operating
system gives you in the way of a prompt. Don't type it.)

You usually want to move into a folder after you've just cloned it:

`$ cd git-workshop`

### Make some changes

Open your favorite text editor and write a few lines about yourself.
Don't say anything too personal, because we're going to share this with
everyone else in a few steps. Save the file as `${your_name}.txt`, where
`${your_name}` is your first name. Make sure to save the file in the
git-workshop folder.

### Commit your changes

Now that you've made your changes to the repository it's time to publish
them so that the rest of us can use them. The first thing to do is to
*commit* your changes to your local copy of the repository. Committing
tells git exactly which changes you want to publish, and it also allows
you to provide a message attached to your changes to inform your fellow
programmers of *why* you made the change.

To commit your changes type:

`$ git add ${your_name}.txt`  
`$ git commit -m "${commit_message}"`  

Where `${commit_message}` is your comment for this commit. In this case,
it should probably be something like "Introducing myself", but feel free
to be creative.

### Publishing your changes

If you type

`$ git status`

You should see something like the following:

```
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
nothing to commit, working tree clean
```

This means that you have a some changes that you've made that only you
can see, because you haven't sent them to anyone else's repo. To fix
this problem type:

`$ git push`

This will contact CS Club's server and upload your changes, so that the
next time anyone does a `git pull` in their own repo, they will download
your changes, an incorporate them into their source tree.

Congrats! You've made your first use of git!
