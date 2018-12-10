---
layout   : course
permalink: bap/tipsandtricks
published: true
#
title: Code - tips and tricks
---

## Linken in Jekyll

Een gekend probleem bij het werken met generators zoals Jekyll maar ook andere CMS'en, is dat je op voorhand moeilijk kan inschatten wat de het juiste pad is naar een afbeelding of voor het leggen van cross-links.

Je herinnert waarschijnlijk dat je via de code '../' naar een map verlaat naar een hogere map of '../../' om twee niveau's hoger te gaan. Bij een generator is het dus moelijk op voorhand in te schatten op welk niveau een andere pagina of afbeelding staat.

De gemakkelijkst weg is dan om een absolute pad te gebruiken die vanuit de root (_site) denkt.

**In html**
{% highlight html linenos %}{% raw %}
    <img src="{{ '/images/logo/logo.png' | relative_url }}">
    <a href="{{ '/kleur/pantone.html' | relative_url }}">
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}

**In Markdown**
{% highlight md linenos %}{% raw %}
    ![mijn afbeelding alt-txt]({{ '/images/logo/logo.png' | relative_url }})
    [mijn link naar een pagina]({{ '/kleur/pantone.html' | relative_url }})
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}


Het resultaat na rendereren wordt dan  
{% highlight html linenos %}
    <img src="{{ '/images/logo/logo.png' | relative_url }}">
    <a href="{{ '/kleur/pantone.html' | relative_url }}">
{% endhighlight %}{:data-file="filepath.html"}

de toevoeging 'relative_url' zorgt ervoor dat de link wordt opgebouwd vanuit de root van je website.

## Classes toevoegen in Markdown

Ook in markdown kan je een class toevoegen aan een afbeelding, tabel, …

**Eén class**
{% highlight md linenos %}{% raw %}
    {: .mijnclass}
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}

**Meerdere class**
{% highlight md linenos %}{% raw %}
    {: .mijnclass .andereclass}
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}

Je plaatst deze code achter of onder het betreffende element

*Afbeelding*
{% highlight md linenos %}{% raw %}
    ![]({{ '/images/logo/logo.png' | relative_url }}){: .mijnclass}
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}

Het resultaat na rendereren wordt dan  
{% highlight html linenos %}
    <img src="{{ '/images/logo/logo.png' | relative_url }}" class="mijnclass">
{% endhighlight %}{:data-file="filepath.html"}

## Permalinken

Op je pagina bevindt zicht bovenaan de Frontmatter. Deze wordt geschreven in yaml. Een belangrijk onderdeel voor de werking van je website is de **permalink**. De functie hiervan is de hierarchische opbouw van je website.

### Een map maken

- eindigen met een slash "/": maakt een map aan
- voeg je daar niets achter dan wordt in deze map een bestand *index.html* gemaakt met daarin de inhoud van de respectievelijke pagina.

{% highlight md linenos %}{% raw %}
    ----
    permalink: logo/
    ----
{% endraw %}{% endhighlight %}

gerendered wordt dit

> Mappen & Bestanden
> ---
> - _site/
>   - logo/
>     - index.html
{:.card.card-tree}

### Een bestand maken

- zonder "/" wordt het bestand gerendered als een html-bestand

{% highlight md linenos %}{% raw %}
    ----
    permalink: logo
    ----
{% endraw %}{% endhighlight %}

gerendered wordt dit

> Mappen & Bestanden
> ---
> - _site/
>   - logo.html
{:.card.card-tree}

### Combinatie map en bestand

- Wil je meerdere bestanden in de zelfde map, noteer dan na de slash de gewenste bestandsnaam. Uiteraard nu zonder "/"

{% highlight md linenos %}{% raw %}
    ----
    permalink: logo/kleur
    ----
{% endraw %}{% endhighlight %}

gerendered wordt dit

> Mappen & Bestanden
> ---
> - _site/
>   - logo/
>     - kleur.html
{:.card.card-tree}