<!-- TITLE: Wsl Ubuntu -->
<!-- SUBTITLE: A quick summary of Wsl Ubuntu -->

# Living the Ubuntu Life
### To update the OS package (aka Windows Update for Ubuntu)

```bash
sudo apt update
sudo apt upgrade

# run update again to verify everything is current
sudo apt update
```

`apt-get` works as well but `apt` is the new hotness. Remember to run those commands once a week for an updated and shiny install.

### Copying ssh keys into Ubuntu

Assuming the keys have already been copied into your Windows `\User\Shawn\.ssh` folder. I store site specific ssh keys on a USB key that's strongly encrypted. It's not a perfect solution and I'll most likely move such keys into something like 1Password or a self-hosted BitWarden.

```bash
mkdir ~/.ssh
cp /mnt/c/Users/Shawn/.ssh/id* ~/.ssh/

# Set permissions
chmod 600 ~/.ssh/config
chmod 400 ~/.ssh/id_rsa

# edit your ssh config
nano ~/.ssh/config

# Add the following lines, save
Host *.some-site.com
User ubuntu
IdentityFile ~/.ssh/id_rsa
ForwardAgent yes
ServerAliveInterval 240
ServerAliveCountMax 2
```