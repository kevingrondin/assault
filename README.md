# Assault

> I learn python, even if i prefer javascript, i programming on linode cloud  

- Exemple to extrat on results.json : assault -c 10 -r 100 --json-file results.json https://google.com
- Exemple to print with variable environement at true : DEBUG=true assault -c 10 -r 100 https://google.com

## Install Python

```Shell
apt update

apt install python3-pip

pip3 --version
```

## A little part of SSH

```Shell
ssh-keygen -t rsa -b 4096 -C "monnom@mail.com" -f ~/.ssh/id_rsa-remote-ssh

ssh-copy-id -i ~/.ssh/id_rsa-remote-ssh.pub moncompte@serveur.com
```

```Shell
# Sur le serveur
ssh-add -K ~/.ssh/id_rsa-remote-ssh.pub
```

dans `.ssh/`

```Bash
Host *
  ForwardAgent yes
  RequestTTY
  AddKeysToAgent yes

  Host mon-serveur
    User cloud_user
    Hostname monserveur.com
    IdentityFile ~/.ssh/id_rsa-remote-ssh
    LocalForward 127.0.0.1:8080 127.0.0.1:8080
```

# Alternativ to npm link of nodejs

```Shell
# For setup your app
curl -O https://raw.githubusercontent.com/kennethreitz/setup.py/master/setup.py

# Get .gitignore python
curl -o .gitignore https://raw.githubusercontent.com/github/gitignore/master/Python.gitignore
```

on __setup.py__

```Python
# on line 107
entry_points={"console_scripts": ["assault=assault.cli:cli"],},
```

```Shell
pip3.7 install -e .
```

