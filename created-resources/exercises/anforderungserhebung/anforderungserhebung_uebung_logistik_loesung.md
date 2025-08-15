# **Musterlösung zur Übungsaufgabe: Anforderungserhebung (Logistik)**

---

### **1. Stakeholder identifizieren und Erhebungsmethoden auswählen**

*   **Identifizierte Stakeholder-Gruppen:**
    1.  **Lagerarbeiter/Kommissionierer:** Die Hauptnutzer der mobilen Anwendung. Sie benötigen ein schnelles, einfaches und robustes Werkzeug für ihre tägliche Arbeit.
    2.  **Lagerleiter/Schichtleiter:** Verantwortlich für die Effizienz des Lagers. Sie benötigen Übersichten, Berichte und Planungsfunktionen.
    3.  **IT-Abteilung:** Verantwortlich für die technische Infrastruktur, Wartung und Integration des neuen Systems in die bestehende IT-Landschaft (z.B. ERP-System).
    4.  *(Weitere mögliche Stakeholder: Geschäftsführung, LKW-Fahrer, Kunden-Support)*

*   **Auswahl und Begründung der Erhebungstechniken:**

    1.  **Technik:** **Beobachtung (Feldbeobachtung)** der **Lagerarbeiter**.
        *   **Begründung:** Viele Arbeitsschritte im Lager sind Routine und werden von den Arbeitern als selbstverständlich angesehen. Durch direkte Beobachtung ("Shadowing") kann man die tatsächlichen Abläufe, inoffizielle Workarounds und unbewusste Ineffizienzen aufdecken, die in einem Interview möglicherweise nicht erwähnt würden.

    2.  **Technik:** **Interview** mit dem **Lagerleiter**.
        *   **Begründung:** Der Lagerleiter hat den strategischen Überblick. In einem Interview können seine Anforderungen an Kennzahlen (KPIs), Reporting-Funktionen, Personalplanung und die Optimierung der Gesamteffizienz gezielt erfragt werden.

---

### **2. Beispielhafte Erhebungsdokumente**

**Beispiel 1: Plan für eine Feldbeobachtung eines Lagerarbeiters**

*   **Ziel:** Den Prozess der "Warenauslagerung" (Kommissionierung) vom Auftragseingang bis zur Übergabe an den Versand vollständig verstehen.
*   **Beobachtungspunkte:**
    1.  **Auftragsaufnahme:** Wie erhält der Arbeiter den Kommissionierauftrag? (Papierliste, Zuruf, etc.)
    2.  **Wegfindung:** Wie findet der Arbeiter den richtigen Lagerplatz? (Gedächtnis, Zonen-System, etc.) Wie lange dauert die Suche?
    3.  **Entnahme:** Welche Werkzeuge werden benutzt? (Handscanner, Wagen, etc.) Wie wird die Entnahme quittiert?
    4.  **Probleme:** Was passiert, wenn ein Artikel nicht am erwarteten Platz ist? Was passiert bei Bestandsabweichungen?
    5.  **Kommunikation:** Wie und wann kommuniziert der Arbeiter mit Kollegen oder dem Schichtleiter?

**Beispiel 2: Interviewleitfaden für den Lagerleiter**

*   **Ziel:** Die übergeordneten Management-Anforderungen an das neue System verstehen.
*   **Fragen:**
    1.  "Was sind aus Ihrer Sicht die drei größten Probleme im Lager, die durch eine neue Software gelöst werden sollten?"
    2.  "Welche Kennzahlen (KPIs) sind für Sie am wichtigsten, um den Erfolg des Lagers zu messen (z.B. Pick-Rate, Inventurgenauigkeit)?"
    3.  "Beschreiben Sie den Prozess, wie neue Ware eingelagert wird. Wo sehen Sie hier Verbesserungspotenzial?"
    4.  "Welche Art von Berichten oder Dashboards würden Ihnen helfen, Ihre täglichen Entscheidungen zu treffen?"
    5.  "Wie stellen Sie aktuell sicher, dass die dringendsten Aufträge zuerst bearbeitet werden?"

---

### **3. Anforderungen als User Stories formulieren (detailliert)**

Gute User Stories sind mehr als nur ein Satz. Sie folgen dem 3-C-Modell (Card, Conversation, Confirmation) und sollten die INVEST-Kriterien erfüllen. Hier sind die User Stories detaillierter ausgearbeitet:

---
**User Story 1: Optimierte Pick-Route**

*   **Card (Karte):** Als **Lagerarbeiter** möchte ich **eine optimierte Pick-Route auf meinem mobilen Gerät angezeigt bekommen**, um **unnötige Laufwege zu vermeiden und Zeit zu sparen**.

