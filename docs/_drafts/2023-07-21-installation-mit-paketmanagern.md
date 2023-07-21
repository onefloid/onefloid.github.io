---
title:  "Installation der Webframeworks mit Paketmanagern"
date:   2023-07-21 00:00:00 +0200
categories: Installation
tags: Python Perl Node.js Django Mojolicious Express
header:
  teaser: /assets/images/download.png
---

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/download.png" alt="Wolke mit Download Symbol">

Skriptsprachen, wie Python, Perl oder Node.js (JavaScript), sind beliebte Sprachen für die Webentwicklung. Jede dieser Skriptsprachen bringt einen Paketmanager, mit der man Module aus öffentlichen Repositories installieren kann.

## Paketmanager

In der Regel wird ein Paketmanager bei der Installation der Programmiersprache mit installiert. Nachfolgend seht ihr eine Übersicht bekannter Paketmanager mit bekannten öffentlichen Repositories für die drei genannten Sprachen.

|Programmiersprache|Paketmanager|Repository|
|--------------|-----------|------------|
|Python|[pip](https://pypi.org/project/pip/)| [Python Package Index (PyPI)](https://pypi.org/)|
|Perl|[cpanm](https://metacpan.org/dist/App-cpanminus/view/bin/cpanm)|[CPAN](https://metacpan.org/)
|Node.js|[npm](https://www.npmjs.com/package/npm)|[npm Registry](https://www.npmjs.com/)

Die Repositories beinhalten allerlei nützliche Module und Frameworks für die entsprechenden Sprachen. Bevor man selbst eine Lösung programmiert, lohnt es sich immer einen Blick in die Repositories zu werfen und zu schauen, ob nicht eine entsprechende Lösung von jemand anderem entwickelt und veröffentlicht wurde. Und hier finden wir jetzt auch eine Vielzahl von Webframeworks und Erweiterungen für diese.

## Installation Django

Zur [Installation von Django](https://www.djangoproject.com/download/) sieht der Kommandozeilenaufruf wie folgt aus

```bash
pip install Django==4.2.3
```

## Installation Mojolicious

Zur [Installation von Mojolicious](https://mojolicious.org) kann folgender Einzeiler verwendet werden:

```bash
curl -L https://cpanmin.us | perl - -M https://cpan.metacpan.org -n Mojolicious
```

Falls das bei dir nicht klappt, z.B. weil du unter Windows entwickelst, kannst du auch alternativ folgendes Kommando absetzen:

```powershell
cpanm Mojolicious
```

## Installation Express

Zur [Installation von Django]https://expressjs.com/) sieht der Kommandozeilenaufruf wie folgt aus:

```bash
npm install express --save
```

## Die Gemeinsamkeiten

Jede Skriptsprache bietet einen Paketmanager mit dem wir die Webframeworks und Erweiterungen installieren können. 0Dieses Vorgehen ist weit verbreitet und findet man bei vielen Webframeworks wieder. Schaut doch mal nach, wie man für die Programmierspache Ruby das beliebte Webframework [Ruby on Rails installiert](https://guides.rubyonrails.org/getting_started.html)...

