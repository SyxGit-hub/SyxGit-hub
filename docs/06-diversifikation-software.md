# Diversifikation: Bezahlte Software im Energiesektor (Desktop / Web+Cloud)

> Brainstorming auf Basis von drei Recherche-Berichten (B2B-Software-Markt, Consumer-/Local-First-Tools, MaStR-Datenintelligenz), Stand August 2026. Ziel: ein Software-Produkt mit direkter Zahlungsbereitschaft — unabhängig von Google-Traffic und Affiliate-Konditionen.

## Die drei wichtigsten Marktbefunde

1. **B2B-Energieberater-/SHK-Software ist Desktop-Dinosaurier-Land.** Die BAFA-zugelassenen Suiten (Hottgenroth, EVEBI, BKI, ZUB Helena) kosten 600–1.600 €/Jahr plus Servicepakete (145–475 €/Jahr) und Zusatzmodule (je 199–299 €), sind Windows-only mit dokumentiertem Support- und Bug-Frust (GEB-Forum, Energieberaterforum). Cloud-Angreifer nach dem „Ein-Workflow"-Muster (iSFP-Turbo 29–69 €/Monat, HeizNorm ab 98 €/Monat) sind 2025/26 entstanden und beweisen den Preispunkt.
2. **Im Consumer-Bereich ist die Lücke „EOS-Ergebnisse ohne EOS-Schmerz".** Monitoring ist Gratis-Commodity (Home Assistant, Hersteller-Apps). Die Optimierung (dynamischer Tarif + Speicher aus dem Netz laden + §14a-Modulwahl) existiert nur als Bastel-Werkzeugkasten (Akkudoktor EOS: Docker-Schmerz, ~1.600 GitHub-Stars, Foren voller Installationsfragen) oder als Cloud-Abo mit Hardware (Solar Manager 48–72 €/Jahr, >50.000 Systeme; clever-PV ~60 €/Jahr). **Einmalkauf funktioniert nachweislich:** evcc verkauft Lifetime-Token für 150 €. Local-first ist ein echtes Kaufargument (Huawei-China-Cloud-Kritik im Photovoltaikforum; Shelly launcht 2026 eine cloudfreie PV-Plattform — Validierung UND kommende Konkurrenz). Abo-Müdigkeit ist messbar (US-Haushalte −32 % bezahlte Abos 2024→2025).
3. **MaStR-Vertriebsintelligenz fürs Handwerk: Nische frei, aber aus gutem Grund.** Kein Anbieter verkauft ein 50–150-€/Monat-Tool an Solarteure — aber das MaStR nennt keine Installateure (keine echte Wettbewerbsanalyse), Standorte sind nur PLZ-scharf (keine Adress-Leads, DSGVO), Gratis-Angebote (solarzubau.de, marktstammdatenregister.dev, Wattbewerb) drücken die Preisobergrenze, und Zahlungsbereitschaft fürs reine Datenprodukt ist unbelegt. → **Zurückgestellt**; höchstens als Feature in einem Vertriebs-Workflow oder für Stadtwerke/Hersteller.

## Kandidat A — „Stromfazit Studio": Lokaler Energie-Optimierer als Desktop-App (Empfehlung)

**Was:** Die bezahlte Weiterentwicklung des Lastprofil-Analyzers als Desktop-Anwendung (cloud-unabhängig). Nutzer importiert Smart-Meter-Export, PV-/Speicher-Daten (Datei-Import, später Modbus lokal) — die App beantwortet die Fragen, die in Photovoltaikforum und Akkudoktor-Forum nachweislich ständig offen bleiben:
- Welcher dynamische Tarif lohnt sich bei MEINEM Profil (rückwirkend simuliert mit echten EPEX-Preisen)?
- Lohnt es sich, MEINEN Speicher nachts aus dem Netz zu laden — und wann?
- §14a: Modul 1, 2 oder 3 bei MEINER Anlage?
- Jahresreport: Eigenverbrauch, Einspeise-/Entnahme-Doku, Wirtschaftlichkeit (den Rest-Steuerfall deckt das als Feature ab — als eigenständiges Steuer-Produkt ist die Nische seit der 30-kWp-Steuerbefreiung tot; SteuerSparErklärung hat ihr PV-Modul eingestellt).

