---
title: How to manage your dotfiles with homesick
date: 2013-01-22
emoji: 🏯
categories: Programming
---

Since quite a while, I try to find a good solution for sharing my dotfiles between my different computers.

[I started with chef](http://www.rocu.de/how-to-setup-your-mac-automatically-with-chef/) — Unfortunately, this did not work so well. Especially if you also want to use your dotfiles on a server. Also, it felt a little complicated.

The next approach I took was putting my dotfiles into my Dropbox and symlink them. This worked ok. But Dropbox on a server? No way.

So, I kept looking. A few days ago, I stumbled over [homesick](https://github.com/technicalpickles/homesick) — an astonishing ruby gem that manages your dotfiles.

## *How to set it up*

First install homesick:

```bash
gem install homesick

```

Now create a “castle”. A castle is a collection of dotfiles.

```bash
homesick generate ~/dotfiles

```

This creates a git repro with a /home folder inside. Just put your dotfiles / dotfolders in there. Then push the stuff to GitHub.

Now install the castle with homesick.

```bash
homesick clone https://github.com/foo/dotfiles.git
```

Now let homesick do its magic.

```bash
homesick symlink dotfiles
```

All the dotfiles from within this castle will be symlinked.

## *This is wonderful!*

- You feel at home at each of your servers in no time
- You share your dotfiles with the world
- [You can learn from others and refine your files](http://dotfiles.github.io/)
- You can put essential little scripts into a .bin directory.
- The castle concept allows you to try someone else’s dotfiles

## *A word of caution*

Please do not put sensitive information into you dotfiles.Especially ssh keys, bash histories and passwords in configurationfiles do not belong on GitHub.

## *Try it!*

Seriously. It’s magical. This is one of those things that you try out, and you ask yourself how you could possibly live without it.

Interested? Have a look [at my dotfiles](https://github.com/shostakovich/dotfiles).