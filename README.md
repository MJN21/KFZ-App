# KFZ-Konfigurator-App

Diese Konsolenanwendung wurde in **.NET 6** mit **C#** entwickelt und verwendet **Entity Framework Core** sowie eine **SQLite-Datenbank**. Über ein einfaches Konsolenmenü können Benutzer Fahrzeuge bestellen, bestehende Bestellungen ändern oder stornieren.

## Verwendete Technologien

- **.NET 6 (C#)**
- **Entity Framework Core**
- **SQLite-Datenbank** 

## Kernfunktionen

1. **Fahrzeug bestellen**  
   - Benutzer gibt Vorname, Nachname und Geburtsdatum ein.  
   - Auswahl von Hersteller, Treibstoff, Motor und Farbe.  
   - Mehrfachauswahl von (Options).  
   - Automatische Preisberechnung und Zusammenfassung mit Bestellnummer.

2. **Bestellung ändern**  
   - Identifikation über Bestellnummer oder Nachname + Geburtsdatum.  
   - Hersteller, Motor, Farbe und Options können neu ausgewählt werden.  
   - Stammdaten (Vorname, Nachname, Geburtsdatum) bleiben unverändert.

3. **Bestellung stornieren**  
   - Identifikation über Bestellnummer oder Nachname + Geburtsdatum.  
   - Löscht die Bestellung endgültig aus der Datenbank.

## Datenbank (Schema & Seeding)

- **Hersteller**, **Treibstoff**, **Motor** und **Option** werden im `OnModelCreating`-Seeding automatisch in die Datenbank eingefügt.  
- **Bestellung** speichert die Kunden- und Fahrzeugdaten.  
- Eine n:m-Beziehung (Zwischentabelle `BestellungOptions`) ermöglicht mehrere Options pro Bestellung.

## Installation & Ausführen

 
1. **.NET 6 SDK** installieren (falls noch nicht vorhanden).  
2. Alle **Migrationen** sind bereits erstellt und angewendet, sodass Sie das Projekt **direkt** ausführen können.    
   - Die Anwendung kann dann direkt gestartet werden.  

Viel Spaß beim Ausprobieren :)
