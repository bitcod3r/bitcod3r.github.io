---
layout: post
title: Using Doctrine CLI on Windows
date: '2014-10-29T19:18:11-05:00'
tags:
- doctrine
- orm
- php
- cli
- api
- framework
tumblr_url: https://bitcod3r.tumblr.com/post/101297492981/using-doctrine-cli-on-windows
---
1. Copy **doctrine.bat** (located at vendor/bin/doctrine.bat) to your project root directory.

2. Create a **bootstrap.php** file in any path inside your project root directory with the following content:

{% highlight javascript %}
use Doctrine\ORM\Tools\Setup;
use Doctrine\ORM\EntityManager;

$paths = array("../model");
$isDevMode = false;
$dbParams = array(
    'driver' => 'pdo_mysql',
    'host' => 'localhost',
    'user' => 'root',
    'password' => '',
    'dbname' => 'angular_php',
);

$config = Setup::createAnnotationMetadataConfiguration($paths, $isDevMode);
{% endhighlight %}

3. Create a **cli-config.php** file in your project root directory with the following content:

{% highlight javascript %}
use Doctrine\ORM\Tools\Console\ConsoleRunner;

// replace with file to your own project bootstrap
require_once 'path/to/file/bootstrap.php';

{% endhighlight %}

4. Execute **Doctrine CLI** from a command line window like this:

{% highlight javascript %}
    c:\path\to\project\root\directory>doctrine --help
{% endhighlight %}