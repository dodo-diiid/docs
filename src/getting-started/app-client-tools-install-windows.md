---
layout: document

title:  "Инсталиране на CloudStrap Client Tools под Windows"
date:   2013-12-02 22:58:04
header_title:  "> gem install cloudstrap Windows"
header_title_fontsize: big
lead: "Как да инсталираме Ruby, Git и CloudStrap Client Tools под Windows"
keywords: "инсталиране git windows, инсталиране на cloudstrap"
description: "Няколко бързи примера как да инсталираме и конфигурираме CloudStrap Client Tools и Git под Windows"
slug: app-client-tools-install-windows
noToc: true
---

{% capture help_links %}
  Интерактивният `setup wizard` ще ти помага и насочва през целия процес при настройване на CloudStrap Client tools. Ако не можеш да стартираш CloudStrap Client Tools на този етап, моля свържи се с нас драсни на [Cloudstrap общността в Google Groups]({{ site.cloudstrap.groups }}) за съдействие.
{% endcapture %}

{% capture after_ruby_and_git_installed %}
  След като вече сте инсталирал Ruby и Git, използвай RubyGem, (който е вграден в Ruby), за да инсталираш и самите CloudStrap Client Tools:
{% endcapture %}

<!-- FIXME: Ugly work around -->
<p style="margin: 25px"></p>

{% section id="install-windows" title="CloudStrap Client Tools под Windows" %}

{% section id="install-ruby-windows" title="Инсталиране на Ruby" %}

[RubyInstaller 1.9](http://rubyinstaller.org/) е най-лесният начин да инсталираш Ruby на Windows XP, Vista и Windows 7. Свали предпочитаната от теб версия от [тази страница](http://rubyinstaller.org/downloads/) и стартирай инсталатора след това.

{% note danger, Важно %}
По време на инсталация прецени, кои от стандартните настройки са ти необходими, но е задължително да избереш тази опция "Add Ruby executables to your PATH", за да можете да стартираш Ruby от командния ред.
{% endnote %}

След като инсталацията приключи, за да разбереш дали Ruby е инсталирано правилно на работната машина използвай тази команда:

{% highlight sh %}
C:\Program Files\> ruby -e 'puts "Welcome to Ruby"'
Welcome to Ruby
{% endhighlight %}

Ако съобщението 'Welcome to Ruby' не се покаже е възможно изпълнимия файл `ruby` да не е добавен в `PATH` променливите на Windows. Опитай се да инсталираш отново Ruby, но този път се увери, че опцията "Add Ruby executables to your PATH" е включен!

{% endsection %}

{% section id="install-git-windows" title="Инсталиране на Git" %}

Следващата стъпка е да инсталираш [Git за Windows](http://git-scm.com/downloads) благодарение, на който ще можеш да синхронизираш сорс кода на твоите локални приложения с тези, които работят на CloudStrap. Git за Windows предлага най-лесния начин за инсталация на Git и затова силно го препоръчваме - ако използваш друга версия на Git, моля да се увериш, че може да се използва през командния ред.

{% note danger, Важно %}
По време на процеса на инсталиране, избери "Use Git from the Windows Command Prompt", за да можеш да управляваш Git от командния ред. Избери и "Checkout as-is commit Unix-style line endings".
{% endnote %}

След като инсталацията приключи, провери Git дали е инсталиран коректно на работната машина с тази команда:

{% highlight sh %}
C:\Program Files\> git --version
git version 1.7.11.msysgit.1
{% endhighlight %}

Версията на Git може да е различна от тази в примера. Ако е по-висока от тази това не трябва да те притеснява.

{% endsection %}

{% section id="install-app-windows" title="Инсталиране на CloudStrap Gem" %}

{{ after_ruby_and_git_installed }}

{% highlight sh %}
C:\Program Files\> gem install cloudstrap
{% endhighlight %}

RubyGems ще свали и ще инсталира `cloudstrap` gem-а от www.rubygems.org/gems/cloudstrap. Принципно инсталацията протича без проблеми, но за да се увериш, че всичко е окей, след инсталацията направи проверка със следната команда:

{% highlight sh %}
C:\Program Files\> app
{% endhighlight %}

{{help_links}}

{% endsection %}
{% endsection %}

