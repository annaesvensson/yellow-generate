<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Generate 0.8.52

Statische Webseite generieren.

<p align="center"><img src="SCREENSHOT.png" alt="Bildschirmfoto"></p>

## Wie man eine Erweiterung installiert

[ZIP-Datei herunterladen](https://github.com/annaesvensson/yellow-generate/archive/refs/heads/main.zip) und in dein `system/extensions`-Verzeichnis kopieren. [Weitere Informationen zu Erweiterungen](https://github.com/annaesvensson/yellow-update/tree/main/README-de.md).

## Wie man eine statische Webseite generiert

Du kannst eine statische Webseite in der [Befehlszeile](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md) generieren. Der Static-Site-Generator macht die gesamte Webseite im Voraus, anstatt darauf zu warten dass eine Datei angefordert wird. Öffne ein Terminalfenster. Gehe ins Installations-Verzeichnis, dort wo sich die Datei `yellow.php` befindet. Gib ein `php yellow.php generate`, du kannst wahlweise ein Verzeichnis und einen Ort angeben. Das generiert eine statische Webseite im `public`-Verzeichnis. Lade die statische Webseite auf deinen Webserver hoch und generiere bei Bedarf eine neue. Zum Löschen der statischen Website gibt man ein: `php yellow.php clean`.

Falls du nicht willst dass eine Seite generiert wird, kannst du `Generate: exclude` in den [Seiteneinstellungen](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md#einstellungen-seite) ganz oben auf einer Seite festlegen.

## Wie man einen statischen Zwischenspeicher generiert

Du kannst einen statischen Zwischenspeicher in der [Befehlszeile](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md) generieren. Der statische Zwischenspeicher unterstützt eine normale Webseite, indem er einige Dateien im Voraus generiert und im Dateisystem abspeichert. Man kann es sich auch so vorstellen, dass man die Funktionen einer statischen Webseite und die Funktionen einer normalen Webseite kombiniert. Öffne ein Terminalfenster. Gehe ins Installations-Verzeichnis, dort wo sich die Datei `yellow.php` befindet. Gib ein `php yellow.php generate system/cache`, du kannst wahlweise einen Ort angeben. Generiere bei Bedarf einen neuen Zwischenspeicher. Zum Löschen des Zwischenspeichers gibt man ein: `php yellow.php clean system/cache`.

Falls du nicht willst dass eine Seite zwischengespeichert wird, kannst du `Generate: exclude` in den [Seiteneinstellungen](https://github.com/annaesvensson/yellow-core/tree/main/README-de.md#einstellungen-seite) ganz oben auf einer Seite festlegen.

## Beispiele

Inhaltsdatei mit Option zum Generieren einer statischen Webseite:

    ---
    Title: Beispielseite
    Generate: exclude
    ---
    Diese Seite ist in einer statischen Webseite nicht enthalten.

Statische Webseite in der Befehlszeile generieren:

`php yellow.php generate`  

Statischen Zwischenspeicher in der Befehlszeile generieren:

`php yellow.php generate system/cache`  

Statischen Zwischenspeicher in der Befehlszeile generieren, unterschiedliche Orte:

`php yellow.php generate system/cache /wiki/`  
`php yellow.php generate system/cache /blog/`  
`php yellow.php generate system/cache /help/how-to-make-a-small-website`  

Statischen Zwischenspeicher in der Befehlszeile löschen:

`php yellow.php clean system/cache`  

## Einstellungen

Die folgenden Einstellungen können in der Datei `system/extensions/yellow-system.ini` vorgenommen werden:

`GenerateStaticUrl` = URL der Webseite bei Verwendung der Befehlszeile  
`GenerateStaticDirectory ` = Verzeichnis für statisch erzeugte Dateien  
`GenerateStaticDefaultFile` = Standard-Datei der statischen Webseite  
`GenerateStaticErrorFile` = Fehler-Datei der statischen Webseite  

## Entwickler

Anna Svensson. [Hilfe finden](https://datenstrom.se/de/yellow/help/).
