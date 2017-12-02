### Créer un serveur web avec Nodejs 

Nous allons d'abord créer un fichier nommé "server.js" et y inclure le module "http"
compris dans Node:

```
var http = require("http");
```

Une fois le module "http" inclus dans notre fichier "server.js", nous aurons accès à la fonction
"http.createServer()" qui comme son nom l'indique, nous permettra de créer notre premier serveur web. Cette fonction
va nous passer deux paramètres : les objets: request et response.

L'objet "request" va nous fournir des informations concernant la requête client tel que l'url, les en-têtes HTTP,...
Tandis que l'objet "response" servira à retourner des données au côté client de notre app. 

```
var server = http.createServer(function(request, response) {
});
```

Le but étant de renvoyer du contenu, ici seul l'objet response va nous intéresser.
la méthode "response.writeHead()" va définir le statut de notre requête http ainsi que le type de contenu
que l'on souhaite retourner. Ensuite "response.write()" va tout simplement, permettre de concevoir notre
document html. Et enfin la "response.end()" va être appelée afin de signifier la fin de notre réponse.

```
 response.writeHead(200, {"Content-Type": "text/html"});
 response.write(`
            <!doctype html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport"
                  content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
            <meta http-equiv="X-UA-Compatible" content="ie=edge">
            <title>Document</title>
        </head>
        <body>
        <p>Helooooow world</p>
        </body>
        </html>
    `);
    response.end();
```
La dernière méthode appelée dans notre fichier sera "server.listen()", qui va lier notre serveur au port 
de notre choix.

```
server.listen(8080);
```

Il ne nous reste plus qu'a lancer notre serveur via le terminal grâce a ligne de commande ci-dessous 
et à admirer notre magnifique message "hello world" à l'adresse :
http://localhost:8080

```
node server.js
```


Liens Utile(s) :  
[Une première application avec Node.js](https://openclassrooms.com/courses/des-applications-ultra-rapides-avec-node-js/une-premiere-application-avec-node-js)
