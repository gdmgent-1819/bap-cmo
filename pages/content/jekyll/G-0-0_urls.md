---
layout   : course
permalink: jekyll/urls
published: true
#
title: Code - Url's genereren
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

*Andere optie*
{% highlight html linenos %}{% raw %}
    <img src="{{ site.baseurl }}/images/logo/logo.png">
    <a href="{{ site.baseurl }}/kleur/pantone.html">
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}


**In Markdown**
{% highlight md linenos %}{% raw %}
    ![mijn afbeelding alt-txt]({{ '/images/logo/logo.png' | relative_url }})
    [mijn link naar een pagina]({{ '/kleur/pantone.html' | relative_url }})
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}

*Andere optie*
{% highlight md linenos %}{% raw %}
    ![figuur 1]({{ site.baseurl }}/images/jekyll_werking_1.png "figuur 1")
{% endraw %}{% endhighlight %}{:data-file="filepath.html"}


Het resultaat na rendereren wordt dan  
{% highlight html linenos %}
    <img src="{{ '/images/logo/logo.png' | relative_url }}">
    <a href="{{ '/kleur/pantone.html' | relative_url }}">
{% endhighlight %}{:data-file="filepath.html"}

de toevoeging 'relative_url' zorgt ervoor dat de link wordt opgebouwd vanuit de root van je website.