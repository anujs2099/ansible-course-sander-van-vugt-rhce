# ansible-modules help
ansible-doc -l | grep -i <search word>
ansible-doc -l | grep -i yum
ansible-doc yum
/EXAMPLE
/^=

# Using Ad Hoc commands
ansible [target] -m [module] [-a 'module options'] [-i inventory]

# Ad Hoc commands to add and remove a user
ansible all -m user -a "name=lisa"
ansible all -m command -a "id lisa"
ansible all -m user -a "name=lisa state=absent"
ansible all -m command -a "id lisa"
ansible all -m command -a "ls -ld /home/lisa"
ansible all -m user -a "name=lisa"
ansible all -m command -a "id lisa"
ansible all -m user -a "name=lisa state=absent remove=yes"
ansible all -m command -a "id lisa"
ansible all -m command -a "ls -ld /home/lisa"

# Ad Hoc command to ping remote hosts
ansible all -m ping

# Ad Hoc command to check if a service is currently running
ansible all -m service -a "name=httpd state=started"

# Ad Hoc command to run any command, but not through a shell
ansible ansible2.example.com -m command -a "systemctl reboot"
ansible all -m ping

# Add Hoc command to run any command through a shell
ansible all -m shell -a "set"

# Add Hoc command to run any command without the need for python
ansible all -m shell -a "id"
ansible all -m raw -a "yum install python3 -y"
ansible all -m raw -a "which python"
ansible all -m raw -a "alternatives --set python /usr/bin/python3"
ansible all -m raw -a "which python"
ansible all -m shell -a "id"

# Ad Hoc command to copy a file to the managed hosts
ansible all -m copy -a 'content="hello world" dest=/etc/motd'
ansible all -m shell -a "cat /etc/motd"
