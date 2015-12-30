# learning-ansible
I'm learning how to use ansible.
Using this directory to track changes as I go.

This should be sweet and simple on how to kick off a vagrant box and 
provision a simple LAMP stack in a single yml file.

Most of the examples I've found split everything up into roles, 
which I do want to go to eventually, but I am still learning how everything works.

This stack uses Vagrant, Parallels, and Ansible

Make sure to install vagrant-hostsupdater if you want vagrant to manage your hosts

https://github.com/cogitatio/vagrant-hostsupdater

Great tutorial and where I learned about Ansible:

https://sysadmincasts.com/episodes/45-learning-ansible-with-vagrant-part-2-4

# Usage
Initialize the box with 
vagrant up

log in the box with

vagrant ssh mgmt

run the ansible playbook

ansible-playbook lamp-install.yml

test in your web browser on host:

http://lamp.local

