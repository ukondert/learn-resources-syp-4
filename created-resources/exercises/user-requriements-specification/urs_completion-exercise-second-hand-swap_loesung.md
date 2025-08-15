# User Requirement Specification (URS) - "TauschRausch" Nachbarschafts-Tauschbörse - Musterlösung

**Version:** 1.0
**Datum:** 2025-08-15

---

## 1. Einleitung

### 1.1. Projektübersicht

In vielen Haushalten sammeln sich Gegenstände an, die nicht mehr gebraucht werden, aber zu schade zum Wegwerfen sind (Bücher, Kleidung, Spiele, kleine Elektrogeräte). Gleichzeitig suchen andere Menschen genau nach diesen Dingen. Kommerzielle Second-Hand-Plattformen sind oft aufwändig und auf den Verkauf ausgerichtet.

Das Projekt "TauschRausch" soll eine mobile App schaffen, die den unkomplizierten, nicht-kommerziellen Tausch von Gegenständen innerhalb einer lokalen Gemeinschaft (z.B. einer Stadt oder eines Bezirks) fördert. Die App soll Nachhaltigkeit unterstützen und den sozialen Zusammenhalt in der Nachbarschaft stärken.

### 1.2. Ziele

*   **Primärziel:** Eine einfach zu bedienende mobile App bereitstellen, mit der Nutzer Gegenstände zum Tausch anbieten und Tauschanfragen stellen können.
*   **Sekundärziel 1:** Einen Beitrag zur Nachhaltigkeit leisten, indem die Lebensdauer von Produkten durch Wiederverwendung verlängert wird.
*   **Sekundärziel 2:** Die lokale Gemeinschaft vernetzen und eine Alternative zum konsumorientierten Kaufverhalten bieten.

### 1.3. Geltungsbereich (Scope)

**In-Scope (Was das System leisten wird):**
*   Benutzerprofile mit Standort (nur auf Bezirksebene, keine genaue Adresse).
*   Erstellung von Inseraten mit Fotos, Beschreibung und "Ich suche"-Angaben.
*   Eine "Wisch"-Funktion (ähnlich wie bei Dating-Apps), um schnell durch Angebote zu stöbern.
*   Ein Chat-System zur Organisation der Übergabe.
*   Ein Bewertungssystem zur Förderung von Vertrauen und Zuverlässigkeit.

**Out-of-Scope (Was das System NICHT leisten wird):**
*   Jegliche Form von Geldtransaktionen oder Bezahlfunktionen.
*   Versand- und Logistikdienstleistungen. Die Übergabe wird von den Nutzern selbst organisiert.
*   Das Anbieten von Dienstleistungen (nur physische Gegenstände).

---

## 2. Systembeschreibung

### 2.1. Akteure & Stakeholder

| Akteur/Stakeholder | Beschreibung |
| :--- | :--- |
| **Nutzer (Tauscher)** | Hauptnutzer der App. Kann Profil erstellen, Inserate einstellen, suchen, Tauschanfragen stellen und chatten. |
| **Administrator** | Verwaltet die Plattform, kann Nutzer sperren, Inserate löschen und Kategorien für Gegenstände pflegen. |
| **Lokale Gemeinschaft** | Profitieren indirekt durch erhöhte Nachhaltigkeit und sozialen Austausch. |
| **App-Store-Betreiber (Apple/Google)** | Stellen die Plattform für den Download bereit und haben eigene Richtlinien, die eingehalten werden müssen. |

### 2.2. Use Cases (Anwendungsfälle)

**Use-Case-Liste:**
*   UC-01: Als Nutzer registrieren
*   UC-02: Tauschinserat erstellen
*   UC-03: Nach Gegenständen suchen/stöbern
*   UC-04: Ein Tauschangebot machen
*   UC-05: Tauschangebot annehmen/ablehnen
*   UC-06: Chat mit Tauschpartner führen
*   UC-07: Tauschpartner nach Übergabe bewerten
*   UC-08: Inserat als "getauscht" markieren
*   UC-09: Inserat oder Nutzer melden

---
**Detaillierter Use Case:**

