LCMS - LinkCMS
==============

Vorwort
-------
LCMS befindet sich noch in der Entwicklung und bietet noch kein Funktionierendes Script.

Installation
------------

###Using Composer

Der beste Weg um LCMS zu installieren ist das Repo zu klonen und via [composer](https://getcomposer.org/) das [ZF2](http://framework.zend.com/) zu installieren. Wie ihr composer installiert erfahrt ihr [hier](https://getcomposer.org/doc/00-intro.md).

1. Repo klonen

    `git clone https://github.com/UltimateHulk/LCMS.git`
2. ZF2 via composer installieren

    ```
    php composer.phar self-update
    php composer.phar install
    ```

###Web Server Setup

WICHTIG: Euer "DocumentRoot", also euer Hauptverzeichnis soll nicht auf `/` zeigen, sondernauf den Unterordner `public/`

Ein Beispiel für den VirtualHost eures Apaches:

    <VirtualHost *:80>
        ServerName lcms.local
        DocumentRoot /path/to/lcms/public
        SetEnv APPLICATION_ENV "development"
        <Directory /path/to/lcms/public>
            DirectoryIndex index.php
            AllowOverride All
            Order allow,deny
            Allow from all
        </Directory>
    </VirtualHost>
