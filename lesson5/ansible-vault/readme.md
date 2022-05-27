
# To create an encrypted file
ansible-vault create playbook.yaml

# To create an encrypted file using a password file
ansible-vault create --vault-password-file=vault-pass playbook.yaml

# To view an encrypted file
ansible-vault view playbook.yaml

# To edit an encrypted file
ansible-vault edit playbook.yaml

# To encrypt an existing file
ansible-vault encrypt playbook.yaml

# To decrypt an encrypted file
ansible-vault decrypt playbook.yaml

# To change password on an existing encrypted file
ansible-vault rekey playbook.yaml

# To run a playbook that access vault encrypted files, use the --ask-vault-pass OR -vault-id @prompt OR use the password file
ansible-playbook --ask-vault-pass create-user.yaml
ansible-playbook -vault-id @prompt pre-playbook.yaml
ansible-playbook --vault-password-file=vault-pass pre-playbook.yaml
