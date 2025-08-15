# Lösung: Projektdokumentation vervollständigen – Schulbibliotheksverwaltung

**Szenario:**
Sie erhalten eine unvollständige Projektdokumentation für die Desktop-Applikation "LibraDesk" zur digitalen Verwaltung der Schulbibliothek. Ihre Aufgabe ist es, die Lücken zu erkennen und fachgerecht zu ergänzen.

---

## Projektdokumentation (Vervollständigt): "LibraDesk – Digitale Schulbibliothek"

### 1. Projektüberblick

**Projektname:** LibraDesk  
**Ziel:** Entwicklung einer Desktop-Anwendung zur effizienten Verwaltung der Schulbibliothek.

**Kurzbeschreibung:**  
Mit LibraDesk sollen Bücher, Medien und Ausleihen digital verwaltet werden. Die Applikation richtet sich an Bibliothekar:innen und Lehrkräfte.

---

### 2. Stakeholder

- Bibliothekar:innen
- Lehrkräfte
- **Schüler:innen** *(als Endnutzer der Bibliothek)*
- **Schulleitung** *(interessiert an Statistiken und Effizienz)*
- **IT-Administrator:in der Schule** *(verantwortlich für Installation und Wartung)*

---

### 3. Hauptfunktionen (Auszug)

- Bücher und Medien erfassen, bearbeiten und löschen
- Ausleihen und Rückgaben verwalten
- **Benutzer (Schüler:innen, Lehrkräfte) verwalten**
- **Mahnwesen (automatische Erinnerungen für überfällige Bücher erstellen)**
- **Inventurfunktion zur Bestandsaufnahme**
- **Such- und Filterfunktion für den gesamten Medienbestand**

---

### 4. Benutzerrollen

- **Bibliothekar:in:** Volle Zugriffsrechte. Kann Medien und Benutzer verwalten, Ausleihen durchführen, Mahnungen erstellen und Inventuren starten.
- **Lehrkraft:** Kann den Buchbestand durchsuchen und eine Liste von Büchern für den Unterricht reservieren. Hat möglicherweise eine längere Ausleihfrist.
- **Schulleitung:** Hat Lesezugriff auf Berichte und Statistiken (z.B. Ausleihzahlen, beliebteste Bücher), um datenbasierte Entscheidungen für die Bibliothek zu treffen. Kann keine operativen Änderungen vornehmen.
- **IT-Administrator:in:** Hat keine Rechte innerhalb der Anwendungslogik, ist aber für die technische Wartung, die Installation von Updates und die Durchführung von Backups verantwortlich.

---

### 5. Use Cases

Eine vollständige Liste der Anwendungsfälle (Use Cases) für das LibraDesk-System.

---
#### **UC-01: Buch ausleihen**
- **Akteur:** Bibliothekar:in
- **Beschreibung:** Eine Bibliothekar:in leiht ein Buch an eine Schüler:in oder Lehrkraft aus.
- **Ablauf:**
    1. Buch im System suchen (per ISBN-Scan oder Titelsuche).
    2. Benutzer:in auswählen (per Ausweis-Scan oder Namenssuche).
    3. Das System prüft, ob der/die Benutzer:in berechtigt ist, weitere Bücher auszuleihen.
    4. Ausleihvorgang bestätigen. Das System berechnet das Rückgabedatum und speichert den Vorgang.
- **Alternativablauf:**
    - Falls das Buch bereits ausgeliehen ist, kann eine Reservierung erstellt werden.
    - Falls der/die Benutzer:in gesperrt ist, wird die Ausleihe verweigert.

---
#### **UC-02: Buch zurückgeben**
- **Akteur:** Bibliothekar:in
- **Beschreibung:** Ein ausgeliehenes Buch wird in das System zurückgebucht.
- **Ablauf:**
    1. Buch identifizieren (per ISBN-Scan).
    2. Das System findet die zugehörige Ausleihe.
    3. Die Bibliothekar:in bestätigt die Rückgabe.
    4. Das Buch wird im System als "verfügbar" markiert.
- **Alternativablauf:**
    - Falls das Buch beschädigt ist, kann der Zustand vermerkt werden.
    - Falls für das Buch eine Reservierung vorliegt, informiert das System die Bibliothekar:in.

