### ssh keys

create ssh key pair from workstation -> server

create ssh key pair from server -> github

[https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent]

`ssh-copy-id -i ~/.ssh/id_ed25519.pub stephen@192.168.86.22`

`ssh stephen@192.168.86.22`

upload to github

`ssh -T git@github.com`

### github

create repo in org
change remote
push