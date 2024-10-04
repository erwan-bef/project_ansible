Bonjour,
Dans ce répèrtoire vous trouveraiez l'ensemble du code qui m'a permis de reproduire à partir de l'outil ansible et en quelques minutes l'ensemble de l'infrastructure réseau complet qui m'a été demandée de configurez et de managée durant mon premier stage en Août 2024.


-inventaire en yaml
all:
  vars:
    ansible_user: admin
serveur:
  hosts:
    server1:
      ansible_host: adresse_ip_server1
    server2:
      ansible_host: adresse_ip_server2

  vars:
    ansible_password: mot_de_passe_admin
    

-vérification avec le module ping que ça fonctionne 
 ansible -i nom_du_fichier all -m ping
