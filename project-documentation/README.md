# PAC-MAN GAME

### Členové skupiny: 
Filip Stryk
* podílel se na programování aplikace, rotačního enkodéru, displeje

David Pěčonka
* podílel se na programování joystiku, dokumentaci, videu

### Cíl projektu
Cílem projektu byl návrh a následná realizace aplikace, která pro svou funkci využívá rotační enkodér, joystik a LCD displej. My jsme se vydali cestou vytvoření známe hry PAC-MAN, která, v našem případě, používá pro ovládání samotného průběhu hraní joystik a pro pohyb ve startovacím menu využívá rotační enkodér.

### Popis HARDWARE

#### ATMega328p
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/atmega.PNG" width="350">

Piny 10,11 [1]:

- slouží pro určení směru roatce enkodéru

Piny 8,9 [2]:

- pomocí těchto pinl se určuje zda bude docházet k zápisu nebo ke čtení

Piny 4,5,6,7 [3]:

- piny k přenosu digitálních dat pro displej

Piny 2,3 [4]:

- piny, které přijímají informaci o tom zda byly tlačitka zabudované v joystiku a enkodréru stisknuta

Tlačitko [7]:

- slouží jako RESET

MicroUSB[6]

- určeno k nahrávání programu do mikrokontroléru

#### Rotační enkodér
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/enkod%C3%A9r.jpg" width="350">
Rotačení enkodér má čtyři piny: 

- Pin GND slouží k uzemnění
- Pin + slouží pro napájení enkodéru
- Pin SW je určen pro přenos informace o tlačítku
- CLK a CT jsou piny pro analogové signály, které obashují informace o rotaci vlevo resp. vpravo

Rotaci a tlačítko enkodéru využíváme pro pohyb v hracím menu na displeji. Tedy spuštění hry, prokliknutí, scrollování.

#### Joystik
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/joystick.jpg" width="300">

- Pin GND slouží k uzemnění
- Pin +5 určen pro napájení joystiku
- Pin Vrx slouží pro určení polohy joystiku v ose x
- Pin Vry slouží pro určení polohy joystiku v ose y
- Pin SW je určen pro přenos informace o tlačítku

#### Digilent PmodCLP LCD modul
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/LCD.PNG" width="300">


https://img.dxcdn.com/productimages/sku_370842_1.jpg
https://udvabony.com/wp-content/uploads/2019/05/arduino-joystick-module-1000x1000.jpg
