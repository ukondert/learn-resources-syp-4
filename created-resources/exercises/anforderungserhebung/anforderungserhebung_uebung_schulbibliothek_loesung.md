# Lösungsvorschlag: Übung zur Anforderungserhebung für eine digitale Schulbibliothek

Dies ist ein detaillierter Lösungsvorschlag für die Übungsaufgabe "Anforderungserhebung für eine digitale Schulbibliothek". Die Ausarbeitung folgt der Struktur der Aufgabenstellung und berücksichtigt die Inhalte aus dem Lernskript "3.2. Methoden der Anforderungserhebung und -beschreibung".

---

### **1. Stakeholder identifizieren und Erhebungsmethoden auswählen**

**Identifizierte Stakeholder-Gruppen:**

1.  **Schüler:** Die Hauptnutzergruppe der Bibliothek. Sie leihen Bücher aus, bringen sie zurück und suchen nach Literatur.
2.  **Lehrer:** Nutzen die Bibliothek für Unterrichtsmaterialien, eigene Recherche und empfehlen Bücher an Schüler. Sie haben möglicherweise andere Anforderungen als Schüler (z.B. längere Leihfristen, Vormerkung für Klassensätze).
3.  **Bibliothekar:** Die Person, die die Bibliothek verwaltet. Er/Sie ist der "Power-User" der zukünftigen Admin-App und kennt die aktuellen Prozesse, Probleme und Engpässe am besten.
4.  **Schulleitung:** Trägt die finanzielle und organisatorische Verantwortung. Sie ist an Effizienz, geringen Kosten und dem positiven Image der Schule interessiert.

**Ausgewählte Erhebungstechniken und ihre Begründung:**

Für eine umfassende Anforderungserhebung werden alle drei im Skript vorgestellten Techniken kombiniert, da sie unterschiedliche Stärken haben und sich gegenseitig ergänzen.

1.  **Interview (mit dem Bibliothekar):**
    *   **Begründung:** Der Bibliothekar besitzt tiefes Expertenwissen über den aktuellen, manuellen Prozess. Ein Interview ist die beste Methode, um dieses Detailwissen zu erlangen, implizite Arbeitsschritte aufzudecken und die größten "Schmerzpunkte" im täglichen Betrieb zu verstehen.
    *   **Erhoffte Informationen:** Detaillierte Beschreibung des Ist-Zustands, häufige Probleme (z.B. bei der Rückgabe), versteckte Workarounds, Wünsche für die Automatisierung und Vereinfachung der Verwaltung.

2.  **Workshop (mit einer gemischten Gruppe aus Schülern, Lehrern und dem Bibliothekar):**
    *   **Begründung:** Ein Workshop bringt die unterschiedlichen Perspektiven an einen Tisch. Konfligierende Anforderungen (z.B. Schüler wünschen lange Leihfristen, Bibliothekar will schnelle Verfügbarkeit) können direkt diskutiert und ein Konsens gefunden werden. Die Gruppendynamik fördert zudem Kreativität für neue Funktionen.
    *   **Erhoffte Informationen:** Gemeinsam erarbeitete und priorisierte Liste von Kernfunktionen, innovative Ideen, Lösung von Zielkonflikten und ein gemeinsames Verständnis für das Projekt.

3.  **Fragebogen/Umfrage (an alle Schüler und Lehrer):**
    *   **Begründung:** Um eine breite Datenbasis zu erhalten und die Meinungen der "stillen Mehrheit" einzufangen, ist eine Umfrage ideal. Sie liefert quantitative Daten, die helfen, die im Workshop oder Interview gewonnenen qualitativen Annahmen zu validieren.
    *   **Erhoffte Informationen:** Statistische Daten zur aktuellen Bibliotheksnutzung (Wie oft? Welche Art von Büchern?), Bewertung der Wichtigkeit potenzieller Funktionen (z.B. "Wie wichtig ist eine Online-Verlängerungsfunktion?"), allgemeine Zufriedenheit.

---

### **2. Detaillierte Ausarbeitung der Erhebungstechniken**

#### **Ausarbeitung der Technik: Interview**

*   **Vorbereitung:**
    *   **Zielsetzung:** Das Hauptziel ist das vollständige Verständnis des aktuellen Ausleih- und Rückgabeprozesses inklusive aller Probleme und manuellen Notlösungen. Am Ende des Interviews sollen die Kernanforderungen für die Admin-App aus Sicht des Bibliothekars klar sein.
    *   **Organisation:**
        *   **Wen:** Der zuständige Bibliothekar der Schule.
        *   **Wo:** Direkt in der Schulbibliothek, um die Arbeitsumgebung und die aktuellen Werkzeuge (Listen, etc.) direkt vor Augen zu haben.
        *   **Wie lange:** 60 Minuten, um genügend Zeit für tiefgehende Fragen zu haben.
        *   **Aufzeichnung:** Es wird um Erlaubnis für eine Audio-Aufzeichnung gebeten, um sich voll auf das Gespräch konzentrieren zu können und die spätere Protokollierung zu erleichtern.

