# Vinon-planeur

Page de test réseau pour « Le Planeur de poche », le petit jeu de planeur de l'Association Aéronautique Verdon Alpilles (AAVA, Vinon-sur-Verdon).

**La page :** https://boboope.github.io/Vinon-planeur/

## À quoi elle sert

Elle répond à une question : sur ce réseau, deux appareils (téléphone, tablette, ordinateur) peuvent-ils se parler directement ? C'est ce qu'il faut savoir avant de construire un mode où un instructeur agit en direct sur le vol d'un élève.

## Comment s'en servir

1. Ouvrir la page sur deux appareils, sur place.
2. Sur chaque appareil, indiquer comment il est connecté : Wi-Fi, 4G / 5G ou câble.
3. Sur le premier, toucher « Créer un code ». Sur le second, saisir ce code puis toucher « Connecter ».
4. Attendre le résultat (une dizaine de secondes), puis toucher « Copier le rapport » sur chaque appareil et coller le rapport dans un message.

À faire deux fois :

- un téléphone en 4G et l'autre appareil sur le Wi-Fi du lieu. Sur le téléphone, couper le Wi-Fi. Dans ce cas la page laisse de côté les adresses locales : seul un lien à travers Internet peut réussir. Sans cela, un téléphone et un ordinateur du même propriétaire se trouvent un chemin privé (partage de connexion, câble, Bluetooth) et l'essai ne prouve rien ;
- puis les deux appareils sur le même Wi-Fi.

Si l'essai en 4G échoue, c'est un vrai résultat : entre ces deux réseaux, un lien direct n'est pas possible.

Le rapport dit si le lien direct reste sur le même réseau ou s'il traverse Internet, et sur quels indices. Quand la page ne peut pas le savoir, elle l'écrit.

## Ce que fait la page

- Un seul fichier, `index.html`. Aucun compte, aucun serveur du club, rien n'est enregistré.
- Elle contacte des services publics gratuits (ntfy.sh, des serveurs MQTT publics, des serveurs STUN). Ils voient l'adresse IP de l'appareil, comme n'importe quel site.
- Les messages échangés pour s'appairer sont chiffrés dans le navigateur avec une clé tirée du code.
- Le rapport ne contient ni adresse IP ni nom.

---

*English: a one-file network test page for the AAVA gliding club's small glider game. Open it on two devices at the venue, create a code on one, type it on the other, then copy the report. No account, no server, nothing stored.*
