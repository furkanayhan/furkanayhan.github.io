---
layout: post
title:  "Import Heroku Postgresql Database to Local Database"
date:   2013-03-01 16:32:30
tags: [import database, heroku, postgresql, local database, restore database]
categories: heroku postgresql database
share: true
comments: true
redirect_from: /import-heroku-postgresql-database-to-local-database/
---


#### When you want to backup your application database on heroku, you can use "PG Backups" add-on.

{% highlight bash %}
heroku pgbackups
{% endhighlight %}
and you will see old saved database.

Select last one, example: b004
{% highlight bash %}
heroku pgbackups:url b004
{% endhighlight %}
and you will get an url, copy it
{% highlight bash %}
curl -o latest.dump "PASTE URL HERE"
{% endhighlight %}
you downloaded your dump.

and this code will restore your database (change 'MYUSER' and 'MYDB'):
{% highlight bash %}
pg_restore --verbose --clean --no-acl --no-owner -h localhost -U MYUSER -d MYDB latest.dump
{% endhighlight %}
And you restored your postgresql local database.