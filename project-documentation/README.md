# PAC-MAN GAME

### Členové skupiny: 
Filip Stryk
* podílel se na programování aplikace, rotačního enkodéru, displeje

David Pěčonka
* podílel se na programování joystiku, dokumentaci, videu

### Cíl projektu
Cílem projektu byl návrh a následná realizace aplikace, která pro svou funkci využívá rotační enkodér, joystik a LCD displej. My jsme se vydali cestou vytvoření známe hry PAC-MAN, která, v našem případě, používá pro ovládání samotného průběhu hraní joystik a pro pohyb ve startovacím menu využívá rotační enkodér.

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

Piny 10,11 [1]:

- slouží pro určení směru roatce enkodéru

Piny 8,9 [2]:

- pomocí těchto pinl se určuje zda bude docházet k zápisu nebo ke čtení

Piny 4,5,6,7 [3]:

- piny k přenosu dat pro displej

Piny 2,3 [4]:

- piny, které přijímají informaci o tom zda byly tlačitka zabudované v joystiku a enkodréru stisknuta

Tlačitko [7]:

- slouží jako RESET

MicroUSB [6]:

- určeno k nahrávání programu do mikrokontroléru

#### Rotační enkodér
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/enkod%C3%A9r.jpg" width="350">

- Pin GND slouží k uzemnění
- Pin + slouží pro napájení enkodéru
- Pin SW je určen pro přenos informace o tlačítku
- CLK a CT jsou piny pro signály, které obashují informace o rotaci vlevo resp. vpravo

Rotaci a tlačítko enkodéru využíváme pro pohyb v hracím menu na displeji. Tedy spuštění hry, prokliknutí, scrollování.

#### Joystik
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/joystick.jpg" width="300">

- Pin GND slouží k uzemnění
- Pin +5 určen pro napájení joystiku
- Pin Vrx slouží pro určení polohy joystiku v ose x
- Pin Vry slouží pro určení polohy joystiku v ose y
- Pin SW je určen pro přenos informace o tlačítku

Joystik využíváme pro ovládání hry. Pohyb všemi směry, tlačítko slouží pro opětovné spuštění hry po skončení. 

#### Digilent PmodCLP LCD modul
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/LCD.PNG" width="300">

- Piny J1.1,2,3,4,5,6,7,8,9,10 slouží pro přenos dat po sběrnici
- Piny J1.5, J1.11, J2.5 slouží jako signálová zem
- Piny J1.6, J1.12, J2.6 jsou určeny pro napájení displeje
- Pin J2.1 slouží pro výběr registru
- Pin J2.2 určuje zda budeme data zapisovat nebo číst
- Pin J2.3 enablovací pin

Dispej slouží k samotnému zobrazení celé vytvořené aplikace (startovací menu, průběh hry).

### Schéma zapojení
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/sch%C3%A9ma%20zapojen%C3%AD.png">
Obr. č. 1 Schéma zapojení v programu SimulIDE

https://img.dxcdn.com/productimages/sku_370842_1.jpg
https://udvabony.com/wp-content/uploads/2019/05/arduino-joystick-module-1000x1000.jpg
