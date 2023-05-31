<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Generate 0.8.51

Generate a static website.

<p align="center"><img src="generate-screenshot.png?raw=true" alt="Screenshot"></p>

## How to install an extension

[Download ZIP file](https://github.com/annaesvensson/yellow-generate/archive/main.zip) and copy it into your `system/extensions` folder. [Learn more about extensions](https://github.com/annaesvensson/yellow-update).

## How to generate a static website

You can generate a static website at the [command line](https://github.com/annaesvensson/yellow-core). The static site generator makes the entire website in advance, instead of waiting for a file to be requested. Open a terminal window. Go to your installation folder, where the file `yellow.php` is. Type `php yellow.php generate`, you can optionally add a folder and a location. This will generate a static website in the `public` folder. Upload the static website to your web server and generate a new one when needed. To clean the static website type: `php yellow.php clean`.

If you don't want that a page is generated, set `Generate: exclude` in the [page settings](https://github.com/annaesvensson/yellow-core#settings-page) at the top of a page.

## How to generate a static cache

You can generate a static cache at the [command line](https://github.com/annaesvensson/yellow-core). The static cache supports a normal website by generating some files in advance and storing them in the file system. You can also think of it as combining the features of a static website and the features of a normal website. Open a terminal window. Go to your installation folder, where the file `yellow.php` is. Type `php yellow.php generate system/cache`. Generate a new cache when needed. To clean the cache type: `php yellow.php clean system/cache`.

If you don't want that a page is cached, set `Generate: exclude` in the [page settings](https://github.com/annaesvensson/yellow-core#settings-page) at the top of a page.

## Examples

Content file with option for generating a static website:

    ---
    Title: Example page
    Generate: exclude
    ---
    This page is not included in a static website.

Generating static website at the command line:

`php yellow.php generate`  

Cleaning static website at the command line:

`php yellow.php clean`  

## Settings

The following settings can be configured in file `system/extensions/yellow-system.ini`:

`GenerateStaticUrl` = URL of the website when using the command line  
`GenerateStaticDirectory` = directory for statically generated files  
`GenerateStaticDefaultFile` = default file for static website  
`GenerateStaticErrorFile` = error file for static website  

## Developer

Anna Svensson. [Get help](https://datenstrom.se/yellow/help/).
