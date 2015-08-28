---
layout: post
title:  "How To Install Ruby on Rails on Mac OS X"
date:   2014-01-09 14:32:20
tags: [ruby, ruby on rails, macosx, install ruby on rails, install ruby, rvm]
categories: ruby rails macosx
share: true
comments: true
redirect_from: /how-to-install-ruby-on-rails-on-mac-os-x/
---


#### 1) Install XCode from App Store 

#### 2) Install Command Line Tools from terminal
{% highlight bash %}
xcode-select --install
{% endhighlight %}

#### 3) Install Homebrew
{% highlight bash %}
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
{% endhighlight %}
And make sure everything is correctly configured
{% highlight bash %}
brew doctor
{% endhighlight %}

If you get an warning like this

{% highlight bash %}
Warning: A newer Command Line Tools release is available

Update them from Software Update in the App Store.

Warning: You have not agreed to the Xcode license.
Builds will fail! Agree to the license by opening Xcode.app or running:
xcodebuild -license
{% endhighlight %}
![Install XCode Command Line Tools](/images/install-xcode-command-line-tools.png)

Open XCode, agree the license, close and run again
{% highlight bash %}
brew doctor
{% endhighlight %}


#### 4) Install RVM
{% highlight bash %}
\curl -sSL https://get.rvm.io | bash -s stable
{% endhighlight %}
{% highlight bash %}
source ~/.rvm/scripts/rvm
{% endhighlight %}
Be sure "rvm is a function"
{% highlight bash %}
type rvm | head -n 1
{% endhighlight %}

#### 5) Install RVM requirements
{% highlight bash %}
brew update
{% endhighlight %}
{% highlight bash %}
rvm requirements
{% endhighlight %}

If you get an error something like:
`No available formula for apple-gcc42`
 and cannot continue installing, run this code:
{% highlight bash %}
brew install autoconf automake libtool pkg-config apple-gcc42 libyaml readline libxml2 libxslt libksba openssl sqlite


rvm requirements
{% endhighlight %}


#### 6) Make sure you install RVM:
{% highlight bash %}
rvm -v
rvm 1.24.4 (master) by Wayne E. Seguin <wayneeseguin@gmail.com>, Michal Papis <mpapis@gmail.com> [https://rvm.io/]
{% endhighlight %}

#### 7) Install Ruby

{% highlight bash %}
rvm get head
{% endhighlight %}

{% highlight bash %}
rvm install 2.0.0-p247
{% endhighlight %}

Make sure you installed Ruby
{% highlight bash %}
ruby -v
ruby 2.0.0p353 (2013-11-22 revision 43784) [x86_64-darwin13.0.0]
{% endhighlight %}

#### 8) Use final version

{% highlight bash %}
rvm use 2.0.0-p247 --default
{% endhighlight %}

#### 9) Install RubyGems

{% highlight bash %}
rvm rubygems current
{% endhighlight %}

#### 10) Install Rails

{% highlight bash %}
gem install rails
{% endhighlight %}

Make sure you installed Rails
{% highlight bash %}
rails -v
Rails 4.0.0
{% endhighlight %}