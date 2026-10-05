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

3. _Single-Page Applications_ (SPA) - mit JavaScript-Frameworks erstellt "Wepapps", die ähnliche Funktionen wie klassische Desptop-Anwenundngen bzw. Handy_apps bieten. Dominant in der 2010er Jahren.

## VibeCoding / AgenticEngineering mit VS-Code und GitHub Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View. Dort können alle Anpassungen des "_Coding Harness_" vorgenommen werden. Wir können unseren _Harness_ mit verschiedenen Methoden anpassen:

-**MCP-Server**:
MCP steht für _Model COntext Protocol_. Es ist ein Standard, der von Anthropic entwickelt wurde. Mit Hilfe von MCP können Chatbots/LLMs auf zustzliche Tools zugreifenm, die sie zu Experten in einem bestimmten Bereich machen.
