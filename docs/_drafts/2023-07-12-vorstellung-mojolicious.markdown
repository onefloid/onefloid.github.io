---
layout: post
title:  "Vorstellung des Perl Webframeworks Mojolicious"
date:   2023-07-12 13:00:00 +0200
categories: allgemein perl mojolicious
---

[Mojolicious](https://mojolicious.org/) ist ein relativ junges Perl Echtzeit Webframework und ein Web Development Toolkit. Es ist möglich, mit einem kleinen Prototypen zu starten und diesen dann mit der Zeit wachsen zu lassen. Mojolicious bietet Routen, Plugins, Kommandos, Templates, Content Negotiation, Session Management, Validierung von Formularen, Tests, einen Server für statische Dateien und Unicode Unterstützung. Das Web Development Toolkit kann unabhängig vom Webframework in allen Arten von Applikationen eingesetzt werden. 

Mojolicious ist von Grund auf neu geschrieben, basierend auf den Erfahrungen bei der Entwicklung von Catalyst 2. Der Quellcode ist frei und quelloffen. Es ist einfach, einen Prototypen, bestehend aus einer Datei, in eine große, gut strukturierte MVC Webapplikation umzuwandeln.<sup>[1](#myfootnote1)</sup>

Die Ideen für Mojolicious wurden von den Hauptentwicklern des Catalysts Webframeworks entwickelt und waren als neue Internals für Catalyst gedacht. Aufgrund von Sorgen um die Abwärtskompatibilität wurden diese Ideen jedoch nicht umgesetzt. Die Hauptentwickler von Catalysts begannen anschließend, Mojolicious als eigenständiges Webframework zu entwickeln. Ein Hauptgrund, wieso es nicht auf Catalyst aufsetzt, ist, dass es ein echtzeit-, nicht-blockierendes Webframework ist <sup>[2](#myfootnote2)</sup>

Mojolicious ist bekannt dafür, eine ganze Reihe von eigenen Implementierungen für übliche Anwendungsfälle zu nutzen. Oft funktionieren diese Neuimplementierungen besser oder sind ausgereifter als die weiterverbreitenden Perl Module, die sie ersetzen. Dieses Vorgehen erlaubt Mojolicious, Abhängigkeiten von anderen Modulen stark zu reduzieren. Die Entwicklung, Wartung und Installation wird dadurch deutlich einfacher. Manchmal wird in Mojolicious ein leistungsfähigeres Perl Modul verwenden, wenn es installiert ist. Im Zweifel funktioniert Mojolicious aber auch ohne dieses Werkzeug.<sup>[3](#myfootnote3)</sup> Aufgrund der geringen Abhängigkeiten kann Mojolicious sehr einfach und schnell installiert werden.<sup>[4](#myfootnote4)</sup>

Mojolicious nutzt eine geringfügig abgewandelte Form des MVC-Entwurfsmusters bei dem bestimmte Applikationslogik in den Controller verankert wird. Dies ist häufig in aktuellen Webframeworks vorzufinden. Der Controller empfängt die Anfrage eines Nutzers und leitet eingehende Daten an das Model weiter. Die Antwort des Modells leitet der Controller wiederum an die View weiter, die die Antwort erzeugt. Letztendlich sendet der Controller den Response an den Nutzer zurück. Dieses Muster wird empfohlen, weil es zu sauberen und besser wartbaren Code führt, wird jedoch nicht erzwungen und deshalb ist es möglich, in einer Mojolicious Applikation davon abzuweichen.<sup>[5](#myfootnote5)</sup>

___

*<a name="myfootnote1">1</a>: Riedel, S. & Mojolicious contributors. (2023). Mojolicious - Perl real-time web framework. Zugriff am
12.07.2023. Verfügbar unter: <https://mojolicious.org/>*


*<a name="myfootnote2">2</a>: Berger, J. (2015). Introducing Mojolicious. Zugriff am 12.07.2023. Verfügbar unter: <https://www.youtube.com/watch?v=1oFF26GyoJk>*

*<a name="myfootnote3">3</a>: Foy, brian d. (2020). Mojolicious Web Clients. Perl School, S. 29*

*<a name="myfootnote4">4</a>: Bäcker, R. (2012). Mojolicious-Tutorial: Teil 1. $ foo Perl-Magazin, 4, S. 30*

*<a name="myfootnote5">5</a>: Riedel, S. (2020). Mojolicious::Guides::Growing - Growing Mojolicious applications Abschn. Model View Controller. Zugriff am 12.07.2023.
Verfügbar unter: <https://metacpan.org/pod/Mojolicious::Guides::Growing>*
