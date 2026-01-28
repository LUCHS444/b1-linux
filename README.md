Partie I
1.
1. ip config /all
   interface wifi: nom = ; adresse IP = 10.152.156.238 ; adresse mac = 50-38-4B-46-70-59 ; adresse réseau = 10.152.156.0 ; adresse broadcast = 10.152.156.255
   interface ethernet: nom = adresse ip = 192.168.56.101 ; adresse mac = 0B-00-29-00-00-08 ; adresse réseau = 192.168.56.0 ; adresse broadcast = 192.168.56.255
   passerelle =  10.152.156.64 (grace à la commande: 'Get-NetIPConfiguration' dans powershell)
  <img width="636" height="576" alt="image" src="https://github.com/user-attachments/assets/2192c1c7-b2f1-4e38-b9c8-4a9466811ab9" />

  pour afficher les informations sur une carte IP: ip config /all
  L'adresse IP de la gateway est: fe80::448a:6ff:fe40:3f17

  Dans le réseau d’Ingésup, la gateway permet aux postes clients d’accéder aux réseaux extérieurs, notamment à Internet et aux autres réseaux internes. Elle joue le rôle de routeur entre le réseau local et le reste du réseau.



2. Première et Derniere ip disponible:

Pour déterminer les IP disponibles, on calcule d’abord l’adresse de réseau et l’adresse de broadcast à l’aide du masque de sous-réseau.
La première IP disponible est l’adresse de réseau + 1, et la dernière IP disponible est l’adresse de broadcast − 1.

Donc:

Réseau : 10.152.156.0

Broadcast : 10.152.156.255

Première IP : 10.152.156.1

Dernière IP : 10.152.156.254


Modification d'adresse IP:

<img width="400" height="87" alt="image" src="https://github.com/user-attachments/assets/b7d1d11d-287c-4e46-9462-ebba48ca1da5" />



B. nmap

Scan du réseau de ma carte wifi: nmap -sP 10.152.156.0/24
 Adresse ip libre = par exemple: 10.152.156.3

 <img width="611" height="97" alt="image" src="https://github.com/user-attachments/assets/0fdb47e5-0cfb-40c2-bfe4-ee70f6bdcf39" />


C. 
Nouvelle modification manuelle d'adresse IP:

<img width="412" height="125" alt="image" src="https://github.com/user-attachments/assets/810797ae-0db7-478e-89e9-bc8333c16e4f" />

Gateway volontairement modifiée:

<img width="470" height="80" alt="image" src="https://github.com/user-attachments/assets/e294c4e4-6330-4d69-997e-4e122c7fe15d" />


DNS = 8.8.8.8



google marche quand j'essaie d'aller dessus


Partie II: A faire en cours




Partie III
1. DHCP

Adresse IP du serveur DHCP du réseau wifi: 
<img width="426" height="142" alt="image" src="https://github.com/user-attachments/assets/9db1cc94-0da0-4f70-935d-156ad1a315ad" />

J'ai utilisé les commandes ipconfig /release puis ipconfig /renew pour demander une nouvelle adresse IP au serveur DHCP.
Cette opération a permis au PC d’obtenir automatiquement une nouvelle adresse IP, ainsi que le masque et la passerelle.

2. DNS
Adresse IP du serveur DNS du réseau wifi: 8.8.8.8


Avec nsLookup je contate que c'est l'adresse DNS du serveur de google.
