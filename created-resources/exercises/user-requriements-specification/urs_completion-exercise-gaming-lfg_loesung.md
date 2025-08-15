# User Requirement Specification (URS) - "TeamUp" LFG-Plattform - Musterlösung

**Version:** 1.0
**Datum:** 2025-08-15

---

## 1. Einleitung

### 1.1. Projektübersicht

Online-Gaming ist oft ein Team-Erlebnis. Viele Spieler haben jedoch Schwierigkeiten, passende Mitspieler für ihre Lieblingsspiele zu finden. Zufällige Mitspieler (Randoms) führen oft zu Frustration aufgrund unterschiedlicher Spielstile, Kommunikationsprobleme oder toxischen Verhaltens.

Das Projekt "TeamUp" zielt darauf ab, eine dedizierte Plattform (Web-App und Mobile-App) zu entwickeln, die es Gamern ermöglicht, gezielt nach Mitspielern zu suchen und Gruppen zu bilden. Die Plattform soll das Spielerlebnis verbessern, indem sie Spieler mit ähnlichen Zielen und Einstellungen zusammenbringt.

### 1.2. Ziele

*   **Primärziel:** Eine benutzerfreundliche Plattform schaffen, auf der Spieler schnell und einfach passende Mitspieler oder Gruppen für spezifische Online-Games finden können.
*   **Sekundärziel 1:** Die Qualität des Online-Spielens durch besseres Matchmaking verbessern und Frustration reduzieren.
*   **Sekundärziel 2:** Eine Community-Funktion integrieren, die es Spielern ermöglicht, Freundeslisten zu pflegen und wiederkehrende Gruppen zu bilden.

### 1.3. Geltungsbereich (Scope)

**In-Scope (Was das System leisten wird):**
*   Benutzerprofile mit Gaming-relevanten Informationen (Spiele, Spielstil, Online-Zeiten).
*   Erstellung von Suchanfragen ("Suche Gruppe für Spiel X, Modus Y").
*   Erstellung von Gruppenangeboten ("Biete 2 Plätze für Spiel Z, ab 18 Uhr").
*   Ein einfaches Bewertungssystem, um die Zuverlässigkeit von Mitspielern zu bewerten.
*   Freundeslisten und private Chat-Funktionen.

**Out-of-Scope (Was das System NICHT leisten wird):**
*   Direkte Integration in die Spiele (kein automatischer Login oder Gruppeneinladung im Spiel selbst).
*   Voice-Chat-Funktionen (Nutzer sollen weiterhin externe Tools wie Discord verwenden).
*   Turnier-Organisation oder Liga-Management.

---

## 2. Systembeschreibung

### 2.1. Akteure & Stakeholder

| Akteur/Stakeholder | Beschreibung |
| :--- | :--- |
| **Registrierter Spieler** | Hauptnutzer der Plattform. Kann Profil erstellen, suchen, Gruppen beitreten/erstellen und andere bewerten. |
| **Moderator** | Überprüft gemeldete Inhalte (Profile, Chats) und kann Nutzer bei Verstößen gegen die Community-Richtlinien verwarnen oder sperren. |
| **Administrator** | Verwaltet die gesamte Plattform, hat Zugriff auf alle Daten, pflegt die Liste der unterstützten Spiele und verwaltet die Moderatoren. |
| **Plattformbetreiber** | Ist am wirtschaftlichen Erfolg und am Wachstum der Plattform interessiert. |

### 2.2. Use Cases (Anwendungsfälle)

**Use-Case-Liste:**
*   UC-01: Als Spieler registrieren
*   UC-02: Spielerprofil verwalten
*   UC-03: Nach einer Gruppe suchen
*   UC-04: Eine Gruppe erstellen und anbieten
*   UC-05: Einer Gruppe beitreten
*   UC-06: Mitspieler nach einer Session bewerten
*   UC-07: Spieler zur Freundesliste hinzufügen/entfernen
*   UC-08: Privaten Chat mit einem Freund führen
*   UC-09: Spieler oder Inhalt melden

---
**Detaillierter Use Case:**

