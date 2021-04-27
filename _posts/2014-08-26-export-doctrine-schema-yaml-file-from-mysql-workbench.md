---
layout: post
title: Export Doctrine Schema YAML file from MySQL Workbench
date: '2014-08-26T01:55:00-05:00'
tags:
- git
- github
- doctrine
- symfony
- php
- mysql
- mysqlworkbench
tumblr_url: https://bitcod3r.tumblr.com/post/95806552461/export-doctrine-schema-yaml-file-from-mysql-workbench
---
Since [MySQL Workbench](http://en.wikipedia.org/wiki/MySQL_Workbench "MySQL Workbench on Wikipedia") is in continuous development and use, poorly maintained plugins get [outdated and](https://code.google.com/p/mysql-workbench-doctrine-plugin/ "mysql-workbench-doctrine-plugin")[non-functional](https://code.google.com/p/mysql-workbench-doctrine-plugin/)&nbsp;quickly. And it is more when we talk in PHP developer environment terms.

Fortunately, we can always&nbsp;find some [good guys](https://github.com/johmue "Johannes Müller from Germany for example...") working around new projects and&nbsp;[better tools](http://github.com/ "Git") to gather the community contribution and their efforts.

![](/tumblr_files/tumblr_9233554d56cb97035f5fa3f30bc2a83f_7eabb9d7_540.jpeg)

This is a how to get work with [mysql-workbench-schema-exporter](https://github.com/johmue/mysql-workbench-schema-exporter "Plugin's page on GitHub")&nbsp;:

<!-- more -->
- Download and install&nbsp;[MySQL Workbench](http://dev.mysql.com/downloads/workbench/ "Download MySQL Workbench")
- Donwload and unpackage [Schema Exporter](https://github.com/johmue/mysql-workbench-schema-exporter/archive/master.zip "Download MySQL Workbench Schema Exporter")&nbsp;into a separated folder.
- Get Composer installed in your Exporter unpackaged folder:
```
php -r “readfile(‘https://getcomposer.org/installer’);” | php
```

- Run composer to get dependencies:
```
php composer.phar install
```

- Now use Schema Exporter to get translated&nbsp;_.MWB_ file to _.YML_ file.
```
php bin/mysql-workbench-schema-export &nbsp;modelo\_bdd.mwb ./myNewYMLsFolder
```
**And that’s it! Enjoy your code!**