**Positionierung: „Analyse & Entscheidung, nicht Steuerung."** Bewusst KEINE Live-Gerätesteuerung im MVP — dort sitzen evcc/Home Assistant/Hersteller-HEMS mit Integrationszoo und Supportlast. Wir verkaufen das fertige, verständliche Ergebnis, nicht den Bastelkasten.

**Warum wir aus der Masse stechen:**
1. **Local-first als Marketing-Kern:** „Deine Verbrauchsdaten verlassen deinen Rechner nicht" — gegen Huawei/Cloud-Frust, DSGVO-sauber, kein Server-Betrieb nötig.
2. **Einmalkauf gegen Abo-Müdigkeit:** ~99–149 € Lifetime (evcc-Beweis: 150 €), optional +29 €/Jahr für automatische Datenpakete — Hybrid-Modell.
3. **Der Funnel existiert schon:** stromfazit.de mit Lastprofil-Analyzer IST die Gratis-Lite-Version; jede Web-Analyse endet mit „Die Vollversion rechnet deinen Speicher und §14a durch — einmal zahlen, deine Daten bleiben lokal". Foren-Distribution über die ohnehin geplante Präsenz.
4. **Die Datenpipeline existiert schon:** Die SMARD-Spot-Daten (GitHub Actions, täglich/monatlich) werden zum Update-Kanal der App — cloud-unabhängig, aber immer aktuell.
5. **Marken-Fit:** „Rechner mit ehrlichem Fazit" ist exakt das Vertrauensversprechen, das eine Kaufentscheidung für 149 € trägt.

**Monetarisierung:** 99–149 € Einmalkauf (Launch-Preis), Datenpaket-Abo 29 €/Jahr optional, später „Pro" (Mehranlagenverwaltung, Berater-Modus). 100 Verkäufe/Monat ≈ 10–15 T€/Monat Potenzial; konservativ sind 10–30 Verkäufe/Monat über den bestehenden Funnel realistisch zu testen.

**Aufwand MVP:** 6–8 Wochen (Tauri/Electron um die bestehende Analyzer-Logik; Parser, Simulation und §14a-Logik existieren in stromfazit bereits als Web-Code).

**Risiken:** Shelly-Plattform 2026 (lokal, aber herstellergebunden und Monitoring-fokussiert — Zeitfenster nutzen); Zielgruppe ist OSS-affin (Antwort: Zeitersparnis + Politur schlagen kostenlos, siehe evcc-Token und Solar Manager); Zahlungsabwicklung/Lizenzierung als neuer Aufwand (Paddle/Lemon Squeezy).

## Kandidat B — „HeizlastCheck": Förderkonforme Heizlast-Schnellrechnung für SHK-Betriebe (Web + Cloud, B2B)

**Was:** Raumweise Heizlastberechnung nach DIN/TS 12831 als schlankes Browser-Tool mit BAFA/KfW-konformem PDF — der **Pflichtnachweis für jede Wärmepumpen-Förderung**.

**Warum die Lücke real ist:** Extern eingekauft kostet die Berechnung 150–800 € pro Gebäude; die günstigsten SaaS-Anbieter (HeizNorm, Mepbau) starten erst bei ~90–98 €/Monat; in den Suiten ist Heizlast ein 299-€-Zusatzmodul auf einer 649-€-Lizenz. **Ein 29–49 €/Monat-Tool oder Pay-per-Use (19–29 €/Berechnung) für den kleinen SHK-Betrieb mit 2–3 Berechnungen/Monat fehlt.**

