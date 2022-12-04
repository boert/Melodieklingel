# Melodieklingel

Leiterplatte für die Melodieklingel nach der Veröffentlichung von S. Lehmann im Funkamateur 4/86

## Eckdaten
Leiterplattengröße: 100 x 100 mm  
Betriebsspannung: 5V DC  
Stromaufnahme: 87 bis 230 mA (min./max.)  
Schaltschwelle (Transistor):   1,4 V  
Schaltschwelle (Optokoppler):  8 V (DC) oder 5,6 V (AC)    

![3D-Vorschau](Melodieklingel__Vorschau.png)


### Stromaufnahme

Alle Messungen erfolgten mit einem 8 Ohm-Kleinlautsprecher.

| Logikfamilie | IC D1   | IC D2     | IC D3 | IC D4   | Ruhezustand      | Wiedergabe       |
| ------------ | ------- | --------- | ----- | ------  | ----------------:| ----------------:|
| TTL          | D104    | U880D     | U2716 | D174    | 183 mA  (0,92 W) | 230 mA  (1,15 W) |
| CMOS         | 74HCT04 | STZ8400   | U2716 | 74LS74  | 128 mA  (0,64 W) | 175 mA  (0,88 W) |
| CMOS         | 74HCT04 | TMPZ84C00 | U2716 | 74LS74  |  87 mA  (0,44 W) | 135 mA  (0,68 W) | 

Hinweis: Da bei D4 nicht alle Eingänge beschaltet wurden, kann es beim Einsatz von 74HCT74 zu Fehlfunktionen kommen. Bei Verwendung von DL074/74LS74 sollte es keine Probleme geben.


## Änderungen gegenüber dem Original
- zusätzliche Bestückungsvariante mit Optokoppler zur galvanischen Trennung des Klingel
- Werte und Baugrößen an vorhandenen Lagerbestand angepasst
- alle liegenden Widerstände auf 15 mm Rastermaß geändert
- Stützkondensator für U880D ergänzt

## Bestückungsvarianten
### Taster
Dieser wird zwischen den Lötpunkten 'Start' und 'GND' angeschlossen.
Da keine galvansiche Trennung und Entstörung vorliegt, eignet sich diese Variante nur für denn Fall, das der Taster mit einer kurzen Leitung angschlossen wird, z.B. bei einer Montage im Gehäuse.

Folgende Bauteile können bei der Bestückung entfallen:  
C3, C4, R5, R6, VD1, VT1  
sowie:  
R100, R101, D100, VD100  

### Transistor
Bei dieser Variante hilft ein Tiefpass und ein Transistor beim Auslösen der Klingel. Es muß eine Verbindung zwischen TP2 und TP3 hergetellt werden.
Als Transistor für VT1 eignet sich jeder beliebige Kleinsignal-NPN-Typ, z.B. SC236, SF126, SF136, SF357, SS125, SS216.

Folgende Bauteile können bei der Bestückung entfallen:  
R100, R101, D100, VD100  

### Optokoppler
Hier wird ein Optokoppler zur galvaischen Trennung genutzt.
Um diese Variante zu Nutzen muß eine Verbindung zwischen TP102 und TP3 hergetellt werden.  
Zum Auslösen der Klingel dient die Gleich- oder Wechselspannung der vorhandenen Klingelanlage. Die Klingel wird mit einem Signal ab 8 V Gleichspannung oder ab 5,6 V Wechselspannung aktiviert. Über den Widerstand R100 kann die Schaltschwelle angepasst werden.  

Der Widerstand R7 sollte ggf. auf 47 kOhm erhöht werden, damit der Pegel am Gatter D1B passt.  
Folgende Bauteile können bei der Bestückung entfallen:  
C3, C4, R5, R6, VD1, VT1  

## Links
https://hc-ddr.hucki.net/wiki/doku.php/elektronik/melodieklingel


# Änderungen / History
## Version 2, 29.11.2022
- C1 von 470 nF zu 470 pF geändert   
- D100, Pin 5 und Pin 6 getauscht   
