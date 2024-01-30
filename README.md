# ansible-secrets
Learning Ansible secrets management

To edit the password.yml file, use ansible-vault edit secret.yml. The 
password is redhat.

To use this, create a user and a password hash. The user can be whatever 
you want. To create the password hash, you can run "mkpasswd -m sha512crypt" 
from the command line, then paste it into the password.yml file.

Play around with ansible-vault create [file] and then ansible-vault edit [file].

To use the vault, use:
ansible-navigator run -m stdout create-users.yml --vault-id @prompt

To remove the user, use:
ansible-navigator run -m stdout remove-users.yml --vault-id @prompt

You can also do things like create a file called my-pass with the password
you want to use (e.g. redhat). Use chmod 600 my-pass to protect it from 
prying eyes.

To use it, run:
ansible-navigator run -m stdout create-users.yml --vault-password-file=my-pass

TODO:
Play with using multiple values for users using loops. This 
will be in a later lab, I think.
