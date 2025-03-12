# Testkonzept DICOM Viewer

## 2. Testarten

### 2.1 Unit Tests
**Werden Unit Tests gemacht?**  
Nein, laut Kunde sehr zeifaufwendig und kompelx deshalb wird dies nicht erwartet.

---

### 2.2 GUI Tests
**Wird das GUI automatisiert oder manuell getestet?**  
- Da das GUI stark auf visuelle Interaktionen basiert, erfolgt das Testen hauptsächlich manuell.
- Explorative Tests durch das Entwicklungsteam

---

### 2.3 Stress-Tests
**Muss die Software hohen Belastungen standhalten?**  

Ja, insbesondere wenn große DICOM-Dateien mit vielen Markierungen verarbeitet werden.

**Testmethoden:**  
- Simulation großer DICOM-Bilder und intensiver Brushing-Vorgänge
- Performance-Messungen zur Reaktionszeit des Viewers

---

### 2.4 Usability-Test
**Wer sind die künftigen Anwender der Software?**  
Radiologen, medizinisches Fachpersonal und Bildanalysten

**Vorkenntnisse der Anwender:**  
- Grundlegende Erfahrung mit DICOM Viewern
- Unterschiedliche Erfahrung im Umgang mit interaktiven Bildbearbeitungstools

**Wer testet die Software auf ihre Bedienbarkeit?**  
- Das Entwicklungsteam
- Falls möglich, Rückmeldungen vom Kunden resp. seinen Mitarbeitern

**Testdurchführung:**  
- Beobachtung der Interaktion mit dem Brushing-Feature
- Erfassung von Feedback zur Benutzerfreundlichkeit
- Anpassung basierend auf Testergebnissen

---

## 3. Datenbank-Tests
**Wie wird die Datenbank getestet?**  
- Prüfung, ob Brushing-Daten korrekt gespeichert und geladen werden

---

## 4. Integrationstests
**Wie werden die Storys getestet?**  
- Testfälle für typische User Stories (z. B. „Benutzer markiert einen Bereich, speichert und lädt das Bild erneut“)


**Testfälle für Spezial- und Grenzfälle:**  
- Markierung an den Bildrändern
- Überlappende Markierungen

---

## 5. Installationstests
**Auf welchen Systemen wird getestet?**  
- Windows, Linux und macOS?
- Browserkompatibilitätstests (Chrome, Edge, Firefox)

**Testkriterien:**  
- Korrekte Darstellung des Viewers und der Brushing-Funktion
- Sicherstellung, dass keine zusätzlichen Installationsschritte erforderlich sind :)

---