*   **Conversation (Diskussionspunkte):**
    *   Was bedeutet "optimiert"? Kürzester Weg? Vermeidung von Engstellen?
    *   Wie wird die Route dargestellt? Als Liste von Lagerplätzen oder auf einem grafischen Lagerplan?
    *   Was passiert, wenn der Arbeiter von der Route abweicht?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ein Kommissionierauftrag mit 5 verschiedenen Lagerplätzen liegt vor.
    *   **Wenn** ich den Auftrag auf meinem Gerät starte,
    *   **Dann** werden mir die Lagerplätze in einer Reihenfolge angezeigt, die den Gesamtlaufweg minimiert.
    *   **Und** der nächste Lagerplatz auf der Route wird immer klar hervorgehoben.

---
**User Story 2: Barcode-Scan zur Verifizierung**

*   **Card (Karte):** Als **Lagerarbeiter** möchte ich **einen Artikel per Barcode-Scan identifizieren**, um **sicherzustellen, dass ich das richtige Produkt kommissioniere**.

*   **Conversation (Diskussionspunkte):**
    *   Was passiert, wenn der falsche Barcode gescannt wird?
    *   Was passiert, wenn der Barcode beschädigt und nicht lesbar ist? Gibt es eine manuelle Eingabemöglichkeit?
    *   Welche Art von Barcodes müssen unterstützt werden (EAN, QR-Code etc.)?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich befinde mich an einem Lagerplatz, um einen bestimmten Artikel zu entnehmen.
    *   **Wenn** ich den Barcode des Artikels scanne,
    *   **Dann** bestätigt das System mit einem grünen Signal, dass es der richtige Artikel ist.
    *   **Wenn** ich den Barcode eines falschen Artikels scanne,
    *   **Dann** gibt das System eine rote Warnmeldung und einen Warnton aus.

---
**User Story 3: Echtzeit-Lagerbestände**

*   **Card (Karte):** Als **Lagerleiter** möchte ich **eine Echtzeit-Übersicht über die aktuellen Lagerbestände sehen**, um **Bestandsengpässe frühzeitig zu erkennen**.

*   **Conversation (Diskussionspunkte):**
    *   Was genau bedeutet "Echtzeit"? Alle 5 Sekunden aktualisiert? Bei jeder Buchung?
    *   Soll es Schwellenwerte geben, bei deren Unterschreitung automatisch eine Warnung ausgelöst wird?
    *   Nach welchen Kriterien soll die Übersicht filterbar sein (z.B. nach Artikel, Lagerzone)?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin als Lagerleiter angemeldet und öffne das Bestands-Dashboard.
    *   **Wenn** ein Lagerarbeiter einen Artikel aus dem Regal nimmt und dies verbucht,
    *   **Dann** wird der angezeigte Bestand dieses Artikels im Dashboard innerhalb von maximal 10 Sekunden aktualisiert.
    *   **Und** Artikel, deren Bestand unter den definierten Meldebestand fällt, werden farblich hervorgehoben.

---
**User Story 4: Rollen- und Rechteverwaltung**

*   **Card (Karte):** Als **IT-Administrator** möchte ich **Benutzerrollen und Zugriffsrechte einfach verwalten können**, um **sicherzustellen, dass Mitarbeiter nur die für sie relevanten Funktionen sehen und nutzen können**.

*   **Conversation (Diskussionspunkte):**
    *   Welche vordefinierten Rollen soll es geben (z.B. "Lagerarbeiter", "Lagerleiter")?
    *   Können auch benutzerdefinierte Rollen erstellt werden?
    *   Wie erfolgt die Zuweisung? Pro Benutzer? Pro Gruppe?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin als IT-Administrator im System angemeldet.
    *   **Wenn** ich einen neuen Benutzer anlege,
    *   **Dann** kann ich ihm eine der vordefinierten Rollen (z.B. "Lagerarbeiter") zuweisen.
    *   **Wenn** sich dieser Benutzer dann in der mobilen App anmeldet,
    *   **Dann** sieht er nur die Menüpunkte und Funktionen, die für die Rolle "Lagerarbeiter" freigegeben sind (z.B. Kommissionierung), aber nicht die für "Lagerleiter" (z.B. Berichte).

---

### **4. Funktionale und Nicht-funktionale Anforderungen unterscheiden**

*   **Beispiele für funktionale Anforderungen:**
    1.  "Das System muss bei der Einlagerung eines neuen Artikels automatisch den optimalen freien Lagerplatz vorschlagen."
    2.  "Das System muss eine Inventurfunktion unterstützen, bei der Bestände pro Lagerplatz gezählt und Differenzen protokolliert werden."
    *(Beschreiben, **was** das System tun soll.)*

*   **Beispiele für nicht-funktionale Anforderungen:**
    1.  "Die mobile Anwendung muss auch in Bereichen des Lagers mit schlechter WLAN-Abdeckung offline-fähig sein und sich automatisch synchronisieren, sobald wieder eine Verbindung besteht."
    2.  "Die Akkulaufzeit der mobilen Endgeräte muss bei durchgehender Nutzung der App eine komplette 8-Stunden-Schicht durchhalten."
    *(Beschreiben eine Eigenschaft oder eine Randbedingung des Systems, also **wie** es etwas tut oder sein soll.)*