**Aus der Masse stechen:** Preispunkt + Geschwindigkeit („Heizlast in 30 Minuten", analog dem iSFP-Turbo-Versprechen) + Pay-per-Use ohne Abozwang. Zahlungsbereitschaft ist die am besten belegte im ganzen Brainstorming (Handwerksbetriebe zahlen nachweislich 30–150 €/Monat für Software; die Berechnung wird mit realem Geld extern eingekauft).

**Risiken:** Normative Korrektheit ist die Eintrittshürde (DIN/TS 12831 fachlich sauber, sonst Förder-Ablehnungen = Reputations-GAU); B2B-Kaltstart ohne bestehenden Kanal (der stromfazit-Funnel ist B2C; Brücke: der WP-Rechner erklärt Endkunden „Ihr Installateur braucht eine Heizlastberechnung" — schwaches, aber vorhandenes Signal); HeizNorm/Mepbau können Preise senken.

**Aufwand MVP:** 8–10 Wochen (Raumerfassung-UI, U-Werte-Kataloge, Normlogik, PDF).

## Kandidat C — Fördermittel-Nachweis-Doku (Energieberater/SHK)

Nach der BEG-Reform (neue TPB-IDs, geänderte Boni, Verwendungsnachweise) existiert kein dediziertes günstiges Tool — die größte dokumentierte B2B-Lücke. **Aber:** regulatorisch hochvolatil (die Reform vom 21.07.2026 hat gerade erst alle alten IDs entwertet — das kann jederzeit wieder passieren) und inhaltlich Dauerpflege. → Nicht als Erstprodukt; als späteres Modul von B denkbar.

## Verworfen / zurückgestellt

- **MaStR-Sales-Radar:** siehe Befund 3 — Datenprodukt ohne belegte Zahlungsbereitschaft gegen Gratis-Konkurrenz. Die MaStR-Pipeline bleibt für Solar-Atlas/PR-Statistiken im Content-Netzwerk geplant (docs/02), nicht als eigenständiges B2B-Produkt.
- **PV-Steuer-Software:** Nische seit Steuerbefreiung (≤30 kWp, 0 % USt) strukturell schrumpfend; Incumbent hat sein Modul eingestellt. Nur als Report-Feature in Kandidat A.
- **JAZ-Rechner als Produkt:** Gratis-Commodity (BWP, dena, Ochsner).

## Entscheidung (19.08.2026)

**Kandidat A wird umgesetzt** — Produktplan und Architektur im eigenen Repo [`stromfazit-studio`](https://github.com/SyxGit-hub/stromfazit-studio) (PRODUKTPLAN.md, ARCHITEKTUR.md; Meilensteine M0–M5 mit Validierungs-Gate). **Kandidat B ist als Zweitprojekt dokumentiert** in [docs/07-projekt-b-heizlastcheck.md](07-projekt-b-heizlastcheck.md) — Start nach Studio-Launch oder falls dessen M0-Gate scheitert.

## Empfehlung & nächste Schritte (ursprüngliche Analyse)

**Kandidat A zuerst** — einziger Kandidat mit existierendem Funnel (stromfazit), existierender Datenpipeline, Marken-Fit und Einmalkauf-Modell ohne B2B-Vertriebslast. **Kandidat B als zweites Standbein**, sobald A läuft — höherer Umsatz pro Kunde, aber Kaltstart und Norm-Haftung.

Validierung vor dem Bau (1 Woche, fast kostenlos):
1. Auf stromfazit.de im Lastprofil-Analyzer eine Warteliste einbauen: „Desktop-Version — einmal zahlen, Daten bleiben lokal. Trag dich ein." → misst echtes Interesse am bestehenden Traffic.
2. Zwei Foren-Threads (Photovoltaikforum, Akkudoktor) mit dem Konzept + Mockup — die Zielgruppe sagt einem dort ungefiltert, ob sie zahlen würde.
3. Parallel für B: fünf SHK-Betriebe anrufen/anschreiben — „Was zahlt ihr heute pro Heizlastberechnung, intern oder extern?"
