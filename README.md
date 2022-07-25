# git-ssh-key-genarate-everywhere

**first step**

```base
ssh-keygen -t ed25519 -C your-email
```

**second step**

```base
$ eval "$(ssh-agent -s)"
> Agent pid 59566
```

**third step**

```base
$ ~/.ssh/config
> zsh: no such file or directory: /home/your-username/.ssh/config
```

**four step**

```base
$ touch ~/.ssh/config
```

**five step**

```base
$ vim ~/.ssh/config
```

**copy and past your file.**

```base
Host *
    AddKeysToAgent yes
    IdentityFile ~/.ssh/id_ed25519
```

**six step**

```base
$ ssh-add ~/.ssh/id_ed25519
```

**seven step**

```base
$ ~/.ssh/config
> bash: /home/your-username/.ssh/config: Permission denied
```

**eight step**

```base
$ cat ~/.ssh/id_ed25519.pub
> ssh-ed25519 your-unique-key email@gmail.com # this line copy and past your github settings/ssh and gpg keys
```

``congratulations your key genarate complete.``