# Roadmap & Umsatzlogik

Sequenzierung nach drei Kriterien: (1) Zeit bis zum ersten Euro, (2) zeitkritische Fenster (BEG-Reform-SEO-Fenster, Heizsaison, Netzentgelt-Runde), (3) Infrastruktur-Wiederverwendung (Datenschichten zuerst dort bauen, wo sie mehrfach genutzt werden).

---

## Phase 0 — Hub monetarisieren (sofort, ~1 Woche)

Kein neues Projekt, sondern den vorhandenen Energiekosten-Rechner zu Geld machen:

- [ ] **Check24-Partnerprogramm** beantragen (alternativ/zusätzlich energyAds) und den **White-Label-Strom/Gas-Vergleichsrechner** einbetten: Der Rechner zeigt hohe Kosten → der Vergleich ist die logische nächste Aktion → 20 € stornofrei pro Lead auf ohnehin vorhandenem Traffic.
- [ ] **EEAT-Fundament:** Autorenprofil, Über-uns, Methodik-Seite, Impressum, Affiliate-Hinweis, Aktualisierungsdatum.
- [ ] **Newsletter-Setup** („Energiepreis-Update") mit Double-Opt-in — von Tag 1 sammeln.
- [ ] **EPV-Tracking:** Conversion-Messung pro Strecke einrichten (die Steuerungskennzahl des ganzen Netzwerks).
- [ ] **GEO-Baustein** auf der Hub-Seite: extrahierbare Zusammenfassung, aktuelle Zahlen („Strom August 2026: 32,95 ct Neukunden vs. ~40 ct Grundversorgung"), FAQ, Schema.org.

**Erwartung:** Erste Einnahmen binnen Wochen (abhängig vom Bestands-Traffic), ohne eine Zeile neues Rechner-Code.

---

## Phase 1 — Die sicheren Geld-Spokes (Monat 1–3)

### 1a. §14a-Modul-Rechner & Wärmepumpenstrom-Vergleich (3 Wochen)
Bestes Aufwand-Nutzen-Verhältnis, einstimmig „bauen". Unbesetzte Rechner-Nische, Heizstrom-Affiliate ab Tag 1, engste Hub-Verzahnung (Hub erkennt >6.000 kWh → verlinkt direkt).
- Gate vor Start: keins nötig. Modul 3 im MVP als „grobe Schätzung" kennzeichnen (Daten nur kommerziell verfügbar).

### 1b. Wärmepumpen-Vollkosten- & Förder-Check (6 Wochen)
Wertvollste Leads des Marktes (50–120 €, EPV 1–5 €), einstimmig „bauen". **Zeitkritisch:** Das SEO-Fenster nach GModG (10.07.2026) + BEG-Neustart (21.07.2026) schließt, sobald Finanztip & Co. ihre Inhalte aktualisiert haben — und der Herbst-Heizsaison-Peak steht vor der Tür. Enthält das reduzierte **BEG-Fördermodul** (statt eigenständigem Förder-Lotsen).
- Lead-Abnehmer parallel zum Bau onboarden (DAA/TapTapHome, Aroundhome) — nicht erst nach Launch.
- Muster: Ergebnis VOR der Kontaktdaten-Abfrage (Selfmade-Energy-Beweis).

**Meilenstein Ende Phase 1:** Zwei Geld-Strecken live, erster Lead-Umsatz, Newsletter wächst.

---

## Phase 2 — Differenzierung & Datenschicht (Monat 3–6)

### 2a. Lastprofil-Labor (5 Wochen)
Top-Score (37,5), einstimmig „bauen". Baut die **Börsenpreis-Datenschicht** (aWATTar + SMARD/energy-charts-Fallback), die drei weitere Projekte versorgt. Distribution über Foren (Photovoltaikforum, Akkudoktor) — funktioniert ohne Google-Autorität.
- CSV-Parsing clientseitig (DSGVO + Marketing-Argument).
- Parser iterativ: mit den 3–4 häufigsten Messstellenbetreiber-Formaten starten, Rest per Nutzer-Feedback.
- **Gate nach 3 Monaten:** EPV ehrlich messen (Auflage des Business-Judges). Referral-Einnahmen vs. Aufwand prüfen.

### 2b. Solarspitzen-Radar (3 Wochen)
Recycelt die Börsenpreis-Schicht aus 2a — deshalb NACH dem Labor. Presse-tauglich (Sommer-Negativpreis-Wellen), baut über den Negativpreis-Alarm die Newsletter-Liste.
- Monatlicher „Negativpreis-Index" als zitierfähige Statistik (AI-Overview- und Presse-Futter).

### 2c. Energy-Sharing-Kompass — schlanke Wette (2 Wochen)
First-Mover auf die stärkste dokumentierte Lücke (Gesetz seit 01.06.2026, null Verbraucher-Tools).
- **Gate VOR dem Bau:** Lead-Zahlungsbereitschaft per E-Mail bei metergrid/Solarize/items validieren. Ohne positives Signal: nur 5 Ratgeber-Seiten zur Keyword-Sicherung, kein Rechner.
- Umfang deckeln: Rechner + 10–15 Seiten, kein Portal. PR-Hook „erster Energy-Sharing-Rechner Deutschlands" aktiv ausspielen.

**Meilenstein Ende Phase 2:** Netzwerk-Newsletter als funktionierender Owned Channel; Domain sammelt Presse-Backlinks; 4–5 Spokes live.

---

## Phase 3 — Skalierung & Infrastruktur (Monat 6–12)

Reihenfolge innerhalb Phase 3 nach Kalender:

- **Netzentgelt-Atlas:** Datenpipeline (BNetzA-Excel) intern ab Monat 6 — öffentlicher Launch **zur Netzentgelt-Runde Oktober/November** mit Presse-Push („Netzentgelt-Report 2027"). Stadtseiten nur mit >25–30 % Unique-Daten.
- **Energie-Widgets, Gratis-Tier:** Börsenpreis-Widget, Grünstrom-Ampel, Mini-Rechner als Embeds mit Brand-Attributions-Link — der Linkbuilding-Motor für die YMYL-Autorität. Paid-Tier NUR bei nachweisbarer Inbound-Nachfrage.
- **PV-Rechner & Solar-Atlas:** Erst jetzt (Domain hat Autorität, Lead-Prozesse aus dem WP-Check erprobt). Ggf. Atlas-Teil (MaStR-Stadtseiten als Backlink-Asset) vor dem Rechner-Teil.
- **Balkonkraftwerk-Speicher-Rechner:** Volumen-Zubringer, 3 Wochen, recycelt PVGIS-/Preis-Layer. Förderdatenbank bewusst reduziert (Bundesländer + Top-20-Städte).

**Nicht in dieser Roadmap:**
- **V2G-Cockpit:** verworfen (Markt erst 2028). Nur 2–3 Ratgeber-Seiten unter `/e-auto/` + THG-Satellit (Januar-Peak). Neubewertung 2027/28.
- **CO2-Vermieter-Tool:** zurückgestellt bis klarer USP gegen mein-nebenkostenrechner.de existiert.
- **Förder-Lotse als Standalone:** ersetzt durch das Fördermodul im WP-Check.

---

## Umsatzlogik (konservative Denkweise, keine Versprechen)

Die Kennzahl ist **EPV (Euro pro Besucher) × Besucher pro Strecke**:

| Strecke | EPV | 1.000 Besucher/Monat bringen |
|---|---:|---:|
| WP-/PV-Lead-Strecke | 1–5 € | 1.000–5.000 € |
| Wechselstrecke (Wechsel-Intent) | 0,60–2 € | 600–2.000 € |
| BKW-Affiliate | 0,40–1 € | 400–1.000 € |
| Display Ads (Info-Traffic) | ~0,01 € | ~10 € |

Konsequenzen:
1. **Traffic-Qualität schlägt Traffic-Menge.** 1.000 Besucher auf der WP-Strecke sind mehr wert als 100.000 auf Info-Artikeln.
2. Ads erst ab ~3.000 Besuchen/Monat (Ezoic) überhaupt aktivieren, ab ~50.000 Sessions Mediavine/Raptive prüfen — immer nur als Zusatzschicht.
3. Digitale Produkte (Tarif-Report-PDF ~12,90 €, Förder-Guide 19–79 €) als Zwischenschicht auf Traffic ohne Lead-Intent.
4. Recurring Revenue (Widget-Abos) ist Endausbau, nicht Start.

## Risiko-Dashboard (laufend prüfen)

| Risiko | Frühindikator | Gegenmaßnahme |
|---|---|---|
| SEO-Fenster WP schließt | Finanztip/co2online aktualisieren BEG-Content | Launch vorziehen, Foren-/Newsletter-Distribution verstärken |
| Core-Update trifft Domain | Sichtbarkeitsverlust trotz Tool-Fokus | EEAT nachschärfen, Autorenprofil, Methodik-Seiten |
| Lead-Preise fallen / Stornoquoten steigen | Abrechnungen der Aufkäufer | Zweitabnehmer onboarden, exklusive Regionalleads testen |
| Referral-Programme gekürzt (Tibber & Co.) | Konditionsänderungen | Check24-Fallback trägt; Premium-PDF ausbauen |
| Scaled-Content-Abstrafung | Indexierungsverluste bei Stadtseiten | Unique-Daten-Anteil erhöhen, dünne Seiten noindexen |
| Wartungsfallen (Förder-DB, Parser) | Pflegeaufwand > 1 Tag/Woche | Umfang reduzieren, Datenstand transparent machen |

## Nächste konkrete Schritte

1. Domain-/Markenentscheidung treffen (Hub-Domain festlegen, ggf. Umzug des bestehenden Rechners planen).
2. Check24-Partnerprogramm + Awin (Verivox) + energyAds beantragen.
3. E-Mail an metergrid/Solarize: Energy-Sharing-Lead-Zahlungsbereitschaft abfragen (Gate für 2c).
4. §14a-Rechner als erstes neues Projekt starten (Repo/Verzeichnisstruktur nach docs/03).
