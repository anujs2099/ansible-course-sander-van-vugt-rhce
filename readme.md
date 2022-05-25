
Course Link: https://learning.oreilly.com/videos/red-hat-certified/9780135987513

Course Name: Red Hat Certified Engineer (RHCE) EX294: Red Hat Ansible Automation

# Make sure that subscription-manager is already setup (for the exam)

# Using repositories to install ansible (for the exam as root or with sudo priviledges)
On control node: 
subscription-manager repos --list
subscription-manager repos --list | grep -i ansible
subscription-manager repos --enable=ansible-2-for-rhel-8-x86_64-rpms
yum install ansible
ansible --version

On managed nodes:
yum install python3


# Using Python pip to install ansible (root or with sudo priviledges)
On control node: 
yum install python3
yum install python3-pip
which python
alternatives --set python /usr/bin/python3
which python
su - ansible
pip3 install ansible --user
ansible --version

On managed nodes:
yum install python3
which python
alternatives --set python /usr/bin/python3
which python
