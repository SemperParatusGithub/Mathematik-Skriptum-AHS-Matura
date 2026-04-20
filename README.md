# Skriptum: Mathematik‑Matura (AHS)

Ein kompaktes Nachschlagewerk zur österreichischen **AHS‑Mathematik‑Matura**, gegliedert nach den vier offiziellen Themenbereichen:

| Kürzel | Bereich | Datei |
|--------|---------|-------|
| **AG** | Algebra und Geometrie | `1_AG.tex` |
| **FA** | Funktionale Abhängigkeiten | `2_FA.tex` |
| **AN** | Analysis | `3_AN.tex` |
| **WS** | Wahrscheinlichkeit und Statistik | `4_WS.tex` |

Das Skriptum wird in LaTeX gesetzt. Die fertig kompilierte **PDF** ist der Referenzpunkt für alle Rückmeldungen — man muss **kein LaTeX** können, um mitzuhelfen.

---

## Inhalt des Repositories

```
main.tex          Haupt-Dokument (hier wird kompiliert)
commands.tex      Eigene LaTeX-Makros und Befehle
0_Titlepage.tex   Titelseite
1_AG.tex          Kapitel: Algebra und Geometrie
2_FA.tex          Kapitel: Funktionale Abhängigkeiten
3_AN.tex          Kapitel: Analysis
4_WS.tex          Kapitel: Wahrscheinlichkeit und Statistik
background.png    Hintergrundgrafik Titelseite
Geogebra.svg.png  Logo/Grafik
```

Kompiliert wird `main.tex` (z. B. in Overleaf oder lokal mit `pdflatex` / `latexmk`).

---

## Mitwirken — wie man Fehler meldet oder Features vorschlägt

Damit das Skriptum immer besser wird, ist **jede Rückmeldung willkommen** — egal ob Tippfehler, Rechenfehler, fehlende Erklärungen oder komplett neue Themen. Damit Vorschläge schnell bearbeitet werden können, **muss** das folgende Schema eingehalten werden.

> **Wichtig:** Man muss kein LaTeX beherrschen. Es reicht, die PDF zu lesen und einen **Issue** mit der passenden Vorlage zu erstellen. Pull Requests mit direkten LaTeX‑Änderungen sind ebenfalls willkommen, aber nicht erforderlich.

### Kurz‑Entscheidungsbaum

```
Etwas ist falsch / fehlt in der PDF?
        │
        ├── Tippfehler, Rechenfehler, falsche Formel,
        │   schlechte Formatierung, kaputtes Bild …
        │        → "Fehler melden" (Bug Issue)
        │
        ├── Es fehlt ein Thema, ein Beispiel, ein Kapitel,
        │   eine Erklärung, eine Grafik …
        │        → "Feature / neuer Inhalt" (Feature Issue)
        │
        └── Du kannst LaTeX und willst die Änderung direkt beitragen?
                 → Pull Request (siehe unten)
```

---

## 1. Fehler melden (Bug)

Erstelle einen neuen **Issue** über *Issues → New issue → „Fehler im Skriptum"* und fülle die Vorlage aus. Das Schema:

### Pflichtangaben

1. **Titel** im Format:
   `[Fehler][<Kürzel>] <kurze Beschreibung>`
   Beispiele:
   - `[Fehler][AG] Vorzeichenfehler im Beispiel zur Kreisgleichung`
   - `[Fehler][WS] Tippfehler im Satz über Erwartungswert`

2. **Fundstelle** — möglichst genau:
   - Kapitel (AG / FA / AN / WS)
   - Abschnitt/Unterabschnitt (z. B. *3.2 Differenzieren*)
   - Seitenzahl in der PDF
   - Falls vorhanden: Nummer des Satzes, Beispiels, Formel oder Abbildung

3. **Was ist falsch?** — der aktuelle Inhalt so, wie er in der PDF steht (gerne abtippen oder Screenshot einfügen).

4. **Was sollte stattdessen dort stehen?** — die korrekte Version bzw. der Vorschlag.

5. **Begründung / Quelle** (optional, aber sehr hilfreich) — z. B. Schulbuch, BIFIE‑Aufgabenpool, kurze Herleitung.

6. **Screenshot** der betroffenen PDF‑Stelle — stark empfohlen.

### Gute vs. schlechte Meldung

**Nicht hilfreich:**
> „Im Kapitel Analysis stimmt was mit den Ableitungen nicht."

