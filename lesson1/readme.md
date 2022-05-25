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
which python
alternatives --set python /usr/bin/python3
which python


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


# Setting up the required environment
On all nodes: (root or with sudo priviledges)
vi /etc/hosts
<add the proper dns static ip addresses with their hosts>
useradd ansible
echo password | passwd --stdin ansible
echo "ansible ALL=(ALL) NOPASSWD:ALL" > /etc/sudoers.d/ansible

On control node:
su - ansible
ssh-keygen
ssh-copy-id ansible1.example.com
ssh-copy-id ansible2.example.com
ssh ansible1
	exit
ssh ansible2
	exit


# 
