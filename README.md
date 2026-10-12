# seiwald-mitschrift

Das ist die README.md - Datei. MD steht für Markdown ist eine heutzutage weit verbreitete Auszeichnungssprach (_Markup Language_, [Wikipedia](https://de.wikipedia.org/wiki/Auszeichnungssprache))

Weitere bekannte Auszeichnungssprachen sind:

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML)

## Installation von NodeJS

Javascript läuft unter normalen Umständen in einer Browsser-Sandbox (nur im Browser, wichtig für Sicherheit).
Seit ca. 2010 gibt es eine Laufzeitumgebung (_Runtime Environment_) für Javascript, damit auch serverseitig JS programmieren und ausführen kann: [Node.js](https://nodejs.org/en/)

## Installation von pnpm

Der standmäßige _Paket Manager_ für Node, ist 'npm' (_node package manager_).

## Typescript

z.B. let x = 5;
int x = 3;
double y = 10.5;
--> JS versucht alles zu berechnen auch wenn es Blödsinn ist, bzw. es das System zum Absturz bringt.

TS ist eine erweiterung von JS, die statische Typen unterstützt. Es ist eine sogenannte _Superset_ von JS, d.h. jedes gültige JS-Programm ist auch ein gültiges TS-Programm, aber nicht umgekehrt.

## Installaton von Strapi

Installation mit dem Skript ´pnpm create strapi´. Daraufhin führt das CLI durch die Installation. Falls bei der Installation sogenannte "Build scripts" nicht ausgeführt werdden können, schlägt die CLI die Fehlerbehebnung selbstständig vor:

1. wechsel in das Inhaltsverzeichnis (mit "cd strapi")
2. Neuerlicher Versuch mit "pnpm install" (oder "npm install") Dieser scheitert in der Regel. Build-Skripte müssen mit "pnpm.approve build" manuell freigegeben werden.

### In der package.json Datei steht alles was in die node_modules installiert wird. Ohne package.json kann man keine node_modules installieren. Wenn es nicht vorhanden ist funktioniert Strapi nicht.

---

# Historische Entwicklung von WebDev

Webdevelopment hat im Laufe der letzten rund 35 Jahre einige Evolutionsstufen durchlaufen:

1. Statische Webseiten (HTML, CSS, ggr. JavaScript) - initiale Phase des Webdevelopments, bei der Inhalte fest im HTML-Code verankert sind. Dominant in der 1990er Jahren.

2. Dynamische Webseiten (mit serverseitiger Programmiersprache - PHP, Python, NodeJS - und Datenanbindung. Dominant in den 2000er Jahren.)  
   --> wichtigstes Feature: Datenbanken

3. _Single-Page Applications_ (SPA) - mit JavaScript-Frameworks (z.B. React, Angular, Vue, Svelte,...) erstellt "Wepapps", die ähnliche Funktionen wie klassische Desptop-Anwenundngen bzw. Handy-apps bieten. Dominant in der 2010er Jahren. Um Handy-Apps möglich nahe zu kommen, wurde der _Progressive Web APP_ (PWA) Standard entwickelt. Damit können Webapps offline funktionieren, Pushbenachrichtigungen senden und auf bestimmmte native Funktionen des Geräts zugreifen:

- Pushbenachrichtungen
- Kamera
- GPS
- Mikrofon
- Kontakte
- Bluetooth

Es gibt drei Voraussetzungen, die eine WebApp erfüllen muss, um als PWA zu gelten:

1. Sie muss über ein Manifest (manfiest.json) verfügen, das die App als solche kennzeichnet.
2. Sie muss über ein Service Worker verfügen, der die App offlinefähig macht. Ein Service Worker ist eine JS-Datei, die im Hintergrund des Browsers läuft - selbst wenn der Browser geschlossen ist.
3. Sie muss über HTTPS ausgeliefert werden, um die Sicherheit der Daten zu gewährleisten.

Frontend-Frameworks wenden folgende Architekturprinzipien an, um einen möglichst gute _User Experience_ (UX) zu erreichen:

- _Componend-based architecture_: Komponenten sind die wiederverwendbaren Bausteine einer WebApp. Sie kapseln HTML, CSS und JS in einer Datei, die dann in der App beliebig oft wiederverwendet werden kann. Weiters können sie unabhängig voneinander entwickelt, getestet und gewartet werden  
  Datenkapselung -- in der objektorientierten Programmierung werden Daten und Methoden, in einer Klasse gekapselt.  
  Datentrennung -- normalisierung von Daten -- atomare Attribute
- _Deklarative Programmierung_: Der JS- und Template(HTML)-Code beschreibt, wie die UI (Benutzeroberfläche) aussehen soll, anstatt die einzelnen Schritte zur Erstellung der UI zu definieren. Dabei kommt **Reactivität** (_Reaktivity_) ins Spiel: Wenn sich der Zustand der Anwendung ändert, aktualisiert das Framework automatisch die UI, um den neunen Zustand widerzuspiegeln. Wenn die Aktualisierung auch in die andere Richtung funktioniert (d.h. wenn sich die Benutzeroberfläche ändert, weil der Benutzer mit ihr interagiert und der Zustand (_state_) der Anwendung entsprechend aktualisiert wird) spricht man von bidirektionaler Datenbindung (_two-way data binding_).

- _Logikbausteiner_ (Schleifen zur Darstellung von Listen und Bedingungen für das konditionale Ein- und Ausblenden von UI-Elementen) werden in den Templates (HTML) definiert, nicht im JS-Code. Das erleichtert die Trennung von Logik und Darstellung. Die Templates werden vom Framework ind die eingentlich UI übersetzt.

- Komponenten können auch andere Komponenten enthalten (verschachtelt werden), wodurch eine hierachische Sturktur entsteht. Die Kommunikation zwischen Komponentne erfolgt über **props** (Eigenschaften) und **Events** (Ereignisse), Props sind Daten, die von einer übergeordneten Komponente an eine untergeordnete weitergeben werden, Events sind Benachrichtigungen, die von einer untergeordenten Komponente an eine übergeordnete Komponente gesednet werden, um auf Benutzerinteraktionen oder andere Ereignisse zu reagieren.
## Interpreted language vs. compiled language

Der Unterschied zwischen _interpretierten_ und _kompilierten_ Programmiersprachen liegt in der Art und Weise, wie der Code ausgeführt wird:
Compiled languages (z.B. C, C++, Rust, Go) werden vor der Ausführung in Maschinencode übersetzt. Dieser Maschinencode kann direkt von der CPU ausgeführt werden, was in der Regel zu einer höheren Ausführungsgeschwindigkeit führt.

Interpreted Langauges - Scriptsprachen (z.B. Python, JavaScript, Ruby) werden zur Laufzeit interpretiert. Der Quellcode wird Zeile für Zeile gelesen und ausgeführt, was die Entwicklung und das Debugging erleichtert, aber oft zu einer geringeren Ausführungsgeschwindigkeit führt.

## VibeCoding / AgenticEngineering mit VS-Code und GitHub Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View. Dort können alle Anpassungen des "_Coding Harness_" vorgenommen werden. Wir können unseren _Harness_ mit verschiedenen Methoden anpassen:

-**MCP-Server**:
MCP steht für _Model COntext Protocol_. Es ist ein Standard, der von Anthropic entwickelt wurde. Mit Hilfe von MCP können Chatbots/LLMs auf zustzliche Tools zugreifenm, die sie zu Experten in einem bestimmten Bereich machen.

uBlock Origin
