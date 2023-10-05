# install-Nodejs
Installation Instructions
If you have root access, you can omit the 'sudo' command as you already have full administrative privileges.

1. Download and import the Nodesource GPG key
  sudo apt-get update
  sudo apt-get install -y ca-certificates curl gnupg
  sudo mkdir -p /etc/apt/keyrings
  curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
