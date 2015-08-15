---
layout: post
title:  "Install Sublime Text 2 on Ubuntu (via Terminal)"
date:   2012-08-04 11:36:50
tags: [sublime, sublime text, ubuntu, install sublime text, terminal]
categories: ubuntu
share: true
comments: true
---


#### Other installations just say that download the Sublime Text 2 and run it, but this installation is like installing usual programs via terminal.
#### How to Install Sublime Text 2 on Ubuntu:

1) Add sublime-text-2 PPA to your system
{% highlight bash %}
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
{% endhighlight %}
2) If there is any Sublime Text 2, uninstall it.
{% highlight bash %}
sudo apt-get remove sublime-text*
{% endhighlight %}
3) And finally, install the stable version of Sublime Text 2
{% highlight bash %}
sudo apt-get install sublime-text
{% endhighlight %}