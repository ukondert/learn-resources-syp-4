# Praxis-Projekt: Agiles Anforderungsmanagement mit GitHub

**Projekt:** "Schul-Event-O-Mat"
**Tool:** GitHub (Projects, Issues, Labels)
**Fokus:** Requirement Engineering, Traceability, Versionsmanagement

---

## 1. Lernziele

In diesem Projekt lernt ihr, wie man Anforderungen an eine Software agil und nachvollziehbar mit GitHub-Tools verwaltet. Am Ende sollt ihr in der Lage sein:

*   Anforderungen (User Stories) als Issues strukturiert in GitHub zu erfassen.
*   Ein GitHub Project Board (Kanban) aufzusetzen, das den Entwicklungsprozess unterstützt.
*   Die **Rückverfolgbarkeit (Traceability)** von einer Anforderung (Issue) bis zum Testfall (Task-Liste) und zu Commits sicherzustellen.
*   Ein einfaches **Versionsmanagement für Anforderungen** direkt in GitHub umzusetzen.
*   Auf Änderungen und Testergebnisse im Projektverlauf zu reagieren.

---

## 2. Szenario

Wir arbeiten weiter am Projekt **"Schul-Event-O-Mat"**. Die erste Phase der Anforderungserhebung ist abgeschlossen. Anstatt die Anforderungen in einem statischen Dokument zu verwalten, entscheiden wir uns für einen agileren Ansatz mit GitHub. Dies ermöglicht es dem gesamten Team, den Status jeder Anforderung jederzeit nachzuvollziehen und direkt mit dem Code zu verknüpfen.

---

## 3. Schritt-für-Schritt-Anleitung

### Schritt 1: GitHub-Projekt aufsetzen

Erstellt ein neues GitHub Repository mit dem Namen "projekt-schul-event-o-mat". Geht dann zum Reiter "Projects" und erstellt ein neues Projekt, wählt das "Kanban"-Template aus. Benennt es "Projektboard". Passt die Spalten wie folgt an, bzw. erstellt eine neue Spalte:

1.  **Todo -> Anforderungen (Backlog)** Hier landen alle Anforderungen (Issues), die noch nicht in Arbeit sind. (Entspricht dem Backlog)
2.  **In Progress -> In Entwicklung:** Anforderungen, an denen gerade programmiert wird.
3.  **Done -> Im Test:** Anforderungen, die fertig entwickelt und bereit für die Qualitätssicherung sind.
4.  **Neue Spalte -> Erledigt**: Erfolgreich getestete und abgeschlossene Anforderungen. 

### Schritt 2: Start-Anforderungen erfassen (Version 1.0)

Geht zum "Issues"-Tab eures Repositorys. Erstellt für jede der folgenden Anforderungen ein eigenes Issue.

*   **FR-01:** Als Schüler möchte ich eine Liste aller zukünftigen Events sehen.
*   **FR-02:** Als Schüler möchte ich die Details eines Events einsehen können.
*   **FR-03:** Als Lehrer möchte ich mich anmelden können, um Events zu verwalten.
*   **FR-04:** Als Lehrer möchte ich neue Events erstellen können.
*   **FR-05:** Als Lehrer möchte ich von mir erstellte Events bearbeiten können.

**Struktur eines Anforderungs-Issues:**
*   **Titel:** Die ID und der Name der Anforderung (z.B. `FR-01: Event-Liste anzeigen`).
*   **Beschreibung (Body):** Die vollständige User Story ("Als Schüler möchte ich...") und die Priorität (z.B. **Priorität: Must-have**).
*   **Labels:** Erstellt und vergebt die Labels `Anforderung` und `Version 1.0` für alle diese Start-Anforderungen.
*   **Project:** Weist jedes Issue eurem "Projektboard" zu. Wählt zusätzlich den entsprechenden **Status** "`Anforderungen`" aus

### Schritt 3: Traceability zu Tests herstellen

Für jede Anforderung müssen wir sicherstellen, dass sie getestet wird. Wir lösen das über eine Task-Liste im Issue selbst.

**Aufgabe:** Bearbeitet jedes eurer 5 Issues. Fügt eine **Task-Liste** (Markdown-Checkliste) mit dem Titel `### Testfälle` hinzu. Erstellt pro Anforderung mindestens zwei fiktive Testfälle als Listeneinträge.

**Beispiel für FR-01:**
```markdown
### Testfälle
- [ ] `T-01.1`: App starten -> Event-Liste wird mit allen Events angezeigt.
- [ ] `T-01.2`: Wenn keine Events vorhanden sind -> Meldung "Keine Events gefunden" wird angezeigt.
```

