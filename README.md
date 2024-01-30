# ansible-secrets
Learning Ansible secrets management
To edit the password.yml file, use ansible-vault edit secret.yml. The 
password is redhat.

To use this, create a user and a password hash. The user can be whatever 
you want. To create the password hash, you can run "mkpasswd -m sha512crypt" 
from the command line, then paste it into the password.yml file.

Play around with ansible-vault create <file>. Play around with it.

To use the vault, use:
ansible-vault run -m stdout create-users.yml --vault-id @prompt

To remove the user, use:
ansible-vault run -m stdout remove-users.yml --vault-id @prompt

TODO:
Play with using multiple values for users using loops. This 
will be in a later lab, I think.
