# Software Requirements Specification (SRS) - Vorlage
## (Pflichtenheft)

**Projekttitel:** [Name des Projekts]

**Dokumentenversion:** 1.0

**Erstellungsdatum:** YYYY-MM-DD

**Autor(en):** [Name/n des/der Autoren, z.B. Systemarchitekt, Lead Developer]

**Genehmigende Personen/Rollen:** [Name/n oder Rolle/n, z.B. Projektleiter, Technischer Leiter]

---

## Dokumentenhistorie

| Version | Datum        | Autor         | Änderungsbeschreibung                               |
| :------ | :----------- | :------------ | :-------------------------------------------------- |
| 1.0     | YYYY-MM-DD   | [Autor]       | Initiale Erstellung basierend auf URD Version [URD Version]. |
|         |              |               |                                                     |

---

## 1. Einleitung

### 1.1. Zweck des Dokuments
Dieses Dokument spezifiziert die detaillierten Software-Anforderungen für das System [Systemname]. Es dient als technische Umsetzungsvorgabe für das Entwicklungs- und Testteam und konkretisiert die im User Requirements Document (URD) beschriebenen Anforderungen.

### 1.2. Projektumfang (Scope)
Der Umfang dieses Dokuments deckt die technische Spezifikation aller unter Abschnitt 1.2 des URD genannten "In Scope"-Punkte ab.

### 1.3. Zielgruppe

Dieses Dokument richtet sich primär an:
- Entwicklerteam
- Systemarchitekten
- Test- & QA-Team
- Datenbankadministratoren
- Technische Projektleiter

### 1.4. Definitionen, Akronyme und Abkürzungen

| Begriff | Beschreibung |
| :--- | :--- |
| SRS | Software Requirements Specification |
| API | Application Programming Interface |
| DB | Datenbank |
| ... | ... |

---

## 2. Allgemeine Beschreibung

### 2.1. Systemarchitektur und Produktperspektive
Das System [Systemname] wird als [z.B. Microservice-Architektur, 3-Schicht-Anwendung, Serverless-Anwendung] auf Basis von [Technologie-Stack, z.B. .NET Core, Node.js mit React] entwickelt. Es integriert sich in die bestehende Systemlandschaft wie folgt: [Diagramm oder Beschreibung der Systemintegration].

### 2.2. Allgemeine Einschränkungen (Constraints)
- **Programmiersprache:** [z.B. C#, Java, Python]
- **Datenbank:** [z.B. PostgreSQL, MongoDB]
- **Hosting-Umgebung:** [z.B. Azure Cloud, On-Premise VMWare Cluster]
- **Frameworks/Bibliotheken:** [z.B. React, Angular, Spring Boot]

### 2.3. Annahmen und Abhängigkeiten
- Die API von [System A] liefert Daten im spezifizierten Format und mit einer Latenz von unter 200ms.
- Das Entwicklerteam hat Zugriff auf die notwendigen Lizenzen für [Software X].

---

## 3. Spezifische Anforderungen

### 3.1. Funktionale Anforderungen (Systemsicht)

Hier werden die funktionalen Anforderungen aus dem URD technisch detailliert.

| URD-ID | SRS-ID | Anforderung (technische Sicht) | Akzeptanzkriterien (technisch) |
| :--- | :--- | :--- | :--- |
| FR-001 | **SRS-FR-001** | Das System muss die Registrierung eines neuen Benutzers über einen POST-Request an den Endpunkt `/api/users/register` ermöglichen. | - E-Mail muss RFC 5322 konform sein. <br> - Passwort muss mit BCrypt gehasht werden. <br> - Ein neuer Eintrag wird in der Tabelle `Users` erstellt. |
| FR-003 | **SRS-FR-002** | Das System muss die Aktualisierung von Profildaten über einen PUT-Request an `/api/users/{userId}` ermöglichen. | - Nur der authentifizierte Benutzer darf seine eigenen Daten ändern. <br> - Die `updated_at` Spalte in der DB wird aktualisiert. |
| ... | ... | ... | ... |

### 3.2. Schnittstellenanforderungen (Interface Requirements)

#### 3.2.1. Externe Software-Schnittstellen (API)

**API-Endpunkt: `GET /api/products`**
- **Beschreibung:** Ruft eine Liste aller verfügbaren Produkte ab.
- **Request-Parameter:** `?category={string}`, `?limit={int}`
- **Response (Success, 200 OK):**
  ```json
  [
    {
      "productId": "string",
      "name": "string",
      "price": "number"
    }
  ]
  ```
- **Response (Error, 404 Not Found):**
  ```json
  { "error": "Category not found" }
  ```

#### 3.2.2. User Interface (UI)
- Das UI muss responsive sein und auf den Viewports 360px (mobil), 768px (Tablet) und 1200px (Desktop) korrekt dargestellt werden.
- Alle interaktiven Elemente müssen die im Styleguide definierten Zustände (hover, active, disabled) implementieren.

### 3.3. Nicht-funktionale Anforderungen (messbar)

| URD-ID | SRS-ID | Kategorie | Anforderung (messbar und testbar) |
| :--- | :--- | :--- | :--- |
| NFR-001 | **SRS-NFR-001** | **Performance** | Die Time to First Byte (TTFB) für den Endpunkt `/api/products` muss bei 100 gleichzeitigen Benutzern unter 250ms liegen. |
| NFR-003 | **SRS-NFR-002** | **Sicherheit** | Alle API-Endpunkte (außer `/login` und `/register`) müssen durch ein gültiges JWT (JSON Web Token) geschützt sein. |
| NFR-004 | **SRS-NFR-003** | **Zuverlässigkeit** | Die API muss einen Health-Check-Endpunkt `/api/health` bereitstellen, der den Status der DB-Verbindung zurückgibt. |
| ... | ... | ... | ... |

---

## 4. Datenmodell

### 4.1. Konzeptionelles Datenmodell (ER-Diagramm)
[Hier ein Bild oder eine Beschreibung des Entity-Relationship-Diagramms einfügen, das die Hauptentitäten und ihre Beziehungen zeigt.]

![](images/er-diagram-example.png)

### 4.2. Logisches Datenmodell (Tabellen)

**Tabelle: `Users`**
| Spaltenname | Datentyp | Constraints | Beschreibung |
| :--- | :--- | :--- | :--- |
| `id` | UUID | PRIMARY KEY | Eindeutiger Identifikator |
| `email` | VARCHAR(255) | NOT NULL, UNIQUE | E-Mail-Adresse des Benutzers |
| `password_hash` | VARCHAR(255) | NOT NULL | Gehashtes Passwort |
| `created_at` | TIMESTAMP | NOT NULL | Zeitstempel der Erstellung |

---

## 5. Anhänge
- **Anhang A:** [Link zu detaillierten UML-Diagrammen (Sequenz-, Aktivitätsdiagramme)]
- **Anhang B:** [Link zur API-Spezifikation (z.B. OpenAPI/Swagger-Dokumentation)]
- **Anhang C:** [Referenz auf den URD]
