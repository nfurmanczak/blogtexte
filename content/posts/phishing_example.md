---
title: "Phishing-Beispiel"
date: 2025-03-26T20:35:41+02:00
draft: false
tags: ["Phishing","IT-Security"]
ShowToc: true
---
# Einleitung

Bei Phishing-E-Mails scheint es nur zwei Kategorien zu geben: Sie sind entweder plump oder erstaunlich raffiniert. Ein echtes Mittelding ist selten. Kürzlich ist mir jedoch ein Exemplar in die Hände gefallen, das – zumindest technisch betrachtet – ein Paradebeispiel für ausgeklügeltes Phishing darstellt.

## Auffälligkeiten im Header

Bereits in den Header-Daten fielen Manipulationen auf: Sowohl der *Return-Path* als auch der *Friendly-From* waren gefälscht. Im Gegensatz zu vielen simpleren Phishing-Versuchen wurde hier gezielt eine glaubwürdige Absenderadresse genutzt.

Auffällig war das die Domain im Return-Path über einen gültigen SPF-Record mit *Hardfail* verfügte. Die E-Mail hätte also entweder abgelehnt oder zumindest als Spam/Verdächtig erkannt werden müssen. Offenbar wurde jedoch keine SPF-Prüfung durchgeführt – stattdessen wurde nur auf eine DKIM-Signatur geprüft, die allerdings fehlte. Das war für mich Grund genug, die Mail genauer zu betrachten.

## Aufbau der E-Mail: Multipart mit Text und HTML

Die E-Mail war korrekt als `multipart/alternative` formatiert – mit einem Plain-Text-Teil sowie einem HTML-Part. Schon im Plain-Text-Teil zeigte sich eine Obfuskation (Verschleierung) indem wahllose Zeichenketten eingefügt werden um Filtermechanismen wie Reguläre Ausdrücke oder NLP-gestützte Erkennung zu umgehen. Interessanterweise bleiben jedoch Schlagworte wie „Steuerdaten“ oder die Anrede intakt – vermutlich, damit sie in der Vorschau des E-Mail-Clients sichtbar bleiben.


    Steuerdaten für das Jahr 2024

    Sehr geehrter Kunde, Sehr geehrte Kundin

    gFkür adtas dJsaxhr t2z0x24 gkyosnkndte rawbgswckhdlwijexßeen fnzogch ikkeiiyne...


## HTML-Part

Im HTML-Teil der Nachricht wurde eine Vielzahl an Verschleierungstechniken kombiniert:

### 1. Zero-Width Obfuscation (versteckte Zeichen)

Unsichtbare Zeichen werden mit `width: 0px`, `display: inline-block` und `overflow: hidden` in das Layout eingebettet. So werden Wörter optisch intakt dargestellt, enthalten aber für Maschinen störende Elemente:

    <tt style="WIDTH: 0px;">k</tt>


### 2. CSS-Visual Noise (visuelle Tarnung)

Einzelne Buchstaben oder Zeichen werden mit ablenkenden Farben, Schatteneffekten oder unnötigen Styles versehen:

    <u style="COLOR: #6569d7; DISPLAY: inline-block;">i</u>

### 3. Zerstückelung kritischer Begriffe

Ein gutes Beispiel ist der „Zum Portal“-Button. Der Button-Text ist so stark fragmentiert, dass er für Filter kaum zu erkennen ist:

    </sup>Z<sup style="...">d</sup>um

### 4. Link-Verschleierung durch URL-Shortener

Der Button verlinkt auf eine TinyURL-Adresse. Einige Mail-Provider blockieren Shortener-Dienste – andere hingegen nicht. Durch URL-Shortener wird der eigentliche Ziel-Link verschleiert, was die Analyse und Erkennung erschwert.

### 5. Vertrauensanker mit legitimen Links

Am Ende der Mail wird ein Link zu einem Wikipedia-Artikel eingebunden – vermutlich, um der Nachricht Seriosität zu verleihen:

    <a href="https://en.wikipedia.org/wiki/Bishehi">Bishehi</a>

Solche „Trust-Links“ sind ein häufig eingesetztes Mittel, um automatisierte Filter zu verwirren oder den Empfänger in Sicherheit zu wiegen.

### 6. Design

Das visuelle Erscheinungsbild der E-Mail orientierte sich stark an dem der offiziellen Webseite. Es wurden aktuelle und authentische Logos verwendet, die über die Google Cloud Platform (GCP) gehostet wurden. Die Rechtschreibung war durchgehend korrekt, wobei in einigen Fällen abschließende Satzzeichen fehlten. Insgesamt war die E-Mail gestalterisch überzeugend und zeugt davon, dass sich der Urheber intensiv mit dem Originaldesign auseinandergesetzt hat. Leider wurde die verlinkte Phishing-Seite zeitnah deaktiviert, sodass eine eingehendere Analyse nicht mehr möglich war.

## Psychologische Komponente

Wie bei den meisten Phishing-Mails wurde auch hier auf **Dringlichkeit und Handlungsdruck** gesetzt: Der Empfänger soll sich angeblich sofort in ein Portal einloggen, um Nachteile zu vermeiden – ein klassischer Social-Engineering-Ansatz.

## Fazit

Diese Phishing-Mail zeigt auf lehrreiche Weise, wie Kriminelle moderne Filter- und Erkennungssysteme gezielt umgehen. Die Kombination aus technischen Tricks, visueller Tarnung und psychologischer Manipulation macht sie zu einem idealen Beispiel für Awareness-Schulungen oder technische Analysen.