*   **Durchführung (Leitfaden mit offenen Fragen):**
    1.  "Können Sie mich durch einen typischen Ausleihvorgang führen, von dem Moment, an dem ein Schüler mit einem Buch zu Ihnen kommt, bis der Vorgang abgeschlossen ist?"
    2.  "Welche Schritte sind am zeitaufwendigsten oder fehleranfälligsten im gesamten Prozess der Bibliotheksverwaltung?"
    3.  "> **Interviewer:** "Erzählen Sie mir von einer Situation, wo das aktuelle System an seine Grenzen gestoßen ist."
>
> **Frau Müller:** "Letztes Jahr vor den Sommerferien war Chaos. Viele Schüler haben ihre Bücher noch nicht zurückgegeben, aber ich wusste nicht mehr genau, wer was hat und seit wann. Meine Excel-Dateien waren völlig durcheinander – teilweise hatte ich doppelte Einträge, teilweise fehlten welche. Dann ist auch noch mein Computer abgestürzt und ich hatte kein aktuelles Backup. Ich musste alles aus dem Gedächtnis und anhand der physischen Bücher rekonstruieren. Am Ende haben wir Rundmails an alle Schüler geschickt und gehofft, dass sie ihre Bücher vorbeibringen. Das war sehr unprofessionell." Was ist passiert und wie haben Sie das Problem gelöst?"
    4.  "Wenn Sie eine 'Wunschfee' für eine neue Software hätten: Welche drei Aufgaben würden Sie ihr als Erstes geben, um Ihren Arbeitsalltag zu erleichtern?"
    5.  "Gibt es spezielle Regeln oder Ausnahmen (z.B. für Lehrer, Ferienzeiten, Vormerkungen), die wir bei der Digitalisierung unbedingt berücksichtigen müssen?"

*   **Nachbereitung:**
    *   **Protokollierung:** Unmittelbar nach dem Interview werden die Notizen und die Audio-Aufzeichnung zu einem sauberen Gesprächsprotokoll zusammengefasst. Dieses Protokoll wird dem Bibliothekar zur Überprüfung und Bestätigung zugesandt.
    *   **Analyse:** Aus dem Protokoll werden die wichtigsten Erkenntnisse extrahiert und in einer ersten Liste von Anforderungen (z.B. als User Stories oder Stichpunkte) für die Admin-App formuliert.

#### **Ausarbeitung der Technik: Workshop**

*   **Vorbereitung:**
    *   **Ziel:** Das Ziel des Workshops ist es, eine priorisierte Liste der Top 5-7 Funktionen für die Schüler- & Lehrer-App zu erstellen und ein gemeinsames Verständnis für das "Minimum Viable Product" (MVP) zu schaffen.
    *   **Teilnehmerkreis:** 1 Bibliothekar, 2 Schüler (verschiedene Altersstufen), 1 Lehrer, 1 Moderator (vom Projektteam), 1 Protokollant.
    *   **Rollen:** Der Moderator leitet den Workshop, achtet auf die Zeit und sorgt für eine konstruktive Atmosphäre. Der Protokollant dokumentiert die Ergebnisse sichtbar für alle auf einem Whiteboard oder Flipchart.

*   **Durchführung (Agenda für 45 Minuten):**
    *   **(5 Min) Phase 1: Eröffnung & Zielsetzung**
        *   Begrüßung, Vorstellungsrunde.
        *   Moderator erklärt das Ziel: "Heute wollen wir gemeinsam die wichtigsten Funktionen für die neue Bibliotheks-App finden."
        *   Vorstellung der Agenda und der Spielregeln (z.B. "Jede Idee ist willkommen").
    *   **(10 Min) Phase 2: Ideen sammeln (Brainstorming)**
        *   Moderator stellt die Frage: "Was sollte die neue App können, um euch das Leben leichter zu machen?"
        *   Alle Teilnehmer schreiben ihre Ideen auf Moderationskarten (eine Idee pro Karte).
    *   **(10 Min) Phase 3: Ideen gruppieren (Clustering)**
        *   Die Karten werden an ein Whiteboard gehängt.
        *   Die Teilnehmer gruppieren gemeinsam thematisch ähnliche Karten (z.B. alles zum Thema "Suchen", "Verlängern", "Erinnern").
    *   **(10 Min) Phase 4: Priorisieren (Dot-Voting)**
        *   Jeder Teilnehmer erhält 3 Klebepunkte.
        *   Die Teilnehmer verteilen ihre Punkte auf die für sie wichtigsten Funktionsgruppen. Sie können alle Punkte auf eine Gruppe kleben oder sie verteilen.
    *   **(5 Min) Phase 5: Abschluss & nächste Schritte**
        *   Moderator fasst die Ergebnisse zusammen (die Gruppen mit den meisten Punkten sind die wichtigsten).
        *   Kurze Erläuterung, wie diese Ergebnisse in die weitere Entwicklung einfließen.
        *   Dank an alle Teilnehmer.

