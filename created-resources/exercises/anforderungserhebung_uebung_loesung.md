# **Musterlösung zur Übungsaufgabe: Anforderungserhebung**

---

### **1. Stakeholder identifizieren und Erhebungsmethoden auswählen**

*   **Identifizierte Stakeholder-Gruppen:**
    1.  **Schüler:** Die Hauptnutzer der App. Sie wollen Bücher einfach finden, ausleihen und ihre Ausleihen verwalten.
    2.  **Lehrer:** Nutzen die Bibliothek für Unterrichtsmaterialien, haben eventuell spezielle Anforderungen (z.B. Reservierung von Klassensätzen).
    3.  **Bibliothekar(in)/Bibliothekspersonal:** Verantwortlich für die Verwaltung des Buchbestands, die Abwicklung von Ausleihen und Rückgaben sowie die Pflege des Systems.
    4.  *(Weitere mögliche Stakeholder: Schulleitung, IT-Abteilung, Eltern)*

*   **Auswahl und Begründung der Erhebungstechniken:**

    1.  **Technik:** **Fragebogen/Umfrage** für die **Schüler**.
        *   **Begründung:** Da es viele Schüler gibt, ist eine Umfrage eine effiziente Methode, um quantitative Daten und allgemeine Präferenzen von einer großen Nutzerbasis zu sammeln. Man kann schnell herausfinden, welche Funktionen am häufigsten gewünscht werden (z.B. "Bewerten Sie die Wichtigkeit einer Erinnerungsfunktion für die Buchrückgabe von 1-5").

    2.  **Technik:** **Interview** mit der/dem **Bibliothekar(in)**.
        *   **Begründung:** Der Bibliothekar kennt die aktuellen Prozesse, Probleme und Arbeitsabläufe im Detail. In einem direkten Gespräch können tiefgehende Fragen gestellt und die genauen Anforderungen an den Verwaltungsteil der App (z.B. Inventur, Mahnwesen) präzise ermittelt werden.

---

### **2. Beispielhafte Erhebungsdokumente**

Hier sind zwei Beispiele, basierend auf den in Aufgabe 1 gewählten Techniken:

**Beispiel 1: Interviewleitfaden für den/die Bibliothekar(in)**

*   **Ziel:** Die genauen Arbeitsabläufe, Schmerzpunkte und Wünsche für den Verwaltungsbereich der App verstehen.
*   **Fragen:**
    1.  "Können Sie mir den aktuellen Prozess der Buchausleihe und -rückgabe von Anfang bis Ende beschreiben?"
    2.  "Was sind die häufigsten Probleme oder Engpässe, die bei diesem Prozess auftreten?"
    3.  "Welche Aufgaben im Bibliotheksalltag sind besonders zeitaufwendig und könnten durch eine App vereinfacht werden?"
    4.  "Gibt es spezielle Anforderungen für die Verwaltung von Klassensätzen oder reservierten Büchern?"
    5.  "Welche Informationen wären für Sie auf einen Blick am wichtigsten, wenn Sie die App öffnen?"

**Beispiel 2: Entwurf für eine Schüler-Umfrage (z.B. in Microsoft Forms)**

*   **Frage 1: Wie oft leihst du Bücher aus der Schulbibliothek aus?**
    *   ( ) Mehrmals pro Woche
    *   ( ) Einmal pro Woche
    *   ( ) Einmal im Monat
    *   ( ) Seltener oder nie

*   **Frage 2: Welche Funktion wäre für dich in einer Bibliotheks-App am nützlichsten? (Bitte wähle die Top 2)**
    *   [ ] Sehen, ob ein Buch verfügbar ist
    *   [ ] Bücher online reservieren
    *   [ ] Ausgeliehene Bücher verlängern
    *   [ ] Eine Erinnerung bekommen, bevor die Leihfrist abläuft
    *   [ ] Buchempfehlungen von Lehrern sehen

*   **Frage 3: Auf einer Skala von 1 (unwichtig) bis 5 (sehr wichtig): Wie wichtig ist es dir, eine Erinnerung zu erhalten, bevor ein Buch zurückgegeben werden muss?**
    *   1 - 2 - 3 - 4 - 5

---

### **3. Anforderungen als User Stories formulieren**

Hier sind vier Beispiele für User Stories aus verschiedenen Perspektiven:

1.  **Als Schüler** möchte ich **eine Push-Benachrichtigung erhalten, wenn ein von mir reserviertes Buch verfügbar ist**, um es **zeitnah abholen zu können**.
2.  **Als Schüler** möchte ich **die Frist für meine ausgeliehenen Bücher direkt in der App verlängern können**, um **Mahngebühren zu vermeiden, wenn ich das Buch länger brauche**.
3.  **Als Bibliothekar** möchte ich **Bücher über einen Barcode-Scan als "zurückgegeben" markieren können**, um **den Rückgabeprozess zu beschleunigen und fehlerfrei zu gestalten**.
4.  **Als Lehrer** möchte ich **eine digitale Liste mit Buchempfehlungen für meine Klasse erstellen und teilen können**, um **den Schülern den Zugang zu relevanten Lernmaterialien zu erleichtern**.

---

### **4. Funktionale und Nicht-funktionale Anforderungen unterscheiden**

*   **Beispiele für funktionale Anforderungen:**
    1.  "Das System muss es einem angemeldeten Benutzer ermöglichen, den Ausleihstatus eines Buches (verfügbar, ausgeliehen bis) zu prüfen."
    2.  "Das System muss eine Suchfunktion bereitstellen, mit der Benutzer den Buchbestand nach Titel, Autor oder Schlagwort durchsuchen können."
    *(Beschreiben, **was** das System tun soll.)*

*   **Beispiele für nicht-funktionale Anforderungen:**
    1.  "Die App muss auf den Betriebssystemen iOS (Version 15 und neuer) und Android (Version 11 und neuer) lauffähig sein."
    2.  "Alle Benutzerdaten müssen gemäß der DSGVO sicher auf Servern innerhalb der EU gespeichert werden."
    *(Beschreiben eine Eigenschaft oder eine Randbedingung des Systems, also **wie** es etwas tut oder sein soll.)*
