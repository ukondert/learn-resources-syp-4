### **Musterlösung: Anforderungserhebung für eine digitale Schulbibliothek**

---

**1. Stakeholder identifizieren und Erhebungsmethoden auswählen**

*   **Identifizierte Stakeholder-Gruppen:**
    1.  **Schüler:** Die Hauptnutzer der Bibliothek. Sie wollen Bücher schnell finden, ausleihen und zurückgeben.
    2.  **Lehrer:** Nutzen die Bibliothek für Unterrichtsmaterialien und haben möglicherweise erweiterte Bedürfnisse (z.B. längere Leihfristen, Reservierung von Klassensätzen).
    3.  **Bibliothekar/Bibliotheks-Team:** Verantwortlich für die Verwaltung des Bestands, die Durchführung von Ausleihen/Rückgaben und die Unterstützung der Nutzer. Dies ist der "Power-User" des Systems.
    4.  **Schulleitung:** Stellt das Budget bereit und ist am Erfolg des Projekts (Effizienzsteigerung, modernes Image der Schule) interessiert.
    5.  **IT-Administrator:** Verantwortlich für die technische Infrastruktur, die Wartung des Systems und den Datenschutz.

*   **Ausgewählte Erhebungstechniken und Begründung:**
    1.  **Interview (mit dem Bibliothekar):** Diese Technik wird gewählt, um ein tiefes Verständnis der bestehenden Prozesse, der täglichen Herausforderungen und der administrativen Anforderungen zu erhalten. Der Bibliothekar besitzt das detaillierteste Wissen über die Abläufe und kann wertvolle Einblicke in Ausnahmefälle und notwendige Verwaltungsfunktionen geben.
    2.  **Fragebogen (für Schüler und Lehrer):** Diese Technik eignet sich, um schnell und effizient quantitative Daten und Meinungen von einer großen Nutzerbasis zu sammeln. Man kann damit Prioritäten ermitteln (z.B. "Wie wichtig ist Ihnen eine Online-Verfügbarkeitssuche?") und die Zufriedenheit mit dem aktuellen System messen, um den Bedarf für die neue App zu untermauern.

---

**2. Erhebungstechnik "Interview" detailliert ausarbeiten**

*   **Vorbereitung:**
    *   **Ziel des Interviews:** Das Hauptziel ist es, den genauen Ablauf der Buchausleihe und -rückgabe zu verstehen, die größten Schmerzpunkte im aktuellen manuellen Prozess zu identifizieren und erste Kernanforderungen für die neue App aus Sicht des Administrators zu sammeln.
    *   **Organisation:**
        *   **Interviewpartner:** Herr/Frau Mustermann (Leiter/in der Schulbibliothek).
        *   **Ort:** Im Büro der Schulbibliothek, um eine ruhige Atmosphäre zu gewährleisten.
        *   **Dauer:** Ca. 45 Minuten.
        *   **Hilfsmittel:** Laptop für Notizen, Smartphone für eine (nach Einverständnis) Audio-Aufnahme zur späteren Protokollierung.

*   **Durchführung (Leitfaden mit offenen Fragen):**
    1.  "Können Sie mir bitte den typischen Ablauf von Anfang bis Ende beschreiben, wenn ein Schüler ein Buch ausleihen möchte?"
    2.  "Welche Schritte in diesem Prozess sind am zeitaufwendigsten oder führen am häufigsten zu Fehlern?"
    3.  "Welche Informationen über Bücher, Schüler oder Ausleihen müssen Sie jederzeit schnell zur Hand haben, um Ihre Arbeit effizient zu erledigen?"
    4.  "Gibt es spezielle Regeln oder Ausnahmefälle, die ein neues System unbedingt berücksichtigen muss? (z.B. unterschiedliche Leihfristen für Lehrer, Umgang mit Verlust oder Beschädigung)"
    5.  "Wenn Sie sich eine ideale Bibliotheks-App wünschen könnten, welche eine Funktion wäre Ihnen persönlich am allerwichtigsten und warum?"

*   **Nachbereitung:**
    *   Die Notizen und die Audio-Aufnahme werden unmittelbar nach dem Interview zu einem strukturierten Protokoll zusammengefasst.
    *   Die identifizierten Probleme und Wünsche werden in eine erste Liste potenzieller Anforderungen überführt.
    *   Das Protokoll wird dem Interviewpartner zur Überprüfung und Bestätigung zugesandt, um Missverständnisse auszuschließen.

---

**3. Anforderungen als User Stories formulieren (3-C-Modell)**

**User Story 1: Buchsuche**
*   **Card:** Als **Schüler** möchte ich **online nach Büchern suchen können**, um **zu sehen, ob sie verfügbar sind und wo sie stehen.**
*   **Conversation (Diskussionspunkte):**
    *   Welche Suchfilter sind notwendig? (Titel, Autor, ISBN, Schlagwort?)
    *   Wie soll der Verfügbarkeitsstatus angezeigt werden? (z.B. "Verfügbar", "Ausgeliehen bis [Datum]")
    *   Welche Detailinformationen zum Standort sind nötig? (Regalnummer, Raum?)
    *   Soll es eine "Meinten Sie..."-Funktion bei Tippfehlern geben?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Wenn ich nach einem existierenden Buchtitel suche, wird das Buch mit Status "Verfügbar" und seiner Regalnummer angezeigt.
    2.  Wenn ich nach einem ausgeliehenen Buch suche, wird der Status korrekt mit dem Rückgabedatum angezeigt.
    3.  Wenn ich nach einem Autor suche, werden alle Bücher dieses Autors aus dem Bestand aufgelistet.

