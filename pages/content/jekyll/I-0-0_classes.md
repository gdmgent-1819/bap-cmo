---
layout   : course
permalink: jekyll/classes
published: true
#
title: Code - Classes toevoegen in Markdown
---

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