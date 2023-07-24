---
title:  "Applikationsgrundgerüste erstellen und testen"
last_modified_at: "2023-07-24"
categories: 
  - Getting Started
tags: Python Perl Node.js Django Mojolicious Express
header:
  teaser: /assets/images/scaffold.jpg
---

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/scaffold.jpg" alt="Grundgerüst eines Gebäudes">

In der Regel bieten Webframeworks kleine Kommandozeilenprogramme (CLI, englisch: command-line interface) an, die einem die Entwicklung der Webanwendung erleichtern, zum Beispiel in dem sie aus einer Vorlage ein funktionsfähiges Grundgerüst einer Webanwendung erstellen. Bei [Full-Stack-Webframeworks](/allgemein/was-ist-ein-webframework/#full-stack-webframeworks-vs-micro-frameworks) ist das Kommandozeilenprogramm meistens von Haus aus dabei. Bei anderen Frameworks muss es ggf. nachinstalliert werden. Der Funktionsumfang der Programme unterscheidet sich von Framework zu Framework. 

Nachfolgend schauen wir uns die Kommandozeilenprogramme von Django, Mojolicious und Express an und erstellen jeweils ein funktionsfähiges Grundgerüst einer Webanwendung und führen sie anschließend mit einem Entwicklungsserver aus.

## Django 

Für die Erstellung eines Projekts stellt Django das Tool [django-admin.py](https://docs.djangoproject.com/en/4.2/ref/django-admin/) zur Verfügung. Mit dem Kommando 

```bash
django-admin.py startproject news_seite
```

wird ein Projektordner mit einem Grundgerüst angelegt. Bei der Zeichenfolge news_seite handelt es sich um den Projektnamen. Dieser kann frei gewählt werden.[^1]

Für die Erstellung einer App innerhalb eines Projekts gibt es ebenfalls ein Kommando.

```bash
python manage.py startapp news
```

Das Kommando erzeugt einen Ordner im Projektverzeichnis mit dem Namen news. Dies ist der Name der App, der frei gewählt werden kann. Wie das Projekt hat auch eine App ein Grundgerüst, welches durch das Ausführen des Kommandos angelegt wird.[^2] Nach der Erstellung der App liegt bereits eine funktionsfähige Webanwendung vor. Diese kann mit dem folgenden Kommando gestartet werden[^3]

```bash
python manage.py runserver
```


## Mojolicious

Mojolicious stellt ein Kommandozeilenprogramm zur Verfügung, dass mit mojo aufgerufen wird. Die [mojo-Befehle](https://docs.mojolicious.org/Mojolicious/Commands) dienen hauptsächlich zum Erstellen, Ausführen und Testen von Mojolicious Webapplikationen.[^4] Mit dem folgenden Kommando wird ein Applikationsordner angelegt für eine voll-funktionsfähige Mojolicious Applikation.[^5]

```bash
mojo generate app MyApp
```
Das Kommando erstellt das Grundgerüst für die Anwendung.[^6] 

Der Entwicklungsserver wird wie folgt gestartet: 

```bash
cd MyApp/
morbo script/MyApp
```

## Express

Der [Express Application Generator](https://expressjs.com/en/starter/generator.html) ist ein npm1 Package, mit dem eine neue Express App angelegt werden kann. Das folgende Kommando legt eine Express App mit dem Namen myapp an und fügt als View-Engine pug hinzu.

```
express --view=pug myapp

```
Das Kommando erzeugt das Grundgerüst der App. Anschließend muss noch in den neu erstellten App-Ordner gewechselt werden und das Kommando 

```
cd myapp
npm install

```

ausgeführt werden, um alle Abhängigkeiten zu installieren.[^7]

Der Entwicklungsserver wird wie folgt gestartet: 

```bash
DEBUG=myexpressapp:* npm start
```

## Zusammenfassung
Bei allen drei Webframeworks haben wir ein Kommandozeilenprogramm mit dem wir ein funktionsfähiges Applikationsgrundgerüst erstellen können. Dieses kann anschließend mit einem Framework-spezifischen Entwicklungsserver getestet werden. 

--------------------------------------------------------

[^1]: Ernesti, J. & Kaiser, P. (2017). Python 3: Das umfassende Handbuch (Galileo computing) (5. Auflage). Bonn:Rheinwerk Computing, Kap. 40.3
[^2]: ebd., Kap. 40.3.1
[^3]: Hochrein, A. (2019). Designing Microservices with Django: An Overview of Tools and Practices. New York, NY: Apress, S. 15
[^4]: Foy, brian d. (2020). Mojolicious Web Clients. Perl School, S. 215
[^5]: Riedel, S. (2021). Mojolicious::Commands - Command line interface. Zugriff am 24.07.2023. Verfügbar unter: <https://metacpan.org/pod/Mojolicious::Commands#generate-app>
[^6]: Bäcker, R. (2012). Mojolicious-Tutorial: Teil 1. $ foo Perl-Magazin, 4, 30–37, S. 31
[^7]: StrongLoop, IBM & Other expressjs.com contributors. (2017). Express application generator. Zugriff am 24.07.2023. Verfügbar unter: <https://expressjs.com/en/starter/generator.html>