| Use Case ID | UC-02 |
| :--- | :--- |
| **Use Case Name** | Tauschinserat erstellen |
| **Akteure** | Nutzer (Tauscher) |
| **Kurzbeschreibung** | Ein Nutzer erstellt ein neues Inserat für einen Gegenstand, den er zum Tausch anbieten möchte. |
| **Vorbedingungen** | Der Nutzer ist in der App angemeldet. |
| **Standardablauf (Happy Path)** | 1. Der Nutzer wählt die Option "Neues Inserat erstellen".<br>2. Der Nutzer lädt mindestens ein Foto des Gegenstands hoch.<br>3. Der Nutzer gibt einen Titel und eine kurze Beschreibung ein.<br>4. Der Nutzer wählt eine passende Kategorie aus (z.B. "Elektronik", "Bücher", "Kleidung").<br>5. Optional gibt der Nutzer an, welche Art von Gegenständen er im Gegenzug sucht.<br>6. Der Nutzer veröffentlicht das Inserat. |
| **Nachbedingungen** | Das Inserat ist für andere Nutzer in der App sichtbar. |
| **Fehlerfälle & Ausnahmen** | - **Kein Foto hochgeladen:** Das System lässt die Veröffentlichung nicht zu und zeigt die Fehlermeldung "Bitte fügen Sie mindestens ein Foto hinzu."<br>- **Unangemessene Inhalte:** Wenn der Titel oder die Beschreibung gegen die Richtlinien verstoßende Wörter enthalten, wird das Inserat zur Überprüfung markiert und nicht sofort veröffentlicht. |

---

## 3. Anforderungen

### 3.1. Funktionale Anforderungen

| ID | Anforderung | Priorität |
| :--- | :--- | :--- |
| FA-01 | Das System muss dem Nutzer ermöglichen, ein Inserat mit mindestens einem Foto und einer Beschreibung zu erstellen. | Muss |
| FA-02 | Das System muss eine Chat-Funktion bereitstellen, damit zwei Nutzer die Details einer Übergabe klären können. | Muss |
| FA-03 | Nutzer müssen die Möglichkeit haben, andere Nutzer nach einem abgeschlossenen Tausch mit 1-5 Sternen zu bewerten. | Muss |
| FA-04 | Inserate müssen einer vordefinierten Kategorie (z.B. "Kleidung", "Haushalt") zugeordnet werden. | Muss |
| FA-05 | Das System muss eine Suchleiste zur Verfügung stellen, mit der Inserate nach Schlüsselwörtern durchsucht werden können. | Soll |
| FA-06 | Nutzer müssen eine persönliche "Merkliste" führen können, auf der sie interessante Inserate speichern. | Kann |

### 3.2. Nicht-funktionale Anforderungen

| ID | Anforderung | Kategorie |
| :--- | :--- | :--- |
| NFA-01 | Die App muss auf den gängigsten iOS- und Android-Versionen der letzten 3 Jahre lauffähig sein. | Kompatibilität |
| NFA-02 | Das Hochladen eines Bildes für ein Inserat darf bei einer durchschnittlichen mobilen Datenverbindung (10 Mbit/s) nicht länger als 5 Sekunden dauern. | Performance |
| NFA-03 | Die Standortdaten der Nutzer dürfen nur auf Bezirksebene gespeichert und angezeigt werden, niemals die exakte Adresse. | Datenschutz (Privacy) |
| NFA-04 | Die App muss eine intuitive Bedienung ermöglichen, sodass Nutzer ohne Einarbeitung ein Inserat erstellen oder ein Angebot machen können. | Benutzbarkeit (Usability) |

---

## 4. Projektrisiken

| ID | Risiko | Eintrittswahrscheinlichkeit | Auswirkung | Maßnahme |
| :--- | :--- | :--- | :--- | :--- |
| R-01 | **Geringe Nutzeraktivität:** Die App ist nur wertvoll, wenn genügend Tauschangebote vorhanden sind. | Hoch | Kritisch | Lokale Werbemaßnahmen (z.B. in Gemeindeblättern, Social-Media-Gruppen der Stadt). Anreize für die ersten 100 aktiven Nutzer schaffen. |
| R-02 | **Sicherheitsbedenken bei Übergaben:** Nutzer haben Angst, sich mit Fremden zu treffen, was die Akzeptanz der App hemmt. | Mittel | Hoch | Implementierung eines verlässlichen Bewertungssystems. Tipps für sichere Übergaben an öffentlichen Orten in die App integrieren. |
| R-03 | **Schlechte Qualität der Angebote:** Nutzer bieten nur "Müll" an, was die Attraktivität der Plattform senkt. | Mittel | Moderat | Community-Management: Nutzer können schlechte Inserate melden. Gamification-Elemente, die gute Anbieter belohnen. |
