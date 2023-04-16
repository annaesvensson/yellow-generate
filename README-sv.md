<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Static 0.8.48

Bygg en statisk webbplats.

<p align="center"><img src="static-screenshot.png?raw=true" alt="Skärmdump"></p>

## Hur man installerar ett tillägg

[Ladda ner ZIP-filen](https://github.com/annaesvensson/yellow-static/archive/main.zip) och kopiera den till din `system/extensions` mapp. [Läs mer om tillägg](https://github.com/annaesvensson/yellow-update/tree/main/README-sv.md).

## Hur man bygger en statisk webbplats

Du kan bygga en statisk webbplats på [kommandoraden](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md). Den static-site-generatorn bygger hella webbsidan i förväg, istället för att vänta på att en fil ska begäras. Öppna ett terminalfönster. Gå till installationsmappen där filen `yellow.php` finns. Skriv `php yellow.php build`, du kan valfritt ange en mapp och en plats. Detta kommer att bygga en statisk webbplats i `public` mappen. Ladda upp den statiska webbplatsen till din webbserver och bygg en ny när det behövs. För att söka efter trasiga länkar skriv: `php yellow.php check`. För att rengöra statiska webbplatsen skriv: `php yellow.php clean`.

Om du inte vill att en sida ska byggas, ställ in `Build: exclude` i [sidinställningar](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md#inställningar-page) högst upp på en sida.

## Hur man bygger en statisk cache

Du kan skapa en statisk cache på [kommandoraden](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md). Den statiska cachen stöder en vanlig webbplats genom att bygga några filer i förväg och lagra dem i filsystemet. Du kan också tänka på det som att kombinera funktionerna hos en statisk webbplats och funktionerna hos en vanlig webbplats. Öppna ett terminalfönster. Gå till installationsmappen där filen `yellow.php` finns. Skriv `php yellow.php build system/cache`. Detta kommer att bygga en cache i `system/cache` mappen. Skapa en ny cache vid behov. För att rensa cachen skriv: `php yellow.php clean system/cache`.

Om du inte vill att en sida ska byggas, ställ in `Build: exclude` i [sidinställningar](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md#inställningar-page) högst upp på en sida.

## Exempel

Innehållsfil med alternativ för att bygga en statisk webbplats:

    ---
    Title: Exempelsida
    Build: exclude
    ---
    Den här sidan ingår inte i en statisk webbplats.

Bygg statisk webbplats på kommandoraden: 

`php yellow.php build`  

Kontrollera statisk webbplats för trasiga länkar på kommandoraden:

`php yellow.php check`  

Rengör statisk webbplats och andra filer på kommandoraden:

`php yellow.php clean`  

## Inställningar

Följande inställningar kan konfigureras i filen `system/extensions/yellow-system.ini`:

`StaticUrl` = webbplatsens URL när man använder kommandoraden  
`StaticDirectory ` = map för statiskt genererade filer  
`StaticDefaultFile` = standardfil för statisk webbplats  
`StaticErrorFile` = felfil för statisk webbplats  

## Utvecklare

Anna Svensson. [Få hjälp](https://datenstrom.se/sv/yellow/help/).
