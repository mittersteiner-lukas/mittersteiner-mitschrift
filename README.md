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

---

# Historische Entwicklung von WebDev

WebDevelopment hat im Lauf der letzten rund 35 Jahre einige Evolutionsstufen durchlaufen:

1. Static Websites (HTML, CSS, JavaScript) -initiale Phase des WebDevelopments, bei der Inhalte fest im HTML-Code verankert sind. Dominant in den 1990er-Jahren.

2. Dynamische Websites (mit serverseitiger Programmiersprache - PHP, Python, NodeJS - und Datenbankanbindungen). Dominant in den 200er-Jahren.

3. _Sigle-Page Application_ (SPA) - mit JavaScript-Frameworks (z.B. React, Vue, Angular, Svelte) erstellte "Webapps", die ähnliche Funktionen wie klassische Desktop-Anwendungen bzw. Handyapps bieten. - Dominant in den 2010er-Jahren. Um Handy-Apps möglichst nahme zu kommen, wurde der _Progressive Web App_ (PWA)-Standard entwickelt. Damit können Webapps auch offline funktionieren und auf bestimmte native Funktionen des Geräts zugreifen. Es gibt drei Vorraussetzungen, die eine PWA erfüllen muss, um als PWA zu gelten:
   1. Die Webapp muss über ein Web App Manifest verfügen.
   2. Die Webapp muss über Service Worker verfügen, die das Caching und die Offline-Funktionalität ermöglichen.
   3. Die Webapp muss über HTTPS bereitgestellt werden, um Sicherheit und Integrität zu gewährleisten.
   - Kompnenten Sind die wiederverwendbaren "Lego"-Bausteine in einer Webapp.

- **Deklarative Programmierung** - der Javascript- und Templet(HTML)-Code beschreiben, wie die Benutzeroberfläche aussehen soll, anstatt die einzelnen Schritte zur Erstellung der Benutzeroberfläche aussehen zu definieren. Das Framework kümmert sich um die Umsetzung. Dabei kommt **Reaktivität** (_reactivity_) ins Spiel: Wenn sich der Zustand der Anwendung ändert, aktualisiert das Framework automatisch die Benutzeroberfläche (UI), um den neuen Zustand (_state_) wiederzuspiegeln. Wenn die Aktualiesirung auch in die andere Richtung funktioniert (d.h. wenn sich die Benutzeroberfläche ändert, weil der Benutzer mit ihr interagiert, und der Zustand (_state_) der Anwendung entsprechend aktualisiert wird), spricht man von bidirektionaler Datenbindung (_two-way data binding_). **Logikbausteine** (Schleifen zur Darstellung von Listen und Beningungen für das kondotionale Ein- und Ausblenden von UI-Elementen) werden in den Templates vom Framework in die eigentliche Benutzeroberfläche übersetzt. Komponenten können auch andere Kompnenten enthalten (verschachtelt werden), wodurch eine hierachische Struktur entsteht. Die Kommunikation zwischen Komponenten erfolgt über **Props** (Eigenschaften) und und **Events** (Ereignisse). Props sind Daten, die von einer übergeordneten Komponente an eine übergeordnete Komponente weitergegeben werden. Events sind BVenachrichtigungen, die con einer untergeordenten Komponente an eine Komponente gesendet werden, um auf Benutzerinteraktionen oder andere Ereignisse zu reagieren.

# VibeCoding / AgenticEngineering mit VS-Code und GitHub Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View.
Dort können alle Anpassungen der "_Coding Harness_" vorgenommen werden. Wir können unseren _Harness_ mit verschiedenen Methoden anpassen:

- **MCP-Server**
  MCP steht für _Model Context Protocoll_. Es ist ein Standard der von Antropic entwickelt wurde. Mit Hilfe von MCP können ChatBots/LLMs (_Lage Language Models_) auf zusätzliche Tools zugreifen, die sie zu Experten in einem bestimmten Themenbereich machen.

---

# Frontend-Entwicklung

## Ordnerstruktur

![Ordnerstruktur einer Svelte anwendung](Ordnerstruktur.png)

Der Ordner .vscode enhält Einstellungen für den VS-Code-Editor. Der Ordner node*modules enhält die Abhängigkeiten (\_Dependencies*) der Anwendung. Das sind jene Pakete, die bei der Entwicklung (_build time_) und bei der Ausführung (_runtime_) der Anwendung benötigt werden. Alle Abhängigkeiten werden in der Datei package.json aufgelistet. Außerdem enthält die Datei package.json Metadaten über die Anwendung (Name, Version, Autor, Lizenz, etc.) und Skripte, die bestimmte Aufgaben automatisieren (z.B. das Starten der Anwendung, das Erstellen einer Produktionsversion, das Testen der Anwendung, etc.). Der Ordner public enthält statische Dateien (Bilder, Fonts, Icons , etc.), die direkt vom Browser unter dem jeweiligen Pfad geladen werden können.

![Unterstruktur des src-Ordners](image.png)

Der Ordner `src` enthält den Quellcode der Anwendung. Die Dateien `app.css`, `app.svelte` und `main.js` sind die Einstiegspunkte der Anwendung (in diesem Fall eine SPA). Sie werden vom Browser als erstes geladen, wenn die entsprechende Website aufgrufen wird. Die Datei `app.css` enthält die globalen Styles der Anwendung. Die Datei `App.svelte`ist die Hauptkomponente der Anwendung, die andere Komponenten importiert und in der Benutzeroberfläche anzeigt. Die Datei `main.js` ist der Einstiegspunktfür das JavaScript / TypeScript der Anwendung. Sie initialisiert die Anwendung in der `App.svelte`und bindet sie an das HTML-Dokument (`index.html` im Root-Ordner).

Der Ordner `lib` enthält`benutzerdefinierende UI-Komponenten und Hilfsfunktionen, die in der Anwendung verwendet werden. Der Ordner `components`enthält die wiederverwendbaren Komponenten der Anwendung. Sie sind die Bausteine der Benutzeroberfläche. Der Ordner`game`enthält die Logik für das Spiel. Die Datei`store.svelte`enthält den Zustand (_state_) der Anwendung. Das heißt sie speichert alle Daten, die sich im Laufe der Zeit ändern können. (z.B. Spielstand, Spielergebnisse, Einstellungen, usw.) und fungiert als zentrale Datenquelle - _Single Source of Truth_ (für mehr Details zum Speichermanagement im Frontend siehe Road-to-IT-Matura Team im Kanal "SWP - 06- Softwarearchitektur").
