---
date: 2024-05-25
slug: 2024-05-25

title: Séance du 25 Mai 2024

categories:
- WebDev

tags:
- HTMTL
- CSS
- JavaScript
- Python
---

## Horaire et Lieu
Le Samedi de 10h à 12h à la MPT de Landerneau.

## Au programme
- Conception d'une page HTML avec du JavaScript pour le dynamisme.
- Utilisation du Module Python HTTP.Server (Serveur Web Local).

## Travaux Pratiques
### Création du répertoire et fichier HTML

Nous nous déplaçons dans notre répertoire de travail
```sh
cd travail
```
Nous y créons un répertoire appelé serveurweb
```sh
mkdir serveurweb
```
Nous nous déplaçons dans le répertoire créé
```sh
cd serveurweb
```
Nous créons un fichier "index.html"
```sh
touch index.html
```

### Ouvrons le fichier "index.html"
Nous ouvrons le fichier "index.html" avec notre editeur de texte
```sh
nano index.html
```

### Ajoutons du contenu HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Ma Page</title>
  </head>

  <body>
    <h1>Ma page Web</h1>
  </body>
</html>
```

### Démarrons le serveur web
Nous utilisons la librairie HTTP de Python
```sh
python -m http.server 8080
```

### Affichons la page web dans notre navigateur
Ouvrons notre navigateur et tapons : [http://localhost:8080](http://localhost:8080).

### Modifions notre page HTML
```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">  
  <title>Ma Page</title>
  <style>
    h1 
    {
      color: red;
      text-align: center;
    }
    
    #vert 
    {
      color: chartreuse;
      text-align: center;
    }
    
    div 
    {
      width: 100px;
      height: 100px;
      background-color: red;
      position: relative;
      animation-name: example;
      animation-duration: 4s;
      animation-delay: 2s;
    }

    @keyframes example 
    {
      0%
      {
        left:0px; top:0px;
        background-color:red;
      }
      25%  
      { 
        left:200px; top:0px;
        background-color:yellow;
      }
      50%  
      {
        left:200px; top:200px;
        background-color:blue;
      }
      75%
      {
        left:0px; top:200px;
        background-color:green; 
      }
      100% 
      {
        left:0px; top:0px;
        background-color:red; 
      }
    }
  </style>
</head>

<body>
  <h1>Ma page Web</h1>
  <p>Je fais du vélo</p>
  <h1 id="vert">Ma page Web Titre 2</h1>
  <div></div>
</body>
</html>
```

## Références
- [Github - Hugo | Générateur de Site Statique écrit en Golang](https://github.com/gohugoio/hugo).
- [Shamacher - Brachiograph | Stylo traceur simple et intuitif](https://shamacher.eu/blog/brachiograph/).
- [Flask - Documentation | Micro Framework en Python](https://flask.palletsprojects.com/en/3.0.x/).
- [Nicegui | Un framework Python pour faire des interfaces web](https://nicegui.io/).