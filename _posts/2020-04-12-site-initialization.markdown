---
layout: post
title:  "Site Initialization"
date:   2020-04-12 20:10:00 -0500
categories: blog jekyll tutorial
---
Setting up Jekyll to use as a general information site and blog was pretty straight forward.
I chose Jekyll for its simplicity and minimal setup.

I modified very little of the out of box that `jekyll new vi1i.github.io` provided.
The setup for the environment to handle Jekyll was very straight forward and easy.
Below I will talk about each step, link resources, and talk about my final impressions.

## My Environment
I am currently running Ubuntu 18.04.4 LTS, using [kitty] for my terminal to support the font `fira-code`, `vim` with vundle and several plugins.
I do have `sudo` privilege on this machine.

This environment is likely prone to change depending on what I am doing.

## Setting up Jekyll
### Ruby
As much as I personally am not a fan of Ruby, I familiar with it.
There are many ways to use Jekyll with ruby, but I chose to use [Ruby Version Manager][rvm] or `rvm`.
I followed the recommended installation from `rvm` for [Ubuntu][rvm-install], so I will not show the command in case they become out of date.

Once `rvm` is set up, I ran `rvm install ruby` and then set the default to the latest version using `rvm --default use ruby`.
**Note:** I ran into an issue where the PPA did not add me to the `rvm` system group, in which I ran `sudo usermod -a -G rvm $USER` and logged in and out to fix this.

Installing ruby can take a minute or two, afterwards you can easily manage your ruby environments.

### Jekyll
Jekyll is easy, we just need to install `jekyll` through Ruby's package manager RubyGem.

If you used something like a local Ruby manager like `rvm`, then you will not need sudo:
{% highlight bash %}
gem install jekyll
{% endhighlight %}
Otherwise:
{% highlight bash %}
sudo gem install jekyll
{% endhighlight %}

## Creating the Base Site
I am going to cover this quickly.
For setting up a base Jekyll site, in whichever folder you want to keep it in (I usually use something like ~/Documents/git/) run `jekyll new <ProjectNameHere>`.

I chose to use GitHub.io to host my site easily, so I created a new repository called `Vi1i.github.io`.
This naming is picked up by GitHub to use this repo as your user site by default.
After that, I ran in the project directory:
{% highlight bash %}
git init
git remote add origin <RepoLinkHere>
{% endhighlight %}

After Jekyll initialized a basic layout, at the time of writing this I believe it was the Jekyll `minima` theme.
I liked the layout, and for now have chosen to stick with it.

## My Impressions
As you can see from this, it was quick and easy to set up.
I still have plenty of time to find issues and advantages.

[rvm]: https://rvm.io/
[rvm-install]: https://rvm.io/rvm/install
[kitty]: https://sw.kovidgoyal.net/kitty/