**User Story 2: Ausleihprozess**
*   **Card:** Als **Bibliothekar** möchte ich **den Ausleihprozess durch Scannen eines Barcodes am Buch und am Schülerausweis durchführen**, um **Zeit zu sparen und Erfassungsfehler zu vermeiden.**
*   **Conversation (Diskussionspunkte):**
    *   Welche Art von Barcode-Scanner wird verwendet?
    *   Was passiert, wenn ein Barcode nicht lesbar ist? Ist eine manuelle Eingabe der Buch- oder Schülernummer möglich?
    *   Wird das Rückgabedatum automatisch gesetzt? Ist dieses Datum (z.B. für Ferien) anpassbar?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Nach dem Scannen des Schülerausweises und des Buch-Barcodes ist das Buch im System als "ausgeliehen" an diesen Schüler vermerkt.
    2.  Das Standard-Rückgabedatum (z.B. heute + 4 Wochen) wird automatisch eingetragen.
    3.  Versucht ein Schüler mit bereits maximaler Anzahl an Ausleihen ein weiteres Buch zu leihen, zeigt das System eine klare Fehlermeldung an.

**User Story 3: Ausleiherinnerung**
*   **Card:** Als **Schüler** möchte ich **eine Erinnerung erhalten, bevor meine Leihfrist abläuft**, um **Mahngebühren zu vermeiden.**
*   **Conversation (Diskussionspunkte):**
    *   Über welchen Kanal soll die Erinnerung erfolgen? (E-Mail, Push-Nachricht in der App?)
    *   Wie viele Tage vor Ablauf der Frist soll die Erinnerung gesendet werden?
    *   Soll die Nachricht einen direkten Link zur Verlängerung der Ausleihe enthalten?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Drei Tage vor Ablauf der Leihfrist wird automatisch eine E-Mail an die hinterlegte Adresse des Schülers gesendet.
    2.  Die E-Mail enthält den Buchtitel und das genaue Rückgabedatum.
    3.  Für bereits überfällige Bücher wird keine Erinnerung, sondern eine Mahnung mit einem anderen Text versendet.

**User Story 4: Übersicht für Bibliothekare**
*   **Card:** Als **Bibliothekar** möchte ich **eine Übersicht aller ausgeliehenen und überfälligen Bücher sehen**, um **den Überblick zu behalten und Mahnungen effizient zu verwalten.**
*   **Conversation (Diskussionspunkte):**
    *   Nach welchen Kriterien soll die Liste sortier- und filterbar sein? (z.B. nach Rückgabedatum, nach Schülername, nur Überfällige anzeigen)
    *   Welche Informationen müssen pro Eintrag sichtbar sein?
    *   Soll es eine Funktion geben, um aus der Liste heraus direkt eine Mahn-E-Mail zu generieren?
*   **Confirmation (Akzeptanzkriterien):**
    1.  Es gibt eine Ansicht, die standardmäßig alle aktuell ausgeliehenen Bücher anzeigt, sortiert nach dem nächstgelegenen Rückgabedatum.
    2.  Ich kann einen Filter aktivieren, der nur Bücher anzeigt, deren Rückgabedatum in der Vergangenheit liegt.
    3.  Bei überfälligen Büchern wird die Anzahl der überfälligen Tage rot hervorgehoben.

---

**4. Funktionale und Nicht-funktionale Anforderungen**

*   **Funktionale Anforderungen:**
    1.  Das System muss es dem Bibliothekar ermöglichen, den Status eines Buches manuell zu ändern (z.B. auf "verloren" oder "beschädigt").
    2.  Ein Schüler muss in seinem Profil eine Liste aller aktuell von ihm ausgeliehenen Bücher inklusive Rückgabedatum einsehen können.

*   **Nicht-funktionale Anforderungen:**
    1.  **Performance:** Die Buchsuche muss auch bei einem Bestand von 10.000 Büchern ein Ergebnis in unter 2 Sekunden liefern.
    2.  **Benutzbarkeit (Usability):** Die Kernfunktionen (Suche, Ausleihe, Rückgabe) müssen so intuitiv sein, dass eine neue Aushilfskraft sie nach maximal 15 Minuten Einweisung selbstständig nutzen kann.
    3.  **Sicherheit:** Personenbezogene Daten der Schüler (Ausleihhistorie) dürfen nur für autorisierte Bibliothekare und den jeweiligen Schüler selbst einsehbar sein und müssen konform zur DSGVO gespeichert werden.
    4.  **Zuverlässigkeit:** Das System muss eine Verfügbarkeit von 99,5 % während der Schulöffnungszeiten aufweisen.
