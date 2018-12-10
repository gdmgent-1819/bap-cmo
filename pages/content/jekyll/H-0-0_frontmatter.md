---
layout   : course
permalink: jekyll/frontmatter
published: true
#
title: Code - Frontmatter
---


## De frontmatter van je pagina

Op je pagina bevindt zicht bovenaan de Frontmatter. Deze wordt geschreven in yaml. 

### Permalink

Een belangrijk onderdeel voor de werking van je website is de **permalink**. De functie hiervan is de hierarchische opbouw van je website.

#### Een map maken

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

#### Een bestand maken

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

#### Combinatie map en bestand

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