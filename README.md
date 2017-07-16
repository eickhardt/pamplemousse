Pamplemousse
=============

Requirements
------------

* PHP 5.6 with ext-exif and ImageMagick extensions
* mysql

Components
----------

* Composer - http://getcomposer.org/
* Twig - http://twig.sensiolabs.org/
* Bootstrap - http://getbootstrap.com/
* HTML5 boilerplate - http://www.initializr.com/
* SASS - http://sass-lang.com/install
* Compass - http://compass-style.org/
* Dropzone.js - http://www.dropzonejs.com/

Installation
------------

Run the following:

```bash
git clone https://github.com/astranchet/pamplemousse.git
cd pamplemousse
curl -s http://getcomposer.org/installer | php
php composer.phar install
cp config/app.yml.dist config/app.yml
```

Run locally
-----------

```sh
php -S localhost:8000 -t web .router.php
compass watch
```

* [Frontend](http://localhost:8000/)
* [Backend](http://localhost:8000/admin/) (login/pwd: admin/foo)

Run migrations
--------------

```bash
./bin/doctrine migrations:migrate
```

Generate migration
------------------

```bash
./bin/doctrine migrations:generate
```

How to install gd on Ubuntu
------------------

```bash
sudo apt-get install php7.0-gd
```

How to install ImageMagick on Ubuntu
------------------

```bash
sudo apt-get install php-imagick
```
```bash
/etc/init.d/php7.0-fpm restart
```
or similar, depends
https://www.cyberciti.biz/faq/unix-linux-restart-php-service-command/

Then restart your webserver:
```bash
service nginx restart
```

Create image folders corresponding to your settings in app.yml
------------------

Defaults:
```bash
mkdir web/tmp
mkdir web/upload
mkdir web/thumbnail
```

The following directories should be writable by the web user:
------------------

Defaults:
```bash
log
web/tmp
web/upload
web/thumbnail
```