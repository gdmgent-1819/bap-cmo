---
layout   : course
permalink: jekyll/commandos
published: true
#
title: Veel gebruikte commando's
---
## Repo van Github binnenhalen

1. Ga naar je repo op github:  
https://github.com/gdmgent-1718-3CMO/1718-3CMO-BaP-loginnaam
2. Rechtsboven groene knop "clone or download"
3. Kopieer het adres die verschijnt in het pop-upvenster
4. Open terminal
5. Ga naar de map 'code'

{% highlight posh %}
/Users/bartmissant/> C
{% endhighlight %}

Clone de repo in de map code

{% highlight posh %}
/Users/bartmissant/Code> git clone https://github.com/gdmgent-1718-3CMO/1718-3CMO-BaP-bartmi.git
{% endhighlight %}

> Opgelet
> ---
> Bij sommige studenten merkten we dat de lokale map de toevoegin "-master" had. In dat geval best de bovenstaande stappen opnieuw volgen en dan de goede repo gebruiken.
{:.card.card-warning}


## Jekyll lokaal draaien

### Naar je lokale map gaan

Ga naar de map code

{% highlight posh %}
/Users/bartmissant/> C
{% endhighlight %}

Ga in de map code naar je eigen map

{% highlight posh %}
/Users/bartmissant/Code> cd 1718-3CMO-BaP-bartmi
{% endhighlight %}

De 2 bovenstaande commando's maar korter

{% highlight posh %}
/Users/bartmissant/> c 1718-3CMO-BaP-bartmi
{% endhighlight %}


### Repo openen in Visual Studio Code

commando: *code spatie punt*

{% highlight posh %}
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> code .
{% endhighlight %}

### Lokale server opstarten

{% highlight posh %}
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> bundle exec jekyll serve
{% endhighlight %}

Wie de dotfiles heeft geïnstalleerd kan bovenstaande code verkorten naar 'js'

{% highlight posh %}
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> js
{% endhighlight %}

### Lokale server stoppen

Voor je je wijzigingen naar Github wenst door te sturen, dien je de lokale server te stoppen.

shortcut: **ctrl+c** (ook voor de mac-gebruikers.)

> ### samengevat
> ----------
> /Users/bartmissant/> c  1718-3CMO-BaP-bartmi  
> /Users/bartmissant/Code/1718-3CMO-BaP-bartmi> code .  
>  /Users/bartmissant/Code/1718-3CMO-BaP-bartmi> js  


## Website publiceren op github

Aan een lokale website heeft je klant uiteraard niets. Daarom moeten de bestanden ook op Github worden geplaatst en gepubliceerd.

**Vergeet niet de lokale server eerst te beëindigen!**

### Nieuwe bestanden uploaden naar je repo op Github

{% highlight posh %}
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> git add .
{% endhighlight %}

### Nieuwe en gewijzigde bestanden publiceren

{% highlight posh %}
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> git commit -m "omschrijving"
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> git push -u origin master
{% endhighlight %}

**Bestanden publiceren shortcut**

De twee vorige commando's kan je uitvoeren met één enkel verkort commando (indien dotfiles geïnstalleerd)

{% highlight posh %}
/Users/bartmissant/Code/1718-3CMO-BaP-bartmi> wip
{% endhighlight %}

> ### samengevat
> ----------
> /Users/bartmissant/Code/1718-3CMO-BaP-bartmi> git add .  
> /Users/bartmissant/Code/1718-3CMO-BaP-bartmi> wip  

### Bestanden geforceerd publiceren

{% highlight posh %}
PS> git push --force
{% endhighlight %}

## Bestanden downloaden van repository

Voor het geval je reeds geüploade bestanden terug binnen wil trekken.

{% highlight posh %}
PS> git pull
{% endhighlight %}

Bestanden downloaden geforceerd

{% highlight posh %}
PS> git pull --force
{% endhighlight %}

## Bundler regelmatig updaten

Vergeet niet ook Jekyll is software die regelmatig updates krijgt. Doe dit in je lokale repo.

{% highlight posh %}
1718-3CMO-BaP-bartmi > UpdateBundler
{% endhighlight %}

## Studenten die geen gebruik maken van Jekyll

Wie geen gebruik maakt van Jekyll, moet sowieso **een statische website opleveren** (zie briefing BaP).

1. ledig je lokale repo-map (vb. /Users/bartmissant/Code/1718-3CMO-BaP-bartmi).
2. deze wordt nu de root van je website. Plaats dus daarin je volledige bestanden- en mappenstructuur.
3. uploaden naar Github zoals beschreven in puntje 2 "bestanden uploaden".

## Testen !!!

> Opgelet
> ---
> Test je website ook voldoende op de Github. Er zijn altijd dingen die lokaal werken, maar er dan toch weer anders uitzien online.  
> url: https://gdmgent-1718-3cmo.github.io/1718-3CMO-BaP-loginnaam
{:.card.card-warning}