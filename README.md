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

# Add swap
# You need to consider size of swap yourself.

mkdir /var/swap

dd if=/dev/zero of=/var/swap/swap0 bs=2M count=4096

chmod 600 /var/swap/swap0

mkswap /var/swap/swap0

swapon /var/swap/swap0

vi /etc/fstab

/var/swap/swap0 swap swap defaults 0 0
