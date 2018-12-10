---
layout   : course
permalink: bap/template
published: true
#
title: Template
---

> Waarschuwing
> ---
> Je zult nooit wijzigen in de map "_site"!!
{:.card.card-warning}


## Reeds voorzien

### Bootstrap 4

- De aangeleverde template maakt gebruik van het framework bootstrap 4.
- Bootstrap 4 is officiëel sinds 23 januari
- Eén van de grote verschillen met versie 3 is de opbouw van het grid via flex-box en niet meer door gebruikt te maken van floating.

[Bootstrap 4 documentatie](https://getbootstrap.com/docs/4.0/getting-started/introduction/){:target="_blank"}


### Horizontale of verticale navigatie

In de map "_layouts" vind je een basis voor een horizontale en een verticale navigatie

{% highlight html %}
_config.yml > regel 22 > layout: vertical //of horizontal
{% endhighlight %}

> Waarschuwing
> ---
> Wijzigingen in de _config tonen zich pas nadat je de lokale server opnieuw hebt opgestart.
{:.card.card-warning}


Voor een enkel pagina een andere lay-out kiezen doe je in de Frontmatter van de betreffend pagina. Op die manier kan je ook zelf afwijkende lay-outs maken voor bijvoorbeeld de home-pagina.
- neem het # en spatie weg voor de regel 'layout' en geef er de naam van het gewenste lay-outbestand.

{% highlight html %}
---
# layout: vertical
permalink: kleur/
published: true
title: Kleur intro
---
{% endhighlight %}


### pages

- Hierin bouw je de contentstructuur op
- Vergeet niet telkens de permalink aan te passen
- Bestanden kunnen geschreven worden in html (extentie .html) of in markdown (extentie .md)
- Mixen van Markdown met HTML kan, maar is redelijk hectisch.

### Automatische navigatie

De navigatie wordt op 2 niveau's opgebouwd.

#### eerste niveau

- _data > navigation.yml
- Voeg hier zelf de gewenste rubrieken toe maar respecteer de opbouw
- Wens je subnavigatie neem dan het **#** weg voor **folder**

#### subnavigatie

- deze wordt automatisch opgebouwd aan de hand van de structuur en de **permalinks** gegeven in de map **pages**

### Inhoudstafel

- De templates zijn nu voorzien van een automtissche inhoudstafel per pagina
- Opname van de h1 en h2-elementen
- Staat nu in de zijkant, maar kan om het even waar worden geplaatst. Voeg daarvoor de voorziene code op de gewenste plaatst in je lay-outbestand.

{% highlight html %}
---
<nav id="toc" data-toggle="toc"></nav>
---
{% endhighlight %}

[Website TOC-plugin](https://afeld.github.io/bootstrap-toc/#usage){:target="_blank"}

### Back-to-top knop

### Lightbox

- Het js-bestand van de originele lightbox versie 2 werd reeds voorzien
- Toepassingsvoorbeeld in het bestand **stijlgids**

[Website Lightbox](http://lokeshdhakar.com/projects/lightbox2/#getting-started){:target="_blank"}