# Energie-Netzwerk — Portfolio-Strategie

Strategie- und Evaluationsdokumente für ein einnahmengenerierendes Netzwerk aus Webprojekten im deutschen Energiesektor, aufgebaut um den bestehenden **Energiekosten-Rechner** als Hub.

> Stand: August 2026. Basis: systematische Marktrecherche (6 Themenfelder, ~90 Quellen), 21 generierte Projektideen aus drei Perspektiven (Umsatz, SEO, Innovation), konsolidiert zu 12 Projekten und von zwei unabhängigen kritischen Bewertungen (Business-Skeptiker, SEO-Realist) gescort.
>
> **Wichtig:** Der Hub existiert bereits als [stromfazit](https://github.com/SyxGit-hub/stromfazit) und hat mehrere der Bauen-Projekte schon live (Lastprofil-Analyzer, §14a-Rechner, Wärmepumpen-Rechner, SMARD-Datenpipeline) — aber **null aktive Monetarisierung**. Abgleich und revidierte Prioritäten: [docs/05](docs/05-bestandsaufnahme-stromfazit.md).

## Die Kernentscheidung: Eine Domain, ein Netz

**Alle Projekte entstehen als Unterverzeichnisse einer starken Hub-Domain** (z. B. `domain.de/waermepumpe/`, `/dynamische-tarife/`, `/energy-sharing/`) — nicht als separate Domains.

Begründung aus der Recherche:
- Google behandelt mehrere ähnlich aufgebaute, stark untereinander verlinkte Domains desselben Betreibers zunehmend als Netzwerk (PBN-/Doorway-Verdacht) und straft alle gleichzeitig ab.
- Topische Autorität auf einer Domain ist 2026 der stärkste Ranking- und AI-Zitier-Hebel: Eine Domain mit ~30 vernetzten Seiten zu einem Thema wird konsistent von AI-Systemen zitiert; Topical-Authority-First-Strategien erzielen bis zu 3× schnellere Ranking-Gewinne.
- Jedes neue Tool zahlt sofort auf die Autorität aller anderen ein.

## Portfolio-Übersicht (12 evaluierte Projekte)

Score = Mittelwert beider Judges über 5 Dimensionen (Umsatzpotenzial, Wettbewerbslücke, Machbarkeit, Innovation, Synergie), max. 50.

| # | Projekt | Score | Urteile | MVP | Phase |
|---|---------|------:|---------|----:|-------|
| 1 | **Lastprofil-Labor** (Dynamik-Tarif-Simulator mit echtem Smart-Meter-Profil) | 37,5 | bauen / bauen | 5 Wo. | 2 |
| 2 | **§14a-Modul-Rechner & Wärmepumpenstrom-Vergleich** | 37,0 | bauen / bauen | 3 Wo. | 1 |
| 3 | **Energy-Sharing-Kompass** (§42c EnWG) | 35,5 | vielleicht / bauen | 4 Wo.* | 2 |
| 4 | **Solarspitzen-Radar** (Negativpreis-Wächter für PV-Besitzer) | 35,0 | vielleicht / vielleicht | 3 Wo. | 2 |
| 5 | **Wärmepumpen-Vollkosten- & Förder-Check** | 33,5 | bauen / bauen | 6 Wo. | 1 |
| 6 | **Netzentgelt-Atlas Deutschland** (PLZ-Karte Strom & Gas) | 32,5 | vielleicht / vielleicht | 5 Wo. | 3 |
| 7 | **Energie-Widgets** (Embed-Baukasten) | 32,5 | vielleicht / vielleicht | 4 Wo. | 3 |
| 8 | V2G-Cockpit (E-Auto als Speicher) | 31,5 | verwerfen / verwerfen | — | ✗ |
| 9 | PV-Rechner & Solar-Atlas (MaStR-Stadtseiten) | 30,0 | vielleicht / vielleicht | 7 Wo. | 3 |
| 10 | Balkonkraftwerk-Speicher-Rechner | 27,5 | vielleicht / vielleicht | 3 Wo. | 3 |
| 11 | Förder-Lotse (KI-gestützter Förder-Finder) | 27,0 | vielleicht / vielleicht | — | als Modul |
| 12 | CO2-Kostenaufteilung für Kleinvermieter | 20,5 | vielleicht / vielleicht | — | zurückgestellt |

\* Empfehlung beider Judges: als schlanke 2-Wochen-Wette starten (Rechner + 10–15 Seiten), nicht als Portal.

## Roadmap in Kurzform

- **Phase 0 (sofort, ~1 Woche):** Hub monetarisieren — Check24-/energyAds-White-Label-Wechselstrecke in den bestehenden Energiekosten-Rechner einbetten (20 € stornofrei pro Strom-/Gas-Lead auf vorhandenem Traffic). Newsletter + EEAT-Fundament (Autorenprofil, Methodik-Seite, Impressum).
- **Phase 1 (Monat 1–3):** §14a-Modul-Rechner (3 Wo., bestes Aufwand-Nutzen-Verhältnis) → Wärmepumpen-Check (6 Wo., wertvollste Leads 50–120 €, SEO-Fenster nach BEG-Neustart 21.07.2026 + Herbst-Heizsaison).
- **Phase 2 (Monat 3–6):** Lastprofil-Labor (baut die gemeinsame Börsenpreis-Datenschicht) → Solarspitzen-Radar (3 Wo., recycelt die Datenschicht, baut Newsletter-Liste) → Energy-Sharing-Kompass als schlanke First-Mover-Wette (Lead-Preise vorher per E-Mail bei metergrid/Solarize validieren).
- **Phase 3 (Monat 6–12):** Netzentgelt-Atlas (Datenpipeline intern zuerst, öffentlicher Launch zur Netzentgelt-Runde Okt/Nov) → Energie-Widgets (Gratis-Tier als Linkbuilding-Motor) → PV-Rechner & Solar-Atlas (sobald Domain-Autorität da ist) → Balkonkraftwerk-Rechner als Volumen-Zubringer.
- **Nicht bauen:** V2G-Cockpit (Markthochlauf erst ab 2028 — nur 2–3 Ratgeber-Seiten zur Keyword-Sicherung, Neubewertung 2027/28). Förder-Lotse nur als BEG-Modul im Wärmepumpen-Check. CO2-Vermieter-Tool nur mit klarem USP gegen den Incumbent.

## Dokumente

| Dokument | Inhalt |
|----------|--------|
| [docs/01-marktanalyse.md](docs/01-marktanalyse.md) | Regulatorik & Trends 2025/2026, Monetarisierungs-Benchmarks, Wettbewerbslücken, Traffic-Strategie, Daten/APIs, erfolgreiche Vorbilder |
| [docs/02-projekt-evaluation.md](docs/02-projekt-evaluation.md) | Alle 12 Projekte im Detail: Konzept, Monetarisierung, Scores, Judge-Begründungen, Risiken |
| [docs/03-netzwerk-architektur.md](docs/03-netzwerk-architektur.md) | Hub-and-Spoke-Struktur, geteilte Datenschichten, Monetarisierungs-Routing, Tech-Stack, EEAT |
| [docs/04-roadmap.md](docs/04-roadmap.md) | Phasenplan mit Entscheidungs-Gates, KPIs und Umsatzlogik |
| [docs/05-bestandsaufnahme-stromfazit.md](docs/05-bestandsaufnahme-stromfazit.md) | **Abgleich mit dem realen Stand von stromfazit.de** — was schon live ist, was fehlt, revidierte Roadmap |

## Die Logik hinter allem: Euro pro Besucher (EPV)

| Monetarisierung | EPV (geschätzt) |
|-----------------|----------------:|
| PV-/Wärmepumpen-Lead-Strecken (50–150 €/Lead × 2–5 % Conversion) | 1,00–5,00 € |
| Strom-/Gas-Wechsel-Affiliate (20 € stornofrei × 3–10 % bei Wechsel-Intent) | 0,60–2,00 € |
| THG-Quoten-Affiliate (10–15 €/Vermittlung, nur E-Auto-Traffic) | 0,50–1,50 € |
| Balkonkraftwerk-Hardware-Affiliate (bis 10 % vom Warenkorb) | 0,40–1,00 € |
| Display Ads (8–15 € RPM Energie-Nische) | 0,005–0,015 € |

**Leads schlagen Ads um Faktor 100+.** Deshalb ist jedes Projekt als interaktives Tool mit Lead-/Affiliate-Strecke konzipiert — Ads sind nur Grundrauschen auf Info-Traffic, nie das Geschäftsmodell.
