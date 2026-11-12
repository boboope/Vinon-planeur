# Le Planeur de poche — copie du club

« Le Planeur de poche » est le petit jeu de planeur proposé à l'Association Aéronautique Verdon Alpilles (AAVA, Vinon-sur-Verdon). Ce dépôt héberge la copie du jeu qui permet les **séances avec un instructeur**.

| Page | Adresse |
|---|---|
| Le jeu | https://boboope.github.io/Vinon-planeur/jeu/ |
| Le poste instructeur | https://boboope.github.io/Vinon-planeur/jeu/instructeur.html |
| La page de test réseau | https://boboope.github.io/Vinon-planeur/ |

La version du jeu est écrite en bas de l'écran d'accueil (« v5.4 »), celle du poste instructeur sous son titre.

## Une séance, en trois gestes

1. **L'instructeur** ouvre le poste instructeur et touche « Ouvrir une séance ». Un code de 8 caractères s'affiche, avec un lien direct.
2. **Chaque élève** (trois au plus) ouvre le jeu sur son propre appareil, saisit le code dans « Séance avec un instructeur » sur l'écran d'accueil (ou ouvre le lien direct), puis décolle.
3. **L'instructeur** voit chaque planeur sur la carte, avec son altitude, sa hauteur au-dessus du sol, sa vitesse, son vario, son inclinaison et son cap. Il peut :
   - imposer le vent (direction, vitesse) et l'agitation de l'air, pour tous ;
   - envoyer à un planeur, ou à tous, une rafale, une aile qui s'enfonce ou une descendance.

Les vols d'une séance ne sont pas classés : ni médaille, ni record, ni défi.

Rien à installer, aucun compte, aucun réglage sur le réseau du club. Il faut seulement que chaque appareil ait accès à Internet (Wi-Fi ou 4G / 5G).

## Si quelque chose ne marche pas

- **L'élève reste sur « connexion… »** : son appareil n'atteint aucun relais. Vérifier sa connexion Internet, puis ouvrir la page de test réseau sur ce même appareil.
- **L'élève reste sur « en attente de l'instructeur »** : le code est différent de celui du poste, ou le poste instructeur est fermé.
- **Le poste instructeur a été fermé par erreur** : le rouvrir et toucher « Reprendre la séance » : le code est le même, les planeurs reviennent.
- **« Séance complète »** : trois planeurs y sont déjà. Un planeur silencieux depuis une minute et demie libère sa place.

## Ce qui circule, et par où

- Pendant une séance, le jeu envoie une fois par seconde la position et les paramètres de vol du planeur ; le poste envoie la météo et les événements. Aucun nom, aucun compte, aucune adresse.
- Ces messages passent par des relais publics gratuits (serveurs MQTT : shiftr.io, TBMQ, EMQX, HiveMQ, Mosquitto), tous à la fois : si l'un tombe, les autres suffisent. Ils voient l'adresse IP des appareils, comme n'importe quel site.
- Les messages sont chiffrés dans le navigateur avec une clé tirée du code de séance : les relais ne transportent que du bruit.
- Hors séance, le jeu n'envoie rien.

## Limites connues

- **Le code est le seul secret.** Quiconque le connaît peut rejoindre la séance, ou envoyer des commandes. Le donner aux élèves seulement, et ouvrir une nouvelle séance (un nouveau code) à chaque fois.
- Les relais sont des services gratuits, sans garantie. Si aucun ne répond, le jeu continue de fonctionner seul, sans instructeur.
- La liaison a été essayée de bout en bout avec des relais de test, sur un ordinateur. Les vrais relais sont ceux que la page de test réseau a atteints au club, à domicile et en 4G / 5G ; la première séance réelle reste à faire.
- Trois élèves au plus par séance.

## Ce que contient ce dépôt

- `jeu/index.html` : le jeu, en un seul fichier.
- `jeu/instructeur.html` : le poste instructeur, en un seul fichier.
- `index.html` : la page de test réseau.

Le jeu est aussi publié sur claude.ai (sans les séances : cette copie-là ne peut pas ouvrir de connexion).

## Droits

Tous droits réservés pour l'instant : la licence sera décidée par le club. Voir le fichier `LICENSE`.

---

*English: the club's own copy of "Le Planeur de poche", the AAVA gliding club's small glider game. It adds sessions with an instructor: the instructor opens the desk page and gets a code; up to three students enter it in the game on their own devices; the instructor then sees each glider (height, speed, climb, position) and sets the wind and the roughness of the air, or sends a gust, a wing drop or sinking air. No account, nothing to install. Messages are encrypted in the browser with a key derived from the session code and travel through free public MQTT relays. All rights reserved for now; the club will decide on a licence.*
