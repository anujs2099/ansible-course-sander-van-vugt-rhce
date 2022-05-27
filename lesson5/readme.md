# Variables can be defined within a playbook or at an host level which is preferred

# host level variables can be defined in the inventory, inclusion files (recommended), local facts

# another type of host level variable is ansible facts which is facts about the hosts

# Variable precedence
Global scope: within inventory / applies to the whole playbook --> fourth precedence
Play scope: within a play in a playbook / applies only to the play --> third precedence
Host scope: within inventory or host variable inclusion file / applies only to the host --> second precedence
Global scope: command line / applies to the whole playbook --> first precedence

# Built-in variables
hostvars
inventory_hostname
inventory_hostname_short
groups
group_names
ansible_check_mode
ansible_play_batch
ansible_play_hosts
ansible_version

