---
title: Séance du 23 Septembre 2023
date: 2023-09-23
slug: 2023-09-23
---

## Horaire et Lieu
Samedi matin de 10h à 12h à la MPT de Landerneau.

## Au Programme
- Tour de table (suite).
- Présentation de l'Atelier (suite).
- Présentation du Raspberry Pi
  - Système d'Exploitation.
- Présenration de Python
  - Installation de l'environnement.
    - Utilisation de l'application Thonny (éditeur pour Python).
  - Premier programme en Python.
- Utilisation de la ligne de commande.
  - `ls` - pour lister les fichiers.
  - `cd` - pour se déplacer dans un répertoire.

## Travaux Pratiques
Création d'un premier programme en Python
```sh
# Nous créons le fichier
touch bonjour.py
# Nous l'éditons
nano bonjour.py
```
### Code Source Python
```py
# Déclaration des variables
mon_nom = "Kevin"
mon_age = 25
ma_température = 37.2

# Affichage des variables
print("mon nom est: ", mon_nom)
print("mon age est: ", mon_age)
print("ma temperature est: ", ma_temperature)
print(f"mon nom est {mon_nom}, mon age {mon_age}")

# Si la variable mon_age est supérieure ou égale à 18 alors
if mon_age >= 18:
  # Nous affichons que la personne est majeure
  print("vous êtes majeur")
# Sinon
else:
    # Nous affichons que la personne est mineure
    print("vous êtes mineur")
```

## Références
- [Wikipedia | Concept de Fichiers et de Répertoires](https://fr.wikipedia.org/wiki/R%C3%A9pertoire_(informatique)).
- [Thonny | IDE pour programmer en Python](https://thonny.org/).
- [WayToLearnX | Tutoriel Python](https://waytolearnx.com/2020/06/tutoriels-python.html).
- [Python Docs | Python sortie et chaîne de caractères formatée](https://docs.python.org/fr/3/tutorial/inputoutput.html#formatted-string-literals).
- [FormaTux | Les fondamentaux GNU/Linux](https://www.formatux.fr/formatux-fondamentaux/index.html).
- [MIT - Terminus | Jeu pour apprendre les commandes Linux](https://web.mit.edu/mprat/Public/web/Terminus/Web/main.html).
- [OverTheWire - Wargames Bandit | CTF pour les débutants](https://overthewire.org/wargames/bandit/).