**Hilfreich:**
> Kapitel AN, Abschnitt 3.4 „Ableitungsregeln", Seite 42, Formel (3.4.2).
> Dort steht: \( (u \cdot v)' = u' \cdot v - u \cdot v' \)
> Korrekt wäre: \( (u \cdot v)' = u' \cdot v + u \cdot v' \)
> Das Minuszeichen ist ein Vorzeichenfehler (Produktregel).

---

## 2. Neues Feature / neuen Inhalt vorschlagen

Für **neue Inhalte** (fehlendes Thema, zusätzliches Beispiel, neue Grafik, neues Kapitel, didaktische Verbesserung) bitte einen Issue mit der Vorlage *„Neuer Inhalt / Feature"* anlegen.

Da neue Inhalte oft Zeit und Arbeit bedeuten, ist eine **präzise Beschreibung besonders wichtig** — nur so kann der Vorschlag umgesetzt oder diskutiert werden.

### Pflichtangaben

1. **Titel** im Format:
   `[Feature][<Kürzel>] <kurze Beschreibung>`
   Beispiele:
   - `[Feature][FA] Kapitel zu Exponentialfunktionen fehlt komplett`
   - `[Feature][AN] Beispiel zur Kurvendiskussion mit gebrochen-rationaler Funktion`

2. **Wo soll der Inhalt hin?**
   - Kapitel (AG / FA / AN / WS) oder „neues Kapitel"
   - Wenn möglich: in welchen Abschnitt / nach welcher Seite / neben welchem Thema

3. **Was genau soll enthalten sein?** — so detailliert wie möglich. Bitte mindestens folgende Punkte klären:
   - **Thema / Definition:** Welches mathematische Konzept?
   - **Formeln / Sätze:** Welche Gleichungen oder Regeln sollen explizit drin sein?
   - **Beispiele:** Mindestens ein durchgerechnetes Beispiel — Angabe + Lösungsweg + Ergebnis.
   - **Grafiken:** Welche Abbildungen oder Skizzen werden gebraucht? (Beschreibung genügt.)
   - **Umfang:** ca. wie viele Seiten oder Absätze?
   - **Schwierigkeitsgrad:** Grundkompetenz, vertiefend, Maturaniveau?

4. **Warum ist das sinnvoll?** — z. B. „kommt regelmäßig in Maturaaufgaben vor", „ist im Lehrplan enthalten", „wird bisher nur erwähnt, aber nicht erklärt".

5. **Quellen / Referenzen** (optional) — Schulbuch, BIFIE‑Aufgabenpool, Wikipedia, Link zur Maturaaufgabe …

### Beispiel für einen guten Feature‑Vorschlag

> **Titel:** `[Feature][FA] Abschnitt „Logarithmische Funktionen" fehlt`
>
> **Wo:** Kapitel FA, nach Abschnitt 2.5 „Exponentialfunktionen", als neuer Abschnitt 2.6.
>
> **Inhalt:**
> - **Definition** der Logarithmusfunktion \(f(x) = \log_a(x)\) als Umkehrfunktion der Exponentialfunktion.
> - **Eigenschaften:** Definitionsmenge, Wertemenge, Monotonie, Nullstelle bei \(x=1\), Verhalten für \(x \to 0\) und \(x \to \infty\).
> - **Rechenregeln:** Produkt‑, Quotienten‑, Potenzregel, Basiswechsel.
> - **Grafik:** Schaubild von \(\log_2(x)\), \(\ln(x)\), \(\log_{10}(x)\) im gleichen Koordinatensystem.
> - **Beispiel 1:** Gleichung \(\log_2(x+3) = 5\) lösen.
> - **Beispiel 2:** Anwendung — Halbwertszeit von Medikamenten im Blut.
> - **Umfang:** ca. 2 Seiten.
>
> **Warum:** Kommt bei der Matura regelmäßig im Kontext Wachstum/Zerfall vor und wird aktuell im Skriptum gar nicht behandelt.
>
> **Quellen:** BIFIE‑Aufgabenpool Frühjahr 2023, Aufgabe 4b.

---

## 3. Pull Requests (nur mit LaTeX‑Kenntnissen)

Wer die Änderung direkt einbauen möchte, ist herzlich eingeladen. Empfohlener Ablauf:

1. **Repository forken** und lokal klonen.
2. **Neuen Branch** anlegen, benannt nach Art und Bereich:
   - `fix/ag-kreisgleichung-vorzeichen`
   - `feat/fa-logarithmus-abschnitt`
   - `docs/readme-beitragshinweise`
3. Änderung umsetzen und **`main.tex` kompilieren**, um sicherzustellen, dass die PDF fehlerfrei baut.
4. **Commits** mit sprechenden Nachrichten schreiben. Empfohlenes Schema:
   - `fix(AG): Vorzeichenfehler in Produktregel korrigiert`
   - `feat(FA): Abschnitt Logarithmusfunktionen ergänzt`
   - `docs: Beitragshinweise in README ergänzt`
5. **Pull Request** öffnen. Der PR‑Titel soll demselben Schema folgen wie der Issue‑Titel, also:
   - `[Fehler][<Kürzel>] …` oder
   - `[Feature][<Kürzel>] …`

### Pflichtangaben im PR

- **Zusammenfassung:** Was wurde geändert und warum?
- **Bezug zu einem Issue:** `Closes #<Nummer>` (falls ein Issue existiert).
- **Art der Änderung:** Fehlerkorrektur / neuer Inhalt / Formatierung / Refactoring.
- **Betroffene Kapitel:** AG / FA / AN / WS / main / commands.
- **Checkliste:**
  - [ ] `main.tex` kompiliert ohne Fehler.
  - [ ] Keine neuen LaTeX‑Warnungen eingeführt (oder begründet).
  - [ ] Seitenzahlen / Querverweise wurden überprüft.
  - [ ] Rechtschreibung/Grammatik geprüft.
  - [ ] Falls neuer Inhalt: passend zum restlichen Stil (Farben, Umgebungen aus `commands.tex`).

### Stilregeln

- Deutsche Rechtschreibung, mathematische Begriffe in der an der AHS üblichen Schreibweise.
- Für wiederkehrende Umgebungen die **bestehenden Makros aus `commands.tex`** verwenden (Definitionen, Sätze, Beispiele, farbige Boxen) — keine parallelen neuen Konstrukte.
- Bilder als PNG oder selbstgezeichnet in **TikZ/pgfplots**.
- Ein Gedanke pro Commit, ein Thema pro Pull Request.

---

## Lizenz & Autor

© Nils Schlager. Das Skriptum entsteht im Rahmen von Nachhilfestunden und dient Schülerinnen und Schülern zur Vorbereitung auf die AHS‑Matura. Es erhebt keinen Anspruch auf Vollständigkeit.
