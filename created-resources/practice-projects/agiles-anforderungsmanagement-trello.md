# Praxis-Projekt: Agiles Anforderungsmanagement mit Trello

**Projekt:** "Schul-Event-O-Mat"
**Tool:** Trello
**Fokus:** Requirement Engineering, Traceability, Versionsmanagement

---

## 1. Lernziele

In diesem Projekt lernt ihr, wie man Anforderungen an eine Software agil und nachvollziehbar mit einem Kanban-Board (Trello) verwaltet. Am Ende sollt ihr in der Lage sein:

*   Anforderungen (User Stories) strukturiert in Trello zu erfassen.
*   Ein Trello-Board so aufzusetzen, dass es den Entwicklungsprozess unterstützt.
*   Die **Rückverfolgbarkeit (Traceability)** von einer Anforderung bis zum Testfall sicherzustellen.
*   Ein einfaches **Versionsmanagement für Anforderungen** direkt in Trello umzusetzen.
*   Auf Änderungen und Testergebnisse im Projektverlauf zu reagieren.

---

## 2. Szenario

Wir arbeiten weiter am Projekt **"Schul-Event-O-Mat"**. Die erste Phase der Anforderungserhebung ist abgeschlossen. Anstatt die Anforderungen in einem statischen Word-Dokument zu verwalten, entscheiden wir uns für einen agileren Ansatz mit Trello. Dies ermöglicht es dem gesamten Team (Entwickler, Tester, Product Owner), den Status jeder Anforderung jederzeit einzusehen.

---

## 3. Schritt-für-Schritt-Anleitung

### Schritt 1: Trello-Board aufsetzen

Erstellt ein neues Trello-Board mit dem Namen "Projekt: Schul-Event-O-Mat". Richtet die folgenden Listen (Spalten) ein:

1.  **Anforderungskatalog (Backlog):** Hier landen alle Anforderungen, die noch nicht in Arbeit sind.
2.  **In Entwicklung:** Anforderungen, an denen gerade programmiert wird.
3.  **Im Test:** Anforderungen, die fertig entwickelt und bereit für die Qualitätssicherung sind.
4.  **Erledigt:** Erfolgreich getestete und abgeschlossene Anforderungen.
5.  **Archiv (Veraltet):** Hier werden alte Versionen von Anforderungen abgelegt.

### Schritt 2: Start-Anforderungen erfassen (Version 1.0)

Erstellt für jede der folgenden Anforderungen eine eigene Karte in der Liste **"Anforderungskatalog (Backlog)"**.

*   **FR-01:** Als Schüler möchte ich eine Liste aller zukünftigen Events sehen.
*   **FR-02:** Als Schüler möchte ich die Details eines Events einsehen können.
*   **FR-03:** Als Lehrer möchte ich mich anmelden können, um Events zu verwalten.
*   **FR-04:** Als Lehrer möchte ich neue Events erstellen können.
*   **FR-05:** Als Lehrer möchte ich von mir erstellte Events bearbeiten können.

**Struktur einer Anforderungs-Karte:**
*   **Titel:** Die ID und der Name der Anforderung (z.B. `FR-01: Event-Liste anzeigen`).
*   **Beschreibung:** Die vollständige User Story ("Als Schüler möchte ich...") und die Priorität (z.B. **Priorität: Must-have**).
*   **Labels:** Erstellt und vergebt ein Label `Version 1.0` für alle diese Start-Anforderungen.

### Schritt 3: Traceability zu Tests herstellen

Für jede Anforderung müssen wir sicherstellen, dass sie getestet wird. Wir lösen das über eine Checkliste.

**Aufgabe:** Fügt zu jeder eurer 5 Anforderungs-Karten eine **Checkliste** mit dem Namen `Testfälle` hinzu. Erstellt pro Anforderung mindestens zwei fiktive Testfälle als Checklisteneinträge.

**Beispiel für FR-01:**
*   Checklisten-Eintrag 1: `T-01.1: App starten -> Event-Liste wird mit allen Events angezeigt.`
*   Checklisten-Eintrag 2: `T-01.2: Wenn keine Events vorhanden sind -> Meldung "Keine Events gefunden" wird angezeigt.`

