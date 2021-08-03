# freebsd-workstation-rpi3
Ansible playbook for configuring FreeBSD as workstation on Raspberry Pi 3

## Configure

After installation FreeBSD 13.0 run below commands
```sh
# As root
pkg install python git-lite py38-ansible sudo
visudo	# Allow your user run with sudo, usualy uncomment line for wheel group
```
```sh
# As user
git clone https://github.com/alet/freebsd-workstation-rpi3.git
cd freebsd-workstation-rpi3
ansible-playbook --ask-become-pass -c local -i 'workstation-rpi3,' site.yml
```
