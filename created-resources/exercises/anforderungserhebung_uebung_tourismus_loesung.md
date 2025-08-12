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

### **3. Anforderungen als User Stories formulieren**

1.  **Als Reisender** möchte ich **meine geplante Reiseroute auf einer Karte visualisiert sehen**, um **ein besseres Gefühl für die Entfernungen und die Lage meiner Stationen zu bekommen**.
2.  **Als Reisender** möchte ich **meinen kompletten Reiseplan als PDF exportieren oder mit meinen Mitreisenden teilen können**, um **alle wichtigen Informationen auch offline verfügbar zu haben**.
3.  **Als Produktmanager** möchte ich **sehen, welche Aktivitäten am häufigsten zu Reisen hinzugefügt werden**, um **zukünftige Partnerschaften mit Tour-Anbietern zu priorisieren**.
4.  **Als Nutzer** möchte ich **Warnungen erhalten, wenn meine geplanten Reisekomponenten nicht zusammenpassen** (z.B. Ankunftszeit des Fluges liegt nach dem Check-in-Schluss des Hotels), um **Planungsfehler zu vermeiden**.

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