### Schritt 4: Simulation – Ein Sprint beginnt

Simuliert nun den ersten Arbeitsdurchlauf (Sprint).

1.  **Verschiebt** die Karten `FR-01`, `FR-02` und `FR-03` von "Anforderungskatalog (Backlog)" in die Liste **"In Entwicklung"**.
2.  Kurze Zeit später sind sie fertig entwickelt. Verschiebt dieselben drei Karten in die Liste **"Im Test"**.

### Schritt 5: Simulation – Testergebnisse und Änderungen

Jetzt kommt Feedback vom Test-Team und vom Kunden. Arbeitet die folgenden Ereignisse ab.

**Ereignis 1: Test schlägt fehl**
*   **Meldung:** Der Test `T-02.1` für die Anforderung `FR-02` ist fehlgeschlagen. Die Detailansicht zeigt die Beschreibung nicht an.
*   **Eure Aufgabe:**
    1.  Öffnet die Karte `FR-02`.
    2.  Hakt den erfolgreichen Testfall ab, lasst den fehlgeschlagenen aber offen.
    3.  Schreibt einen **Kommentar** auf die Karte: `@Test-Team: Fehler bei T-02.1 gemeldet. Beschreibung fehlt.`
    4.  Verschiebt die Karte `FR-02` zurück in die Liste **"In Entwicklung"**.

**Ereignis 2: Anforderung wird geändert (Versionsmanagement)**
*   **Meldung:** Der Kunde wünscht sich, dass die Bearbeiten-Funktion (`FR-05`) wichtiger wird. Die Priorität soll von "Should-have" auf "Must-have" geändert werden.
*   **Eure Aufgabe (So wird versioniert!):**
    1.  Findet die Karte `FR-05 (Version 1.0)`.
    2.  **Kopiert** die Karte. Der Name der Kopie lautet `FR-05: Event bearbeiten`.
    3.  Verschiebt die **originale Karte** `FR-05` in die Liste **"Archiv (Veraltet)"**.
    4.  Öffnet die **neue, kopierte Karte** und führt die Änderungen durch:
        *   Ändert die Priorität in der Beschreibung auf **Must-have**.
        *   Erstellt ein neues Label `Version 1.1` und weist es der Karte zu. Entfernt das `Version 1.0` Label.
        *   Fügt einen **Kommentar** hinzu, der die Änderung dokumentiert: `Änderung (V1.1): Priorität auf Kundenwunsch zu "Must-have" geändert.`

**Ereignis 3: Neue Anforderung kommt hinzu**
*   **Meldung:** Der Kunde wünscht sich eine neue Funktion: Events nach Kategorien filtern.
*   **Eure Aufgabe:**
    1.  Erstellt eine neue Karte `FR-06: Events filtern` im **"Anforderungskatalog (Backlog)"**.
    2.  Formuliert eine passende User Story und setzt die Priorität auf **Could-have**.
    3.  Vergebt das Label `Version 1.1`.
    4.  Fügt eine Checkliste mit mindestens einem Testfall hinzu.

---

## 4. Abgabekriterien

*   Ein funktionierendes Trello-Board, das alle oben genannten Schritte widerspiegelt.
*   Alle Anforderungen (inkl. der neuen und geänderten) sind korrekt erfasst.
*   Die Traceability zu den Testfällen ist auf jeder Karte ersichtlich.
*   Die Versionierung von `FR-05` wurde korrekt durchgeführt (alte Karte im Archiv, neue Karte mit Kommentar und Label).

### Abgabe   

*   Macht Screenshots von den einzelnen Listen, fügt diese alle in ein Markdown-Dokument, wobei jeder Screenshot eine passende Überschrift haben soll (z.B. `Trello Board mit Startanforderungen` -> Screenshot von Trello Board, `Ereignis 1 - Test schlägt fehlt` -> Screenshots von `Karte FR-01` und dem Trello Board selbst)
    *   Die Abgabe des Dokuments selbst soll als PDF-Dokument erfolgen.
