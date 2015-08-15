---
layout: post
title:  "How to Instal Ruby On Rails on Ubuntu"
date:   2012-07-21 11:31:55
tags: [ruby, ruby on rails, ubuntu, install ruby on rails, install ruby, rvm]
categories: ruby rails ubuntu
share: true
comments: true
---

#### We have to install "RVM", "Ruby", "Gem" and "Rails" one by one.

0) Update your packages
{% highlight bash %}
sudo apt-get update
{% endhighlight %}

1) Install RVM (Ruby Version Manager)

{% highlight bash %}
sudo apt-get install curl
curl -L https://get.rvm.io | bash -s stable
source ~/.rvm/scripts/rvm
{% endhighlight %}

2) Be sure "rvm is a function"

{% highlight bash %}
type rvm | head -n 1
{% endhighlight %}

3) Find requirements and Install all of them

{% highlight bash %}
rvm requirements
{% endhighlight %}

> sudo /usr/bin/apt-get install build-essential openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev ncurses-dev automake libtool bison subversion pkg-config

{% highlight bash %}
sudo apt-get install build-essential openssl libreadline6 libreadline6-dev curl git-core zlib1g zlib1g-dev libssl-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt-dev autoconf libc6-dev ncurses-dev automake libtool bison subversion pkg-config
{% endhighlight %}


4) Install Ruby

{% highlight bash %}
rvm install 2.0.0-p247
{% endhighlight %}
5) Use final version

{% highlight bash %}
rvm use 2.0.0-p247 --default
{% endhighlight %}

6) Install RubyGems

{% highlight bash %}
rvm rubygems current
{% endhighlight %}

7) Install Rails

{% highlight bash %}
gem install rails
{% endhighlight %}

And you have Ruby On Rails on you Ubuntu