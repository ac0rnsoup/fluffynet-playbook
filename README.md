This is a playbook to set up a fluffynet tier 4 node from source code on Ubuntu Xenial.

This is meant to be run directly on a clean dedicated box as is.

Make sure you have the latest ansible installed (2.3) - I usually install a python virtual environment and install ansible in there.

git clone https://github.com/ac0rnsoup/fluffynet-playbook.git
cd fluffynet-playbook
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml

After a while (the build from source can take a while depending on your system) you should have a tier 4 fluffynet node.
RPC port is open and unrestricted. If you know how to tweak ansible variables, you'll be able to change this easy enough.

The underlying monero role is not documented yet, you'll have to look in defaults/main.yml to see a complete list of the variables you can mess with.
