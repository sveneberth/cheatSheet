# SSH

### gen key as local machine
```sh
ssh-keygen -t ed25519
# RSA (obsolete): ssh-keygen -t rsa -b 4096
# or
ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519_myserver
```

### copy key to server
```sh
ssh-copy-id -i /root/.ssh/id_rsa.pub root@myserver
```

### login with key
```sh
ssh -i .ssh/id_rsa username@192.168.XXX.XXX
```


### Register SSH key for host:
```sh
vim ~/.ssh/config
```
```config
Host server-sven
  HostName server.example.com
  User sven
  IdentityFile ~/.ssh/id_ed25519_myserver
  IdentitiesOnly yes

Host 192.168.XXX.XXX
  User sven
  IdentityFile ~/.ssh/id_rsa_myserver
  IdentitiesOnly yes
```
