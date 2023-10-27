# SSH

# gen key
ssh-keygen -t rsa -b 4096

# copy key
ssh-copy-id -i /root/.ssh/id_rsa.pub root@10.176.18.15

# login with key
ssh -i .ssh/id_rsa username@192.168.178.118
