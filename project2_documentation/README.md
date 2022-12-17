# Servo applicatiton

### Členové skupiny: 
Filip Stryk
* podílel se na programování aplikace

David Pěčonka
* podílel dokumentaci a videu

### Cíl projektu
Cílem projektu byl návrh a následná realizace aplikace, která pro svou funkci využívá joystik a dva servo motory. Naším návrhem je vytvoření ovládání smeru otáčení obou servo motorů pomocí pohybu joystikem.

### Struktura projektu
   ```c
   YOUR_PROJECT        // PlatfomIO project
   ├── include         // Included files
   │   └── timer.h
   ├── lib             // Libraries
   │   └── adc
   │        └── adc.c
   │        └── adc.h
   │   └── gpio
   │        └── gpio.c
   │        └── gpio.h
   │   └── lcd
   │        └── lcd.c
   │        └── lcd.h
   │        └── lcd_definitions.h
   │   └── uart
   │        └── uart.c
   │        └── uart.h
   ├── src             // Source file(s)
   │   └── main.c
   ├── test            // No need this
   ├── platformio.ini  // Project Configuration File
   └── README.md       // Report of this project
   ```

### Popis HARDWARE

#### ATMega328p
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/atmega.PNG" width="350">

Piny 9,10 [1]:

- slouží pro připojení dvou servo motorů (PWM)

Piny 2 [2]:

- slouží pro připojení tlíčka, které obashuje joystik

Piny 0,1 [3]:

- slouží pro čtení informace v jaké poloze se joystik nachází

Tlačitko [7]:

- slouží jako RESET

MicroUSB [6]:

- určeno k nahrávání programu do mikrokontroléru

#### Joystik
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/joystick.jpg" width="300">

- Pin GND slouží k uzemnění
- Pin +5 určen pro napájení joystiku
- Pin Vrx slouží pro určení polohy joystiku v ose x
- Pin Vry slouží pro určení polohy joystiku v ose y
- Pin SW je určen pro přenos informace o tlačítku

Joystik využíváme pro ovládání hry. Pohyb všemi směry, tlačítko slouží pro opětovné spuštění hry po skončení. 

#### Dva servo motory 
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project2_documentation/images/servo.jpg" width="300">

- Hnedý drátek GND slouží pro uzemnění
- Červené drátek slouží pro napájení 5V
- Oranžový drátek souží pro příjem PWM z mikrokontroleru

### Schéma zapojení
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project2_documentation/images/projekt%202%20de.png">
Obr. č. 1 Schéma zapojení v programu SimulIDE

### Popis SOFTWARE

* První vývojový diagram znázorńuje zobrazení hlavního menu. Kdy při otáčení enkodérem vybíráme ze dvou možností START GAME a SHOW RECORDS. Pro indikaci zvoleného řádku je zde vždy na začátek zvoleného řádku vložen znak '>'. Dále je zde znázorněn také výpis prvních deseti míst posledních odehraných rekordů. 
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project2_documentation/images/flow1.png">

* Dále zde máme enkodér u kterého jsme museli rozlišit rotaci vlevo a rotaci vpravo, to je zařízeno pomocí signálu, které generuje samotný enkodér při rotaci. Velký problém zde dělali zákmity, jelikož se jedná o mechanický enkodér. Tento problém jsme vyřešili tím, že projdou změny pouze delší než 10ms, čimž zajistíme ignoraci krátkých zákmitů. Enkodér jsme využili pro pohyb nahoru a dolů v main menu.  
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project2_documentation/images/flow2.png">

### Video
https://www.youtube.com/watch?v=a37RBYJj6u0

### Zdroje

1. https://img.dxcdn.com/productimages/sku_370842_1.jpg
2. https://udvabony.com/wp-content/uploads/2019/05/arduino-joystick-module-1000x1000.jpg
3. https://m.media-amazon.com/images/I/61yfIwAxe0L._SL1421_.jpg

