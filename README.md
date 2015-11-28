### Django Setup automation using Ansible

This is a project which aims to automate the setup of a Django project based on [Django setup guide](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-django-with-postgres-nginx-and-gunicorn).

It uses a [Ansible](http://docs.ansible.com/) playbook to do this. 

1. To install ansible , refer [here](http://docs.ansible.com/ansible/intro_installation.html).

2. Then edit or create a `/etc/ansible/hosts` file and add the IP address or hostname of server you want to deploy on. More instructions can be found [here](http://docs.ansible.com/ansible/intro_getting_started.html#your-first-commands). Also follow commands to setup ssh-agent given here.

3. As ansible authenticates using ssh , you need to add your public ssh key in `authorized_keys` on the machine you want to deploy to.

4. You can test your server is reponding by running `ansible all -m ping`

5. If the last command is a success then you can run the playbook on the machine using `ansible-playbook playbook.yml --ask-become-pass` after replacing `{{host}}` in the `playbook.yml` file with the IP address or hostname.

This project is a work in progress.

