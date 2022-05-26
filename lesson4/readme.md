# check the directory structure
tree

# ansible-playbook syntax check
ansible-playbook --syntax-check vsftpd.yaml

# ansible-playbook dry run
# if something is not installed, it will not be started so it is of limited use
ansible-playbook --check vsftpd.yaml
ansible-playbook -C vsftpd.yaml

# ansible-playbook execution
ansible-playbook vsftpd.yaml

# ansible-playbook execution with verbosity
ansible-playbook -v vsftpd.yaml
ansible-playbook -vv vsftpd.yaml
ansible-playbook -vvv vsftpd.yaml
ansible-playbook -vvvv vsftpd.yaml

# to undo changes made by a playbook, you have to write a dedicated undo playbook
