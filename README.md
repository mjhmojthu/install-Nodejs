# install-Nodejs
Installation Instructions
Node.js
If you have root access, you can omit the 'sudo' command as you already have full administrative privileges.

Download and import the Nodesource GPG key
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
Create deb repository
NODE_MAJOR=20
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list
Optional: NODE_MAJOR can be changed depending on the version you need.

NODE_MAJOR=16
NODE_MAJOR=18
NODE_MAJOR=20
Run Update and Install
sudo apt-get update
sudo apt-get install nodejs -y
Uninstall nodejs Ubuntu & Debian packages
To completely remove Node.js installed from the deb.nodesource.com package methods above:

use sudo on Ubuntu or run this as root on debian
apt-get purge nodejs &&\
rm -r /etc/apt/sources.list.d/nodesource.list &&\
rm -r /etc/apt/keyrings/nodesource.gpg
