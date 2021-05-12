# fully-sources.list-linux-repositories

This repository created for completely sources.list files ( Repositories for APT ) from other systems.


# NOTE:
If you're using this sources.list(s) don't use "apt-get install <Package> -y".
Becase it's have multi repository and they're not eval. May be some packages not work or delete your packages !

# Solution:
Move this files are end with '.list' to '/etc/apt/sources.list.d/'.
Then use "apt-get update" to update list of packages are found.
Then with "apt-get install <Package_Name>" 

REMEMBER:
Remember read list of packages are Install/Remove/Upgrade to make sure it's working safe.
Some times with installing packages all of packages on your system will be removed.
If before enter 'y' to accept and install package you see this event, Run "apt-get download <Package_Name>" in directory have 777 access (-rwxrwxrwx . you can see with "ls -la" and if not had 777 access change with "chmod 0777 <Directory_Name>").
OK, In next step use "dpkg --install <Downloaded_File_Name>" to install package. Then Run "apt-get install -f" to fix depends not installed for this package.


# Enjoy :)
