# Lösungsvorschlag: Anforderungsanalyse "Schul-Event-O-Mat"

---

## 1. Vervollständigte und präzisierte Anforderungen

### a) Überarbeitete Anforderungen:

*   **REQ-03 (vorher: Die App soll einfach zu bedienen sein.)**
    *   **Typ:** Nicht-funktionale Anforderung (Benutzerfreundlichkeit)
    *   **Präzisierung (NFR-01):** Ein neuer Benutzer muss die Hauptfunktionen (Events ansehen, Details öffnen) ohne Anleitung innerhalb von 60 Sekunden verstehen können. (Messbar durch Nutzertest)

*   **REQ-04 (vorher: Lehrer sollen auch irgendwie Events eintragen können.)**
    *   **Typ:** Funktionale Anforderung
    *   **Präzisierung (User Story, FR-06):** Als **Lehrer** möchte ich ein **neues Event** mit Titel, Datum, Uhrzeit, Ort und einer kurzen Beschreibung **erstellen** können, um Schüler über die Veranstaltung zu informieren.

*   **REQ-05 (vorher: Die App muss auf einem Smartphone gut aussehen.)**
    *   **Typ:** Nicht-funktionale Anforderung (UI/UX)
    *   **Präzisierung (NFR-02):** Die Anwendung muss ein **responsives Design** besitzen, das auf den gängigsten Smartphone-Displaygrößen (z.B. zwischen 360px und 420px Breite) ohne horizontales Scrollen korrekt dargestellt wird.

### b) Zusätzliche nicht-funktionale Anforderungen:

*   **NFR-03 (Performance):** Die Ladezeit für die Event-Liste darf auf einem durchschnittlichen Schul-WLAN nicht länger als 2 Sekunden betragen.
*   **NFR-04 (Sicherheit):** Nur authentifizierte Lehrer dürfen Events erstellen oder bearbeiten. Schüler haben nur Lesezugriff.
*   **NFR-05 (Verfügbarkeit):** Das System muss eine Verfügbarkeit von 99% während der Schulzeiten (Mo-Fr, 7:00-18:00 Uhr) aufweisen.

### c) Benutzerrollen und Rechte:

*   **Rolle: Schüler**
    *   **Rechte:**
        *   Events in einer Liste ansehen.
        *   Details zu Events einsehen.
        *   (Optional) Events nach Kategorien filtern (z.B. Sport, Musik, Allgemein).

*   **Rolle: Lehrer**
    *   **Rechte:**
        *   Alle Rechte der Rolle "Schüler".
        *   Neue Events erstellen.
        *   Eigene erstellte Events bearbeiten und löschen.

---

## 2. Ausformulierte Use Cases

### a) Use Case: Eventdetails anzeigen

*   **Use Case Name:** UC-01: Eventdetails anzeigen
*   **Akteur:** Schüler, Lehrer
*   **Vorbedingung:** Der Benutzer ist in der App und sieht die Event-Liste.
*   **Standardablauf (Happy Path):**
    1.  Der Benutzer tippt auf ein Event in der Liste.
    2.  Das System öffnet eine neue Ansicht (Detailansicht).
    3.  Das System zeigt alle verfügbaren Informationen zum Event an: Titel, Datum, Uhrzeit, Ort, detaillierte Beschreibung.
*   **Alternativer Ablauf (Event abgesagt):**
    *   *3a. Wenn das Event als "abgesagt" markiert ist:* Das System zeigt alle Eventdetails an, hebt aber den Status "ABGESAGT" deutlich sichtbar (z.B. in roter Schrift) hervor.

### b) Use Case: Neues Event erstellen

*   **Use Case Name:** UC-02: Neues Event erstellen
*   **Akteur:** Lehrer
*   **Vorbedingung:** Der Lehrer ist in der App angemeldet und befindet sich in der Event-Listenansicht.
*   **Standardablauf (Happy Path):**
    1.  Der Lehrer tippt auf den "Neues Event erstellen"-Button.
    2.  Das System öffnet ein Formular mit Eingabefeldern für: Titel, Datum, Uhrzeit, Ort, Beschreibung.
    3.  Der Lehrer füllt alle Pflichtfelder (Titel, Datum, Ort) aus.
    4.  Der Lehrer tippt auf den "Speichern"-Button.
    5.  Das System validiert die Eingaben.
    6.  Das System speichert das neue Event und kehrt zur Event-Liste zurück, wo das neue Event nun sichtbar ist.
*   **Fehlerfall (Pflichtfelder nicht ausgefüllt):**
    *   *5a. Wenn der Lehrer auf "Speichern" tippt, aber ein Pflichtfeld leer ist:* Das System speichert nicht, markiert das fehlende Feld rot und zeigt die Fehlermeldung "Bitte füllen Sie alle Pflichtfelder aus."

---

## 3. Mockup / Wireframe (Beschreibung)

### a) Hauptansicht (Event-Liste)

*   **Layout:** Eine einfache, vertikal scrollbare Liste.
*   **Header:** Überschrift "Schul-Events".
*   **Listenelement:** Jeder Eintrag in der Liste ist eine "Karte" und zeigt die wichtigsten Infos auf einen Blick:
    *   **Links:** Datum (z.B. "15. OKT")
    *   **Rechts:** Event-Titel ("Tag der offenen Tür") und Ort ("Ganzes Schulhaus").
*   **Button (nur für Lehrer sichtbar):** Ein "+" (Plus) Button am unteren rechten Bildschirmrand, um ein neues Event zu erstellen.

### b) Detailansicht eines Events

*   **Layout:** Eine statische Ansicht.
*   **Header:** Der Titel des Events als große Überschrift.
*   **Inhaltsbereich:**
    *   Datum und Uhrzeit (z.B. "15. Oktober 2025, 09:00 - 15:00 Uhr")
    *   Ort (z.B. "Aula und Festsaal")
    *   Ein längerer Absatz mit der detaillierten Beschreibung des Events.
*   **Footer (nur für Lehrer, der das Event erstellt hat):** Buttons für "Bearbeiten" und "Löschen".
