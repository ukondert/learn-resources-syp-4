# Projektaufgabe: Digitales Sammelalbum für In-Game-Items

**Version:** 2.0
**Datum:** 2025-08-15

---

## 1. Projektbeschreibung & Zielsetzung

In diesem Projekt soll eine Desktop-Anwendung zum Thema "Digitales Sammelalbum für In-Game-Items" entwickelt werden. Ziel ist es, eine robuste, wartbare und benutzerfreundliche Software zu erstellen, in der Spieler ihre Sammlung an digitalen Gegenständen (Skins, Items, Erfolge) aus verschiedenen Computerspielen katalogisieren, verwalten und präsentieren können. Die App soll es Gamern ermöglichen, den Überblick über ihre Sammlungen zu behalten und ihren Fortschritt zu visualisieren.

## 2. Rahmenbedingungen & Vorgehen
-   **Teamgröße:** 4 Personen
-   **Rollen:** 
    -   Projektleiter/Scrum Master
    -   Frontend-Entwickler
    -   Backend-Entwickler
    -   Datenbank-Spezialist/Tester
-   **Zeitlicher Umfang:** 21 Unterrichtseinheiten (ca. 17.5 Stunden)
-   **Projektmethode:** Scrum
-   **Projektmanagement-Tool:** Das Team kann für die Verwaltung der Anforderungen und des Projektfortschritts zwischen **Trello** oder **GitHub Projects** (inkl. Issues) wählen.

## 3. Technische Anforderungen (Stack)
-   **Programmiersprache:** Java
-   **Architektur:** Layered Architecture
-   **UI-Framework:** JavaFX
-   **Datenpersistenz:** H2-Datenbank mit JDBC
-   **Design Patterns:** Singleton, Factory

## 4. Anforderungen & Dokumentation

### 4.1. Startinformationen

Das Projekt startet mit den folgenden grundlegenden User Stories (Product Backlog Items). Eure erste Aufgabe als Team ist es, diese User Stories zu verfeinern und detaillierte Akzeptanzkriterien zu erarbeiten.

**Product Vision:**
*Eine zentrale Anlaufstelle für Gamer, um ihre digitalen Schätze aus allen Lieblingsspielen zu sammeln, zu organisieren und stolz zu präsentieren.*

**Must-Have User Stories (Version 1.0):**
-   **Story 1:** Als neuer Benutzer möchte ich mich mit einem Benutzernamen und Passwort registrieren können, um ein persönliches Konto zu erstellen.
-   **Story 2:** Als registrierter Benutzer möchte ich mich in der App anmelden können, um auf meine Sammlungen zuzugreifen.
-   **Story 3:** Als angemeldeter Benutzer möchte ich ein neues Spiel (z.B. "League of Legends", "Valorant") zu meiner Bibliothek hinzufügen können, um Items dafür zu sammeln.
-   **Story 4:** Als angemeldeter Benutzer möchte ich ein neues Item zu einem Spiel hinzufügen können, wobei ich Name, Seltenheit (z.B. "Gewöhnlich", "Selten", "Episch") und ein Bild des Items angeben kann.
-   **Story 5:** Als angemeldeter Benutzer möchte ich alle gesammelten Items für ein ausgewähltes Spiel in einer übersichtlichen Galerieansicht sehen können.

### 4.2. Zu erstellende Dokumentation

Während des Projekts sind folgende Dokumente zu erstellen und zu pflegen:

-   **Product Backlog:** Vollständige User Stories (inkl. Akzeptanzkriterien), verwaltet im gewählten Tool (Trello/GitHub).
-   **Change Log:** Änderungen an Anforderungen werden direkt im gewählten Tool dokumentiert (z.B. durch Kommentare und Versionen/Labels).
-   **Testdokumentation:**
    -   **Backend:** Unit-Tests für die Geschäftslogik (als JUnit-Tests im Code).
    -   **Frontend:** Ein Testprotokoll (als Markdown-Datei im Repository), das die manuelle Überprüfung der Benutzeroberfläche dokumentiert.

## 5. Abgabekriterien & Bewertung

-   **Funktionstüchtige Anwendung:** Die Software erfüllt alle selbst erarbeiteten Anforderungen und ist lauffähig.
-   **Codequalität:** Der Code ist sauber, gut strukturiert, kommentiert und folgt den Prinzipien der Layered Architecture.
-   **Dokumentation:** Das Product Backlog und das Change Log sind im gewählten Tool nachvollziehbar gepflegt. Die Testdokumentation ist vollständig.
-   **Technische Umsetzung:** Die vorgegebenen Technologien und Design Patterns wurden korrekt eingesetzt.
-   **Abschlusspräsentation:** Das Team präsentiert das fertige Produkt, die technische Umsetzung und die Erfahrungen im Projekt (ca. 15 Minuten).

> <span style="font-size: 1.5em">:bulb:</span>Die angeführten User-Stories stellen die Mindestanforderung an das Projekt dar. Für eine bessere Bewertung sollten die Anforderungen mit eigenen User-Stories erweitert werden, auch wenn diese nicht aktuell umgesetzt werden (`nice-to-have` Features, die in einem theoretisch folgendem Release umgesetzt werden) 