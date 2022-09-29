<p align="right"><a href="README-de.md">Deutsch</a> &nbsp; <a href="README.md">English</a> &nbsp; <a href="README-sv.md">Svenska</a></p>

# Command 0.8.42

Command line of the website.

<p align="center"><img src="command-screenshot.png?raw=true" alt="Screenshot"></p>

## How to use the command line

Open a terminal window. Go to your installation folder, where the file `yellow.php` is. Type `php yellow.php` to show available commands. The available commands depend on extensions installed. Type `php yellow.php about` to show the installed extensions and version numbers. If you don't have PHP on your computer, [see PHP installation](https://www.php.net/manual/en/install.php).

## How to build a static website

You can build a static website at the command line. The biggest difference between a static website and a normal website is that a static site generator builds everything in advance, instead of waiting for a file to be requested. Open a terminal window. Go to your installation folder, where the file `yellow.php` is. Type `php yellow.php build`, you can optionally add a folder and a location. This will build a static website in the `public` folder. Upload the static website to your web server and build a new one when needed. To check for broken links type: `php yellow.php check`. To clean the static website type: `php yellow.php clean`.

If you don't want that a page is built, set `Build: exclude` in the [page settings](https://github.com/annaesvensson/yellow-core#settings-page) at the top of a page.

## How to build a static cache

You can build a static cache at the command line. The static cache supports a normal website by building some files in advance and storing them in the file system. You can also think of it as combining the features of a static website and the features of a normal website. Open a terminal window. Go to your installation folder, where the file `yellow.php` is. Type `php yellow.php build system/cache`. This will build a cache in the `system/cache` folder. Build a new cache when needed. To clean the cache type: `php yellow.php clean system/cache`.

If you don't want that a page is built, set `Build: exclude` in the [page settings](https://github.com/annaesvensson/yellow-core#settings-page) at the top of a page.

## Examples

Content file with option for building a static website:

    ---
    Title: Example page
    Build: exclude
    ---
    This page is not included in a static website and cache.

Overview of available commands:

`php yellow.php about` = Show current version, [requires update extension](https://github.com/annaesvensson/yellow-update)  
`php yellow.php build` = Build static website, requires command extension  
`php yellow.php check` = Check static website, requires command extension  
`php yellow.php clean` = Clean static website, requires command extension  
`php yellow.php install` = Add extensions, [requires update extension](https://github.com/annaesvensson/yellow-update)  
`php yellow.php publish` = Publish extensions, [requires publish extension](https://github.com/annaesvensson/yellow-publish)  
`php yellow.php serve` = Start built-in web server, [requires serve extension](https://github.com/annaesvensson/yellow-serve)  
`php yellow.php traffic` = Create traffic analytics, [requires traffic extension](https://github.com/annaesvensson/yellow-traffic)  
`php yellow.php uninstall` = Remove extensions, [requires update extension](https://github.com/annaesvensson/yellow-update)  
`php yellow.php update` = Update website, [requires update extension](https://github.com/annaesvensson/yellow-update)  
`php yellow.php user` = Create user accounts, [requires edit extension](https://github.com/annaesvensson/yellow-edit)  

Showing available commands at the command line:

`php yellow.php`

Building static website at the command line:

`php yellow.php build`  

Checking static website for broken links at the command line:

`php yellow.php check`  

Cleaning static website and other files at the command line:

`php yellow.php clean`  

## Settings

The following settings can be configured in file `system/extensions/yellow-system.ini`:

`CoreStaticUrl` = URL of the website, when used as a static site generator  
`CommandStaticBuildDirectory` = directory for statically generated files  
`CommandStaticDefaultFile` = default file for static website  
`CommandStaticErrorFile` = error file for static website  

## Installation

[Download extension](https://github.com/annaesvensson/yellow-command/archive/main.zip) and copy zip file into your `system/extensions` folder. Right click if you use Safari.

## Developer

Datenstrom. [Get help](https://datenstrom.se/yellow/help/).
