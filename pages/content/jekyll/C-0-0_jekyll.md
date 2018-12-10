---
layout   : course
permalink: jekyll/jekyll_install
published: true
#
title: Installatie van Jekyll
---

## Website Jekyll

[Jekyll installatie - rechtlijnen GDM](http://www.gdm.gent/1718-ehbi/){:target="_blank"}

[Jekyll installatie - richtlijnen website Jekyll](https://jekyllrb.com/docs/installation/){:target="_blank"}

Wat hebben we nodig?
--------------------

 1. [Dotfiles](http://www.gdm.gent/1718-ehbi/dotfiles/){:target="_blank"};
 2. [Ruby](https://rubygems.org/pages/download){:target="_blank"};
 3. [Bundler](https://bundler.io/){:target="_blank"}.

Installatie
-----------

### gdm.gent Dotfiles

[*&nbsp;*{:.fa.fa-fw.fa-download}Dotfiles][]{:.button.button--outline.button--primary}

### Ruby

[Ruby][] is een programmeertaal. Samen met Ruby wordt **Gem** geïnstalleerd, waarmee je [Ruby Gems](https://rubygems.org) (Ruby-programma's) kan installeren.

Installeer [Ruby][] met **gdm.gent Dotfiles**.

{% highlight posh %}
PS> InstallRuby
{% endhighlight %}

### Bundler

Ruby Gems kunnen afhankelijk zijn van andere Ruby Gems. Die Ruby Gems noemen we **afhankelijkheden** *(Eng.: dependencies).* Omdat Ruby Gems globaal geïnstalleerd worden en niet per project kan dit problemen geven als verschillende Ruby Gems eenzelfde afhankelijkheid hebben die van versie verschilt.

Om deze afhankelijkheden makkelijker te beheren is er de Ruby Gem [Bundler][]. De afhankelijkheden worden in een bestand `Gemfile` beschreven en de gebruikte **afhankelijkheden en hun versie** worden in een bestand `Gemfile.lock` bewaard.

Installeer [Bundler][] met **gdm.gent Dotfiles**.

{% highlight posh %}
PS> InstallBundler
{% endhighlight %}

> Opmerking
> ---
> `InstallBundler` is eigenlijk niet meer dan de CLI-opdracht `gem install bundler` met nog een aantal extra controles.
{:.card.card-remark}