*   **Nachbereitung:**
    *   **Dokumentation:** Der Protokollant fotografiert das Whiteboard mit den priorisierten Funktionsgruppen. Die Ergebnisse werden in einem kurzen Ergebnisprotokoll zusammengefasst und an alle Teilnehmer verschickt.
    *   **Umsetzung:** Die priorisierte Liste dient dem Product Owner als Grundlage für die Erstellung und Priorisierung des Product Backlogs.

#### **Ausarbeitung der Technik: Fragebogen**

*   **Vorbereitung:**
    *   **Ziel:** Das Ziel der Umfrage ist es, quantitative Daten über die Nutzungsgewohnheiten und die Wichtigkeit von potenziellen App-Funktionen von einer großen Anzahl an Schülern und Lehrern zu erhalten.

*   **Durchführung (Entwurf einer Online-Umfrage):**
    *   **Tool:** Ein Online-Umfragetool wie Google Forms oder Microsoft Forms.
    *   **Fragen:**
        1.  **Rolle (Geschlossene Frage, Single-Choice):** "Ich bin: ( ) Schüler/in ( ) Lehrer/in"
        2.  **Nutzungshäufigkeit (Geschlossene Frage, Skala):** "Wie oft leihst du/leihen Sie im Durchschnitt Bücher aus der Schulbibliothek aus?"
            *   ( ) Mehrmals pro Woche
            *   ( ) Etwa einmal pro Woche
            *   ( ) Etwa einmal im Monat
            *   ( ) Seltener als einmal im Monat
            *   ( ) Nie
        3.  **Funktions-Wichtigkeit (Skalenfrage, Matrix):** "Bitte bewerten Sie, wie wichtig Ihnen die folgenden Funktionen für eine neue Bibliotheks-App wären (1 = unwichtig, 5 = sehr wichtig):"
            *   Verfügbarkeit eines Buches prüfen
            *   Bücher online verlängern
            *   Bücher online vormerken/reservieren
            *   Erinnerung vor Ablauf der Leihfrist erhalten
            *   Buchempfehlungen erhalten
        4.  **Offene Frage:** "Welche eine Funktion, die hier nicht genannt wurde, würden Sie sich am meisten wünschen?"

*   **Nachbereitung:**
    *   **Auswertung:** Die Antworten der geschlossenen Fragen werden statistisch ausgewertet (z.B. "75% der Schüler bewerten die Erinnerungsfunktion als 'sehr wichtig'"). Die Ergebnisse werden in Diagrammen visualisiert. Die Antworten der offenen Frage werden kategorisiert, um neue, unerwartete Anforderungen zu identifizieren.
    *   **Interpretation:** Die Ergebnisse helfen, die im Workshop priorisierten Features zu validieren und datengestützte Entscheidungen für den Entwicklungsprozess zu treffen.

---

### **3. Anforderungen als User Stories formulieren**

Hier sind 5 User Stories, ausgearbeitet nach dem 3-C-Modell:

**User Story 1**
*   **Card:** `Als Schüler möchte ich online nach Büchern suchen können, um schnell herauszufinden, ob ein bestimmtes Buch in der Bibliothek verfügbar ist.`
*   **Conversation (Diskussionspunkte):**
    *   Nach welchen Kriterien soll gesucht werden können (Titel, Autor, ISBN, Schlagwort)?
    *   Was wird in den Suchergebnissen angezeigt (Titel, Autor, Standort, Verfügbarkeitsstatus)?
    *   Soll es eine Autovervollständigung bei der Eingabe geben?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Wenn ich einen Buchtitel eingebe, sehe ich eine Liste passender Bücher.
    2.  Für jedes Buch in der Liste wird mir angezeigt, ob es "Verfügbar" oder "Ausgeliehen" ist.
    3.  Wenn keine Treffer gefunden wurden, erhalte ich eine freundliche "Nichts gefunden"-Meldung.

**User Story 2**
*   **Card:** `Als Schüler möchte ich eine Erinnerung per Push-Nachricht erhalten, bevor meine Leihfrist abläuft, um Strafgebühren zu vermeiden.`
*   **Conversation (Diskussionspunkte):**
    *   Wie viele Tage vor Ablauf soll die Erinnerung gesendet werden (z.B. 3 Tage vorher)?
    *   Was passiert, wenn die App keine Internetverbindung hat?
    *   Soll der Nutzer das Intervall selbst einstellen können?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Drei Tage vor Ablauf der Leihfrist erhalte ich eine Push-Nachricht auf meinem Handy.
    2.  Die Nachricht enthält den Titel des Buches und das genaue Rückgabedatum.
    3.  Wenn ich auf die Benachrichtigung tippe, öffnet sich die App direkt auf der Seite "Meine Ausleihen".

