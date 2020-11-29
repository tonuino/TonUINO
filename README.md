# TonUINO

Die DIY Musikbox (nicht nur) für Kinder

# Abhängigkeiten installieren

Um den `Tonuino.ino` Sketch kompilieren zu können brauchst du folgende externe Bibliotheken:

- [DFPlayer Mini mp3 by Makuna](https://github.com/Makuna/DFMiniMp3/tree/master):
  beinhalted Funktionalität um den DFPlayer Mini zu verwenden (`DFMiniMp3.h`).
- [JC\_Button](https://github.com/JChristensen/JC_Button):
  wird verwendet um Signale von Druckknöpfen zu verarbeiten (`JC_Button.h`).
- [MFRC522](https://github.com/miguelbalboa/rfid):
  für die Verwendung des NFC-Readers (`MFRC522.h`).

Alle drei Bibliotheken können direkt in der _Arduino IDE_ installiert werden:
1. Öffne dazu die Bibliotheksverwaltung
   im Menü _Sketch_ > _Include Library_ > _Manage Libraries ..._
   oder mit der Tastenkombination <kbd>Strg</kbd> + <kbd>⇧ Umschalt</kbd> + <kbd>I</kbd>.
2. Suche die drei Bibliotheken indem du nach ihrem Namen filterst.
3. Klicke rechts unter der Beschreibung auf den _Install_ Knopf.

# Change Log

## Version 2.1 (xx.xx.xxxx) noch WIP
- Partymodus hat nun eine Queue -> jedes Lied kommt nur genau 1x vorkommt
- Neue Wiedergabe-Modi "Spezialmodus Von-Bis" - Hörspiel, Album und Party -> erlaubt z.B. verschiedene Alben in einem Ordner zu haben und je mit einer Karte zu verknüpfen
- Admin-Menü
- Maximale, Minimale und Initiale Lautstärke
- Karten werden nun über das Admin-Menü neu konfiguriert
- die Funktion der Lautstärketasten (lauter/leiser oder vor/zurück) kann im Adminmenü vertauscht werden
- Shortcuts können konfiguriert werden!
- Support für 5 Knöpfe hinzugefügt
- Reset der Einstellungen ins Adminmenü verschoben
- Modikationskarten (Sleeptimer, Tastensperre, Stopptanz, KiTa-Modus)
- Admin-Menü kann abgesichert werden

## Version 2.01 (01.11.2018)
- kleiner Fix um die Probleme beim Anlernen von Karten zu reduzieren

## Version 2.0 (26.08.2018)

- Lautstärke wird nun über einen langen Tastendruck geändert
- bei kurzem Tastendruck wird der nächste / vorherige Track abgespielt (je nach Wiedergabemodus nicht verfügbar)
- Während der Wiedergabe wird bei langem Tastendruck auf Play/Pause die Nummer des aktuellen Tracks angesagt
- Neuer Wiedergabemodus: **Einzelmodus**
  Eine Karte kann mit einer einzelnen Datei aus einem Ordner verknüpft werden. Dadurch sind theoretisch 25000 verschiedene Karten für je eine Datei möglich
- Neuer Wiedergabemodus: **Hörbuch-Modus**
  Funktioniert genau wie der Album-Modus. Zusätzlich wir der Fortschritt im EEPROM des Arduinos gespeichert und beim nächsten mal wird bei der jeweils letzten Datei neu gestartet. Leider kann nur der Track, nicht die Stelle im Track gespeichert werden
- Um mehr als 100 Karten zu unterstützen wird die Konfiguration der Karten nicht mehr im EEPROM gespeichert sondern direkt auf den Karten - die Karte muss daher beim Anlernen aufgelegt bleiben!
- Durch einen langen Druck auf Play/Pause kann **eine Karte neu konfiguriert** werden
- In den Auswahldialogen kann durch langen Druck auf die Lautstärketasten jeweils um 10 Ordner oder Dateien vor und zurück gesprungen werden
- Reset des MP3 Moduls beim Start entfernt - war nicht nötig und hat "Krach" gemacht
