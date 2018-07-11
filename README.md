# DEPRECATED

Please note that this repository has been marked as deprecated. We will be deleting it from our organization at 31 August 2018.

We want to be able to offer our community with quality work, and we cannot simply maintain all the available repositories. If you feel that this repository should be kept you can talk to us in our discord server (https://phalcon.link/discord). You can also fork the repository if you wish to and/or archive it for your purposes.

For more see: https://blog.phalconphp.com/post/repository-reorganization

PHP Alternative Site
====================

Phalcon PHP is a web framework delivered as a C extension providing high
performance and lower resource consumption.

This is a sample application for the Phalcon PHP Framework. We wanted to create
an alternative version of the PHP site powered by the C-extension framework.

Thanks.

Get Started
-----------

### Requirements

To run this application on your machine, you need at least:

* PHP >= 5.3.6
* Apache Web Server with mod rewrite enabled
* Latest Phalcon Framework extension enabled (0.4.x)

### Configuration

Check your database configuration and website's base URI.

    app/config/config.php

Then you'll need to create the database and initialize schema:

    php -r '
    require "app/config/config.php";

    $n = $config->database->name;
    $u = $config->database->username;
    $p = $config->database->password;

    echo `echo "CREATE DATABASE {$n}" | mysql -u {$u} -p {$p}`;
    echo `cat schemas/php_site.sql | mysql -u {$u} -p {$p} {$n}`;
    '
