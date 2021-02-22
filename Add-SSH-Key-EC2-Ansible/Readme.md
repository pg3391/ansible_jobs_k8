Refer:
https://www.middlewareinventory.com/blog/ansible-ec2-ssh-key/
https://github.com/AKSarav/Add-SSH-Key-EC2-Ansible

USAGE:
ansible-playbook add-key.yml 
-i ansible_hosts 
--user <remote instance user name> 
--key-file <Private key for ec2 instnce> 
-e "key=<User's public key file full qualified path>" #this is additional paramter to let the ansible know to put the key in specific location

Example:  ansible-playbook add-key.yml -i ansible_hosts --user ubuntu --key-file ec2_instance_privateKey.pem -e "key=~/.ssh/id_rsa.pub"
