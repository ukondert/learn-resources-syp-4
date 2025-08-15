# **Musterlösung zur Übungsaufgabe: Anforderungserhebung (Gaming)**

---

### **1. Stakeholder identifizieren und Erhebungsmethoden auswählen**

*   **Identifizierte Stakeholder-Gruppen:**
    1.  **Spieler (Casual & Hardcore):** Die Endnutzer des Systems. Ihre Bedürfnisse und Wünsche sind entscheidend für den Erfolg des Features.
    2.  **Game Designer:** Verantwortlich für das Spielerlebnis. Sie definieren, wie sich das Guild-System in das bestehende Spiel integriert und welche Belohnungen es gibt.
    3.  **Community Manager:** Die Schnittstelle zur Spieler-Community. Sie kennen das Feedback der Spieler und müssen das System später moderieren können.
    4.  *(Weitere mögliche Stakeholder: Backend-Entwickler, Marketing-Abteilung, Geschäftsführung)*

*   **Auswahl und Begründung der Erhebungstechniken:**

    1.  **Technik:** **Fragebogen/Umfrage** für die **Spieler**.
        *   **Begründung:** Ideal, um schnell ein breites Stimmungsbild aus der Community zu erhalten. Man kann abfragen, welche Arten von Gilden-Aktivitäten (z.B. PvE, PvP, Social) am beliebtesten sind und welche Features (z.B. Gilden-Bank, Kalender) am meisten gewünscht werden.

    2.  **Technik:** **Workshop** mit **Game Designern und Community Managern**.
        *   **Begründung:** Ein Workshop ist perfekt, um die kreativen und administrativen Anforderungen zu konsolidieren. Game Designer können ihre Vision für das Gameplay einbringen, während Community Manager auf potenzielle Probleme im sozialen Miteinander und notwendige Moderations-Tools hinweisen können.

---

### **2. Erhebungstechnik detailliert ausarbeiten (Beispiel: Workshop)**

*   **Technik:** Workshop mit Game Designern und Community Managern.

*   **Vorbereitung:**
    *   **Ziel:** Gemeinsame Erarbeitung und Priorisierung der Kernfunktionen für das neue Guild-System. Am Ende soll ein Konsens über den "Minimum Viable Product"-Umfang bestehen.
    *   **Teilnehmer:** 2 Game Designer, 1 Community Manager, 1 Lead-Entwickler.
    *   **Rollen:**
        *   *Moderator:* Der Anforderungsanalyst (Sie).
        *   *Protokollant:* Ein Junior-Entwickler.
        *   *Teilnehmer:* Alle oben genannten Personen.
    *   **Dauer:** 45 Minuten.
    *   **Ort:** Meetingraum "High-Score".

*   **Durchführung (Agenda):**
    *   **(5 Min) Begrüßung & Zielsetzung:** Vorstellung der Agenda und des Ziels des Workshops.
    *   **(15 Min) Brainstorming & Sammlung:** Alle Teilnehmer sammeln auf Kärtchen Ideen für Gilden-Features (z.B. Gilden-Chat, Gilden-Bank, Events, Ränge).
    *   **(15 Min) Clustering & Priorisierung:** Die Ideen werden an einem Whiteboard geclustert (z.B. nach "Kommunikation", "Verwaltung", "Gameplay"). Anschließend priorisieren die Teilnehmer die Cluster mittels Punktabstimmung (jeder hat 3 Klebepunkte).
    *   **(10 Min) Abschluss & nächste Schritte:** Zusammenfassung der Ergebnisse (Top 3 Features). Klärung der nächsten Schritte (z.B. "Die Top-Features werden als User Stories ausformuliert").

*   **Nachbereitung:**
    *   Das erstellte Protokoll wird an alle Teilnehmer versendet.
    *   Die priorisierte Liste der Features wird in das Projektmanagement-Tool (z.B. Jira, Trello) als erste Backlog-Items übertragen.
    *   Die Fotos vom Whiteboard werden zur Dokumentation im Projektverzeichnis gespeichert.

---

### **3. Anforderungen als User Stories formulieren (detailliert)**

Gute User Stories sind mehr als nur ein Satz. Sie folgen dem 3-C-Modell (Card, Conversation, Confirmation) und sollten die INVEST-Kriterien erfüllen. Hier sind die User Stories detaillierter ausgearbeitet:

---
**User Story 1: Gilden-Einladung**

*   **Card (Karte):** Als **Gilden-Anführer** möchte ich **neue Mitglieder in die Gilde einladen können**, um **unsere Gemeinschaft zu vergrößern**.

