---
layout   : course
permalink: huistijlgids/
published: true
#
title: Quick Start
---

# Aanpak Online huistijlgids

## Uit de briefing

> Presentatie
> ---
> Alle elementen van de huisstijl worden gepresenteerd in een multiple page-website die online kan worden geraadpleegd.
> Het eindresultaat is een statische website. Gebruik voor de uitvoering bij voorkeur een 
> Static Site Generator zoals Jekyll, Grav, …
> Op de startpagina en in de footer van elke pagina plaats je de naam van de organisatie, het logo van de vzw, je eigen naam, academiejaar, logo AHS, …
{:.card.card-Definition}



## Methodiek

- Jekyll is hiervoor uiterst geschikt. Zie bijvoorbeeld deze cursus die ook met Jekyll wordt gemaakt.
- Je website wordt gehost op **Github Classroom**.
- In github classroom staat een basi klaar die jullie vrij kunnen benutten.



## Github Classroom

- Op github classroom staat een bron bestand klaar die jullie kunnen gebruiken. Maak hiervoor eerst je eigen repo aan via deze uitnodgings link. [Uitnodiging Github Classroom](https://classroom.github.com/a/7nypU-Gc){:target="_blank"}
- Github maakte jou eigen repo met daarin de template.


### Master Branch instellen

- Open je repo en klik op "settings"
- Scroll naar beneden naar het deel "Github pages"
- Activeer de "source" als "master branch" en bewaar de instelling. De url die daarboven verschijnt is de url van jullie huisstijlgids.

> GitHub
> ---
> Ga naar je repository en open de instellingen.  
> <kbd class="menu"><kbd>Settings</kbd>&#9656;<kbd>GitHub Pages</kbd>&#9656;<kbd>Source</kbd></kbd> moet op `Master Branch` staan 
{:.card.card-github}


### repository klonen

Open **Teminal** (mac) of **PowerShell 6** en ga naar de map `Code`.

{% highlight posh %}
PS> c
{% endhighlight %}

Kloon de nieuw aangemaakte repository

{% highlight posh %}
PS> c
PS> git clone https://github.com/gdmgent-1718-3CMO/1718-3CMO-BaP-mijnrepo.git
{% endhighlight %}

> Opgelet
> ---
> In bovenstaande URI vervang je 'mijnrepo' door je eigen GitHub-account!
{:.card.card-warning}


## Jekyll-configuratie

In `_config.yml` pas je de `baseurl` aan, van:

```
# Site settings
# ─────────────
baseurl: /1718-BaP # the subpath of your site, e.g. /blog
```

naar `«repositorynaam»` (bv. `1718-3CMO-BaP-Bartmi`):

```
# Site settings
# ─────────────
baseurl: /1718-3CMO-BaP-Bartmi # the subpath of your site, e.g. /blog
```