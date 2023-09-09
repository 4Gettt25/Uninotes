---
status: angefangen
date: 2023-09-03
thumbnail: https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/Rust_programming_language_black_logo.svg/1920px-Rust_programming_language_black_logo.svg.png
tags:
  - Project
---
# Vorstellung
- CLI tool um bestimmte Dateien dir wichtig für Setup sind in einzelne Ordner einzuteilen und zu komprimieren
- Soll reproduciable sein
- einfach zu bedienen

# Funktionen
- Sagen welche Ordner wichtig sind für das Setup und diese in einen eigene Ordner/Vault kopieren
- Ordner im CLI tool Benennbar
- bei veränderungen an Orginal datein auch veränderung in "Vault"
- möglichkeit automatisch bash skript zu erstellen was alle Programme und dependencies installiert (soll automatisch nach Packagemanager gucken)
- in cli menü zur auswahl welches setup man haben möchte

# Zeitplan 

```mermaid
gantt
    title Zeitplan für Projekt
    dateFormat  DD-MM
    
    section Grundstruktur
    erstellen           :a1, 06-09 , 5d
    Another task     :a3, after a1, 5d
    fertig           :milestone, after a3, 0d
    section Implimentierung
    implimentieren      :b1, 15-09  , 12d
    another task      :after b1 , 24d
```