*   **Conversation (Diskussionspunkte):**
    *   Wie genau erfolgt die Einladung? Über den Spielernamen?
    *   Gibt es ein Limit für ausstehende Einladungen?
    *   Kann eine Einladung ablaufen?
    *   Was passiert, wenn der eingeladene Spieler bereits in einer Gilde ist?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin Gilden-Anführer und habe das Gilden-Menü geöffnet.
    *   **Wenn** ich den Namen eines Spielers eingebe und auf "Einladen" klicke,
    *   **Dann** erhält dieser Spieler eine Benachrichtigung mit der Einladung.
    *   **Und** die Einladung erscheint in meiner Liste der "ausstehenden Einladungen".

---
**User Story 2: Gilden-Chat**

*   **Card (Karte):** Als **Gilden-Mitglied** möchte ich **einen exklusiven Gilden-Chat haben**, um **mich mit meinen Gilden-Kollegen abzustimmen, ohne dass andere mitlesen**.

*   **Conversation (Diskussionspunkte):**
    *   Soll der Chat persistent sein (Nachrichtenverlauf speichern)?
    *   Gibt es spezielle Chat-Befehle (z.B. /g)?
    *   Wie werden neue Nachrichten signalisiert?
    *   Sollen Links oder Bilder im Chat möglich sein?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin Mitglied einer Gilde.
    *   **Wenn** ich eine Nachricht in den Gilden-Chat-Tab eingebe,
    *   **Dann** sehen alle anderen online befindlichen Gilden-Mitglieder diese Nachricht.
    *   **Und** die Nachricht erscheint nicht in öffentlichen Kanälen.

---
**User Story 3: Gilde finden und bewerben**

*   **Card (Karte):** Als **Spieler** möchte ich **eine Liste aller Gilden durchsuchen und mich bei einer bewerben können**, um **eine passende Gemeinschaft für mich zu finden**.

*   **Conversation (Diskussionspunkte):**
    *   Nach welchen Kriterien kann man die Gildenliste filtern/sortieren (z.B. Mitgliederzahl, Spielstil)?
    *   Kann man eine Bewerbungsnachricht hinzufügen?
    *   Wie viele Bewerbungen kann ein Spieler gleichzeitig offen haben?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin ein Spieler ohne Gilde.
    *   **Wenn** ich das Gilden-Browser-Fenster öffne,
    *   **Dann** sehe ich eine durchsuchbare und sortierbare Liste von Gilden.
    *   **Wenn** ich auf "Bewerben" bei einer Gilde klicke,
    *   **Dann** erhält der Gilden-Anführer eine Benachrichtigung über meine Bewerbung.

---
**User Story 4: Gilden-Quests**

*   **Card (Karte):** Als **Game Designer** möchte ich **gildenspezifische Quests und Belohnungen definieren können**, um **die Spieler zur Teilnahme am Gildenleben zu motivieren**.

*   **Conversation (Diskussionspunkte):**
    *   Welche Arten von Quests soll es geben (z.B. "Tötet X Monster als Gruppe", "Sammelt Y Ressourcen")?
    *   Wie werden die Belohnungen verteilt? An die Gilde oder an Einzelspieler?
    *   Brauchen wir ein eigenes Interface zur Erstellung dieser Quests?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin als Game Designer im Admin-Tool angemeldet.
    *   **Wenn** ich eine neue Gilden-Quest mit Zielbedingung und Belohnung erstelle,
    *   **Dann** wird diese Quest für alle Gilden im Spiel aktiv.
    *   **Und** wenn eine Gilde die Bedingung erfüllt, wird die Belohnung automatisch ausgeschüttet.

---

### **4. Funktionale und Nicht-funktionale Anforderungen unterscheiden**

*   **Beispiele für funktionale Anforderungen:**
    1.  "Das System muss einem Gilden-Anführer erlauben, ein Mitglied aus der Gilde zu entfernen."
    2.  "Das System muss allen Gilden-Mitgliedern eine tägliche Nachricht des Tages (MOTD) anzeigen, wenn sie sich einloggen."
    *(Beschreiben, **was** das System tun soll.)*

*   **Beispiele für nicht-funktionale Anforderungen:**
    1.  "Die Ladezeit der Gilden-Mitgliederliste darf bei 100 Mitgliedern nicht länger als 1 Sekunde betragen."
    2.  "Das Guild-System muss in der Lage sein, mindestens 50.000 Gilden gleichzeitig zu verwalten, ohne die Server-Performance zu beeinträchtigen."
    *(Beschreiben eine Eigenschaft oder eine Randbedingung des Systems, also **wie** es etwas tut oder sein soll.)*
