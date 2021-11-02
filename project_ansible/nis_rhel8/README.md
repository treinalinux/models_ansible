# nis


## Files and Folders

mkdir nis_rhel8
touch inventory.yml playbook.yml README.md

mkdir -vp roles
cd roles/

ansible-galaxy init master
mkdir -vp master/files

ansible-galaxy init auxiliary
mkdir -vp auxiliary/files

ansible-galaxy init nfs
mkdir -vp nfs/files

ansible-galaxy init clients
mkdir -vp clients/files


