# Scraping The Internet Archive

--- analyzing media trends with data scraped from the Internet Archive / Wayback Machine ---

## Einleitung

Am 25.2.2020 wurde die erste Coronainfektion in der Schweiz nachgewiesen. Seitdem hat das Virus nicht nur die Infizierten im Griff, sondern sich tief in unser aller Leben gefressen. Das lässt sich auch daran ablesen, dass auf der Startseite der NZZ nur wenige Themen gegen den (facettenreichen) Corona-Reigen eine Chance hatten: Lockdown und Schliessungen, die Maskenpflicht und deren Verweigerung, finanzielle und psychische Belastungen, die Toten, das stets unperfekte Testen und Tracen, die Impfstoffe. Wie viel Raum diese Themen in den letzten 12 Monaten auf der Frontpage der NZZ hatten, zeichne ich in einer Visualisierung nach.

## Publikation

am [25. Februar 2021 (online)](https://www.nzz.ch/das-jahr-der-unruhe-ld.1602331) und [am 9. M�rz 2021 (print)](https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/NZZ210309il_DatenanalyseCorona.pdf) im Ressort Schweiz der NZZ.

## Idee

Snapshots (auch 'Captures') von www.nzz.ch sind im Internet Archive (https://archive.org/) hinterlegt. Ich baue einen Scraper, der diese Snapshots als .html abspeichert. Mit BeautifulSoup extrahiere ich aus diesen Dokumenten die Titel, Teaser und URL aller Artikel, die zum Zeitpunkt des Captures auf der Frontpage der NZZ publiziert waren. Mit Pandas durchsuche ich die so erstellte Datenbank nach geeigneten Schlagworten.

Zum Beispiel können wir mit diesem Datensatz
- das Coronajahr analysieren: Wann standen Tests, Impfungen, Lockdown, Kinder & Homeschoooling, Homeoffice, Psyche und Krise im Vordergrund?
- die mediale Karriere von Donald Trump nachzeichnen: Wann beherrschte er die News? Und weshalb?
- nachschauen, ob die Popularität bestimmter sozialer Medien parallel zu deren Medienpräsenz verläuft (vgl. Hype um Clubhouse Anfang 2021, Snapchat 2015/16 etc pp)

Der Datensatz bietet sich gerade jetzt dafür an, visuell nachzuzeichnen, welche Themen die öffentliche Diskussion in der Schweiz bestimmt haben, seitdem am 25.2.2020 die erste Coronainfektion hierzulande nachgewiesen wurde. Damit die lange Zeitachse auch mobile ein gutes Leseerlebnis bietet, möchte ich die Grafik im fertigen Artikel um 90 Grad drehen. So läuft beim Scrollen von oben nach unten die Zeit von Februar 2020 bis Februar 2021. Annotationen markieren wichtige Ereignisse.  

# Einschätzung von Aufwand und Ertrag

**Programmierung des Scrapers, Datenbereinigung, Analyse:** ca. 3 Arbeitstage

**Visualisierung, Finetuning der Analyse, Texte erstellen:** ca. 2 Arbeitstage

Im Netz findet man schnell viele Vorbilder für das Scraping verschiedenster Inhalte von archive.org, die als Hilfestellung herangezogen werden können. Mir haben vor allem die [Erläuterungen von Abhi Kumbar auf medium.com](https://medium.com/analytics-vidhya/the-wayback-machine-scraper-63238f6abb66) geholfen. Bei der Textanalyse der Titel und Teaser habe ich mich an den Beispielen von Thomas Ebermann im MAZ-Kurs DJ 2020/21 orientiert.

**Erwarteter Ertrag:** 

Ein von einer einzigen, grossen Grafik getragener Beitrag für [nzz.ch/schweiz](https://nzz.ch/schweiz), der vor allem auf mobilen Endgeräten ein unterhaltsames Leseerlebnis bietet. Durch den engen Bezug auf das eigene Erleben der Coronapandemie in der Schweiz wird die Visualisierung beim Leser verschiedenste Emotionen wecken.

Der journalistische Impact und die Tiefe des Inhalts sind eher im unteren Drittel anzusiedeln; aus der Datenanalyse ergeben sich ja keine vollkommen neuen Erkenntnisse. Dafür könnte der Beitrag, da für den Austausch auf sozialen Medien geeignet, eine sehr hohe Reichweite erzielen. Die zugrunde liegenden Programme und erstellten Datenbanken können, wie oben skizziert, in leicht abgewandelter Form für zahlreiche andere Fragestellungen genutzt werden. Die Erzählweise in Form einer grossen Datenvisualisierung wird in den Tageszeitungen bisher noch selten genutzt und ist insofern innovativ.

**Knackpunkte**

Die eigentliche Schwierigkeit besteht darin, die Visualisierung so zu optmieren, dass sie für den Leser gut verständlich ist und das "Schweizer Coronajahr" beim Durchscrollen nach-erlebbar macht, Erinnerungen an das besondere Jahr im Zeichen des Coronavirus weckt. Die Kategorien von Suchworten dürfen weder zu eng noch zu grob gefasst werden, sonst gehen womöglich erkenntnisreiche Unterschiede verloren. Deshalb muss genügend Zeit für die Feinjustierung der Analyse eingplant werden.

## Briefing

Mein Briefing fand nicht mit den "klassischen" Experten statt, sondern auf der Strasse und zwischen Tür und Angel. "Wie hast Du die Medienberichterstattung während der Pandemie erlebt?" - das habe ich meine Nachbarn, Freunde, Kollegen, Bekannte gefragt. Haben die NZZ und andere zu viel über Corona berichtet? Was hat gefehlt, was war zu viel? Stimmt der Eindruck, dass die Omnipräsenz des Themenreigens rund um Corona das ganze Jahr lang nie so richtig abriss, dass es nicht einmal im doch relativ unbeschwerten Sommer eine "Sendepause für das Virus" gab?

Das müsste man mal nachzählen! - befanden viele. Und genau das tut diese Datenanalyse. 

# Code, Daten und Visualisierung

[IAScraper.ipynb](https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/IAScraper.ipynb) - Scraper zur Datenbeschaffung von archive.org.

[CoronaTrendsSchweiz.ipynb](https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/CoronaTrendsSchweiz.ipynb) - Datenbereinigung, -exploration und -analyse, Konzept der Visualisierung.

[DataViz-Sandbox.ipynb](https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/DataViz-Sandbox.ipynb) - Feinjustage Visualisierung; Algorithmus zur Ermittlung von Peaks (wann war welches Thema am stärksten präsent).

Die Daten des untersuchten Zeitraums sind aufgrund ihres Umfangs [auf Google Drive](https://drive.google.com/drive/folders/1vNWtfJrk_fRe8HZgz8DtqbRqwHGj_h12) abgelegt. 

[Finale Grafiken](https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/grafik/) für Weiterverarbeitung in Illustrator etc. pp.

[Fertiges Print-Produkt](https://github.com/h-rtz/Scraping-The-Internet-Archive/blob/main/NZZ210309il_DatenanalyseCorona.pdf

# Arbeitsprotokoll


Datum | Zeitaufwand | Beschreibung
-------- | -------- | :--------
29./30.12.2020 | 2h | Idee entwickeln, Scraper für Internet Archive recherchieren
01.02.2021 | 6h | Scraper programmieren
02.02.2021 | 6h | Daten zusammenführen und bereinigen
04.02.2021 | 6h | Analyse & erste Visualisierungen
08.-12.02.2021 | 2h | Briefings mit Anja Lemcke (NZZ Visuals), Christina Neuhaus (RL NZZ Schweiz), Barnaby Skinner (RL NZZ Visuals)
08.02.2021 | 4h | versch. Bugfixes & Erweiterungen
11./17.02.2021 | 3h | Projektdokumentation anlegen
17.-19.02.2021 | 12h | Grafiken überarbeitet, Annotationen erstellet, Übergabe an Jonas Oesch (NZZ Visuals)
24.-25.02.2021 | 2h | Produktion und Veröffentlichung, Social Media (tbd.)

Gesamt ca. 40 Arbeitsstunden 
