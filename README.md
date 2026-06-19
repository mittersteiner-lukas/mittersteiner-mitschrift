# mittersteiner-mitschrift

Das ist die README.md-Datei. MD steht für Markdown. Markdown ist eine heutzuatage weit verbreitete Auszeichnungssprache (*Markup Language*, [Wikipedia](https://en.wikipedia.org/wiki/Markdown))

Weitere bekannte Auszeichnungsprachen sind: 
- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML, YML)

## Installation von Node.js

Javascript läuft unter normalen Umständen in einer Browser-Sandbox (nur im Browser)
Seit ca. 2010 gibt es eine Laufzeitumgebung (*Runtime Environment*) für JS, damit man auch Serverseitig JS programieren und ausführen kann: [Node.js](https://nodejs.org/).

## Installation von pnpm

Der Standardmäßige *Package Manager* für Node.js ist `npm` (*Note package manager*). Eine etwas modernere und inzwischen beliebtere Variante ist [`pnpm`](https://pnpm.io/) (*Performant npm*).

## Installation von Stra

Installation mit dem Skript `pnpm create strapi`. 
Daraufhin führt das CLI (Command Line Interface) durch die Installation. 
Falls bei der Installation sogenannte build `build scripts` nicht ausgeführt werden können, schlägt die CLI die Fehlerbehandlung selbstständig vor:

1. Welchsel in das Installationsverzeichnis (z.B. mit `cd` mittersteiner-strapi-project1)

2. Neuerlicher Versuch der Installation mit `pnpm install`. Dieser scheitert in der Regel - die Build-Scripts müssen mit `pnpm approved-builds` manuell freigegeben werden.
