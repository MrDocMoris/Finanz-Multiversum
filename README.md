# Finanz-Multiversum

Deine eigene kleine Finanz-App – ähnlich wie Finanzguru, aber nur für dich und komplett auf deinem Handy. Gleicher Stil und gleicher Update-Weg wie TCG Multiversum, Familien-Multiversum und Metin2-Multiversum.

## Funktionen
- **Startseite**: Kontostand gesamt und je Konto, Einnahmen/Ausgaben des Monats, „frei bis Monatsende“ (Kontostand minus noch kommende Fixkosten), Hinweise und die nächsten Abbuchungen
- **Buchungen**: Ausgaben, Einnahmen und Umbuchungen (z. B. Geld abheben) in Sekunden eintragen; die Kategorie wird aus dem Namen erraten (Rewe → Lebensmittel, Aral → Tanken …) und die App lernt aus deinen Korrekturen; Suche über alle Monate
- **Verträge & Fixkosten**: Miete, Handy, Versicherungen, Abos … monatlich, vierteljährlich, halbjährlich oder jährlich; werden am Fälligkeitstag automatisch gebucht; Fixkosten pro Monat und Jahr
- **Kündigungsfristen**: Mindestlaufzeit, Frist und Verlängerung eintragen; die App rechnet aus, bis wann du kündigen musst, erinnert per Push (z. B. 30, 7 und 1 Tag vorher) und schreibt dir das Kündigungsschreiben
- **Fixkosten-Erkennung**: wiederkehrende Zahlungen in deinen Buchungen werden erkannt und als Vertrag vorgeschlagen
- **Budgets** pro Kategorie mit Fortschrittsbalken, Warnung beim Überziehen und „ca. X € pro Tag übrig“
- **Spartöpfe** mit Ziel, Datum und „so viel pro Monat nötig“
- **Auswertung**: Ausgaben nach Kategorie (Kreisdiagramm), letzte 6 Monate, Vergleich zum Vormonat, Sparquote, Jahressumme
- **ING-Import (optional)**: CSV aus dem ING-Banking laden, doppelte werden übersprungen, Kontostand kann übernommen werden
- **CSV-Export** (z. B. für die Steuer), automatische Sicherung in *Dokumente/Finanz-Multiversum*, Update-Prüfung

## Datenschutz
Es gibt keine Verbindung zur Bank und keinen Server. Alle Daten liegen nur auf deinem Handy (und in der Sicherungsdatei). Dieses Repo enthält nur den App-Code, keine Finanzdaten.

## Aufbau
- `finanz.html` – die komplette App (HTML/CSS/JS), läuft auch im Browser zum Testen
- `assets/icon.svg` – App-Icon
- `.github/workflows/build-apk.yml` – baut bei jeder Änderung die Android-App, signiert sie mit `signing/debug.keystore` (wird beim ersten Lauf angelegt), veröffentlicht sie als Release und schreibt `app/version.json`
