# mittersteiner-mitschrift

Das ist die README.md-Datei. MD steht für Markdown. Markdown ist eine heutzuatage weit verbreitete Auszeichnungssprache (_Markup Language_, [Wikipedia](https://en.wikipedia.org/wiki/Markdown))

Weitere bekannte Auszeichnungsprachen sind:

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML, YML)

## Installation von Node.js

Javascript läuft unter normalen Umständen in einer Browser-Sandbox (nur im Browser)
Seit ca. 2010 gibt es eine Laufzeitumgebung (_Runtime Environment_) für JS, damit man auch Serverseitig JS programieren und ausführen kann: [Node.js](https://nodejs.org/).

## Installation von pnpm

Der Standardmäßige _Package Manager_ für Node.js ist `npm` (_Note package manager_). Eine etwas modernere und inzwischen beliebtere Variante ist [`pnpm`](https://pnpm.io/) (_Performant npm_).

## Installation von Strapi

Installation mit dem Skript `pnpm create strapi`.
Daraufhin führt das CLI (Command Line Interface) durch die Installation.
Falls bei der Installation sogenannte build `build scripts` nicht ausgeführt werden können, schlägt die CLI die Fehlerbehandlung selbstständig vor:

1. Welchsel in das Installationsverzeichnis (z.B. mit `cd` mittersteiner-strapi-project1)

2. Neuerlicher Versuch der Installation mit `pnpm install`. Dieser scheitert in der Regel - die Build-Scripts müssen mit `pnpm approved-builds` manuell freigegeben werden.

# VibeCoding / AgenticEngineering mit VS-Code und GitHub Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View.
Dort können alle Anpassungen der "_Coding Harness_" vorgenommen werden. Wir können unseren _Harmess_ mit verschiedenen Methoden anpassen:

- **MCP-Server**
  MCP steht für _Model Context Protocoll_. Es ist ein Standard der von Antropic entwickelt wurde. Mit Hilfe von MCP können ChatBots/LLMs (_Lage Language Models_) auf zusätzliche Tools zugreifen, die sie zu Experten in einem bestimmten Themenbereich machen.

- Dom: Document Object Model
- Dom-Tree = Hierachie
- Start der Hierachie nennt man Wurzel oder Root
