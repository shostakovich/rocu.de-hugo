---
title: Host your emails with Mail-in-a-Box
date: 2017-10-22
emoji: 🏤
---

At our cooperative ([TechGenossen](https://techgenossen.de/)) we used Gmail as our Email-Provider at first. But we found Gmail to be too expensive for our many members.

So, we decided to self-host our emails.

Setting up your email server can be quite hard and involves many moving parts. Fortunately, we found [Mail-in-a-Box](https://mailinabox.email), a fantastic open-source project, which helps you set up a mail server in no time.

![Mail-in-a-Box lets you become your mail service provider in a few easy steps. It’s somewhat like making your own Gmail, but one you control from top to bottom.](/images/bbec599ab9.png)

Mail-in-a-Box lets you become your mail service provider in a few easy steps. It’s somewhat like making your own Gmail, but one you control from top to bottom.

Technically, Mail-in-a-Box turns a fresh cloud computer into a working mail server. But you don’t need to be a technology expert to set it up.

*Source: mailinabox.email*

[Mail-in-a-Box](https://mailinabox.email) features an

- IMAP-Server
- An easy to use Control-Panel
- Nextcloud for contacts
- Roundcube for webmail

It is easy to set up on fresh Ubuntu 14.04. machine.

```bash
curl -s https://mailinabox.email/setup.sh | sudo bash
```

The software will guide you through the installation.

All you have to do is change some DNS-Records and voilà — it works out of the box.

As the admin of the server, you regularly receive emails about how to maintain the box.

I am pleased with the mail server and with the project.