Partie 1
A.
1. ip config /all
   interface wifi: nom = ; adresse IP = 10.152.156.238 ; adresse mac = 50-38-4B-46-70-59 ; adresse réseau = 10.152.156.0 ; adresse broadcast = 10.152.156.255
   interface ethernet: nom = adresse ip = 192.168.56.101 ; adresse mac = 0B-00-29-00-00-08 ; adresse réseau = 192.168.56.0 ; adresse broadcast = 192.168.56.255
   passerelle =  10.152.156.64 (grace à la commande: 'Get-NetIPConfiguration' dans powershell)
  <img width="636" height="576" alt="image" src="https://github.com/user-attachments/assets/2192c1c7-b2f1-4e38-b9c8-4a9466811ab9" />

  pour afficher les informations sur une carte IP: ip config /all

  Dans le réseau d’Ingésup, la gateway permet aux postes clients d’accéder aux réseaux extérieurs, notamment à Internet et aux autres réseaux internes. Elle joue le rôle de routeur entre le réseau local et le reste du réseau.
