ssh as root

# Update all packages(This takes time sometime)
apt update
apt upgrade

# Set up Japanese
apt install language-pack-ja
update-locale LANG=ja_JP.UTF-8

# Create user
adduser [username]

# Edit entitlement
visudo 
[username] ALL=(ALL) ALL

