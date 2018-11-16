---
layout: sushi
title: Scratch Space Shooter
description: In dieser Übung schießt du mit deinem Raumschiff herabfallende Meteoriten ab bevor sie dein Raumschiff zerstören.
scratch-images:
- scratch-space-shooter/space-shooter.png
- scratch-space-shooter/skripte-laser.png
scratch-level: 2
scratch-sprites: 3
scratch-scripts: 13
scratch-data: 4
---

# Scratch Space Shooter

In dieser Übung schießt du mit deinem Raumschiff herabfallende Meteoriten ab bevor sie dein Raumschiff zerstören.

## Bühne und Figuren anlegen

1. ![Bühnenbild und Figuren anlegen](scratch-space-shooter/space-shooter.png){: .right}
Als erstes legst du fest, wie deine Bühne aussehen soll. Für dieses Spiel brauchst du das Weltall als Hintergrund. 
Wähle ein passendes Bild aus oder male selbst eines.

2. ![Raumschiff](scratch-space-shooter/raumschiff.png){: .right}
Als erste Figur brauchst du das Raumschiff. Es besteht aus zwei Kostümen: dem Raumschiff selbst und einem weiteren Kostüm das angezeigt wird, 
wenn das Spiel vorbei ist. Zeige den Text "Game Over" an oder male ein passendes Bild

3. ![Laser](scratch-space-shooter/laser.png){: .right}
Die nächste Figur ist der Laserstrahl, der von der Rakete abgefeuert werden kann.

4. ![Meteroit](scratch-space-shooter/meteroit.png){: .right}
Und als letzte Figur brauchst du noch einen Meteoriten.

## Daten

1. ![Daten](scratch-space-shooter/daten.png){: .right}
Wir brauchen für den Space Shooter einige Daten: die Anzahl der Treffer, die Enstehungszeit von Meteoriten, deren Geschwindigkeit und 
einen Indikator, ob ein Meteroit getroffen wurde. ACHTUNG: die Variable getroffen gilt nur für die Figur "Meteroit", 
alle anderen Variablen gelten für alle Figuren.

## Skripte für das Raumschiff

Das Raumschiff hat drei Aufgaben:

<div class="plainOrderedList">
    <ol>
        <li>Es muss erkennen, wann es von einem Meteoriten getroffen wurde und dann das Spiel beenden.</li>
        <li>Mit den Pfeiltasten kann es nach links und rechts bewegt werden.</li>
        <li>Mit den Tasten a und d kann es nach links und rechts gedreht werden.</li>
    </ol>
</div>

![Skripte für das Raumschiff](scratch-space-shooter/skripte-raumschiff.png)

## Skripte für den Laser

Jedesmal wenn die Leertaste gedrückt wird, muss ein neuer Laserstrahl erzeugt und abgefeuert werden.

![Skripte für den Laser](scratch-space-shooter/skripte-laser.png)

## Skripte für den Meteoriten

![Skripte für den Meteoriten](scratch-space-shooter/skripte-meteoriten.png)

## Weitere Ideen

* Füge Klänge für das Abfeuern eines Laserstrahls, für das Treffen eines Meteoriten und das Zerstören des Raumschiffes hinzu.
* Verwende Variablen um die Geschwindigkeit der Meteoriten und die Anzahl der erzeugten Meteoriten mit der Zeit zu erhöhen.

## Ausprobieren

Du kannst das fertige Projekt unter [https://scratch.mit.edu/projects/70593136/](https://scratch.mit.edu/projects/70593136/){:target="_blank"} ausprobieren.
