
| Action      | Press | Release |
| ----------- | -------- | -------- |
| Menu Left   | 1309     | 2309     |
| Menu Right  | 1308     | 2308     |
| Up Arrow    | 1331     | 2331     |
| Down Arrow  | 1335     | 2335     |
| Left Arrow  | 1337     | 2337     |
| Right Arrow | 1333     | 2333     |
| A Button    | 1300     | 2300     |
| B Button    | 1302     | 2302     |

Les touches des jeux:[🖼️](https://github.com/user-attachments/assets/e82976cc-f99b-42dc-b181-0c987451eea4)   
Mots clés: [📖](https://miro.com/app/board/uXjVGUVLhc8=/)   

-------------------------

## Planning

*Va changer durant la semaine*

### Lundi : 10 Seconds Ninja

**Matin :**

* Ouvrir Godot et utiliser des boutons pour jouer
  * Utiliser : gauche, droite, sword, shuriken et restart
* Bouger le Ninja avec son code

**Après-midi :**

* "Hello World" : delay et await
* Challenge sans manette :
  * Essayer de faire le meilleur score au niveau 1
  * Essayer de finir 3 niveaux

---

### Mardi : Stealth Bastard

**Matin :**

* Le code, c’est quoi : variable, méthode, paramètre, énumération
* Finir le niveau 1 avec du code en utilisant les méthodes

**Après-midi :**

* Utiliser les boutons d’une manette NES pour jouer

---

### Mercredi : TowerFall

**Matin :**

* Créons notre propre langage :
  `A. 80 > a`
  `1000 > b`
  `80 > b1`

**Après-midi :**

* Permettre de jouer à quatre sur TowerFall
* Challenge :
  * Ajouter une macro pour tirer vers le haut
  * Ajouter une macro pour lancer deux flèches
  * Ajouter une macro pour sauter le plus haut possible

---

### Jeudi : Silksong

**Matin :**

* Améliorons le code d’hier avec des dictionnaires
* Challenge A :
  * Redémarrer le niveau
  * Supprimer la sauvegarde et recommencer le niveau

**Après-midi :**

* Challenge B :
  * Aller jusqu’au boss avec du code
* Challenge S :
  * Trouver des automatisations pour finir le boss
* Challenge S+ :
  * Finir le boss sans manette

---

### Vendredi : Vous choisissez le jeu

**Matin :**

* Faire la vidéo de Brackeys sur le jeu 2D

**Après-midi :**

* Essayer l’atelier sur un jeu que vous avez choisi

---

# Introduction

Salut à toi ;)

Nous allons apprendre à programmer en Godot et jouer à des jeux avec des simulateurs de manette Xbox 😋.

J’ai créé un atelier pour Unity 3D qui s’appelle **De Zéro à NES** .
Cours:[📖](https://github.com/EloiStree/2026_02_05_workshop_nid_nes_git_and_sobel/tree/main/CreateNesInUnity) Vidéo : [🎥](https://youtu.be/dLRaB3z-4DQ)   

Que j’ai refait en Godot, ici : [🎥](https://youtu.be/vK-fF6DpObk)  
(_Vidéo montrant comment j’ai créé le cours._)

L’idée est d’apprendre la programmation en créant une manette NES sur téléphone avec les UI de Godot ainsi que les touches clavier / manette.

---------

## À voir

* [ ] `print("Hello World")`
* [ ] **Label**

  * [ ] Comment changer un Label en « Hello World » avec des boutons
  * [ ] Comment changer un Label en « Hello World » avec du code
* [ ] **Button**

  * [ ] Appel d’une méthode
  * [ ] Appel d’une méthode avec un paramètre
* [ ] **Toggle**

  * [ ] Méthode recevant un booléen
* [ ] Afficher 100 × « Hello World » ([Simpsons](https://simpsons.fandom.com/wiki/List_of_chalkboard_gags))

  * [ ] Utiliser `await` pour prendre son temps
* [ ] **LineEdit**

  * [ ] Changer un Label
  * [ ] Utiliser un `print` lors du changement
  * [ ] Utiliser un `print` lors de la validation
  * [ ] * Ajouter de la mémoire au LineEdit
* [ ] Faire parler un cube

  * [ ] **StaticBody3D**

    * [ ] **MeshInstance3D**
    * [ ] **CollisionShape3D**
* [ ] Un Panel dans un Panel

  * [ ] Utiliser les ancres et pas les offsets
  * [ ] Ratio
  * [ ] VBox et HBox
  * [ ] Faire une NES
  * [ ] Ajouter une image cliquable
* [ ] Réseau

  * [ ] UDP ?
  * [ ] 101010 ?
  * [ ] IP ?
  * [ ] Port ?
* [ ] Input Map

  * [ ] Ajouter une action / touche(s)
  * [ ] Écouter la touche
  * [ ] * Ajouter quatre axes de joystick

    * [ ] * Utiliser en Vector2
* [ ] Exporter son jeu

  * [ ] Exporter sur Android

---

## Pour le fun

* [ ] Avancer et reculer un cube
* [ ] Tourner un cube de gauche à droite
* [ ] Ajouter une texture au cube




--------------------


# Godot NES

## Node

* [ ] **FacadeNesToUdp**

  * Permet de faire tous les exercices.

## Enum

* [ ] **XboxControllerToInt.XboxCommandBasic**
* [ ] **NesControllerToInt.NesButton**

## Script

* [ ] **NesControllerToInt** : Simuler une NES
* [ ] **XboxControllerToInt** : Simuler une Xbox
* [ ] **NesIntDelayer** : Retarde l’envoi d’un entier

## Input Map

* [ ] **NesInputMapActionDownUp** : Écouter une touche
* [ ] **NesInputMapActionFloatAxis** : Écouter un axe

## Brute

* [ ] **NesFloatAxisToBoolEvent** : Transforme un joystick en signal
* [ ] **NesInputDisplayButtonNameId** : Voir les boutons de la manette NES et leur nom
* [ ] **NesInputDeviceButtonDownUp** : Écouter les boutons de la manette NES

## LineEdit / InputField

* [ ] **NesInputFieldFileMemory** : Donner de la mémoire au LineEdit
* [ ] **NesSaveLoadStringValueFromFileMemory** : Sauvegarder et charger du texte

## Texture Button

* [ ] **NesRelayButtonS2wIntDownUp** : Écouter tous les boutons
* [ ] **NesTextureButtonPlusToS2wIntDownUpBool** : Devenir un bouton écoutable

## UDP

* [ ] **NesSendIntegerMessageUdp** : Envoyer des entiers sur le réseau
* [ ] **NesHelloWorldUdp** : Envoyer du texte sur le réseau

## Autre

* [ ] **NesParseIntegerToString** : De int à String, d’un entier à du texte

---

## Code du cours


* [https://github.com/EloiStree/2026_01_18_godot_nes_controller_udp](https://github.com/EloiStree/2026_01_18_godot_nes_controller_udp)
* [https://github.com/HelloGodotPi/2026_02_16_godot_nes_g300](https://github.com/HelloGodotPi/2026_02_16_godot_nes_g300)
* [https://github.com/EloiStree/2026_01_18_gdp_nes_controller_udp](https://github.com/EloiStree/2026_01_18_gdp_nes_controller_udp)
* [https://github.com/EloiStree/2026_01_18_unity_nes_multi_controller/releases/tag/2026_02_12](https://github.com/EloiStree/2026_01_18_unity_nes_multi_controller/releases/tag/2026_02_12)
* [https://github.com/EloiStree/2026_01_18_gdp_nes_udp_multiplayer/releases/tag/V2026_02_15](https://github.com/EloiStree/2026_01_18_gdp_nes_udp_multiplayer/releases/tag/V2026_02_15)

---

# Note annexe

## Decimal to integer

[https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=42](https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=42)
[https://hardwaretester.com/gamepad](https://hardwaretester.com/gamepad)




# De Zero a NES version  Godot
- [00:03](https://www.youtube.com/watch?v=vK-fF6DpObk&t=3s) Configurer un ESP32 pour simuler une manette Xbox en Bluetooth
- [05:50](https://www.youtube.com/watch?v=vK-fF6DpObk&t=350s) Faire un Hello World sur Godot pour le fun
- [08:06](https://www.youtube.com/watch?v=vK-fF6DpObk&t=486s) Définir un Label dans Godot
- [08:52](https://www.youtube.com/watch?v=vK-fF6DpObk&t=532s) Créer un envoyeur UDP pour du texte UTF-8
- [12:43](https://www.youtube.com/watch?v=vK-fF6DpObk&t=763s) Le tester sur NES Multi dans Unity3D
- [14:48](https://www.youtube.com/watch?v=vK-fF6DpObk&t=888s) Utiliser un Toggle dans Godot
- [18:49](https://www.youtube.com/watch?v=vK-fF6DpObk&t=1129s) C’est quoi un entier et le binaire ?
- [20:30](https://www.youtube.com/watch?v=vK-fF6DpObk&t=1230s) Créer un envoyeur UDP pour des entiers (int)
- [24:29](https://www.youtube.com/watch?v=vK-fF6DpObk&t=1469s) Tester l’envoyeur avec un format NES S2W
- [26:29](https://www.youtube.com/watch?v=vK-fF6DpObk&t=1589s) Créer un utilitaire pour envoyer des commandes NES S2W
- [31:40](https://www.youtube.com/watch?v=vK-fF6DpObk&t=1900s) Créer des méthodes génériques pour l’utilitaire
- [38:38](https://www.youtube.com/watch?v=vK-fF6DpObk&t=2318s) Raccorder les boutons à ce script
- [40:13](https://www.youtube.com/watch?v=vK-fF6DpObk&t=2413s) Le bouton n’a pas de down_up(bool)
- [43:33](https://www.youtube.com/watch?v=vK-fF6DpObk&t=2613s) Jouons avec le ratio
- [49:45](https://www.youtube.com/watch?v=vK-fF6DpObk&t=2985s) Ajouter des InputField (LineEdit) pour l’IP, le port et l’index
- [53:35](https://www.youtube.com/watch?v=vK-fF6DpObk&t=3215s) Créer de la mémoire pour l’InputField
- [56:51](https://www.youtube.com/watch?v=vK-fF6DpObk&t=3411s) Gestion des erreurs dans Godot ?
- [01:01:59](https://www.youtube.com/watch?v=vK-fF6DpObk&t=3719s) Installer XOMI pour jouer à des jeux
- [01:10:43](https://www.youtube.com/watch?v=vK-fF6DpObk&t=4243s&pp=0gcJCTAAlc8ueATH) Ajouter un debugger pour les entiers envoyés
- [01:16:44](https://www.youtube.com/watch?v=vK-fF6DpObk&t=4604s) Un peu de Krita pour les icônes
- [01:17:03](https://www.youtube.com/watch?v=vK-fF6DpObk&t=4623s) Ajouter des icônes Xbox depuis GitHub
- [01:19:55](https://www.youtube.com/watch?v=vK-fF6DpObk&t=4795s) Skip la partie Xbox et TextureButton (oublié)
- [01:20:25](https://www.youtube.com/watch?v=vK-fF6DpObk&t=4825s) De Unity à Godot pour l’utilitaire Xbox
- [01:31:00](https://www.youtube.com/watch?v=vK-fF6DpObk&t=5460s&pp=0gcJCTAAlc8ueATH) Ajouter une méthode pour tester les mouvements du joueur
- [01:31:58](https://www.youtube.com/watch?v=vK-fF6DpObk&t=5518s) Écouter les inputs bruts sur Godot
- [01:36:48](https://www.youtube.com/watch?v=vK-fF6DpObk&t=5808s) Un petit script pour debugger les inputs bruts et leurs noms
- [01:40:21](https://www.youtube.com/watch?v=vK-fF6DpObk&t=6021s&pp=0gcJCTAAlc8ueATH) L’Input Map pour les gens normaux
- [01:43:47](https://www.youtube.com/watch?v=vK-fF6DpObk&t=6227s) Pour les joysticks (axes) ?
- [01:52:46](https://www.youtube.com/watch?v=vK-fF6DpObk&t=6766s&pp=0gcJCTAAlc8ueATH) Permettre de réécrire les boutons et les flèches
- [01:58:09](https://www.youtube.com/watch?v=vK-fF6DpObk&t=7089s) Un dernier check-up



## Still to do

* [ ] Upload du code sur les ESP32
* [ ] Trouver une méthode pour avoir des boutons utilisant le touch du téléphone



