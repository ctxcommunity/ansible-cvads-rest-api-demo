Copy the template in the pwd_vars/ sub-folder to a new file such as pwd_vars/bob.yml
Enter in the Client_ID and Secret given from the cloud.citrix.com Identity and Access Management section

Encrypt you file by running:
  ansible-vault encrypt pwd_vars/bob.yml

To run the playbook:
  ansible-playbook _converge_demo_cvads_rest.yml --extra-vars="runas_admin=<File you defined in the pwd_vars folder>" --ask-vault-pass
  
For Example:
  ansible-playbook _converge_demo_cvads_rest.yml --extra-vars="runas_admin=bob" --ask-vault-pass
  
