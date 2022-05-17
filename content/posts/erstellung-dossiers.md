---
title: Erstellung Dossiers
date: 2022-05-17T06:10:56+06:00
hero: /assets/images/background.jpg
menu:
  sidebar:
    name: Unterrichtsmaterial
    identifier: analytics-and-comments
    weight: 500
---

Erläuterung einer Idee, wie Dossiers/Arbeitsblätter für den Unterricht kooperativ und nachvollziehbar erstellt werden können. 
<!--more-->

## Problematik
Werden Unterlagen für den Schulunterricht erstellt, sind diese häufig in einem Wordformat. Da bei Word die Nachvollziehbarkeit bei mehreren Autoren schwierig ist und der Fokus zu stark auf die Formatierung gelegt wird, wird in dieser Notiz ein anderes Vorgehen vorgeschlagen. 

Das nachfolgende Vorgehen arbeitet mit Markdown, Pandoc, LaTeX und Git.

## Eingesetzte Tools

Für die Erstellung der Inhalte dienen Markdowndateien, welche in einem normalen Texteditor (bspw. VSCode) erfasst werden. Bilder und Grafiken werden entweder in einem separaten lokalen Ordner oder über das Internet aufrufbar (bspw. www.cloudinary.com) abgelegt. Da die Inhalte der Dossiers damit nur aus Text bestehen, kann ein Git-Repository zur Versionierung, Verwaltung und Zusammenarbeit eingesetzt werden.

Aus den Markdowndateien (entweder eine oder mehrere) wird über Pandoc ein PDF generiert (als Template dient eine LaTeX-Vorlage). Dieses PDF wird den Lernenden über die gewünschte Plattform zur Verfügung gestellt (OneNote, Moodle, etc.).

### Markdown

Über Markdown werden die Inhalte für die Dossiers oder Arbeitsblätter erfasst. Dabei sind auch LaTeX-Befehle für math. Formeln oder spezielle Formatierungen für Aufgabenstellungen, Informationsboxen o.ä. möglich. Der Fokus liegt dabei lediglich auf dem Inhalt und nicht der Formatierung.

Für die einzelnen Kapitel eines Dossiers können unterschiedliche Markdowndateien erstellt und gepflegt werden. Dies fördert die Übersichtlichkeit. Bei der Erstellung des PDFs über Pandoc kann später angegeben werden, welche Markdowndateien zur Generierung des PDFs verwendet werden sollen. Damit bietet sich auch die Flexibilität, unterschiedliche Dossiers zu erstellen oder Inhalte in anderen Modulen ebenfalls zu integrieren.

Sämtliche Grafiken werden entweder in einem separaten Ordner lokal oder besser online gespeichert. Gerade im Zusammenhang mit Git macht es Sinn, die Grafiken nicht über das Git-Repository zu verwalten, sondern im Internet über eine URL zur Verfügung zu stellen. Dazu eignen sich Bildermanagement-Tools wie bspw. www.cloudinary.com. Da können Grafiken gespeichert werden. Beim Aufruf der Grafikdatei können in der URL Parameter mitgegeben werden, damit die Grafik manipuliert werden kann (Verkleiner, Ausschneiden, unterschiedliche Formate, etc.).

Grundlegende Informationen wie Autor, Version, etc. werden über Frontmatter (d.h. im Kopf der Markdowndatei) angegeben.

### Pandoc

Mittels Pandoc wird über die Kommandozeile das PDF (oder auch andere Ausgabeformate wie bspw. HTML) generiert. Diese Generierung könnte allenfalls über bspw. Github-Actions automatisiert werden.

### Git

Die einzelnen Markdowndateien werden über eine Versionsverwaltung gepflegt. Dabei eignet sich Git am besten. Damit ist eine Versionierung und gemeinsames Arbeiten sichergestellt.

## Weitere Informationen

Unter https://plain-text.co/ ist der Prozess detailliert beschrieben.

