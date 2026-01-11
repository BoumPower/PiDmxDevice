# PiDmxDevice - Français
## Caractéristiques
Carte esclave galvaniquement isolée pour réaliser un élément de scène "maison" piloté par [console DMX](https://fr.wikipedia.org/wiki/DMX_(%C3%A9clairage))
- éclairage LED personalisé
  - Strip LED RGB
  - LEDs disposées pour un rendu particulier
- asservissement motorisé
  - moteurs de modélisme
  - moteurs assrvi par une carte externe (I2C)
- relais électro-mécanique par une carte externe (I2C)

Le faible coût des boards Raspberry et la facilité de programmer, en Python par exemple, permettent de réaliser rapidement des éléments de scènes particuliers.
- pas de routines critiques temporellement pour gérer 
  - DMX : 512 registres décodés par hardware et accessible en lecture par bus I2C
  - LEDs : 3600 bytes de RAM accessible I2C et gestion des LEDs par hardware spécialisé (fréquence de rafraichissement 27 Hz)
  - PWM hardware (Raspberry uniquement)
### DMX
- full DMX512 isolé
- résistance 120 ohm de terminaison
- selecteur d'adresse DMX 9+1 bits
- LED d'activité DMX
### Micro-contrôlleur
Cette carte peut être pilotée par une grande variété de micro-contrôleurs, mais principalement le Raspberry Pico
- connecteur 40 pins pour Raspberry Pico 1 RP2040 ou Raspberry Pico 2 RP2350
- connecteur 40 pins pour Raspberry Pi
- connecteur I2C Qwiic pour Arduino, STM32, ATmega, ...
### Sortie jusqu'à 1200 LEDs
– WS2811, WS2812 / WS2812B / WS2812C, WS2813, WS2815, NeoPixel, SK6812, GS8208
– toutes sequences: GRB, RGB, etc.
– LEDs avec 3, 4, couleurs ou plus: GRBW, RGBW, RGBWC (LEDs avec warm and cold blanc)
- fréquence de rafraichissement 27 Hz
- bornier de connection GND/+5V/LED
### Raspberry uniquement
- avec Raspberry Pico
  - 16 I/O/PWM avec connectique adaptée (GND/+5V/PWM) aux servos-moteurs de modélisme ou I/O
  - les 40 pins du Raspberry Pico sont accessibles
- avec Raspberry PI
  - 2 I/O/PWM avec connectique adaptée (GND/+5V/PWM) aux servos-moteurs de modélisme ou I/O
- possibilité d'interconnecter un Raspberry Pi et un Raspberry Pico via un second bus I2C
### Extensions
- connecteur I2C Qwiic pour intégrer la carte à d'autres éléments
- 5 I/O câblées à 5 LEDs, 5 boutons, un DIP5

