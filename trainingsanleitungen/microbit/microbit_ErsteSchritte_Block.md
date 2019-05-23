---
layout: sushi
title: Deine ersten Schritte mit micro:bit - Blockprogrammierung
description: Baue einen elektronischen Würfel mit micro:bit
---

# Deine ersten Schritte mit micro:bit - Blockprogrammierung

Der BBC micro:bit ist ein kleiner anprogrammierbarer Computer mit Bewegungssensoren und Kompass. Weitere Informationen und einer ausführerlichen Anleitung zu den ersten Schritten gibt es [hier](http://microbit.org/de/guide/).

### Ausstattung
![](microbit_ErsteSchritte_Block/microbit_Front.gif)

In der Mitte befinden sich 25 LED-Lämpchen in einem 5x5 Raster. Links hast du den A-Knopf (Button) und rechts den B-Knopf. Auf der Rückseite befinden sich die Anschlüsse für das Batteriefach und ein Micro-USB-Kabel.


### Verbinde den micro:bit
Um zu Beginnen verbinde deinen micro:bit mit dem zusätzlichen Batteriefach oder mit einem USB-Kabel mit deinem Laptop.

Drücke die Knöpfe (Buttons) wenn dich dein micro:bit mit Lichtzeichen (A und B) dazu auffordert. 

### Entwicklungsumgebung

Wir empfehlen dir, die Entwicklungsumgebung im Chrome Browser zu öffnen, da dies der einzige Browser ist, welcher den automatischen Programmdownload unterstützt.

Öffne in einem Webbrowser die folgende URL: [https://makecode.microbit.org/](https://makecode.microbit.org/) 

![Startseite von https://makecode.microbit.org/](microbit_ErsteSchritte_Block/microbit_startpage.JPG)

Das ist der Editor mit dem wir ähnlich wie bei Scratch mit den bunten Blöcken oder mit JavaScript programmieren können. 

## Erstes Programm - Würfel

Dein erstes Programm soll einen zufälligen Würfelwurf nachstellen. Wenn der micro:bit geschüttelt wird soll er danach eine Augenzahl von 1-6 anzeigen.

1. Lege eine Variable für die Zufallszahl an.

    ![](microbit_ErsteSchritte_Block/microbit_wuerfel_01.PNG)

2. Bei Eingabe können wir auf das Schütteln reagieren und uns eine Zufallszahl speichern. Unter Mathematik findest du den Block für eine Zufallszahl. Zufallszahlen starten immer bei 0, daher benötigen wir eine Zufallszahl von 0-5. Ist die Zufallszahl eine 0, dann zeigt der Würfel eine 1. Ist die Zahl eine 5, zeigt der Würfel eine 6.

    ![](microbit_ErsteSchritte_Block/microbit_wuerfel_02.PNG)

3. Für die Entscheidung welche Augenzahl angezeigt werden soll verwendest du den Wenn-Dann-Block und den Vergleichsoperator = unter Logik. Mit dem Zeige-LEDs-Block unter Grundlagen kannst du einzelne LEDs zum Leucht bringen und somit ein Muster für die Augenzahlen entwerfen.

    ![](microbit_ErsteSchritte_Block/microbit_wuerfel_03.PNG)

4. Probiere die weiteren Augenzahlen selbstständig zu lösen.

### Übertragung des Programms auf den micro:bit

Es gibt zwei Möglichkeiten, dein Programm auf deinen micro:bit zu übertragen. Die automatische Übertragung funktioniert noch nicht bei allen micro:bits und
Webbrowser, weshalb hier beide Varianten aufgelistet sind.

#### Automatisch

Die automatische Übertragung funktioniert nur mit dem Chrome Browser.

Kopple dafür dein micro:bit mit deiner Entwicklungsumgebung. Wähle dazu das Zahnrad in der oberen rechten Ecke und wähle __Gerät koppeln__. Folge der Anleitung im Popup.

![](microbit_ErsteSchritte_Block/microbit_pairDevice.png)

Beim anschliessenden klicken auf den Herunterladen Knopf, wird dein Programm automatisch an deinen micro:bit übertragen und gestartet.

#### Hinweise für Mentoren

Falls die automatische Übertragung nicht funktioniert, müssen folgende Dinge geprüft werden:

1. Chrome Browser muss in der Version 65 oder höher installiert sein.
2. Auf dem micro:bit muss die Firmwareversion 0249 oder höher installiert sein. Die Versionsnummer findest du in der `DETAILS.TXT` Datei im `MICROBIT` drive.  
    ![](microbit_ErsteSchritte_Block/microbit_version.png)  
[Hier](https://makecode.microbit.org/device/usb/webusb/troubleshoot) findest du eine Anleitung wie die Firmware aktualisiert werden kann.
3. Auf Linux muss WebUSB zuerst via udev freigeschaltet werden.  
Folge dazu folgenden Schritten:
    1. Schliesse Chrome
    2. Erstelle `/etc/udev/rules.d/50-microbit.rules` mit folgendem Inhalt:  
    `SUBSYSTEM=="usb", ATTR{idVendor}=="0d28", MODE="0664", GROUP="plugdev"`  
    Dies erlaubt die Kommunikation mit Geräten welche die Vendor-ID von micro:bit besitzen.
    3. Füge den Benutzer der `plugdev` Gruppe hinzu  
    `sudo adduser <username> plugdev`
    4. Lade die udev Regeln neu  
    `sudo udevadm control --reload-rules`
    5. Logge den Benutzer aus und wieder ein.

#### Manuell

Falls die automatische Übertragung auf deinem Computer nicht funktioniert, kannst du die Programme auch manuell an deinen micro:bit übertragen. Dazu muss der micro:bit über ein USB-Kabel mit dem Laptop verbunden sein.

1. Lade das Programm vom Webbrowser herunter.
2. Öffne den Ordner in den du das Programm heruntergeladen hast.
3. Übertage das Programm auf den Microbit. Klicke mit der rechten Maustaste auf die Datei um das Context Menu zu öffnen. (Oder kopiere in von den Ordner auf den Micro:bit).

![](microbit_ErsteSchritte_Block/microbit_wuerfel_06.PNG)

### Fertiges Programm

Das fertige Programm könnten so aussehen:  
![](microbit_ErsteSchritte_Block/microbit_wuerfel_04.PNG)