### Schritt 4: Simulation – Ein Sprint beginnt

Simuliert nun den ersten Arbeitsdurchlauf (Sprint).

1.  Geht zu eurem "Projektboard".
2.  **Verschiebt** die Karten (Issues) `FR-01`, `FR-02` und `FR-03` von **"Anforderungen"** in die Spalte **"In Entwicklung"**.

### Schritt 5: Simulation – Testergebnisse und Änderungen

Jetzt kommt Feedback vom Test-Team und vom Kunden. Arbeitet die folgenden Ereignisse ab.

**Ereignis 1: Test schlägt fehl**
*   **Meldung:** Der Test `T-02.1` für die Anforderung `FR-02` ist fehlgeschlagen. Die Detailansicht zeigt die Beschreibung nicht an.
*   **Eure Aufgabe:**
    1.  Öffnet das Issue `FR-02`.
    2.  Hakt den erfolgreichen Testfall in der Task-Liste ab, lasst den fehlgeschlagenen aber offen.
    3.  Schreibt einen **Kommentar** im Issue: `@BenutzernameDesTesters: Fehler bei T-02.1 gemeldet. Beschreibung fehlt.`
    4.  Verschiebt die Karte `FR-02` auf dem Projektboard zurück in die Spalte **"In Entwicklung"**.

**Ereignis 2: Anforderung wird geändert (Versionsmanagement)**
*   **Meldung:** Der Kunde wünscht sich, dass die Bearbeiten-Funktion (`FR-05`) wichtiger wird. Die Priorität soll von "Should-have" auf "Must-have" geändert werden.
*   **Eure Aufgabe (So wird versioniert!):**
    1.  Findet das Issue `FR-05`.
    2.  **Schließt das alte Issue.** Schreibt einen letzten Kommentar: `Wird durch #IssueNummer ersetzt (Priorität geändert).` (Die neue Issue-Nummer wisst ihr erst im nächsten Schritt).
    3.  Erstellt ein **neues Issue** mit dem Titel `FR-05: Event bearbeiten`.
    4.  Kopiert die Beschreibung vom alten Issue und ändert die Priorität auf **Must-have**.
    5.  Fügt einen **Kommentar** hinzu, der die Änderung dokumentiert: `Änderung (V1.1): Priorität auf Kundenwunsch zu "Must-have" geändert. Ersetzt #AlteIssueNummer.`
    6.  Vergebt die Labels `Anforderung` und `Version 1.1`.
    7.  Fügt das neue Issue zum Projektboard hinzu.
    8.  Geht zurück zum alten, geschlossenen Issue und tragt die korrekte neue Issue-Nummer im Kommentar ein.

**Ereignis 3: Neue Anforderung kommt hinzu**
*   **Meldung:** Der Kunde wünscht sich eine neue Funktion: Events nach Kategorien filtern.
*   **Eure Aufgabe:**
    1.  Erstellt ein neues Issue `FR-06: Events filtern`.
    2.  Formuliert eine passende User Story und setzt die Priorität auf **Could-have**.
    3.  Vergebt die Labels `Anforderung` und `Version 1.1`.
    4.  Fügt eine Task-Liste mit mindestens einem Testfall hinzu.
    5.  Fügt das Issue zum Projektboard hinzu.

---

## 4. Abgabekriterien

*   Ein funktionierendes GitHub Repository mit Projektboard und Issues, das alle oben genannten Schritte widerspiegelt.
*   Alle Anforderungen (inkl. der neuen und geänderten) sind als Issues korrekt erfasst.
*   Die Traceability zu den Testfällen ist in jedem Issue ersichtlich.
*   Die Versionierung von `FR-05` wurde korrekt durchgeführt (altes Issue geschlossen und verlinkt, neues Issue erstellt).
*   Macht Screenshots von eurem Projektboard und den relevanten Issues (vorher/nachher bei Änderungen), fügt diese in ein Markdown-Dokument ein und gebt es als PDF ab.

### Abgabe

*   Macht Screenshots von dem Board und den einzelnen Issues, fügt diese alle in ein Markdown-Dokument, wobei jeder Screenshot eine passende Überschrift haben soll (z.B. `Trello Board mit Startanforderungen` -> Screenshot von Trello Board, `Ereignis 1 - Test schlägt fehlt` -> Screenshots von `Karte FR-01` und dem Trello Board selbst)
    *   Die Abgabe des Dokuments selbst soll als PDF-Dokument erfolgen.