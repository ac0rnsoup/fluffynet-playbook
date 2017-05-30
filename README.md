This is an ansible playbook to set up a fluffynet tier 4 node from source code on Ubuntu Xenial.

This is meant to be run directly on a clean dedicated box as is.

Make sure you have the latest ansible installed (2.3) - I usually install a python virtual environment and install ansible in there.

If you want to tweak the variables, they are located in group_vars/monero

The underlying monero role is not documented yet. To see all tweakable variables, look in roles/ac0rnsoup.monero/defaults/main.yml after running the ansible-galaxy install. 

    git clone https://github.com/ac0rnsoup/fluffynet-playbook.git
    cd fluffynet-playbook
    ansible-galaxy install -r requirements.yml
    ansible-playbook playbook.yml

After a while (the build from source can take quite a while depending on your system) you should have a tier 4 fluffynet node.
RPC port is open and unrestricted. If you know how to tweak ansible variables, you'll be able to change this easy enough.
