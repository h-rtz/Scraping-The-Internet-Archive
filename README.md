# Scraping-The-Internet-Archive

--- A python programme analyzing media trends with data scraped from the Internet Archive / Wayback Machine ---

# Einleitung

Am 25.2.2020 wurde die erste Coronainfektion in der Schweiz nachgewiesen. Dann hat das Virus nicht nur die Infizierten im Griff, sondern sich tief in unser Leben gefressen. Das lässt sich auch daran ablesen, dass auf der Startseite der NZZ nur wenige Themen gegen den (facettenreichen) Corona-Reigen eine Chance hatten: Lockdown und Schliessungen, Maskenpflicht und -Verweigerung, finanzielle und psychische Belastung, die Toten, Testen und Tracen, Impfstoffe. Wie viel Raum diese Themen in den letzten 12 Monaten auf der Frontpage der NZZ hatten, zeichne ich in einer Visualisierung nach.

# Publikation am 25. Februar 2021

www.nzz.ch/ld.xxxxxxxx

# Idee

Snapshots (auch 'Captures') von www.nzz.ch sind im Internet Archive (https://archive.org/) hinterlegt. Ich baue einen Scraper, der diese Snapshots als .html abspeichert. Mit BeautifulSoup extrahiere ich aus diesen die Titel, Teaser und URL aller Artikel, die zum Zeitpunkt des Captures auf der Frontpage der NZZ publiziert waren. Mit Pandas durchsuche ich die so erstellte Datenbank nach geeigneten Schlagworten.

Zum Beispiel können wir mit diesem Datensatz
- die mediale Karriere von Trump nachzeichnen: Wann beherrschte er die News? Und weshalb?
- das Coronajahr analysieren: Wann standen Tests, Impfungen, Lockdown, Kinder & Homeschoooling, Homeoffice, Psyche und Krise im Vordergrund?

# Einschätzung von Aufwand und Ertrag

Programmierung des Scrapers, Datenbereinigung, Analyse: ca. 3 Arbeitstage
Da sich im Netz viele Vorbilder für das Scraping von Inhalten von archive.org finden, sollte es keine grundsätzlichen Prolbeme geben.

Visualisierung, Finetunig, Texte: ca. 2 Arbeitstage
Die eigentliche Schwierigkeit besteht darin, die Visualisierung so zu optmieren, dass sie für den Leser gut verständlich ist und das "Schweizer Coronajahr" beim Durchscrollen nach-erlebbar macht, Erinnerungen weckt. Die Kategorien von Suchworten dürfen weder zu eng noch zu grob gefasst werden, sonst gehen womöglich erkenntnisreiche Unterschiede verloren.  

Spiderplot???

# Knackpunkte



# Briefing

# Programmcode

IAScraper.ipynb - Scraper
CoronaTrendsSchweiz.ipynb - Datenbereinigung und -analyse, Visualisierung

# Daten

html-Dateien der IA-Captures von www.nzz.ch zwischen Januar 2020 und Ende Februar 2021
csv-Dateien mit Titeln, Teasern und URL der Artikel eines Captures
fp-nzz-complete.csv - Die Daten des untersuchten Zeitraums in einem CSV aggregiert

# Visualisierung

xxxxxx.svg - finale Grafik für Weiterverarbeitung in Illustrator etc. pp.

# Arbeitsprotokoll

29./30.12.2020  2h  Idee entwickeln, Scraper für Internet Archive recherchieren
01.02.2021      6h  Scraper programmieren
02.02.2021      6h  Daten zusammenführen und bereinigen
04.02.2021      6h  Analyse & erste Visualisierungen
08.-12.02.2021  2h  Briefings mit Anja Lemcke, Christina Neuhaus, Barnaby Skinner
08.02.2021      4h  versch. Bugfixes & Erweiterungen
11.02.2021      1h  Projektdokumentation anlegen
  finale Grafiken erstellen, Annotationen verfassen
24.-25.02.2021  xh  Produktion und Veröffentlichung, Social Media
