## edi Packages for Debian

This repository contains edi debs targeting Debian.

To install edi on Debian stretch use the following commands to add the edi repository:

```bash
sudo apt install apt-transport-https
wget -qO - https://get-edi.github.io/edi-repository/debian/repo.key | sudo apt-key add -
sudo echo "deb https://get-edi.github.io/edi-repository/debian stretch main" > /etc/apt/sources.list.d/edi-repository.list
sudo apt update
```

Now you are able to install edi.

```bash
sudo apt install edi
```

### Cheat Sheet for the Maintainer

Add a package:

```bash
reprepro --basedir debian includedeb stretch ../edi_0.12.1+deb9_all.deb
```

Remove a package:

```bash
reprepro --basedir debian remove stretch edi
```

List the packages:

```bash
reprepro --basedir debian list stretch
```
