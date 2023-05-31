<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Generate 0.8.51

Generera en statisk webbplats.

<p align="center"><img src="generate-screenshot.png?raw=true" alt="Skärmdump"></p>

## Hur man installerar ett tillägg

[Ladda ner ZIP-filen](https://github.com/annaesvensson/yellow-generate/archive/main.zip) och kopiera den till din `system/extensions` mapp. [Läs mer om tillägg](https://github.com/annaesvensson/yellow-update/tree/main/README-sv.md).

## Hur man genererar en statisk webbplats

Du kan generera en statisk webbplats på [kommandoraden](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md). Den static-site-generatorn skapar hella webbsidan i förväg, istället för att vänta på att en fil ska begäras. Öppna ett terminalfönster. Gå till installationsmappen där filen `yellow.php` finns. Skriv `php yellow.php generate`, du kan valfritt ange en mapp och en plats. Detta kommer att generera en statisk webbplats i `public` mappen. Ladda upp den statiska webbplatsen till din webbserver och generera en ny när det behövs. För att rengöra statiska webbplatsen skriv: `php yellow.php clean`.

Om du inte vill att en sida ska genereras, ställ in `Generate: exclude` i [sidinställningar](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md#inställningar-page) högst upp på en sida.

## Hur man genererar en statisk cache

Du kan skapa en statisk cache på [kommandoraden](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md). Den statiska cachen stöder en vanlig webbplats genom att generera några filer i förväg och lagra dem i filsystemet. Du kan också tänka på det som att kombinera funktionerna hos en statisk webbplats och funktionerna hos en vanlig webbplats. Öppna ett terminalfönster. Gå till installationsmappen där filen `yellow.php` finns. Skriv `php yellow.php generate system/cache`, du kan valfritt ange en plats. Skapa en ny cache vid behov. För att rensa cachen skriv: `php yellow.php clean system/cache`.

Om du inte vill att en sida ska cachelagras, ställ in `Generate: exclude` i [sidinställningar](https://github.com/annaesvensson/yellow-core/tree/main/README-sv.md#inställningar-page) högst upp på en sida.

## Exempel

Innehållsfil med alternativ för att generera en statisk webbplats:

    ---
    Title: Exempelsida
    Generate: exclude
    ---
    Den här sidan ingår inte i en statisk webbplats.

Generera statisk webbplats på kommandoraden:

`php yellow.php generate`  

Generera statisk cache på kommandoraden:

`php yellow.php generate system/cache`  

Generera statisk cache på kommandoraden, olika platser:

`php yellow.php generate system/cache /wiki/`  
`php yellow.php generate system/cache /blog/`  
`php yellow.php generate system/cache /help/how-to-make-a-small-website`  

Rengör statisk webbplats på kommandoraden:

`php yellow.php clean`  

## Inställningar

Följande inställningar kan konfigureras i filen `system/extensions/yellow-system.ini`:

`GenerateStaticUrl` = webbplatsens URL när man använder kommandoraden  
`GenerateStaticDirectory ` = map för statiskt genererade filer  
`GenerateStaticDefaultFile` = standardfil för statisk webbplats  
`GenerateStaticErrorFile` = felfil för statisk webbplats  

## Utvecklare

Anna Svensson. [Få hjälp](https://datenstrom.se/sv/yellow/help/).
