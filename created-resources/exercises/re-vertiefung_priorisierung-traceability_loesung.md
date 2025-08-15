# Lösungsvorschlag: Anforderungs-Vertiefung "Schul-Event-O-Mat"

---

## 1. Priorisierung mit der MoSCoW-Methode (Beispiellösung)

| Anforderung | Kategorie | Begründung                                                              |
| :---------- | :-------- | :---------------------------------------------------------------------- |
| **FR-01**   | **M**ust  | Ohne Event-Liste ist die App nutzlos. Kernfunktion.                     |
| **FR-02**   | **M**ust  | Nur Titel reicht nicht, Details sind essenziell.                        |
| **FR-03**   | **M**ust  | Ohne Login für Lehrer können keine Events erstellt werden.              |
| **FR-04**   | **M**ust  | Ohne diese Funktion gibt es keine Events in der App.                    |
| **FR-05**   | **S**hould| Wichtig für die Datenqualität, aber zur Not könnte man löschen & neu erstellen. |
| **FR-06**   | **S**hould| Wichtig, aber weniger kritisch als das Erstellen.                       |
| **FR-07**   | **C**ould | "Nice-to-have" für eine bessere Übersicht bei vielen Events.            |
| **FR-08**   | **C**ould | Begeistert die Nutzer, ist aber für die Kernfunktion nicht notwendig.   |
| **FR-09**   | **W**on't | Komplex in der Umsetzung (DSGVO, etc.), wird auf ein späteres Release verschoben. |

---

## 2. Analyse mit dem Kano-Modell (Beispiellösung)

| Anforderung | Kano-Kategorie | Begründung                                                              |
| :---------- | :------------- | :---------------------------------------------------------------------- |
| **FR-01**   | **Basis**      | Wird vom Nutzer als selbstverständlich erwartet. Fehlt es, ist er unzufrieden. |
| **FR-02**   | **Basis**      | Gehört zur Grundfunktionalität einer Event-App.                         |
| **FR-03**   | **Basis**      | Standard für geschützte Bereiche.                                       |
| **FR-04**   | **Basis**      | Die App wäre ohne diese Funktion sinnlos.                               |
| **FR-05**   | **Leistung**   | Je besser die Bearbeitung funktioniert, desto zufriedener der Lehrer.   |
| **FR-06**   | **Leistung**   | Eine einfache Löschfunktion erhöht die Zufriedenheit.                   |
| **FR-07**   | **Leistung**   | Je besser die Filter, desto zufriedener der Nutzer bei der Suche.       |
| **FR-08**   | **Begeisterung**| Unerwartet, aber sehr nützlich. Schafft einen "Wow"-Effekt.             |
| **FR-09**   | **Begeisterung**| Sehr nützlich für Lehrer, wird aber initial nicht erwartet.             |

---

## 3. Traceability Matrix

| Anforderung | UC-01 (Liste) | UC-02 (Details) | UC-03 (Erstellen) | UC-04 (Bearbeiten) | UC-05 (Löschen) | UC-06 (Login) |
| :---------- | :-----------: | :-------------: | :---------------: | :----------------: | :-------------: | :-----------: |
| **FR-01**   |       X       |                 |                   |                    |                 |               |
| **FR-02**   |               |        X        |                   |                    |                 |               |
| **FR-03**   |               |                 |                   |                    |                 |       X       |
| **FR-04**   |               |                 |         X         |                    |                 |               |
| **FR-05**   |               |                 |                   |         X          |                 |               |
| **FR-06**   |               |                 |                   |                    |        X        |               |

---

## 4. Akzeptanzkriterien für FR-04 (Beispiellösung)

**User Story:** Als Lehrer möchte ich neue Events erstellen können.

*   **AC-1: Erfolgreiches Erstellen**
    *   **Gegeben** der Lehrer ist im "Neues Event"-Formular,
    *   **Wenn** er alle Pflichtfelder (Titel, Datum, Ort) ausfüllt und auf "Speichern" klickt,
    *   **Dann** wird das Event in der Datenbank gespeichert und der Lehrer wird zur Event-Liste weitergeleitet, wo das neue Event sichtbar ist.

*   **AC-2: Fehlende Pflichtfelder**
    *   **Gegeben** der Lehrer ist im "Neues Event"-Formular,
    *   **Wenn** er auf "Speichern" klickt, aber das "Titel"-Feld leer lässt,
    *   **Dann** wird das Event nicht gespeichert, das Titelfeld wird rot markiert und eine Fehlermeldung "Bitte geben Sie einen Titel an." erscheint.

*   **AC-3: Ungültiges Datum**
    *   **Gegeben** der Lehrer ist im "Neues Event"-Formular,
    *   **Wenn** er ein Datum in der Vergangenheit auswählt und auf "Speichern" klickt,
    *   **Dann** wird das Event nicht gespeichert und eine Fehlermeldung "Das Datum darf nicht in der Vergangenheit liegen." wird angezeigt.

*   **AC-4: Abbrechen-Button**
    *   **Gegeben** der Lehrer befindet sich im "Neues Event"-Formular,
    *   **Wenn** er auf den "Abbrechen"-Button klickt,
    *   **Dann** werden alle Eingaben verworfen und er wird zur Event-Liste zurückgeleitet.

*   **AC-5: Zeichenbegrenzung Beschreibung**
    *   **Gegeben** der Lehrer ist im "Neues Event"-Formular,
    *   **Wenn** er mehr als 500 Zeichen in das Beschreibungsfeld eingibt,
    *   **Dann** wird die weitere Eingabe blockiert und ein Zähler zeigt "500/500" an.