**User Story 3**
*   **Card:** `Als Lehrer möchte ich ein ausgeliehenes Buch direkt in der App verlängern können, um Zeit zu sparen und nicht extra in die Bibliothek gehen zu müssen.`
*   **Conversation (Diskussionspunkte):**
    *   Wie oft darf ein Buch verlängert werden?
    *   Kann ein Buch verlängert werden, wenn es bereits von jemand anderem vorbestellt wurde?
    *   Welches Feedback erhält der Nutzer nach der Verlängerung (Erfolg, Fehler)?
*   **Confirmation (Akzeptanzkriterien):**
    1.  In meiner Liste der ausgeliehenen Bücher gibt es einen "Verlängern"-Button.
    2.  Wenn ich den Button drücke und eine Verlängerung möglich ist, wird das neue Rückgabedatum angezeigt und ich erhalte eine Erfolgsmeldung.
    3.  Wenn eine Verlängerung nicht möglich ist (z.B. weil das Buch vorbestellt ist), wird der Button nicht angezeigt oder ist deaktiviert und ich erhalte eine erklärende Meldung.

**User Story 4**
*   **Card:** `Als Bibliothekar möchte ich mit der Kamera meines Tablets den Barcode eines Buches scannen können, um den Ausleih- oder Rückgabeprozess zu beschleunigen.`
*   **Conversation (Diskussionspunkte):**
    *   Welche Barcode-Typen müssen unterstützt werden?
    *   Was passiert, wenn ein Barcode nicht lesbar ist? Gibt es eine manuelle Eingabemöglichkeit?
    *   Wie wird der Schüler zugeordnet? (Scan eines Schülerausweises?)
*   **Confirmation (Akzeptanzkriterien):**
    1.  Wenn ich auf "Ausleihe starten" tippe, aktiviert sich die Kamera.
    2.  Wenn ich die Kamera auf den Buch-Barcode richte, wird das Buch sofort erkannt und in der Maske angezeigt.
    3.  Nach dem Scannen des Schülerausweises wird die Ausleihe mit einem Klick dem korrekten Schüler zugeordnet.

**User Story 5**
*   **Card:** `Als Schüler möchte ich ein Buch, das gerade ausgeliehen ist, vormerken können, um benachrichtigt zu werden, sobald es verfügbar ist.`
*   **Conversation (Diskussionspunkte):**
    *   Wie viele Bücher darf man gleichzeitig vormerken?
    *   Wie lange hat man Zeit, ein vorgemerktes Buch abzuholen, nachdem es zurückgegeben wurde?
    *   Was passiert, wenn man es nicht rechtzeitig abholt?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Bei einem ausgeliehenen Buch sehe ich einen "Vormerken"-Button.
    2.  Nach dem Klick auf den Button erscheint das Buch in meiner persönlichen "Vormerkliste".
    3.  Sobald das Buch in der Bibliothek zurückgegeben wird, erhalte ich eine Push-Nachricht, dass ich es abholen kann.

---

### **4. Funktionale und Nicht-funktionale Anforderungen**

**Funktionale Anforderungen (Was soll das System tun?):**

1.  Das System muss es einem Benutzer ermöglichen, sich mit seiner Schul-E-Mail-Adresse und einem Passwort zu authentifizieren.
2.  Das System muss dem Bibliothekar ermöglichen, den Status eines Buches von "verfügbar" auf "ausgeliehen" zu ändern und dies einem bestimmten Benutzer zuzuordnen.
3.  Das System muss eine Suchfunktion bereitstellen, die es erlaubt, den Buchbestand nach Titel und Autor zu durchsuchen.

**Nicht-funktionale Anforderungen (Wie soll das System etwas tun?):**

1.  **Performance:** Die Suchergebnisse für eine Buchsuche müssen innerhalb von 2 Sekunden auf dem Bildschirm des Nutzers angezeigt werden.
2.  **Benutzerfreundlichkeit/Usability:** Ein neuer Schüler muss in der Lage sein, ohne Anleitung innerhalb von 60 Sekunden ein Buch zu finden und dessen Verfügbarkeit zu prüfen.
3.  **Sicherheit:** Passwörter der Benutzer müssen verschlüsselt (gehasht) in der Datenbank gespeichert werden.
4.  **Kompatibilität:** Die mobile App muss auf den Betriebssystemen iOS (Version 15 und neuer) und Android (Version 11 und neuer) lauffähig sein.
