# Übung: Anforderungs-Vertiefung "Schul-Event-O-Mat"

**Lernziele:**
*   Anforderungen mittels MoSCoW-Methode priorisieren.
*   Anforderungen mit dem Kano-Modell klassifizieren und bewerten.
*   Die Rückverfolgbarkeit (Traceability) von Anforderungen zu Use Cases herstellen.
*   Konkrete Akzeptanzkriterien für eine User Story formulieren.

**Ausgangssituation:**
Sie arbeiten weiterhin am Projekt "Schul-Event-O-Mat". Die erste Anforderungsanalyse ist abgeschlossen. Die folgende Liste von Anforderungen (eine Mischung aus funktionalen und nicht-funktionalen) und Use Cases wurde bereits erarbeitet.

**Anforderungsliste:**
*   **FR-01:** Als Schüler möchte ich eine Liste aller zukünftigen Events sehen.
*   **FR-02:** Als Schüler möchte ich die Details eines Events einsehen können.
*   **FR-03:** Als Lehrer möchte ich mich anmelden können, um Events zu verwalten.
*   **FR-04:** Als Lehrer möchte ich neue Events erstellen können.
*   **FR-05:** Als Lehrer möchte ich von mir erstellte Events bearbeiten können.
*   **FR-06:** Als Lehrer möchte ich von mir erstellte Events löschen können.
*   **FR-07:** Als Schüler möchte ich Events nach Kategorien filtern (z.B. Sport, Musik, Info).
*   **FR-08:** Als Schüler möchte ich eine Push-Benachrichtigung für neue Events erhalten.
*   **FR-09:** Als Lehrer möchte ich eine Teilnehmerliste für mein Event sehen.
*   **NFR-01:** Die App muss auf Android und iOS laufen.
*   **NFR-02:** Die App muss auch ohne Internetverbindung die bereits geladenen Events anzeigen (Offline-Fähigkeit).
*   **NFR-03:** Das Design soll modern und ansprechend sein.

**Use-Case-Liste:**
*   **UC-01:** Event-Liste anzeigen
*   **UC-02:** Event-Details anzeigen
*   **UC-03:** Neues Event erstellen
*   **UC-04:** Event bearbeiten
*   **UC-05:** Event löschen
*   **UC-06:** Benutzer anmelden

---

## Aufgaben

### 1. Priorisierung mit der MoSCoW-Methode
Priorisieren Sie die oben genannten **funktionalen Anforderungen (FR-01 bis FR-09)**. Ordnen Sie jede Anforderung einer der vier Kategorien zu:
*   **M**ust-have
*   **S**hould-have
*   **C**ould-have
*   **W**on't-have (für dieses Release)

**Ihre Aufgabe:** Erstellen Sie eine Tabelle und begründen Sie kurz Ihre Entscheidung für die jeweilige Kategorie.

### 2. Analyse mit dem Kano-Modell
Analysieren Sie dieselben **funktionalen Anforderungen (FR-01 bis FR-09)** aus Sicht des Kano-Modells.
*   Welche Anforderungen sind **Basis-Merkmale**?
*   Welche sind **Leistungs-Merkmale**?
*   Welche sind **Begeisterungs-Merkmale**?
*   Gibt es **unerhebliche Merkmale**?

**Ihre Aufgabe:** Ordnen Sie jede Anforderung einer Kano-Kategorie zu und begründen Sie Ihre Wahl.

### 3. Traceability Matrix
Die Rückverfolgbarkeit stellt sicher, dass jede Anforderung durch einen oder mehrere Use Cases abgedeckt wird.

**Ihre Aufgabe:** Erstellen Sie eine Traceability Matrix (Rückverfolgbarkeitsmatrix).
*   Die Zeilen repräsentieren die **Anforderungen (FR-01 bis FR-06)**.
*   Die Spalten repräsentieren die **Use Cases (UC-01 bis UC-06)**.
*   Markieren Sie mit einem "X" in der Zelle, welcher Use Case welche Anforderung umsetzt.

### 4. Akzeptanzkriterien formulieren
Wählen Sie die folgende User Story aus:
> **FR-04:** Als Lehrer möchte ich neue Events erstellen können.

**Ihre Aufgabe:** Formulieren Sie mindestens **fünf** konkrete Akzeptanzkriterien für diese User Story. Nutzen Sie das "Gegeben-Wenn-Dann"-Format (Given-When-Then).

**Beispiel für ein Akzeptanzkriterium:**
*   **Gegeben** der Lehrer ist auf der "Neues Event"-Seite,
*   **Wenn** er alle Pflichtfelder korrekt ausfüllt und auf "Speichern" klickt,
*   **Dann** wird das Event erstellt und in der Event-Liste angezeigt.
