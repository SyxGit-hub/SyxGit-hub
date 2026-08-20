# Bestandsaufnahme: stromfazit.de (Repo `SyxGit-hub/stromfazit`)

> Abgleich der Portfolio-Evaluation (docs/02) mit dem tatsächlichen Stand des bestehenden Projekts. Stand: 19.08.2026, Branch `release`, Commit `1e0c954`.

## Was bereits live ist

Das Projekt ist deutlich weiter als „ein Energiekosten-Rechner" — es ist bereits ein kleines Hub-and-Spoke-Netzwerk auf einer Domain (exakt die in docs/03 empfohlene Architektur) mit der Marke **„Stromfazit — Rechner mit ehrlichem Fazit"** (die Neutralitäts-Positionierung nach Akkudoktor-Muster aus der Evaluation):

| Seite | Entspricht Evaluations-Projekt | Status |
|---|---|---|
| `stromtarif-schnellcheck.html` | Dynamik-Tarif-Check (Hub-Funktion) | ✅ live |
| `lastprofil-analyzer.html` | **Lastprofil-Labor** (Top-Score 37,5) | ✅ live |
| `14a-enwg-rechner.html` | **§14a-Modul-Rechner** (37,0) | ✅ live |
| `waermepumpe-rechner.html` | **Wärmepumpen-Check** (33,5) | ✅ live (Förder-Logik vorhanden — prüfen: BEG-Stand 21.07.2026?) |
| `balkonkraftwerk-speicher.html` | BKW-Speicher-Rechner (27,5) | ✅ live |
| `smart-meter-pflicht.html` | Smart-Meter-Check | ✅ live |
| `eauto-ladekosten.html` | E-Auto-Content (statt V2G-Cockpit — genau richtig) | ✅ live |
| `ueber-uns.html`, Impressum, Datenschutz | EEAT-Fundament | ✅ live |
| `scripts/fetch_smard.py` + GitHub Actions (monatlich/jährlich) + `data/spot/2023–2026` | **Börsenpreis-Datenschicht** | ✅ live, automatisiert |
| `scripts/sync_jsonld.py` (FAQPage-JSON-LD aus sichtbarem FAQ) | GEO-/AI-Zitierbarkeits-Baustein | ✅ live |
| `partner.json` mit 4 Slots (dynamic_tariff, fixed_tariff, balkonspeicher, waermepumpe) + sauberem Disclosure-Text | Affiliate-Infrastruktur | ⚠️ **gebaut, aber alle `partners`-Arrays sind LEER** |

Damit sind **Phase 1 und 2a der Roadmap (docs/04) im Wesentlichen schon gebaut.** Drei einstimmige „Bauen"-Projekte existieren bereits als Tools.

## Die Lücken (nach Hebelwirkung sortiert)

### 1. Die Seite verdient null Euro — Monetarisierung ist die einzige echte Baustelle
Die gesamte Partner-Infrastruktur existiert, aber `partner.json` ist leer: kein einziger Affiliate-Link, kein Lead-Funnel. Die Evaluation zeigt, was das kostet: EPV 1–5 € auf der WP-Strecke, 0,60–2 € auf der Wechselstrecke — aktuell realisiert: 0 €.

**Sofortmaßnahmen (kein neues Tool nötig):**
- Partnerprogramme beantragen: **Check24-Partnerprogramm** (20 € stornofrei/Lead, White-Label-Rechner), **Awin/Verivox** (~20 €/Abschluss, auch Heizstrom für den §14a-Rechner), **energyAds** (E.ON, MAINGAU …), Referral-Programme der Dynamik-Anbieter (Tibber, Ostrom, Rabot) für den `dynamic_tariff`-Slot, **Kleines Kraftwerk/Yuma/priwatt** (bis 10 %/Sale) für den `balkonspeicher`-Slot.
- `partner.json`-Slots füllen — die Anzeige-Logik existiert schon.
- **WP-Lead-Strecke ergänzen:** Der `waermepumpe`-Slot verweist bisher nur auf „Angebote vergleichen". Die wertvollste Monetarisierung (50–120 €/Lead via DAA/TapTapHome oder Aroundhome) braucht ein eigenes Anfrage-Formular nach dem Muster „Ergebnis zuerst, dann optional 3 Angebote" — das größte fehlende Umsatz-Stück.

### 2. Newsletter fehlt komplett
Kein Formular, kein Verteiler. Der Owned Channel ist laut Recherche der wichtigste Google-unabhängige Kanal (Finanztip-Muster). Natürliche Anlässe sind schon da: Preisalarm aus der Spot-Datenschicht, „Wechsel-Erinnerung nach 11 Monaten" aus dem Schnellcheck.

### 3. Solarspitzen-Radar ist quasi geschenkt
Die Daten liegen bereits im Repo: `summary.json` enthält den Negativpreis-Anteil pro Jahr — **2023: 3,4 % → 2024: 5,2 % → 2025: 6,5 % → 2026 (YTD): 7,1 %**. Ein strukturell wachsender, presse-tauglicher Trend aus der eigenen Datenpipeline. Der in der Evaluation geschätzte 3-Wochen-Aufwand schrumpft auf ~1–2 Wochen, weil Datenlayer und Automatisierung existieren.

### 4. Energy-Sharing-Kompass (First-Mover-Fenster läuft)
§42c gilt seit 01.06.2026, noch existiert kein Verbraucher-Tool. Jeder Monat Wartezeit verkleinert den Vorsprung. Gate bleibt: Lead-Zahlungsbereitschaft bei metergrid/Solarize per E-Mail validieren, dann schlanke 2-Wochen-Version.

### 5. Kleinere Prüfpunkte
- **Wärmepumpen-Rechner auf BEG-Stand 21.07.2026 heben** (30 % Grundförderung, max. 28.000 €/WE) — das SEO-Fenster lebt davon, aktueller zu sein als die Konkurrenz.
- Interne Verlinkung als Diagnose-Routing schärfen (Hub erkennt >6.000 kWh → §14a; hohe Heizkosten → WP-Rechner) — Seiten existieren, das kontextuelle Weiterreichen der Eingabedaten laut docs/03 prüfen/ausbauen.
- Später (Phase 3 unverändert): Netzentgelt-Atlas, Widget-Gratis-Tier (der Spot-Datenlayer ist das halbe Widget), PV-Rechner.

## Revidierte Roadmap

Die ursprüngliche Phase 0–2 aus docs/04 ist größtenteils gebaut. Neue Reihenfolge:

1. **Monetarisierung an (1–2 Wochen):** Partnerprogramme beantragen → `partner.json` füllen → WP-Lead-Formular bauen → EPV-Tracking pro Slot.
2. **Newsletter an (wenige Tage):** Formular + Double-Opt-in + erster Anlass (Preisalarm).
3. **BEG-Stand prüfen/aktualisieren** im Wärmepumpen-Rechner (SEO-Fenster).
4. **Solarspitzen-Radar** aus vorhandener Datenschicht (~1–2 Wochen) — inkl. monatlichem „Negativpreis-Index" als Presse-/AI-Zitier-Asset.
5. **Energy-Sharing-Kompass** nach Lead-Preis-Validierung (2 Wochen).
6. Danach Phase 3 wie geplant (Netzentgelt-Atlas zur Okt/Nov-Runde, Widgets, PV).

**Kernbotschaft:** Nicht mehr bauen ist der Engpass — **verdienen** ist es. Die Seite hat drei einstimmig empfohlene Tools live und null Monetarisierung aktiv.
