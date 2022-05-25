# list hosts
ansible -i inventory all --list-hosts
ansible -i inventory ungrouped --list-hosts
ansible all --list-hosts

# Understanding ansible.cfg
cat /etc/ansible/ansible.cfg | grep -v '#' | sed '/^$/d'

# Precedence of ansible.cfg
/etc/ansible/ansible.cfg (default)
~/.ansible.cfg (overwrites the default)
./ansible.cfg (have precedence over the above two)
variable ANSIBLE_CONFIG (have precendence the above three)
ansible --version (shows which configuration file is currently being used)