---
#### **UC-03: Neues Buch erfassen**
- **Akteur:** Bibliothekar:in
- **Beschreibung:** Ein neues Buch wird dem Bibliotheksbestand hinzugefügt.
- **Ablauf:**
    1. Funktion "Neues Buch" auswählen.
    2. ISBN scannen/eingeben.
    3. Das System versucht, Metadaten online abzurufen.
    4. Die Bibliothekar:in prüft/ergänzt die Daten (z.B. Standort, Schlagwörter).
    5. Das Buch wird gespeichert und erhält eine Inventarnummer.
- **Alternativablauf:**
    - Falls keine Online-Daten gefunden werden, müssen alle Felder manuell ausgefüllt werden.
    - Falls die ISBN bereits existiert, fragt das System, ob ein weiteres Exemplar hinzugefügt werden soll.

---
#### **UC-04: Benutzer verwalten**
- **Akteur:** Bibliothekar:in
- **Beschreibung:** Die Daten von Schüler:innen und Lehrkräften werden verwaltet.
- **Ablauf (Benutzer anlegen):**
    1. Funktion "Neuen Benutzer anlegen" wählen.
    2. Daten eingeben (Name, Klasse/Kürzel, Benutzertyp).
    3. Benutzer speichern.
- **Ablauf (Benutzer bearbeiten):**
    1. Benutzer suchen und auswählen.
    2. Daten ändern (z.B. bei Klassenwechsel).
    3. Änderungen speichern.

---
#### **UC-05: Mahnung erstellen**
- **Akteur:** Bibliothekar:in
- **Beschreibung:** Für überfällige Bücher werden Mahnungen generiert.
- **Vorbedingung:** Mindestens ein Buch ist überfällig.
- **Ablauf:**
    1. Ansicht "Überfällige Medien" öffnen.
    2. Das System listet alle überfälligen Ausleihen auf.
    3. Die Bibliothekar:in wählt eine oder mehrere Ausleihen aus.
    4. Das System generiert ein standardisiertes Mahnschreiben als PDF.
- **Nachbedingung:** Die Ausleihe wird als "gemahnt" markiert.

---
#### **UC-06: Statistik anzeigen**
- **Akteur:** Schulleitung, Bibliothekar:in
- **Beschreibung:** Das System stellt Berichte und Statistiken zur Nutzung der Bibliothek dar.
- **Ablauf:**
    1. Den Menüpunkt "Berichte" auswählen.
    2. Einen Berichtstyp auswählen (z.B. "Top 10 der beliebtesten Bücher", "Ausleihen pro Klasse").
    3. Zeitraum für den Bericht festlegen.
    4. Das System generiert und visualisiert den Bericht (als Tabelle oder Diagramm).

---

### 6. Nicht-funktionale Anforderungen (Auszug)

- Die Anwendung soll auf Windows 10 und Windows 11 lauffähig sein.
- **Die Suchfunktion muss auch bei einem Bestand von über 10.000 Büchern ein Ergebnis in weniger als 2 Sekunden liefern (Performance).**
- **Alle personenbezogenen Daten (Namen, Klassen) müssen gemäß DSGVO geschützt und sicher gespeichert werden (Sicherheit/Datenschutz).**

---

### 7. Mockup / UI-Skizze

**Beschreibung der Startseite (Dashboard):**
Die Benutzeroberfläche ist klar und einfach strukturiert. Nach dem Start sehen Bibliothekar:innen ein Dashboard mit den folgenden Elementen:
-   **Großes, zentrales Suchfeld:** "Suche nach Buch, ISBN oder Schüler:in..."
-   **Schnellzugriffs-Buttons:** "Buch ausleihen", "Buch zurückgeben", "Neues Buch erfassen".
-   **Übersichtsbox:** Zeigt auf einen Blick die Anzahl der heute fälligen Rückgaben und die Gesamtzahl der überfälligen Bücher.
-   **Navigationsleiste (links):** Menüpunkte für "Medienverwaltung", "Benutzerverwaltung", "Berichte", "Einstellungen".

---

### 8. Offene Fragen

- Wie sollen Benutzer (Bibliothekar:innen) authentifiziert werden? (z.B. einfaches Passwort, Schul-Login)
- **Soll eine Schnittstelle für den Import von Schülerdaten aus der Schulverwaltungssoftware vorgesehen werden, um die manuelle Eingabe zu vermeiden?**
- **Welche Statistiken sind für die Schulleitung relevant (z.B. beliebteste Bücher, Ausleihzahlen pro Klasse)?**

---
