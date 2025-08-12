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

### **2. Beispielhafte Erhebungsdokumente**

**Beispiel 1: Entwurf für eine Spieler-Umfrage (z.B. via In-Game-News)**

*   **Frage 1: Worauf würdest du in einer Gilde den größten Wert legen? (Wähle deine Top-Priorität)**
    *   ( ) Gemeinsam schwere Dungeons & Raids meistern (PvE)
    *   ( ) Gegen andere Gilden in Turnieren antreten (PvP)
    *   ( ) Eine entspannte Community zum Chatten und Handeln (Social)
    *   ( ) Exklusive kosmetische Belohnungen freischalten (Rewards)

*   **Frage 2: Welches der folgenden Features wäre für dich unverzichtbar?**
    *   [ ] Ein gemeinsamer Chat-Kanal nur für die Gilde
    *   [ ] Eine Gilden-Bank, um Gegenstände zu teilen
    *   [ ] Ein Kalender für die Planung von Gilden-Events
    *   [ ] Ein Rängesystem mit unterschiedlichen Rechten (Anführer, Offizier, Mitglied)

*   **Frage 3: Wie groß sollte eine Gilde maximal sein dürfen?**
    *   ( ) Klein und familiär (bis 20 Mitglieder)
    *   ( ) Mittelgroß (bis 50 Mitglieder)
    *   ( ) Groß und schlagkräftig (100+ Mitglieder)

---

### **3. Anforderungen als User Stories formulieren**

1.  **Als Gilden-Anführer** möchte ich **neue Mitglieder in die Gilde einladen können**, um **unsere Gemeinschaft zu vergrößern**.
2.  **Als Gilden-Mitglied** möchte ich **einen exklusiven Gilden-Chat haben**, um **mich mit meinen Gilden-Kollegen abzustimmen, ohne dass andere mitlesen**.
3.  **Als Spieler** möchte ich **eine Liste aller Gilden durchsuchen und mich bei einer bewerben können**, um **eine passende Gemeinschaft für mich zu finden**.
4.  **Als Game Designer** möchte ich **gildenspezifische Quests und Belohnungen definieren können**, um **die Spieler zur Teilnahme am Gildenleben zu motivieren**.

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
