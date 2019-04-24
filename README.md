# ansible_windows

Cette configuration est un exemple pour pouvoir manipuler des machines windows via ansible .

Une fois ansible installer, il vous suffit de cloner le repositories git.

le Repo présente 2 playbooks ansible et une configuration spécifique du fichier host

Le 1er playbook (install_choco.yml) va permettre d'installer chocolatey qui le gestionnaire de paquets pour Windows, il va nous permettre par la suite d'installer Tomcat,mysql etc ..

Le 2e playbook (choco3.yml) va installer tomcat et mysql

la configuration du fichier fonctionnne seulement pour des machines Windows : 

nous avons spécifier l'ip de la machine dans un groupe win, nous avons spécifier plusieurs variables ,
 - ansible_user : l'utilisateur avec lequelle ansible va se connecter a la machine
 - ansible_password : le mot de passe de l'utilisateur
 - ansible_connection : le type de connection que windows utilise (ici WinRM)
 - ansible_winrm_server_cert_validation : permet d'éviter la création de certificat 
 
 
 
