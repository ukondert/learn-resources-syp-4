# User Requirement Specification (URS) - "TeamUp" LFG-Plattform

**Version:** 0.1 (Draft)
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

*Vervollständigen Sie diese Liste. Wer sind die wichtigsten Akteure und Stakeholder?*

| Akteur/Stakeholder | Beschreibung |
| :--- | :--- |
| **Registrierter Spieler** | Hauptnutzer der Plattform. Kann Profil erstellen, suchen, Gruppen beitreten/erstellen. |
| **Moderator** | ... |
| ... | ... |

### 2.2. Use Cases (Anwendungsfälle)

*Identifizieren Sie die wichtigsten Use Cases für das System und listen Sie sie auf. Arbeiten Sie anschließend EINEN davon detailliert aus.*

**Use-Case-Liste:**
*   UC-01: Als Spieler registrieren
*   UC-02: Spielerprofil verwalten
*   UC-03: Nach einer Gruppe suchen
*   ...
*   ...

---
**Detaillierter Use Case:**

| Use Case ID | UC-XX |
| :--- | :--- |
| **Use Case Name** | ... |
| **Akteure** | ... |
| **Kurzbeschreibung** | ... |
| **Vorbedingungen** | ... |
| **Standardablauf (Happy Path)** | 1. ...<br>2. ...<br>3. ... |
| **Nachbedingungen** | ... |
| **Fehlerfälle & Ausnahmen** | - ...<br>- ... |

---

## 3. Anforderungen

### 3.1. Funktionale Anforderungen

*Leiten Sie aus der Beschreibung und den Use Cases eine Liste von funktionalen Anforderungen ab.*

| ID | Anforderung | Priorität |
| :--- | :--- | :--- |
| FA-01 | Das System muss eine Benutzerregistrierung mittels E-Mail und Passwort ermöglichen. | Muss |
| FA-02 | ... | ... |
| FA-03 | ... | ... |
| ... | ... | ... |

### 3.2. Nicht-funktionale Anforderungen

*Formulieren Sie mindestens 3 relevante nicht-funktionale Anforderungen.*

| ID | Anforderung | Kategorie |
| :--- | :--- | :--- |
| NFA-01 | Die Suchergebnisse für Gruppenanfragen müssen innerhalb von 2 Sekunden angezeigt werden. | Performance |
| NFA-02 | ... | ... |
| NFA-03 | ... | ... |

---

## 4. Projektrisiken

*Identifizieren Sie mindestens 3 potenzielle Risiken für den Erfolg dieses Projekts.*

| ID | Risiko | Eintrittswahrscheinlichkeit | Auswirkung | Maßnahme |
| :--- | :--- | :--- | :--- | :--- |
| R-01 | **Kritische Masse an Nutzern wird nicht erreicht:** Die Plattform ist nur nützlich, wenn genügend Spieler sie aktiv nutzen. | Hoch | Kritisch | Marketing-Kampagnen in sozialen Medien und Gaming-Foren zum Start. |
| R-02 | ... | ... | ... | ... |
| R-03 | ... | ... | ... | ... |

---
*Dieses Dokument dient als Übung zur Vervollständigung im Rahmen des Unterrichts.*
