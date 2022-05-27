# You can run fact gathering in an ad hoc command using the setup module
ansible all -m setup

# To show facts, use the debug module to print the vaule of the ansible_facts variable

# To disable fact gathering, set the gather_facts to false at either global scope by mentioning it in the ansible.cfg file or at a play scope by mentioning it in the playbook
vi /etc/ansible/ansible.cfg
/gather

# Custom facts are stored in an ini or json file in the /etc/ansible/facts.d directory on the managed hosts and the name of the files must end in .fact

# Custom facts are stored in the ansible_facts.ansible_local variable
ansible all -m setup -a "filter=ansible_local"
