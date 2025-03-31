# Testkonzept DICOM Viewer – Version 2

## 1. Einleitung
Dieses Testkonzept beschreibt die Teststrategie für den DICOM Viewer mit Fokus auf die neuen Features **Brushing** und **Drag & Drop**. Ziel ist es, eine hohe Softwarequalität und Benutzerfreundlichkeit sicherzustellen. Falls weitere Implementierungen hinzukommen, wird das Testkonzept entsprechend erweitert, genauso wird das Testkonzept gekürzt, falls bestimmte Funktionalitäten nicht implementiert wurden.

## 2. Testarten

### 2.1 Unit Tests
Unit Tests werden im Rahmen dieses Projekts nicht durchgeführt. Laut Kundenfeedback sind sie zu zeitaufwendig und komplex, weshalb der Fokus auf anderen Testarten liegt. Stattdessen setzen wir verstärkt auf **Integrationstests** und **manuelle Überprüfungen** der Funktionalitäten.

### 2.2 GUI Tests
Die Benutzeroberfläche des DICOM Viewers wird primär **manuell getestet**. Da die Software stark auf visuelle Interaktionen setzt, sind automatisierte GUI-Tests weniger sinnvoll. Stattdessen werden **explorative Tests** durchgeführt, um eine intuitive und reibungslose Bedienbarkeit sicherzustellen.

Beim **Brushing-Feature** testen wir folgende Funktionalitäten:
- Die Pinselgröße und -intensität werden korrekt angewendet.
- Verschiedene Eingabemethoden (Maus, Touch) funktionieren zuverlässig.
- Die Rückgängig- und Wiederherstellen-Funktion arbeitet problemlos.
- Verhalten der Markierung beim Anpassen der Fenstergröße.
- Wird jeder Pixel markiert? (Je nach Schnelligkeit der Bewegung).
- Intuitive Bedienung durch Tests mit Drittpersonen, die das Projekt nicht kennen.

Beim **Drag & Drop-Feature** wird geprüft, ob:
- Einzelne und mehrere DICOM-Dateien problemlos geladen werden können.
- Der Viewer auf inkompatible Dateiformate angemessen reagiert.
- Sehr große Dateien ohne größere Verzögerung verarbeitet werden.

### 2.3 Stress-Tests
Da der DICOM Viewer große Bilddateien und komplexe Markierungen verarbeiten muss, planen wir **Belastungstests** durchzuführen. Hierzu werden verschiedene Szenarien simuliert, darunter:
- Das Laden sehr großer DICOM-Dateien sowie mehrerer hintereinander.
- Intensive Brushing-Vorgänge (großflächiges Markieren und Speichern).
- Überprüfung auf Verzögerungen oder sonstige Probleme beim erneuten Anzeigen.

### 2.4 Usability-Tests
Die Hauptanwender des DICOM Viewers sind **Radiologen, medizinisches Fachpersonal und Bildanalysten**. Diese verfügen über unterschiedliche Vorkenntnisse im Umgang mit DICOM-Software, jedoch haben sie in der Regel eine grundlegende Erfahrung mit medizinischer Bildbearbeitung.

Um die Benutzerfreundlichkeit sicherzustellen, wird die Software in realistischen Anwendungsfällen getestet. Dabei werden folgende Aspekte evaluiert:
- Wie intuitiv lassen sich Brushing und Drag & Drop nutzen?
- Gibt es potenzielle Stolpersteine bei der Bedienung?
- Wie effizient können Anwender ihre Aufgaben mit dem Viewer durchführen?

Das Entwicklungsteam führt erste Usability-Tests durch. Falls möglich, werden zusätzlich Rückmeldungen vom Kunden oder deren Mitarbeitern eingeholt, sowie von Drittpersonen, die auch das GUI testen, um weitere Optimierungsmöglichkeiten zu identifizieren.

## 3. Datenbank-Tests
Da der DICOM Viewer Brushing-Daten speichern und wieder laden können muss, ist eine zuverlässige **Datenbankintegration** essenziell.

Es wird geprüft, ob:
- Die Markierungsdaten korrekt gespeichert und wiederhergestellt werden.
- Wiederholtes Speichern und Laden die Datenintegrität gewährleistet.
- Die Datenbank auch große Mengen an Brushing-Daten performant verwalten kann.

## 4. Integrationstests
Um eine reibungslose Zusammenarbeit aller Softwarekomponenten zu gewährleisten, werden verschiedene **Integrationstests** durchgeführt. Diese decken typische Nutzungsszenarien ab, darunter:
- Das Markieren eines Bereichs, Speichern des Bildes und erneutes Laden zur Kontrolle.
- Das Testen des Drag & Drop-Features mit verschiedenen Dateiformaten und -größen.

Zusätzlich werden Spezial- und Grenzfälle geprüft, z. B.:
- Markierungen an den Bildrändern.
- Überlappende Markierungen.
- Das Verhalten der Software beim Import fehlerhafter oder inkompatibler Dateien.

## 5. Installationstests
Der DICOM Viewer wird auf verschiedenen Betriebssystemen getestet, um eine breite **Kompatibilität** sicherzustellen. Getestet werden:
- **Windows, Linux und macOS** als Betriebssysteme.
- **Chrome, Edge und Firefox** als unterstützte Browser.

Es wird überprüft, ob:
- Die Software korrekt dargestellt wird und die Brushing-Funktion einwandfrei arbeitet.
- Keine zusätzlichen Installationsschritte erforderlich sind.
- Die Drag & Drop-Funktion auf allen Plattformen stabil läuft.

## 6. Dokumentation und Fehlerverwaltung
Jede Testdurchführung wird systematisch **dokumentiert**, um eine lückenlose Nachverfolgbarkeit der Testergebnisse zu gewährleisten. Fehler werden in **Trello** erfasst und priorisiert.

Um sicherzustellen, dass erkannte Fehler behoben werden, erfolgt nach jedem Bugfix ein gezielter erneuter Test. Kritische Fehler haben dabei höchste Priorität und werden umgehend bearbeitet.
