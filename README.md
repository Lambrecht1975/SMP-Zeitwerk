# SMP ZEITWERK 2.5 – Mitarbeiteranmeldung (Testversion)

## Änderungen
- Mitarbeiter melden sich mit Personalnummer und persönlichem Passwort an. Nach erfolgreicher Prüfung ist die Person automatisch zugeordnet. Keine freie Mitarbeiterauswahl.
- Verwaltung legt zunächst Mitarbeiter an, dann unter Mitarbeiterverwaltung das persönliche Passwort (mindestens 12 Zeichen).
- Verwaltung exportiert ein AES-256-GCM-verschlüsseltes Einrichtungsprofil und überträgt es manuell auf das Firmen-iPhone. Export-Passwort separat übermitteln.
- Mitarbeiter importiert die Einrichtungsdatei auf seinem Firmen-iPhone und meldet sich mit Personalnummer und Mitarbeiter-Passwort an.
- Mitarbeiter können ihr Profil nicht mehr frei umstellen. Abmeldung möglich. Verwalteranmeldung bleibt separat.

## Installation
App über HTTPS bereitstellen, nicht per file:// öffnen. Vor Update bestehende verschlüsselte Exporte/Backups sichern. Version 2.5 nutzt denselben lokalen verschlüsselten Speicher wie 2.4, wenn HTTPS-Ursprung und Browserprofil identisch bleiben.

## Wichtige Grenzen
Nur lokaler Prototyp. Die Verwaltungskonten und Mitarbeiterkonten sind nicht zentral synchronisiert. Passwortänderungen auf dem PC werden nicht automatisch auf iPhones übertragen. Ein neues Einrichtungsprofil muss erneut importiert werden. Lokale Anmeldung kann durch technisch versierte Nutzer mit Zugriff auf Browserdaten manipuliert werden; keine serverseitige Autorisierung, keine manipulationssichere Zeitaufzeichnung, keine zentrale Gerätesperre. Auch die Geräteverschlüsselung basiert auf dem lokalen Geräte-Passwort, das separat eingegeben wird. Nicht produktiv mit echten Beschäftigtendaten einsetzen, bevor Sicherheitsprüfung, Datenmigration, Backups und Tests auf iPhones/Windows abgeschlossen sind.

## Tests
JavaScript-Syntaxprüfung automatisiert. Browser-/iPhone-Funktionstest noch ausstehend.
