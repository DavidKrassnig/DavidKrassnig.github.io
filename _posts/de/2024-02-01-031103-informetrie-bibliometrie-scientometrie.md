---
layout: post
title: Informetrie, Bibliometrie und Scientometrie
date: 2023-11-04 11:15:00+0200
description: Vorlesungsmitschrift für Lehrgebiet 11.03 (Modul 3)
tags: library-science DE-only
categories: lecture-notes
giscus_comments: true
related_posts: false
toc:
  sidebar: left
  beginning: true
pretty_table: true
---

## 1. Konsultation

### Einleitung

#### Ziele

- Überblick über Gegenstand & Methoden des Fachgebiets
- Schwerpunkt: Empirische Bibliometrie & Praxisrelevanz für Bibliotheken und Informationseinrichtungen
- Verständnis über Anwendungsmöglichkeiten und deren Grenzen
- Befähigung zur Anbahnung bibliometrischer Analysen

#### Wichtige Literatur

- Frank Havemann. 2016. Einführung in die Bibliometrie. 2. Auflage. Berlin. [http://d-nb.info/1113795433](http://d-nb.info/1113795433)
- Cassidy R. Sugimoto & Vincent Larivière. 2018. Measuring Research. What Everyone Needs to Know. Oxford.

### Theoretische Grundlagen & Geschichte

#### Definition(en)

> DEFINITION (Bibliometrie)
>
> Die Bibliometrie analysiert bibliographische Informationen mit statistischen Methoden (Otlet 1934, Pritchard 1969).
> {: .block-tip }

> DEFINITION (Scientometrie)
>
> Scientometrie (auch Szientometrie) untersucht Bedingungen und Ergebnisse wissenschaftlicher Informationsprozesse mit statistischen Methoden (Nalimov & Mulchenko 1969).
> {: .block-tip }

> DEFINITION (Informetrie)
>
> Die Informetrie ist die Lehre der Messung von Information (Nacke 1979).
> {: .block-tip }

> DEFINITION (Webometrie)
>
> Untersucht wissenschaftliche Kommunikation im Web mit bibliometrischen und informetrischen Methoden (Almind & Ingwersen 1997)
> {: .block-tip }

> ANMERKUNG
>
> Webometrie ist ein veralteter Begriff der aktuell kaum noch verwendet wird, da der wissenschaftliche Diskurs inzwischen hauptsächlich online stattfindet.
> {: .block-warning }

> DEFINITION (Altmetrics)
>
> Abgrenzung zu traditionellen Verfahren der Bibliometrie mit Fokus auf neuartige Kommunikationsformen in der Wissenschaft (Priem et al. 2010).
> {: .block-tip }

> DEFINITION (Science of Science)
>
> The science of science (SciSci) is based on a transdisciplinary approach that uses large data sets to study the mechanisms underlying the doing of science—from the choice of a research problem to career trajectories and progess within a field (Fortunato et al. 2018).
> {: .block-tip }

- Beziehung zwischen den verschiedenen Metriken:
  - Informetrie: Obermenge zu allen anderen Feldern
  - Bibliometrie zu Scientometrie: Große Schnittmenge ohne Teilmengenrelation (Scientometrie behandelt mehr als nur Publikationsverhalten)
  - Webometrie zu Bibliometrie: Teilmengenrelation
- Bestehende Kontroverse über Verhältnis zwischen Science of Science und Bibliometrie (Sugimoto 2021).

#### Bibliometrische Verteilungen

- Gründung des Fachgebiets durch Beobachtung von statistischen Regelmäßigkeiten bei der Analyse von Bibliographien:
  - Lotka-Verteilung (1926)
  - Bradford-Verteilung (1934)
  - Wachstum wissenschaftlicher Literatur (de Solla Price 1963)

##### Lotka-Verteilung

> It would be of interest to determine, if possible, the part which men of different calibre contribute to the progress of science.

- Lotka untersuchte die Häufigkeit von erwähnten wissenschaftlichen Beiträgen pro Person in Fachbibliografie & versuchte die Verteilung mathematisch zu beschreiben
  - Schiefe Verteilung der Produktion
  - Potenzfunktion mit fallender Tendenz -> Potenzgesetz (en. _power law_)
  - Beobachtet über verschiedene Bibliographien hinweg
  - Potenzgesetze auch bei sozio-ökonomischen (Pareto) und linguistischen Phänomenen (Zipf-Gesetz)
  - Reduktiv zusammengefasst: die meisten haben nur sehr wenige Beiträge; einige wenige sind hyperproduktiv

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/lectures-notes/031103-lotka-verteilung.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    <b>Abbildung:</b> Lotka-Diagramm der <i>Chemical Abstracts</i> 1907–1916 (Buchstaben A und B) in doppelt-logarithmischer Darstellung. Die Gerade entspricht einer fallenden Potenzfunktion mit α = 1.888. Daten: Lotka (1926). Darstellung: Havemann (2016).
</div>

> **Zusammenfassung:** Die Lotka-Verteilung wissenschaftlicher Autoren nach ihrer Produktivität folgt einem Potenzgesetz, nach dem
> die Zahl $$ f(j) $$ der Autoren mit $$ j $$ Beiträgen zu einer Fachbibliographie
> mit $$ 1/j^\alpha $$ abnimmt. Lotka fand $$ \alpha \approx 2 $$ und für den Anteil von Autoren
> mit nur einem Beitrag Werte nahe 60 %. (Havemann 2016)

##### Bradford-Verteilung

- Bradfordsche Gesetz zur Literaturstreuung (en. _Bradford's Law of Scattering_)
  - Verteilung wissenschaftlicher Fachzeitschriften nach Zahl ihrer fachich relevanten Artikel
  - Aufteilung in Kern und Zonen (_Kernzeitschriften_) mit jeweils gleicher Anzahl an relevanten Artikeln
  - Bradfords Schlussfolgerung: Abschaffung von Referatezeitschriften zugunsten übergreifender Indizes
  - Reduktives Beispiel: die Top10 Zeitschriften beinhalten 1/3 aller relevanten Artikel, die Top50 beinhalten 2/3 aller relevanten Artikel etc.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/lectures-notes/031103-bradford-verteilung.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    <b>Abbildung:</b> Das Bradford-Diagramm der Schmiermittel-Forschung 1931–1933 (halb-logarithmische Darstellung). Die Kurve entspricht einer Leimkuhler-Funktion mit a = 107.7 und b = 0.233. Die waagerechten Linien unterteilen die Artikel in drei gleich große Teilmengen, die senkrechten zeigen den Kern und zwei Zonen von Zeitschriften (10, 45 − 10 = 35 und 168 − 45 = 123 Journale). Darstellung: Havemann (2016).
</div>

> **Zusammenfassung:** Die Bradford-Verteilung wissenschaftlicher
> Fachzeitschriften nach der Zahl ihrer Beiträge zu einer Fachbibliographie lässt sich durch die Einteilung der Journale in einen Kern der
> am meisten zum Thema beitragenden und weitere Zonen von weniger beitragenden Periodika charakterisieren. Kern und Zonen können
> so gewählt werden, dass sie jeweils die gleiche Zahl von Artikeln
> enthalten, die aber über jeweils immer mehr Zeitschriften verstreut
> sind. Bradford’s law of scattering ist in vielen Bibliographien so realisiert,
> dass sich die Zahlen der Zeitschriften in Kern und Zonen an-
> genähert so verhalten wie $$ 1:k :k^2 \ldots $$.
> Das Problem einer möglichst allgemeingültigen mathematischen Modellierung empirischer Bradford-Verteilungen wurde > in der bibliometrischen Literatur lange diskutiert,
> aber ohne abschließendes Ergebnis. (Havemann 2016)

##### Wachstum wissenschaftlicher Literatur

- Wissenschaftliche Literatur wächst exponentiell (de Solla Price 1963)
  - Rate: Verdopplung alle 10-15 Jahre
  - Erwartet Übergang von exponentielles ins logarithmische Wachstum (Sättigung)
- Erwartete Sättigung kann bisher nicht beobachtet werden!

#### Bibliometrische Netzwerke

- Wissenschaftliche Publikationsaktivitäten lassen sich als Graph modellieren
- Deren relationale Eigenschaften lassen sich mit Methoden der (Sozialen) Netzwerkanalyse statistisch beschreiben
- Beispiele
  - Zitationsnetzwerke (de Solla Price 1965)
  - Ko-Autorenschaftsnetzwerke (de Beaver & Rosen 1978)

##### Zitationsnetzwerke

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/lectures-notes/031103-zitationsnetzwerk.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    <b>Abbildung:</b> Zeitlich geordneter Graph des Zitationsnetzwerks zwischen den ersten zwölf Artikeln über N-rays. Datenquelle: de Solla Price (1965). Darstellung: Havemann (2016).
</div>

> DEFINITION (Bibliographische Kopplung)
>
> Zwei Artikel sind bibliographisch gekoppelt, wenn mindestens eine Quelle in beiden Artikeln zitiert wird (Kessler 1963).
> {: .block-tip }

- Nachnutzung im Information Retrieval (_related records_)
  - Verwandtschaft von Artikeln über Anzahl gemeinsamer Referenzen definiert
  - I.e.: Vermutung dass für Leser Artikel mit ähnlichen Quellenangaben relevant sind

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/lectures-notes/031103-bibliographische-kopplung.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    <b>Abbildung:</b> Beispiel einer bibliographischen Kopplung. In den Artikeln 1 und 2 wird Artikel 3 zitiert. Darstellung: Havemann (2016).
</div>

> DEFINITION (Ko-Zitation)
>
> Zwei Artikel werden kozitiert, wenn sie von mindestens einem Dritten gemeinsam zitiert werden. (Marshakova 1973, Small 1973)
> {: .block-tip }

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/lectures-notes/031103-kozitation.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    <b>Abbildung:</b> Beispiel einer Kozitation. Die Artikel 2 und 3 werden beide in Artikel 1 zitiert. Darstellung: Havemann (2016).
</div>

> DEFINITION (Mapping of Science)
>
> Abbildung von Beziehungen zwischen Autoren, Journalen oder Disziplinen auf Basis von Ko-Zitationen.
> {: .block-tip }

##### Ko-Autorenschaftsnetzwerke

> DEFINITION (Ko-Autorenschaftsnetzwerk)
>
> Netzwerk zwischen Forschenden mittels gemeinsamer Publikationen
> {: .block-tip }

- de Beaver und Rosen (1978) untersuchten solche Beziehungen zwischen europäischen Gelehrten im 17.-19. Jahrhundert
  - Datenquelle: Alte zeitgenössische Bibliografien
- Ko-Autorenschaftsnetzwerk kann bipartit dargestellt werden
  - Eine Methode: Actor & Event

## 2. Konsultation (Abschluss)

### Bibliometrische Indikatoren

> DEFINITION (Indikator)
>
> Ein Indikator quantifiziert theoretische Begriffe und Hypothesen durch messbare Ereignisse.
> {: .block-tip }

- Mögliche Indikatorereignisse:

  - Input (z.B. Forschungsgelder)
  - Output (z.B Publikation)
  - Rezeption (z.B. Zitationen)

- Es gibt 4 verschiedene relevante Indikatorarten
  - Produktivität
  - Wirkung (en. _Impact_)
  - Kooperation
  - Gesellschaftliche Herausforderungen

#### Produktivität

- Gemessen anhand der Anzahl der Publikationen einer Untersuchungseinheit
- Aggregationsebenen:
  - Mikroebene (individuelle Forschende oder Gruppen)
  - Mesoebene (Institutionen, Journal)
  - Makroebene (Gesamtheit eines Landes oder Disziplin)

##### Ko-Autorenschaft

- Frühere Jahrhunderte: Einfacher, Produktivität zu messen
- Heute: Hauptsächlich kollaborative Artikel
  - Variiert zwischen Fachgebieten (Humanities: Low-Increasing; MINT: High-Increasing)
- Zählweisen
  - Straight Counting: Publikation wird nur einer Autorin zugerechnet (z.B. Lotka)
  - Full/Whole Counting: Publikation wird allen Autoren ganzzahlig zugerechnet
  - Fractional Counting: Publikation wird jedem Autor anteilig zugerechnet

<div class="caption">
    <b>Tabelle:</b> Beispielrechnung für die verschiedenen Zählweisen für Publikationen.
</div>

|                      | Autor 1 | Autor 2 | Autor 3 | Autor 4 |
| -------------------- | ------- | ------- | ------- | ------- |
| Full Counting        | 1       | 1       | 1       | 1       |
| Fractional Counting  | 0.25    | 0.25    | 0.25    | 0.25    |
| First Author         | 1       | 0       | 0       | 0       |
| Corresponding Author | 0       | 0       | 0       | 1       |

- Alternative Zählmethode: Autorschaftsrollen
  - Z.B. First Author, Corresponding Author, CRediT (Contributor Roles Taxonomy)

#### Wirkung

> Impact is a fundamental concept in measuring research and the Holy Grail for policy makers, university administrators, and funding agencies.
> However, impact is perhaps the most difficult concept to capture and operationalize. (Sugimoto & Larivière 2018)

##### Problematik

- Akademische Wirkung wird häufig via Zitationsdaten gemessen
- Mögliche Verzerrungsquellen
  - Verschiedene Fachgebiete zitieren unterschiedlich viele Quellen pro Artikel
  - Verschiedene Fachgebiete publizieren unterschiedlich viele Artikel
  - Verschiedene Fachgebiete zitieren neue Quellen unterschiedlich schnell

##### Anpassungsstrategien

- CWTS: Normalisierung erfolgt bezüglich Forschungsfeld und Alter der Publikation

<div class="caption">
    <b>Tabelle:</b> Übersicht über die CWTS-Anpassungsstrategien.
</div>

|                           | Size-dependent                      | Size-independent                        |
| ------------------------- | ----------------------------------- | --------------------------------------- |
| Citations                 | Total citation score                | Mean citation score                     |
|                           | Total normalized citation score     | Mean normalized citation score          |
| Highly cited publications | Number of highly cited publications | Proportion of highly cited publications |

- Definitionen:
  \begin{equation}
  S\_\text{TotalCitationScore}=C_1+\ldots+C_n
  \end{equation}

\begin{equation}
S*\text{MeanCitationScore}=\frac{S*\text{TotalCitationScore}}{n}
\end{equation}

\begin{equation}
S*\text{TotalNormalizedCitationScore}=\frac{C_1}{S*\text{MeanCitationScore}}+\ldots+\frac{C*n}{S*\text{MeanCitationScore}}
\end{equation}

\begin{equation}
S*\text{MeanNormalizedCitationScore}=\frac{S*\text{TotalNormalizedCitationScore}}{n}
\end{equation}

- [Rechenbeispiele für Feldnormalisierung](https://pad.gwdg.de/VTk32MDdQ7usmEOKnqnP6Q#Normalisierung-Zitationen)
- Zitationskontext
  - Weniger nachschauen wie häufig zitiert wird
  - Mehr nachschauen in welchem Kontext zitiert wird (z.B. Zusammenfassung in der Hintergrund-Sektion)
  - Beispiel: SemanticScholar

##### Journal Impact Factor (JIF)

- Formel, wo C=Zitierungen aus einem Jahr von Publikationen aus den beiden Vorjahren, P=Publikationen und y=Jahr:

\begin{equation}
\frac{C*{y}}{P*{y-1}+P\_{y-2}}
\end{equation}

- Entwickelt von Garfield & Sher (1963)
- Veröffentlicht im Journal Citation Report
- Keine Vorhersagekraft für die Zitierung einelner Artikel
- Verzerrung durch wenige Artikel mit hohen Zitationsraten möglich
  - Auswirkung von Long Tail)
- Mittelpunkt von Gaming-Strategien wissenschaftlicher Journale (Zitationskartelle)

##### CiteScore

- Formel, wo C=Zitierungen von Publikationen aus einem Jahr und den drei Jahren davor, P=Publikationen und y=Jahr:

\begin{equation}
\frac{C*{y}+C*{y-1}+C*{y-2}+C*{y-3}}{P*{y}+P*{y-1}+P*{y-2}+P*{y-3}}
\end{equation}

##### Hirsch-Index (h-Index)

> DEFINITION (h-Index)
>
> Der h-Index entspricht dem maximalen Wert h, so dass der Autor mindestens h Publikationen hat, die h-mal zitiert worden sind.
> {: .block-tip }

- Entwickelt von Jorge E. Hirsch (2005)
- Absteigende Sortierung einer Bibliographie nach Anzahl der Zitationen
- Dämpft den sog. Matthäus-Effekt, bevorzugt aber umfangreiche Bibliographien
- Hirsch stellte selbst disziplinspezifische Abweichungen fest!

- Beispiel:

  - Autor-1 hat zwei Publikationen: A (2x zitiert), B (1x zitiert), h-index=1
  - Autor-2 hat zwei Publikationen: A (2x zitiert), B (2x zitiert), h-index=2
  - Autor-3 hat zwei Publikationen: A (2x zitiert), B (365x zitiert), h-index=2

- Anwendungsfelder:

  - Produktivität und Wirkung eines Autors (Originalanwendung)
  - Produktivität und Wirkung einer Forschergruppe
  - Produktivität und Wirkung eines Journals

- Kontra-Argumente:
  - Arbeitsalter nicht berücksichtigt
  - Disziplinabhängigkeit
  - Zitationskontext
  - Manipulation
  - Publikationsarten Unterschiede nicht gewürdigt
- Pro-Argumente:
  - Mathäus-Effekt eingedämpft
  - Sehr einfach

#### Kooperation

- Ko-Autorschaft als Indikator für die formelle Zusammenarbeit zwischen
  - Personen
  - Einrichtungen
  - Länder oder Regionen
- Indikatoren:
  - Anzahl, Anteile oder Mittelwerte
  - Maße der sozialen Netzwerkanalyse (z.B. Zentralitätsmaße)
- Ist Ko-Autorschaft tatsächlich repräsentativ für Zusammenarbeit von Institutionen?
  - Fragwürdig! (Katz & Martin 1995)
  - Z.B. eine Professorin ist an zwei Institutionen tätig; indikativ für institutionelle Zusammenarbeit?
  - Hottenrott et al. (2021): ~16% aller Autoren haben mehr als eine Affiliationen
    - Davon 60% zwischen akademischen Einrichtungen
    - Davon 25% zwischen verschiedenen Ländern
  - Nur ein Teilindikator!

#### Gesellschaftliche Herausforderungen

- Gleichstellung & Geschlecht
  - Z.B. Einfluss von Geschlecht auf Publikationsleistung prä-COVID vs während COVID (Frauen stärkere Abnahme)
  - Warum wichtig? U.a.: Medizinische Artikel mit weiblichen (Co-)Autoren haben robustere Evidenz-Grundlage
- Mobilität
  - Scientometrie: Messung welche Wissenschaftlergattungen von wo wegziehen und hinziehen?
  - Bibliometrie: Welche Länder haben wie viele publizierte Autoren?
- Innovation
- Open Access
  - Hoher Bedarf bei Förderern & Einrichtungen zum Monitoring von OA-Policies/OA-Transformation
  - Wachsende Anzahl bibliometrischer Studien widmet sich OA im Zuge einer verbesserten Datenbasis (Piwowar et al. 2018)
- Nachhaltigkeit
  - Nachhaltigkeitsziele der Vereinten Nationen (Sustainable Development Guides (SDG))
- COVID-19
  - Z.B. Aufnahme von Preprints während COVID-Zeit
- Goodhartsche Gesetz:
  - "When a measure becomes a target, it ceases to be a good measure"
- San Francisco Declaration on Research Assessment (DORA)
  - Welche Praxen werden nicht als verantwortungsbewusst erachtet von Wissenschaftlern?
  - Forderung, dass solche Indikatoren zurückgefahren werden
- Etc.

### Datenquellen und Tools

#### Datenquellen

- Versuch einer Einordnung bibliometrischer Datenbanken:
  - Beispiele: Google Scholar, Microsoft Academic, Scopus, Web of Science, COCI, Dimensions
  - Umfang: Selektiv / Umfassend
  - Zugang:
    - Online-Datenbank, API, Rohdaten, Big Data Analytics Interfaces
    - Kostenpflichtig, Forschugnszugang, Freemium Modell, Kostenfrei
  - Nachnutzung: Nicht gestattet, Scientific Use, Open
  - Geschäftsmodell: Kommerziell (z.B. Scopus), Non-Profit, öffentlich finanziert
- Vergleich Datenquellen von Martin-Martin et al. (2021)
  - Übersicht, inwiefern sich bibliographische Datenbanken überschneiden
  - Z.B. 26% aller Quellen findet man nur in Google Scholar
- OpenAlex: Offene bibliographische Dateninfrastruktur
- Bibliometrische Dateninfrastrukturen
  - DE: Kompetenzzentrum/-netzwerk Bibliometrie
- Scholarly Knowledge Graph (z.B. OpenAIRE ResearchGraph)

#### Tools

- Spezifische Berichte (Kompetenznetzwerk Bibliometrie)
- Analysewerkzeuge von Anbietern bibliometrischer Datenbanken und Forschungsinformationssystemen (InCite, SciVal, PURE)
- Visualisierungswerkzeuge (VosViewer)
- REST APIs
- Statistische Software
- Data Analytics Workflow

#### Zusammenfassung

- Starkes Anwachsen bibliometrischer Datenquellen machen komparative Analysen & Qualitätssicherungsmaßnahmen erforderlich
- Gefahr der Kommodifizierung von bibliometrischen Daten durch wissenschaftliche Verlage und Datenbankanbieter
- Bibliotheken haben Schlüsselrolle inne, für offene & umfangreiche Metadaten über wissenschaftliche Publikationen zu sorgen
- Hohe Diversität an Werkzeugen, wobei ein Trend hin zu Data-Science-Werkzeugen zu beobachten ist

### Anwendungsgebiete in der Informationspraxis

- Abschnitt motiviert von Dr. Stephan Gauch: Territorien der Bibliometrie
  1. Beratungskontexte
     - Evaluieren
       - Z.B. Produktivität der Einrichtung evaluieren für Entscheidungen bei Vergabe von Verträgen
     - Explorieren
       - Z.B. Wissenslandschaften abbilden / Evaluieren, welche Journals verloren gegangen sind oder gesichert werden müssen
     - Replizieren
       - Z.B. Status Quo Abbildung, Rankings für Entscheidungsträgerinnen abbilden / Beobachtung von wissenschaftlichen Trends
     - Vermitteln
       - Z.B. Vermittlung von Impact an wissenschaftliches Personal / Vor und Nachteile vermitteln
     - Reflektieren
       - Unbeabsichtigte Folgen, bewusster Umgang etc.
       - Z.B. DORA. Coalition for Advancing Research Assessment (CoARA), Leiden Manifesto etc.
  2. Kurative Aufgaben
     - Betrieb & Pflege einer Hochschulbibliographie / eines Hochschulinformationssystems
     - Entwicklung und Anwendung von Verfahren zur Qualitätssicherung (z.B. PID)
     - Monitoring von OA-Verlagsmetadaten
     - Analyse Datenqualität in Bibliometriedatenbank
     - Bereitstellung von bibliometrischen Datenbeständen und Tools
  3. Information / Data Literacy
     - Schulungen
     - Curriculumentwicklung
     - Forschungsunterstützung
