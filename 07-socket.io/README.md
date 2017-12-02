# WebSocket
 Les websockets c'est chouette !!
 Pourquoi me direz-vous? Parce que vous pouvez communiquer en temps réel entre la page web et node.Plus besoin de rafrachir la page pour afficher les nouvelles informations.

 La même page peut envoyer des informations sans passer par un formulaire et recevoir des infromations en direct et tout ça en javascript !

 ## Ce dont vous avez besoin
  1. Coté serveur

    Pour gerer les websocket avec nodeJS vous aurez besoin d'installer le module ```socket.io```  avec npm.

  2. Coté  client

    Pour communiquer avec les websockets , vous aurez besoin d'inclure la version client de socket.io sur vos pages web.
    ```
    <script src="https://cdnjs.cloudflare.com/ajax/libs/socket.io/2.0.4/socket.io.js"></script>
    ```
## Fonctionnement de base