| Use Case ID | UC-03 |
| :--- | :--- |
| **Use Case Name** | Nach einer Gruppe suchen |
| **Akteure** | Registrierter Spieler |
| **Kurzbeschreibung** | Ein Spieler sucht nach offenen Gruppen für ein bestimmtes Spiel und kann die Suche durch Filter verfeinern. |
| **Vorbedingungen** | Der Spieler ist eingeloggt. Es gibt mindestens eine erstellte Gruppe im System. |
| **Standardablauf (Happy Path)** | 1. Der Spieler wählt die Funktion "Gruppe suchen".<br>2. Der Spieler wählt das gewünschte Spiel aus einer Liste aus.<br>3. Das System zeigt eine Liste aller offenen Gruppen für dieses Spiel an.<br>4. Der Spieler filtert die Liste nach Spielmodus (z.B. "Ranked", "Casual") und Sprache.<br>5. Das System aktualisiert die Liste entsprechend der Filter.<br>6. Der Spieler wählt eine Gruppe aus der Liste aus, um Details anzuzeigen. |
| **Nachbedingungen** | Dem Spieler wird eine gefilterte Liste von Gruppenangeboten angezeigt. |
| **Fehlerfälle & Ausnahmen** | - **Keine Gruppen gefunden:** Das System zeigt eine Meldung an: "Für deine Suche wurden keine Gruppen gefunden. Erstelle doch selbst eine!"<br>- **Ungültige Filterkombination:** Das System ignoriert den ungültigen Filter und zeigt eine entsprechende Hinweismeldung. |

---

## 3. Anforderungen

### 3.1. Funktionale Anforderungen

| ID | Anforderung | Priorität |
| :--- | :--- | :--- |
| FA-01 | Das System muss eine Benutzerregistrierung mittels E-Mail und Passwort ermöglichen. | Muss |
| FA-02 | Ein Spieler muss sein Profil mit Informationen zu seinen Spielen, seinem Spielstil (z.B. "Ehrgeizig", "Entspannt") und seinen üblichen Online-Zeiten bearbeiten können. | Muss |
| FA-03 | Das System muss eine Suchfunktion mit Filtern für Spiel, Modus, Sprache und Mindestbewertung bieten. | Muss |
| FA-04 | Spieler müssen die Möglichkeit haben, anderen Spielern nach einer gemeinsamen Session eine Bewertung (z.B. 1-5 Sterne) und einen kurzen Kommentar zu geben. | Soll |
| FA-05 | Das System muss eine Meldefunktion für unangemessenes Verhalten oder Inhalte bereitstellen, die an die Moderatoren weitergeleitet wird. | Muss |
| FA-06 | Spieler müssen eine Freundesliste führen können. | Soll |

### 3.2. Nicht-funktionale Anforderungen

| ID | Anforderung | Kategorie |
| :--- | :--- | :--- |
| NFA-01 | Die Suchergebnisse für Gruppenanfragen müssen innerhalb von 2 Sekunden angezeigt werden, auch bei 10.000 gleichzeitigen Nutzern. | Performance |
| NFA-02 | Die Benutzeroberfläche muss so gestaltet sein, dass ein neuer Nutzer ohne Anleitung in der Lage ist, eine Gruppe zu finden oder zu erstellen. | Benutzbarkeit (Usability) |
| NFA-03 | Alle Passwörter und privaten Chat-Nachrichten müssen verschlüsselt in der Datenbank gespeichert werden. | Sicherheit |
| NFA-04 | Die Plattform muss eine Verfügbarkeit von 99.8% aufweisen. | Zuverlässigkeit |

---

## 4. Projektrisiken

| ID | Risiko | Eintrittswahrscheinlichkeit | Auswirkung | Maßnahme |
| :--- | :--- | :--- | :--- | :--- |
| R-01 | **Kritische Masse an Nutzern wird nicht erreicht:** Die Plattform ist nur nützlich, wenn genügend Spieler sie aktiv nutzen. | Hoch | Kritisch | Marketing-Kampagnen in sozialen Medien und Gaming-Foren zum Start. Partnerschaften mit kleinen Influencern. |
| R-02 | **Toxisches Verhalten schreckt Nutzer ab:** Wenn das Melde- und Moderationssystem nicht effektiv ist, verlassen "gute" Spieler die Plattform. | Mittel | Kritisch | Implementierung eines robusten Moderations-Tools. Klare Community-Richtlinien von Anfang an kommunizieren. |
| R-03 | **Spiele-APIs ändern sich:** Wenn die Plattform Spieldaten (z.B. unterstützte Modi) automatisch abruft, können Änderungen an den APIs zu Ausfällen führen. | Mittel | Moderat | Die Liste der Spiele und Modi manuell durch Administratoren pflegen lassen, anstatt sich auf externe APIs zu verlassen. |
