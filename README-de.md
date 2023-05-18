<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Static 0.8.49

Statische Webseite erstellen.

<p align="center"><img src="static-screenshot.png?raw=true" alt="Bildschirmfoto"></p>

## Wie man eine Erweiterung installiert

[ZIP-Datei herunterladen](https://github.com/annaesvensson/yellow-static/archive/main.zip) und in dein `system/extensions`-Verzeichnis kopieren. [Weitere Informationen zu Erweiterungen](https://github.com/annaesvensson/yellow-update/tree/main/README-de.md).

## Wie man eine statische Webseite erstellt

Du kannst eine statische Webseite in der [Befehlszeile](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md) erstellen. Der Static-Site-Generator erstellt die gesamte Webseite im Voraus, anstatt darauf zu warten dass eine Datei angefordert wird. Öffne ein Terminalfenster. Gehe ins Installations-Verzeichnis, dort wo sich die Datei `yellow.php` befindet. Gib ein `php yellow.php build`, du kannst wahlweise ein Verzeichnis und einen Ort angeben. Das erstellt eine statische Webseite im `public`-Verzeichnis. Lade die statische Webseite auf deinen Webserver hoch und erstelle bei Bedarf eine neue. Zum Überprüfen nach defekten Links gibt man ein: `php yellow.php check`. Zum Löschen gibt man ein: `php yellow.php clean`.

Falls du nicht willst dass eine Seite erstellt wird, kannst du `Build: exclude` in den [Seiteneinstellungen](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md#einstellungen-seite) ganz oben auf einer Seite festlegen.

## Wie man einen statischen Zwischenspeicher erstellt

Du kannst einen statischen Zwischenspeicher in der [Befehlszeile](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md) erstellen. Der statische Zwischenspeicher unterstützt eine normale Webseite, indem er einige Dateien im Voraus erstellt und im Dateisystem abspeichert. Man kann es sich auch so vorstellen, dass man die Funktionen einer statischen Webseite und die Funktionen einer normalen Webseite kombiniert. Öffne ein Terminalfenster. Gehe ins Installations-Verzeichnis, dort wo sich die Datei `yellow.php` befindet. Gib ein `php yellow.php build system/cache`. Das erstellt einen Zwischenspeicher im `system/cache`-Verzeichnis. Erstelle bei Bedarf einen neuen Zwischenspeicher. Zum Löschen gibt man ein: `php yellow.php clean system/cache`.

Falls du nicht willst dass eine Seite erstellt wird, kannst du `Build: exclude` in den [Seiteneinstellungen](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md#einstellungen-seite) ganz oben auf einer Seite festlegen.

## Beispiele

Inhaltsdatei mit Option zum Erstellen einer statischen Webseite:

    ---
    Title: Beispielseite
    Build: exclude
    ---
    Diese Seite ist in einer statischen Webseite nicht enthalten.

Statische Webseite in der Befehlszeile erstellen:

`php yellow.php build`  

Statische Webseite in der Befehlszeile nach fehlerhaften Links überprüfen:

`php yellow.php check`  

Statische Webseite und andere Dateien in der Befehlszeile löschen:

`php yellow.php clean`  

## Einstellungen

Die folgenden Einstellungen können in der Datei `system/extensions/yellow-system.ini` vorgenommen werden:

`StaticUrl` = URL der Webseite bei Verwendung der Befehlszeile  
`StaticDirectory ` = Verzeichnis für statisch erzeugte Dateien  
`StaticDefaultFile` = Standard-Datei der statischen Webseite  
`StaticErrorFile` = Fehler-Datei der statischen Webseite  

## Entwickler

Anna Svensson. [Hilfe finden](https://datenstrom.se/de/yellow/help/).
