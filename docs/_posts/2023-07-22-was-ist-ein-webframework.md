---
title:  "Was ist ein (Web-)Framework?"
date:   "2023-07-22"
last_modified_at: "2023-07-22"
categories: allgemein
header:
  teaser: /assets/images/library.jpg
---

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/library.jpg" alt="Raum mit Sessel und Bücherregal">

Ein Framework ist eine Sammlung von generischem Code, der in einer Vielzahl von neuen Projekten wiederverwendet werden kann. Dieser wird in Form von Libraries oder Klassen anderen Entwicklern <!--more--> bereitgestellt. Generisch bedeutet, dass der Code so allgemein gehalten ist, dass er ganz unterschiedliche Problemstellungen lösen kann. Für ein Webframework bedeutet das, dass mithilfe des Frameworks unterschiedliche Webanwendungen geschrieben werden können, z. B. kann ein Zahnarzt eine Seite über seine Praxis erstellen und ein Unternehmer kann einen Online-Shop programmieren. Web Frameworks sind besonders nützlich, um dynamische Webseiten zu erzeugen, d.b. erst im Moment der Anforderung wird das HTML-Dokument erzeugt und an den Client ausgeliefert. Zum Beispiel können Daten aus einer Datenbank abgerufen werden und in einer Liste auf der Webseite dargestellt werden. 

## Es gibt keine präzise Framework Definition

Es gibt keine präzise Definition darüber, welche Funktionen ein Framework umfassen muss. So wird in der Informationstechnologie der Begriff für ganz unterschiedliche Softwarebibliotheken mit jeweils sehr unterschiedlichen Anwendungsfällen genutzt.[^1] Zum Beispiel wird häufig der Begriff Test Framework genutzt, für Test-Bibliotheken. Es gibt JavaScript Frameworks wie jQuery, die die Benutzerinteraktionen in einem Browser vereinfachen und vereinheitlichen sollen.[^2]

## Was bietet ein Webframework?

Die meisten Webframeworks bieten Lösungen für die folgenden Themenfelder: 
* URL-Routing
* Request- und Repsonse-Handling
* Templates
* Entwicklungswebserver zum Debugging [^3]

Der Zweck eines Webframeworks ist, Entwicklern zu helfen, Webanwendungen zu erstellen.[^4]

## Full-Stack-Webframeworks vs. Micro-Frameworks

Die Funktionen die ein Webframework bietet, ist von Framework zu Framework unterschiedlich. Einige Frameworks bieten eine Vielzahl von zusätzlichen Funktionen, wie ORM zur Interaktion mit relationalen Datenbanken, Sicherheitsfunktionen, Sessions und Formulargenerierung. Diese Frameworks werden auch als Full-Stack-Webframeworks bezeichnet. Andere Frameworks bieten einen geringeren Satz an Funktionen und die Einfachheit steht im Fokus. Sie bieten in der Regel URL-Routing und die Nutzung von Templates an. Diese Frameworks werden häufig als Micro-Frameworks bezeichnet.[^5]

## Backend- vs. Frontend-Webframework

In diesem Blog unterscheiden wir zwischen Backend-Webframework und Frontend-Webframework. In  Backend-Webframeworks geschieht das Routing und das Rendern der Templates auf dem Server, wohingegen bei Frontend-Webframeworks dies auf den Clients ("in deinem Browser") mithilfe von JavaScript geschieht. 

Zu den Backend-Webframeworks zählen wir, u.a.
* [Django](https://www.djangoproject.com/)
* [Mojolicious](https://mojolicious.org/)
* [Express.js](https://expressjs.com/)

Zu den Fronend-Webframeworks zählen wir, u.a.
* [Angular](https://angular.io/)
* [React](https://react.dev/vue) 
* [Vue.js](https://vuejs.org/)


## Wieso sollte ein Webframework genutzt werden?

Ohne den Einsatz von Webframeworks oder anderen Bibliotheken, müsste eine Anwendung, die als Webanwendung eingesetzt werden soll, die Funktionalität, wie eine Anfrage interpretiert wird, wie man die darin enthaltenen Parameter dekodiert und diese Informationen dann an den spezifischen Code der Anwendung, der für diese URL ausgeführt werden soll, übergibt, selbst implementieren. Am Ende soll eine HTML-Seite in eine Antwort kodiert und zurückgeschickt werden. Weil HTTP ein zustandsloses Protokoll ist, d.h. es werden keine Sitzungsinformationen von Anfrage zu Anfrage gespeichert, muss die Anwendung eine Möglichkeit haben, um zu erkennen, ob ein Benutzer an- oder abgemeldet ist, und sicherzustellen, dass die richtigen Informationen für jeden Benutzer verwendet werden. Das führt dazu, dass die Anwendung mehr Code benötigt, wenn sie im Web funktionieren soll. Bei kleinen Projekten kann die eigentliche Logik der Anwendung weniger Code sein, als der Code für die grundlegenden Funktionen, die erforderlich sind, damit die Applikation im Web funktioniert.[^6]

Unter anderem aus diesem Grund ist es nicht empfehlenswert, eine komplette Webapplikation von Grund auf neu zu schreiben. Durch den Einsatz eines geeigneten Webframeworks kann der Entwicklungsaufwand reduziert werden und die Wartbarkeit des Projekts erhöht werden. Häufig genutzte Funktionen sind in den Modulen des Frameworks gekapselt und geben eine gewisse Standardstruktur vor, sodass andere Entwickler es einfacher haben, sich in den Quellcode der Applikation einzuarbeiten. Frameworks werden häufig von vielen Entwicklern weltweit entwickelt und gewartet, sodass häufig durch ein Upgrade der Release Version Bugfixes und neue Features zur Verfügung stehen.[^7]

--------------------------------------------------------

[^1]: Hooks, J. & Fallow, L. (2011). ActionScript Developer’s Guide to Robotlegs. Sebastopol, CA: O’Reilly Media, Kap. 1 What does Robotlegs actually do
[^2]: Burchard, E. (2017). Refactoring JavaScript : Turning Bad Code Into Good Code. Sebastopol, CA: O’Reilly Media, Kap. 2 Frameworks
[^3]: Reitz, K. & Schlusser, T. (2016). The Hitchhiker’s Guide to Python. Sebastopol, CA: O’Reilly Media, Kap. 7 Web Frameworks/Microframeworks
[^4]: Puglisi, S. (2015). Restful Rails Development. Sebastopol, CA: O’Reilly Media, Kap. 16 Is Rails Secure?
[^5]: Guardia, C. de la. (2016). Python Web Frameworks. Sebastopol, CA: O’Reilly Media, Kap. Introduction
[^6]: ebd., Kap. Appendix A. Python Web Development Fundamentals-It’s All HTTP Underneath
[^7]: D’mello, B. J., Satheesh, M. & Krol, J. (2017). Web Development with MongoDB and Node : Build fast web applications for handling any kind of data (3. Auflage). Birmingham, UK: Packt Publishing, S. 63
