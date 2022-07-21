---
title: Script to disable internet connectivity for Mac OS
date: 2012-09-30
emoji: 🚫
categories: Programming
---

<aside>
💡 **Little update (18.09.21):** I do use [Freedom](https://freedom.to/) now. It got even more expensive - but it syncs between all my devices and changed from a simple internet kill-switch to something even more useful. I found it great to disable news sites and other addictive sites during the corona years.
</aside>

From time to time, I really want to make it hard for me to seek for distractions.

I found myself using the nice Mac OS X tool [Freedom](https://freedom.to/) all the time. Freedom disables the network connectivity, which means no Twitter, Facebook etc.

But when I revisited the site, I found that the author now charges $10 for it - That’s just a little too expensive in my opinion.

So, I went out, and it took me 5 minutes to come up with freedom.sh.

```bash
# !/bin/bash
echo "Enough of this filthy internet" | cowsay -s
sudo route -n delete default &> /dev/null
```

[Cowsay](http://en.wikipedia.org/wiki/Cowsay) required. (If you prefer not to install cowsay just remove the line!)

```text
________________________________
< Enough of this filthy internet >
--------------------------------
            ^__^
            (**)_______
            (__)       )/
             U  ||----w |
                ||     ||
```

To reenable your internet, you have to add back the default route or restart your computer.