# DHGE Zitierstil

## Einführung

Dies ist eine CSL-Implementierung des von der Dualen Hochschule Gera Eisenach vorgeschlagenen Zitiertstils für die Verwendung mit Zotero, Mendely, Paperpile, etc. Da die DHGE sowohl bei den In-Text-Citations und der Bibliographie sogenannte Citekeys (z.B. [LB89]) verwendet, ist außerdem das Zotero-Plugin [Better BibTeX](https://retorque.re/zotero-better-bibtex/) erforderlich.

Das Erstellen eines Zitierstils ist ein relativ kompexer Prozess bei dem viel bedacht werden muss (weswegen man eigentlich einfach einen Standard wie APA, MLA, etc. verwendet). Sollte euch also Unerwartetes/ein Fehler auffallen bitte rein damit in die Issues.

## Installation

1. **Klonen des Repositories**
2. **Hinzufügen des Zitierstils**
   1. Aufrufen von Zotero → Settings → Cite → +
   2. Hinzufügen von `duale-hochschule-gera-eisenach.csl`
   ![Bild 1](https://github.com/DeEskalator/dhge-zitierstil/blob/main/Bilder/Bild%201.png)

3. **Einrichtung der Citekeys**
   1. Download und Installation des Better BibTeX-Plugins ([Installationsanweisung](https://retorque.re/zotero-better-bibtex/installation/index.html))
   2. Aufgrufen von Zotero → Settings →  Better BibTeX  → Import → Import BetterBibTeX preferences/citation keys...
   3. Import der Citekey-Einstellungen aus `BibTeX.json`
   ![Bild 2](https://github.com/DeEskalator/dhge-zitierstil/blob/main/Bilder/Bild%202.png)

1. **Aktualisieren der bestehenden Citekeys auf das neue Format:**
   1. Markieren aller betreffenenden Einträge in Zotero
   2. Rechtsklick auf alle Einträge → Better BibTeX → Refresh BibTeX key

## Hinweise/Bekannte Probleme

- [SSPK00] sollte laut "Hinweise und Empfehlungen zur Anfertigung schriftlicher Arbeiten" [SSP+00] sein. Ab 4. Autoren wird aber das korrekt das "+" angezeigt. Dies ist eine Limitierung von Better BibTeX
- Quellen aus Sammelwerken/Zeitschriften sollte man immer als Dokumenttyp "Book Section" und nicht als "Journal Article" hinzufügen da nur "Book Section" das CSL-Feld Verlag hat wie es unter Hinweise und Empfehlungen zur Anfertigung schriftlicher Arbeiten
- Erstelldatum von Onlinequellen wird in meiner Erfahrung von Zotero nur unzuverlässig erkannt und sollte hinzugefügt werden. Das Abrufdatum wird aber automatisch hinzugefügt
- für Webquellen ist in kein Feld für "Ort" vorgesehen. In den "Hinweisen und Empfehlungen zur Anfertigung schriftlicher Arbeiten" wird dieses Feld auch bei Onlinequellen hinzugefügt
- Keine Erkennung von Standarddokumenten in für Citekeys (z.B. [ISO99]). Citekey kann aber in Zotero einfach geändert werden

## Warum?

Im Vergleich zum bestehenden Citavi-Stil sollte diese Implementierung eine bessere Unterstützung von Sammelwerken und Online-Quellen bieten. Diesen fehlen in Citavi bestimmte Felder. Da die Basis von APA 7th. Edition kommt erhoffe ich mir ebenfalls ein robusteres Handling anderer Quellenarten.

Außerdem entgeht man hiermit dem Krebsgeschwür was Citavi eine Windows-Anwendung nennt was mir die Möglichkeit gibt Citekeys auch auf macOS (oder Linux) sinnvoll zu nutzen. Weiterhin bietet Zotero meiner Meinung nach die weitaus überzeugendere Quellenverwaltung in Bezug auf Geschwindkeit, Trefferrate bei Metadaten, Integration mit TeX, Safari. The list goes on ...

## Links

[Verwendetes Template](http://www.zotero.org/styles/apa-6th-edition)

[Visual CSL-Editor](https://editor.citationstyles.org/visualEditor/)

[DHGE Hinweise und Empfehlungen zur Anfertigung schriftlicher Arbeiten](https://backstage.dhge.de/mod/resource/view.php?id=417)

