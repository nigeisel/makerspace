## CNC 
### 2D jobs
// TODO: 
* Wie Schnittdatenrechner nutzen && wo Werte eingeben für (Drehzahl + Vorschub?)

1. Design als `.dxf` erstellen
1. Design in vCarve laden und
    1. Ausgangsmaterial anlegen
    1. Ggf. Design bearbeiten
    1. Werkzeugwege anlegen (Mehrere Durchgänge anlegen bei Konturenschnitt, max 3-4mm? )
    1. Fräser aus vorgestellter Liste auswählen
    1. Wenn mehr als ein Fräser ausgewählt wird, muss eine eindeutige Werkzeugnr. vergeben werden (und ggf. notiert werden, da später von der Maschine nur noch die Anweisung kommt Fräser x einzulegen)
    1. `Werkzeugweg speichern` klicken
        1. `USBCNC` Präprozessor wählen
        1. alle angelegten Wege auswählen
        1. `.nc` Datei ablegen
1. Fräse vorbereiten
    1. (ggf. anschalten, reinigen)
    1. Fräser einspannen
    1. Werkstück einspannen (mit Opferplatte)
1. Karte an Terminal halten
1. `USBCNC` (`CNCv3`) starten
    1. Referenzsequenz starten ![Referenzsequenz](docs/referenzsequenz.png)
        * Maschine sollte zum Startpunkt vorne-rechts fahren
    1. Nullpunkt relativ zum Werkstück definieren
        1. Zum `Jog` Menu navigieren (F9)
        1. Geschindigkeit (x10 oder x100 wählen) -> wählt automatisch eine Achse an, und kann abgefahren werden
        1. Rot: wechselt achse, Grün setzt Nullpunkt
        1. Für z-achse Papier unterlegen und langsam senken bis Papier fest ist
    1. gcode laden: `Auto` anwählen -> `Load` -> select `.nc` gcode file
    1. ggf zurück zum `Jog` menu und Weg abfahren/checken dass keine Spannbratze angefräst wird
    1. Tür schließen
    1. Zurück zu Menu `Auto` -> `Start` -> Fräse fährt ganz nach oben und zum Maschinennullpunkt (vorne-rechts)
        1. Werkzeug-Dialog (Da von Anfang an der passende Fräser eingesetzt sein sollte, hier einfach `Ok`)
        1. Sollten in `vCarve` mehrere Fräser konfiguriert sein, poppt das wieder auf mit der Aufforderung den Fräser während des jobs zu wechseln (mit Angabe der vorher festgelegten Werkzeugnummern)
        1. Werkzeuglänge eingeben (wichtig, wenn Fräser länger als 10mm ist, damit Fräser langsam auf Fräsmessknopf gesenkt wird)
        1. Werkzeug wird vermessen
        1. `Ok` -> Job startet
1. Fräser zu startpunkt fahren
1. Saugen

### References
* https://docs.google.com/document/d/1xTgaVwwVuVnixO0SK6TbEKIL_G5LFGB28NkLh8X6AHM/edit
* https://wiki.happylab.at/w/BZT_Fr%C3%A4se

### 2.5D / 3D CNC jobs


## Lasercutter
    1. Design in corel draw erstellen?
        1. RGB rote haarlinien als schnitte
        1. RFB blaue linien als gravur
    1. TODO: zeroing?
