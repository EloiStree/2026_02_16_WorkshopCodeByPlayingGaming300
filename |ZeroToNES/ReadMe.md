
Salut a toi ;)

Nous allons apprendre a programmer en Godot en partant de Zero.
Mais plutot que de faire un jeu, nous allons jouer a des jeux avec des simulateurs de Manete Xbox 😋.

J ai creer un atelier pour Unity 3D qui s appelle de Zero a NES.
Cours: https://github.com/EloiStree/2025_01_19_WorkshopNesOnAndroid
Video: https://youtu.be/dLRaB3z-4DQ

L idee est d apprendre la programmation en creant une manette NES sur telephone avec les UI du game engine et les touches de claviers / manettes.
Une fois la manette NES creer, on essai de jouer as des jeux avec du code en creant ce que lon appelle des macros.

Pour cela nous devons apprendre ce qu est un String ( du text) et pratiquer le fait de faire attendre notre code.

Nous le pratiquons en creant une manette NES 
Mais comme la repetition est mere du savoir, je vous laisserai pratiquer le fait de faire une manette Xbox par la suite.
Il faut re-pratiquer pour que notre cerveaux assimile bien la matiere.

---------------

Comme vous ne savez pas encore ce qu est de la programmation.
Je vous ai installer sur votre ordinateur un project (si vous etes en atelier avec moi)

Lien du project: 
https://github.com/EloiStree/2026_01_18_godot_nes_controller_udp

Qui utilie une boite a outils que je vous ai preparer:   
https://github.com/EloiStree/2026_01_18_gdp_nes_controller_udp  

Pratiquons notre code sur ce jeu localement avant de faire du pilote mes ordinateurs distances:
https://github.com/EloiStree/2026_01_18_unity_nes_multi_controller/releases/tag/2026_02_12

[<img width="1275" height="662" alt="image" src="https://github.com/user-attachments/assets/74f2d2fd-162c-4f7e-b769-b17701446292" />](https://github.com/EloiStree/2026_01_18_unity_nes_multi_controller/releases/tag/2026_02_12
)

----------------------------------

La permier etape est pour moi.

Je ne peux pas vous apprendre le premier jour comment on envoi des petites messages entre les ordinateurs.

Je dois donc coder en godot un outil qui vise quelque part.
- Vers une addresse IP :  lordinateur que l on veut viser.
- Vers un port : l application que lon veut viser
- vers une joueur : le numbero du joueur ou de la manette.

Et comme on veut pas le changer en permanence, je dois creer un script que ce souviendra de ce que vous lui donner.

----------------------|

# Premier exercice

## Hello World ;)

Par tradition le premier exercice est d afficher dans la console un message qui dit "bonjour le monde"

- [ ] Ajoutons un bouton
- [ ] Creatons un script godot
- [ ] Affichons print dans _ready.
- [ ] Voir ce que ca donne
- [ ] Faire un methode qui est appellable
- [ ] Appeler la methode avec le bouton
- [ ] Ajouter un Label dans la fenetre
- [ ] Ajouter un export dans dans le script du label
- [ ] Deposer le label
- [ ] Changer le text du label avec du code.
- [ ] Tada vous etes maintenant un developeur d application.


## Envoyons un Hello World sur mon ordinateur.

To DO:
- [ ] Rajouter a Unity NES un recepteur UDP pour le text sur le port 3614.
  - [ ] Pour apprendre le fait d envoyer un messsage sur le reseau plus facilement.

Comme on veut envoyer le message sur un autre ordinateur.
Il faut utiliser mon script.

- [ ] Deposons un Node (un element du projet) pour envoyer des messages
- [ ] Changeons vers qui il vise : ip , port , player
- [ ] Ajoutons dans votre script un export qui visera vers mon script
- [ ] Appelons la methode send_text avec en parametre un Hello World
- [ ] Ta da, normamlement vous devriez voir un message Hello World dans le jeu NES Multi.











