---
title: How to install your SSH key on a remote server
date: 2017-10-26
emoji: 🔐
---

## 1*. Nice way*

You can install an SSH key by executing

```bash
ssh-copy-id user@example.com
```

Now you can log in to the remote server with your password and ssh-copy-id will do the rest.

## *2. Manual way*

Append your public ssh key to the `authorized_key` file on the server.

As a one-liner:

```bash
cat ~/.ssh/id_rsa.pub | ssh user@example.com 'cat>> ~/.ssh/authorized_keys'
```

## *Conclusion*

Both commands pretty much do the same. The first way is way easier though.

The next time you can connect to the server using your SSH key.

```bash
ssh user@example.com
```