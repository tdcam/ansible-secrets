# ansible-secrets
Learning Ansible secrets management
To edit the password.yml file, use ansible-vault edit secret.yml. The 
password is redhat.

To use this, create a user and a password hash. The user can be whatever 
you want. To create the password hash, you can run "mkpasswd -m sha512crypt" 
from the command line, then paste it into the password.yml file.
