# Scraping-The-Internet-Archive

--- A python programme analyzing media trends with data scraped from the Internet Archive / Wayback Machine ---

## Einleitung

Am 25.2.2020 wurde die erste Coronainfektion in der Schweiz nachgewiesen. Seitdem hat das Virus nicht nur die Infizierten im Griff, sondern sich tief in unser aller Leben gefressen. Das lässt sich auch daran ablesen, dass auf der Startseite der NZZ nur wenige Themen gegen den (facettenreichen) Corona-Reigen eine Chance hatten: Lockdown und Schliessungen, die Maskenpflicht und deren Verweigerung, finanzielle und psychische Belastungen, die Toten, das stets unperfekte Testen und Tracen, die Impfstoffe. Wie viel Raum diese Themen in den letzten 12 Monaten auf der Frontpage der NZZ hatten, zeichne ich in einer Visualisierung nach.

## Publikation am 25. Februar 2021

im Ressort Schweiz der NZZ:

www.nzz.ch/ld.xxxxxxxx

## Idee

Snapshots (auch 'Captures') von www.nzz.ch sind im Internet Archive (https://archive.org/) hinterlegt. Ich baue einen Scraper, der diese Snapshots als .html abspeichert. Mit BeautifulSoup extrahiere ich aus diesen Dokumenten die Titel, Teaser und URL aller Artikel, die zum Zeitpunkt des Captures auf der Frontpage der NZZ publiziert waren. Mit Pandas durchsuche ich die so erstellte Datenbank nach geeigneten Schlagworten.

Zum Beispiel können wir mit diesem Datensatz
- das Coronajahr analysieren: Wann standen Tests, Impfungen, Lockdown, Kinder & Homeschoooling, Homeoffice, Psyche und Krise im Vordergrund?
- die mediale Karriere von Trump nachzeichnen: Wann beherrschte er die News? Und weshalb?
- nachschauen, ob die Popularität bestimmter sozialer Medien parallel zu deren Medienpräsenz verläuft (vgl. Hype um Clubhouse Anfang 2021, Snapchat 2015/16 etc pp)

# Einschätzung von Aufwand und Ertrag

**Programmierung des Scrapers, Datenbereinigung, Analyse:** ca. 3 Arbeitstage

Im Netz findet man schnell viele Vorbilder für das Scraping von Inhalten von archive.org, die als Hilfestellung herangezogen werden können.

**Visualisierung, Finetuning der Analyse, Texte erstellen:** ca. 2 Arbeitstage

Die eigentliche Schwierigkeit besteht darin, die Visualisierung so zu optmieren, dass sie für den Leser gut verständlich ist und das "Schweizer Coronajahr" beim Durchscrollen nach-erlebbar macht, Erinnerungen an das besondere Jahr im Zeichen des Coronavirus weckt. Die Kategorien von Suchworten dürfen weder zu eng noch zu grob gefasst werden, sonst gehen womöglich erkenntnisreiche Unterschiede verloren.  

**Erwarteter Ertrag:** 

Ein von einer einzigen, grossen Grafik getragener Beitrag für nzz.ch/schweiz, der vor allem auf mobilen Endgeräten ein unterhaltsames Leseerlebnis bietet. Durch den engen Bezug auf das eigene Erleben der Coronapandemie in der Schweiz wird die Visualisierung beim Leser verschiedenste Emotionen wecken.

Der journalistische Impact und die Tiefe des Inhalts sind eher im unteren Drittel anzusiedeln; aus der Datenanalyse ergeben sich ja keine vollkommen neuen Erkenntnisse. Dafür könnte der Beitrag, da für den Austausch auf sozialen Medien geeignet, eine sehr hohe Reichweite erzielen. Die zugrunde liegenden Programme und erstellten Datenbanken können, wie oben skizziert, in leicht abgewandelter Form für zahlreiche andere Fragestellungen genutzt werden. Die Erzählweise in Form einer grossen Datenvisualisierung wird in den Tageszeitungen bisher noch selten genutzt und ist insofern innovativ.

# Code, Daten und Visualisierung

<a href=https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/IAScraper.ipynb>IAScraper.ipynb</a> - Scraper

<a href=https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/CoronaTrendsSchweiz.ipynb>CoronaTrendsSchweiz.ipynb</a> - Datenbereinigung und -analyse, Visualisierung

<a href=https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/fp-nzz-complete.csv>fp-nzz-complete.csv</a> - Die Daten des untersuchten Zeitraums in einem CSV aggregiert

<a href=https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/CoronatrendsSteamgraph.svg>CoronatrendsSteamgraph.svg</a> - finale Grafiken für Weiterverarbeitung in Illustrator etc. pp.

# Arbeitsprotokoll


Datum | Zeitaufwand | Beschreibung
-------- | -------- | :--------
29./30.12.2020 | 2h | Idee entwickeln, Scraper für Internet Archive recherchieren
01.02.2021 | 6h | Scraper programmieren
02.02.2021 | 6h | Daten zusammenführen und bereinigen
04.02.2021 | 6h | Analyse & erste Visualisierungen
08.-12.02.2021 | 2h | Briefings mit Anja Lemcke (NZZ Visuals), Christina Neuhaus (RL NZZ Schweiz), Barnaby Skinner (RL NZZ Visuals)
08.02.2021 | 4h | versch. Bugfixes & Erweiterungen
11.02.2021 | 1h | Projektdokumentation anlegen
17./18.02.2021 | 6h |finale Grafiken erstellen, Annotationen verfassen
24.-25.02.2021 | 2h | Produktion und Veröffentlichung, Social Media

Gesamter Aufwand: ca. 35 Arbeitsstunden 


```python

```
