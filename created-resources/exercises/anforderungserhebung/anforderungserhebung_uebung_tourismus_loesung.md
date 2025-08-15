# **Musterlösung zur Übungsaufgabe: Anforderungserhebung (Reise & Tourismus)**

---

### **1. Stakeholder identifizieren und Erhebungsmethoden auswählen**

*   **Identifizierte Stakeholder-Gruppen:**
    1.  **Reisende/Nutzer:** Die Endkunden, die ihre Reisen planen und buchen. Ihre Bedürfnisse nach Einfachheit, Übersichtlichkeit und Flexibilität sind zentral.
    2.  **Produktmanager:** Verantwortlich für den wirtschaftlichen Erfolg des neuen Features. Er definiert die Business-Ziele und die strategische Ausrichtung.
    3.  **Partner-Unternehmen (Airlines, Hotels, etc.):** Stellen ihre Dienstleistungen und Daten über Schnittstellen (APIs) zur Verfügung. Sie haben Anforderungen an die korrekte Darstellung ihrer Angebote und die zuverlässige Abwicklung von Buchungen.
    4.  *(Weitere mögliche Stakeholder: Marketing-Team, Kundenservice, Entwicklerteam)*

*   **Auswahl und Begründung der Erhebungstechniken:**

    1.  **Technik:** **Fragebogen/Umfrage** für die **Reisenden/Nutzer**.
        *   **Begründung:** Um die Gewohnheiten und "Schmerzpunkte" einer großen, heterogenen Nutzergruppe zu verstehen. Eine Umfrage kann schnell Daten darüber liefern, wie Nutzer aktuell ihre Reisen planen, welche Tools sie nutzen und welche Funktionen sie sich am meisten wünschen würden.

    2.  **Technik:** **Workshop** mit dem **Produktmanager, einem Lead-Entwickler und einem UX-Designer**.
        *   **Begründung:** Ein Workshop ist ideal, um die Business-Ziele (Produktmanager) mit der technischen Machbarkeit (Entwickler) und der optimalen User Experience (UX-Designer) in Einklang zu bringen. Hier können erste Konzepte und Prioritäten gemeinsam erarbeitet werden.

---

### **2. Beispielhafte Erhebungsdokumente**

**Beispiel 1: Entwurf für eine Nutzer-Umfrage**

*   **Frage 1: Wie planen Sie typischerweise eine Reise mit mehreren Stationen?**
    *   ( ) Ich buche alles auf einer einzigen Webseite.
    *   ( ) Ich nutze mehrere verschiedene Webseiten (eine für Flüge, eine für Hotels etc.).
    *   ( ) Ich gehe in ein traditionelles Reisebüro.
    *   ( ) Sonstiges: ________

*   **Frage 2: Was ist für Sie die größte Herausforderung bei der Planung einer komplexen Reise?**
    *   ( ) Den Überblick über alle Buchungen zu behalten.
    *   ( ) Die besten Preise für alle Komponenten zu finden.
    *   ( ) Die zeitliche Abstimmung von Flügen, Transfers und Hotels.
    *   ( ) Inspiration für Aktivitäten vor Ort zu finden.

*   **Frage 3: Auf einer Skala von 1 (unwichtig) bis 5 (sehr wichtig): Wie wichtig wäre es Ihnen, alle Reisebestandteile (Flug, Hotel, Mietwagen) in einer einzigen Ansicht zu sehen?**
    *   1 - 2 - 3 - 4 - 5

---

### **3. Anforderungen als User Stories formulieren (detailliert)**

Gute User Stories sind mehr als nur ein Satz. Sie folgen dem 3-C-Modell (Card, Conversation, Confirmation) und sollten die INVEST-Kriterien erfüllen. Hier sind die User Stories detaillierter ausgearbeitet:

---
**User Story 1: Reiseroute visualisieren**

*   **Card (Karte):** Als **Reisender** möchte ich **meine geplante Reiseroute auf einer Karte visualisiert sehen**, um **ein besseres Gefühl für die Entfernungen und die Lage meiner Stationen zu bekommen**.

*   **Conversation (Diskussionspunkte):**
    *   Welcher Kartendienst wird verwendet (z.B. Google Maps, OpenStreetMap)?
    *   Was wird auf der Karte angezeigt? Nur die Orte oder auch die Verbindungen (Flugrouten, Fahrstrecken)?
    *   Kann man mit der Karte interagieren (zoomen, verschieben)?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich habe einen Reiseplan mit den Stationen "Wien", "Rom" und "Barcelona" erstellt.
    *   **Wenn** ich auf den "Karte anzeigen"-Button klicke,
    *   **Dann** öffnet sich eine Kartenansicht, auf der die drei Städte mit Pins markiert sind.
    *   **Und** die Pins sind in der Reihenfolge der Reise miteinander verbunden.

