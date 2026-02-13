
To Do:
- [ ] Ajouter un script qui utiliser le action system de Godot pour les 8 bouttons de la NES
- [ ] Ajouter un script qui prendre un nom de manette, un button et transform en event
- [ ] Ajotuer un script qui prenre un nom de manette, un axis et let transform en event sur les bord et la death zone
- [ ] Finir la page A4 pour les touches Xbox
- [ ] Uploaded the code sur les ESP32

--------- 


Salut a toi ;)

Nous allons apprendre a programmer en Godot en partant de Zero.
Mais plutot que de faire un jeu, nous allons jouer a des jeux avec des simulateurs de Manete Xbox 😋.

J ai creer un atelier pour Unity 3D qui s appelle de Zero a NES.
Cours: https://github.com/EloiStree/2026_02_05_workshop_nid_nes_git_and_sobel/tree/main/CreateNesInUnity
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




## Ca ressemble a quoi en Python et en Godot d envoyer des messages text ?

``` python
import socket
import time
import random

PORT = 3614
BROADCAST_IP = "127.0.0.1"  

messages = [
    "Hello, this is a random message!",
    "How are you doing today?",
    "Python is great for socket programming.",
    "This is a test message.",
    "Random message number 5.",
    "Did you know that Python was named after Monty Python?",
    "Sockets are a way to communicate between processes.",
]

# Create UDP socket
with socket.socket(socket.AF_INET, socket.SOCK_DGRAM) as s:
    s.setsockopt(socket.SOL_SOCKET, socket.SO_BROADCAST, 1)
    print(f"Broadcasting messages on UDP port {PORT} every 2 seconds")

    try:
        while True:
            message = random.choice(messages)
            s.sendto(message.encode("utf-8"), (BROADCAST_IP, PORT))
            print(f"Broadcasted: {message}")
            time.sleep(2)
    except KeyboardInterrupt:
        print("Exiting...")
```

``` gdscript
extends Node

var udp := PacketPeerUDP.new()
var messages := [
    "Hello, this is a random message!",
    "How are you doing today?",
    "Python is great for socket programming.",
    "This is a test message.",
    "Random message number 5.",
    "Did you know that Python was named after Monty Python?",
    "Sockets are a way to communicate between processes."
]

func _ready():
    # Bind to any port to send (0 means OS picks)
    var err = udp.listen(0)
    if err != OK:
        print("Failed to open UDP socket")
        return

    # Use a timer to send messages every 2 seconds
    var timer = Timer.new()
    timer.wait_time = 2
    timer.autostart = true
    timer.one_shot = false
    add_child(timer)
    timer.connect("timeout", self, "_on_Timer_timeout")


func _on_Timer_timeout():
    var message = messages[randi() % messages.size()]
    var data = message.to_utf8()
    udp.set_dest_address("127.0.0.1", 3614)
    var sent = udp.put_packet(data)
    if sent != OK:
        print("Failed to send packet")
    else:
        print("Sent:", message)
```


# Decimal to integer

https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=42



# Lets avoid anchor for now

-Resolution of Screen https://www.youtube.com/watch?v=Ua3qYveevow
- Anchor and pixel https://youtu.be/9eAYhlStl-Q?t=545


- https://hardwaretester.com/gamepad




