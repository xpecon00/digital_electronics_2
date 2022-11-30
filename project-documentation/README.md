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
#### Rotační enkodér
<img src="https://github.com/xpecon00/digital_electronics_2/blob/main/project-documentation/images/enkod%C3%A9r.jpg" width="350">
Rotačení enkodér má čtyři piny: 

-   Pin GND je pro uzemnění 
-   Pin + slouží pro napájení
-   SW slouží jako výstupní pin pro analogový signál tlačítka
-   CLK a CT jsou piny pro analogové signály, které obashují informace o rotaci vlevo resp. vpravo

Rotaci a tlačítko enkodéru využíváme pro pohyb v hracím menu na displeji. Tedy spuštění hry, prokliknutí, scrollování.

#### Joystik

#### Digilent PmodCLP LCD modul