---
**User Story 2: Reiseplan exportieren/teilen**

*   **Card (Karte):** Als **Reisender** möchte ich **meinen kompletten Reiseplan als PDF exportieren oder mit meinen Mitreisenden teilen können**, um **alle wichtigen Informationen auch offline verfügbar zu haben**.

*   **Conversation (Diskussionspunkte):**
    *   Welche Informationen soll das PDF genau enthalten (Flugnummern, Hoteladressen, Buchungsnummern)?
    *   Wie funktioniert das "Teilen"? Per E-Mail? Per Link?
    *   Hat der geteilte Link eine Gültigkeit?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich habe einen fertigen Reiseplan.
    *   **Wenn** ich auf "PDF exportieren" klicke,
    *   **Dann** wird ein PDF-Dokument generiert, das alle Flüge, Hotels und Aktivitäten in chronologischer Reihenfolge auflistet.
    *   **Wenn** ich auf "Teilen" klicke,
    *   **Dann** wird ein eindeutiger Link generiert, den ich kopieren und versenden kann.

---
**User Story 3: Nutzungsanalyse für Produktmanager**

*   **Card (Karte):** Als **Produktmanager** möchte ich **sehen, welche Aktivitäten am häufigsten zu Reisen hinzugefügt werden**, um **zukünftige Partnerschaften mit Tour-Anbietern zu priorisieren**.

*   **Conversation (Diskussionspunkte):**
    *   Welche Filter braucht das Dashboard (z.B. nach Region, Zeitraum, Reisetyp)?
    *   Wie werden die Daten visualisiert (Tabelle, Balkendiagramm)?
    *   Wer hat Zugriff auf dieses Dashboard?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich bin als Produktmanager im Admin-Backend angemeldet.
    *   **Wenn** ich das "Aktivitäten-Dashboard" öffne,
    *   **Dann** sehe ich eine Top-10-Liste der meistgebuchten Aktivitäten des letzten Monats.
    *   **Und** ich kann diese Liste nach Ländern filtern.

---
**User Story 4: Planungs-Warnungen**

*   **Card (Karte):** Als **Nutzer** möchte ich **Warnungen erhalten, wenn meine geplanten Reisekomponenten nicht zusammenpassen**, um **Planungsfehler zu vermeiden**.

*   **Conversation (Diskussionspunkte):**
    *   Welche Arten von Konflikten sollen erkannt werden (zeitliche Überlappungen, zu knappe Umsteigezeiten)?
    *   Wie wird die Warnung angezeigt? Als Pop-up? Als permanenter Hinweis?
    *   Kann der Nutzer die Warnung ignorieren?

*   **Confirmation (Akzeptanzkriterien):**
    *   **Gegeben sei,** ich habe einen Flug gebucht, der um 22:00 Uhr landet.
    *   **Wenn** ich versuche, ein Hotel hinzuzufügen, dessen Check-in nur bis 21:00 Uhr möglich ist,
    *   **Dann** zeigt das System eine deutliche Warnmeldung an: "Achtung: Der Check-in für dieses Hotel schließt vor Ihrer Ankunft."
    *   **Und** der Button "Buchen" ist vorerst deaktiviert, bis ich den Konflikt zur Kenntnis genommen habe.

---

### **4. Funktionale und Nicht-funktionale Anforderungen unterscheiden**

*   **Beispiele für funktionale Anforderungen:**
    1.  "Das System muss dem Nutzer ermöglichen, die Reihenfolge der Reiseziele innerhalb eines Reiseplans per Drag-and-Drop zu ändern."
    2.  "Das System muss die Gesamtkosten des Reiseplans in Echtzeit aktualisieren, wenn ein neuer Bestandteil (z.B. ein Hotel) hinzugefügt wird."
    *(Beschreiben, **was** das System tun soll.)*

*   **Beispiele für nicht-funktionale Anforderungen:**
    1.  "Die Abfrage von Flug- und Hotelverfügbarkeiten über externe Partner-APIs darf im Durchschnitt nicht länger als 5 Sekunden dauern."
    2.  "Das System muss in der Lage sein, Preisangaben in mindestens 10 verschiedenen Währungen anzuzeigen, basierend auf der Einstellung des Nutzers."
    *(Beschreiben eine Eigenschaft oder eine Randbedingung des Systems, also **wie** es etwas tut oder sein soll.)*
