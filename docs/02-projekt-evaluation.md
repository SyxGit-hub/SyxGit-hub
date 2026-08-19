# Projekt-Evaluation: 12 Kandidaten im Detail

## Methodik

1. **Recherche:** 6 parallele Berichte (Regulatorik, Monetarisierung, Wettbewerb, SEO/Traffic, Daten/APIs, Vorbilder) mit ~90 Quellen.
2. **Ideation:** 3 unabhängige Runden mit je 7 Ideen aus drei Linsen (Umsatz-first, SEO-first, Innovation-first) = 21 Ideen.
3. **Konsolidierung:** Dedup zu 12 klar unterscheidbaren Projekten.
4. **Bewertung:** Zwei unabhängige kritische Judges — ein **Business-Skeptiker** („Zahlt wirklich jemand? Wie lange bis zum ersten Euro?") und ein **SEO-Realist** („Kommt da 2026 mit AI Overviews überhaupt noch Traffic an? Ist die Nische wirklich frei?").

Skalen je 1–10: Umsatzpotenzial · Wettbewerbslücke (10 = frei) · Machbarkeit (10 = schnell solo machbar) · Innovation · Synergie. Score = Summe, gemittelt über beide Judges (max. 50).

## Score-Matrix

| Projekt | Umsatz | Lücke | Machbk. | Innov. | Synergie | Ø Score | Business | SEO |
|---------|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Lastprofil-Labor | 5–6 | 8 | 6 | 9 | 9 | **37,5** | bauen | bauen |
| §14a-Modul-Rechner | 5 | 8–9 | 7–8 | 7 | 9 | **37,0** | bauen | bauen |
| Energy-Sharing-Kompass | 3–5 | **10** | 6 | 9 | 6–7 | **35,5** | vielleicht | bauen |
| Solarspitzen-Radar | 4 | 8 | 7–8 | 7–8 | 8 | **35,0** | vielleicht | vielleicht |
| Wärmepumpen-Check | **8–9** | 4–6 | 6 | 5 | 9 | **33,5** | bauen | bauen |
| Netzentgelt-Atlas | 4–5 | 7 | 6 | 6 | 9 | **32,5** | vielleicht | vielleicht |
| Energie-Widgets | 3–4 | 6–7 | 6–7 | 6–7 | **9–10** | **32,5** | vielleicht | vielleicht |
| V2G-Cockpit | 2–3 | 8 | 7–8 | 7–8 | 6 | 31,5 | **verwerfen** | **verwerfen** |
| PV-Rechner & Solar-Atlas | 7–8 | 4 | 4–5 | 6 | 8 | 30,0 | vielleicht | vielleicht |
| BKW-Speicher-Rechner | 4–5 | 4 | 7 | 5 | 7 | 27,5 | vielleicht | vielleicht |
| Förder-Lotse | 7 | 3–5 | 3–4 | 4–5 | 8 | 27,0 | vielleicht | vielleicht |
| CO2-Vermieter-Tool | 6 | 3 | 4 | 3 | 4–5 | 20,5 | vielleicht | vielleicht |

---

## Die Bauen-Projekte

### 1. Wärmepumpen-Vollkosten- & Förder-Check — *bauen / bauen* (33,5)

**Konzept:** Interaktiver Rechner „Gasheizung behalten oder Wärmepumpe?" mit Vollkostenvergleich über 10–15 Jahre auf dem Stand nach dem BEG-Neustart vom 21.07.2026 (30 % Grundförderung, max. 28.000 €/Wohneinheit): CO2-Preispfad (2026: 55–65 €/t → 2030: 120–150 €/t), strukturell steigende Gasnetzentgelte (+10–12 %, regional bis +48,7 %), JAZ-Schätzung nach VDI 4650 (nachbaubar, Referenz Fraunhofer-Feldtest JAZ 4,1–4,3). Ergebnis erscheint **vor** der Kontaktdaten-Abfrage (Selfmade-Energy-Muster), dahinter die Lead-Strecke „3 kostenlose Angebote von Fachbetrieben".

**Monetarisierung:** WP-Leads 50–120 € (DAA/TapTapHome, Aroundhome), später exklusive vorqualifizierte Leads 150 €+ an regionale Installateure; bei 2–5 % Formular-Conversion **1–5 € Umsatz pro Besucher** — die wertvollste Monetarisierung im Netzwerk. Sekundär: Sanierungs-Leads (50–100 €), Heizstrom-Affiliate (~20 €).

**Warum bauen (beide Judges):** Zahlungsbereitschaft am besten belegt im ganzen Portfolio; das SEO-Fenster ist real und datierbar (GModG 10.07. + BEG-Neustart 21.07.2026 haben Konkurrenz-Content objektiv entwertet); Herbst-Saisonpeak steht bevor; kein anderes Projekt monetarisiert den Bestands-Traffic des Energiekosten-Rechners so direkt („Ihre Heizkosten sind hoch — lohnt sich eine Wärmepumpe?"). Erster Euro realistisch in 3–5 Monaten.

**Risiken:** YMYL-Kernland von Finanztip/co2online/Verivox — neue Domain rankt nicht auf Kopf-Keywords, der Plan muss auf Rechner-Long-Tail, Hub-Traffic und Foren setzen. heizungsfinder.de gehört ausgerechnet Lead-Abnehmer DAA — man konkurriert mit dem eigenen Kunden. Das Fenster schließt binnen Wochen, nicht Monaten. Stornoquoten können den effektiven Leadpreis drücken. 6 Wochen sind die Untergrenze.

**MVP: 6 Wochen · Phase 1**

---

### 2. Lastprofil-Labor (Dynamik-Tarif-Simulator) — *bauen / bauen* (37,5, Top-Score)

**Konzept:** Der einzige Verbraucher-Rechner, der nicht mit Standardprofilen arbeitet: Smart-Meter-Export (CSV/HTML) hochladen, das Tool simuliert rückwirkend Tibber, Ostrom, Rabot, Octopus gegen den eigenen Festpreistarif mit realen EPEX-Day-Ahead-Preisen (aWATTar ohne Key, SMARD/energy-charts als CC-BY-Fallback). Dazu Live-Widget „Wann ist Strom heute am billigsten?" und Smart-Meter-Check als Einstieg. Beantwortet exakt die in Photovoltaikforum/Akkudoktor ständig unbeantwortete Kombinationsfrage (PV + Speicher + WP + dynamischer Tarif). Bestehende Nischenrechner (wattplaner, stromweise) nutzen nur Standardprofile — **Datentiefe ist das Produkt**.

**Monetarisierung:** Beide Ausgänge monetarisiert — Referral-Prämien der Dynamik-Anbieter als Kern; fällt die Simulation zugunsten Festpreis aus, greift der Check24-White-Label-Vergleich (20 € stornofrei). Premium-PDF „Dein Tarif-Report" (~12,90 €); WP-Lastprofile leiten in die WP-Lead-Strecke.

**Warum bauen (beide Judges):** Die am besten belegte Produkt-Lücke im Dossier. CSV-Upload ist maximal AI-Overview-resistent und wird in Foren organisch geteilt — **Distribution funktioniert ohne Google-Autorität**, der entscheidende Punkt für eine neue Domain. Die Börsenpreis-Datenschicht wird von drei weiteren Projekten wiederverwendet. Zielgruppe kaufkräftig und multiplikatorstark (Akkudoktor-Community: 431k Abonnenten).

**Risiken:** Adressierbarer Markt heute klein (Smart-Meter-Rollout hinkt, 20 %-Ziel gerissen); Format-Zoo der Messstellenbetreiber-Exporte macht den Parser zur Dauerbaustelle; Referral-Programme kündbar, teils Gutschriften statt Cash; DSGVO: Lastprofile sind sensible Verbrauchsdaten — **idealerweise clientseitig verarbeiten**; Upload ist kopierbar (Vorsprung = Ausführung). Auflage des Business-Judges: EPV nach 3 Monaten ehrlich messen.

**MVP: 5 Wochen · Phase 2 (baut die gemeinsame Börsenpreis-Datenschicht)**

---

### 3. §14a-Modul-Rechner & Wärmepumpenstrom-Vergleich — *bauen / bauen* (37,0)

**Konzept:** „Modul 1, 2 oder 3 — was spart mehr?": pauschal 110–190 €/Jahr vs. 60 % Arbeitspreis-Rabatt (typisch 350–500 €/Jahr, lohnt ab ~6.000 kWh, separater Zähler) vs. zeitvariable Netzentgelte. Gekoppelt mit Wärmepumpenstromtarif-Vergleich (20–26 ct vs. ~37 ct Haushaltsstrom = bis 17 ct Ersparnis). Viele Erklärtexte, **fast keine Rechner**.

**Monetarisierung:** Heizstrom-Affiliate (Verivox ~20 € über Awin, energyAds-White-Label mit E.ON/MAINGAU); Elektriker-Lead bei separatem Zähler; Wallbox-/Speicher-Leads; THG-Satellit für die E-Auto-Fraktion.

**Warum bauen (beide Judges):** **Bestes Aufwand-Nutzen-Verhältnis der Liste** — 3 Wochen für eine dokumentiert unbesetzte Nische, die Check24/Verivox strukturell nicht besetzen (passt nicht ins Provisionsmodell). Zielgruppe wächst gesetzlich erzwungen (jede WP/Wallbox ab 2024 ist §14a-pflichtig) und ist maximal kaufkräftig. Engste Hub-Verzahnung im Netzwerk. Erster Euro in 2–3 Monaten.

**Risiken:** Geringes Suchvolumen deckelt den Umsatz strukturell — Long-Tail-Baustein, kein Traffic-Motor; Modul-3-Daten nur über kommerzielle APIs (GET AG) oder manuelle Pflege; Verivox zahlt erst nach Vertragsprüfung; Finanztip könnte mit eigenem Rechner die SERP übernehmen; jährliche Regulatorik-Pflege.

**MVP: 3 Wochen · Phase 1 (erstes neues Projekt)**

---

### 4. Energy-Sharing-Kompass (§42c EnWG) — *vielleicht / bauen* (35,5)

**Konzept:** First-Mover-Portal zur stärksten dokumentierten Marktlücke: Seit 01.06.2026 darf Erneuerbaren-Strom bilanziell mit Nachbarn geteilt werden — sichtbar publizieren nur Kanzleien und B2B-Plattformen, **kein einziges Verbraucher-Tool existiert**. Kernstücke: „Lohnt sich Strom teilen?"-Rechner, Plattform-Vergleich (metergrid, items …), Entscheidungs-Ratgeber „Mieterstrom vs. Energy Sharing" (Zuschlag 1,59–2,54 ct/kWh, wirtschaftlich ab ~6 WE/30 kWp).

**Warum der SEO-Realist „bauen" sagt:** Der seltene Fall, in dem eine neue Domain ohne Autorität ranken kann, **weil niemand Autorität hat**. Wer jetzt mit Rechner und konkreten Zahlen publiziert, wird die Zitierquelle der AI Overviews von morgen (+35 % Klicks) und hält den PR-Hook „erster Energy-Sharing-Rechner Deutschlands".

**Warum der Business-Skeptiker bremst:** Lücke ≠ Markt. „Preisniveau verhandelbar, da kein etablierter Lead-Markt existiert" ist die Definition vager Monetarisierung. Ob metergrid/Solarize 50–150 €/Lead zahlen, ist eine Hypothese, die man **vor dem Bau per E-Mail validieren kann und muss**. Erster Euro möglicherweise erst in 12+ Monaten.

**Konsens-Empfehlung:** Als schlanke 2-Wochen-Wette (Rechner + 10–15 Seiten), nicht als 4-Wochen-Portal. Gate: Lead-Preis-Validierung per Anfrage bei den Plattformen vorab.

**MVP: 2 Wochen (schlank) · Phase 2**

---

## Die Vielleicht-Projekte (richtig sequenziert sinnvoll)

### 5. Solarspitzen-Radar — *vielleicht / vielleicht* (35,0)

Live-Dashboard + Alarm-Dienst zum Solarspitzengesetz: zählt Negativpreis-Stunden aus SMARD (573 h in 2025), zeigt PV-Besitzern personalisiert ihren Vergütungsverlust, prognostiziert „Morgen 11–15 Uhr negative Preise — Speicher laden statt einspeisen". **Konsens beider Judges:** Als eigenständiges frühes Projekt überschätzt — der individuelle Verlust ist klein (niedrige zweistellige €/Jahr bei 10 kWp), der Conversion-Sprung zur 5.000-€-Speicher-Kaufentscheidung weit. Aber als **billiges Add-on nach dem Lastprofil-Labor** (geteilte SMARD/aWATTar-Schicht, 3 Wochen) mit Presse-Potenzial (jede Sommer-Negativpreis-Rekordmeldung erzeugt Suchspitzen, das Radar ist die einzige Live-Antwort) und als Newsletter-Aufbau-Maschine (Negativpreis-Alarm als Abo-Anlass): dann bauen. Risiko: extreme Saisonalität, trivial nachbaubar durch Fachmedien.

### 6. Netzentgelt-Atlas Deutschland — *vielleicht / vielleicht* (32,5)

Interaktive PLZ-Karte + Stadtseiten aus BNetzA-§23b-Daten (nur als Excel verfügbar — die Lücke ist die Chance) und MaStR-Export. **Konsens:** Der Wert ist überwiegend **infrastrukturell** — regionale Datenschicht für Hub (PLZ-genaue Preise), §14a-Modul-3 und WP-Check (teure Gasnetze), plus Backlink-Magnet zur jährlichen Netzentgelt-Runde. Als eigenständige Geld-Maschine schwach (Info-Intent konvertiert schlecht in 20-€-Wechsel-Leads; stromauskunft.de besetzt „strompreis [stadt]" seit 20 Jahren). **Empfehlung SEO-Realist:** Datenpipeline intern bauen (wird ohnehin gebraucht), öffentlichen Atlas als Phase-3-Asset zur Netzentgelt-Runde Okt/Nov mit Presse-Push nachschieben. Risiko: Scaled-Content-Abstrafung bei tausenden Stadtseiten ohne genug Unique-Nutzwert schlägt auf die ganze Hub-Domain durch.

### 7. Energie-Widgets (Embed-Baukasten) — *vielleicht / vielleicht* (32,5)

Einbettbare Widgets aus den freien Datenquellen (Börsenstrompreis, Grünstrom-Ampel, CO2-Ticker, Mini-Rechner): gratis mit Attributions-Backlink, White-Label im Abo (29–99 €/Monat). **Konsens:** Strategisch das wertvollste Stück Infrastruktur — jedes Gratis-Embed ist ein themenrelevanter redaktioneller Backlink (wirkt stärker als 50 Directory-Links, exakt die EEAT-Signale, die eine junge YMYL-Domain braucht). Aber als Micro-SaaS zu früh: Stadtwerke kaufen nicht self-serve bei Einzelpersonen, der Weg zu 20–30 zahlenden Kunden ist Monate Kaltakquise. **Empfehlung:** Gratis-Tier als Linkbuilding-Motor in Phase 3 ausrollen (recycelt die Datenpipelines), Paid-Tier erst bei nachweisbarer Inbound-Nachfrage. Risiko: Widget-Backlinks mit optimierten Ankertexten können als Linkschema gewertet werden — Brand-Links sind Pflicht.

### 8. PV-Rechner & Solar-Atlas — *vielleicht / vielleicht* (30,0)

PVGIS-basierter Wirtschaftlichkeitsrechner mit Solarspitzengesetz-Logik (als erster: Negativpreis-Ausfall + 60 %-Kappung einrechnen) + programmatische MaStR-Stadtseiten („X PV-Anlagen, Y Speicher, Z kWp Zubau in Musterstadt"). PV-Leads 50–150 € sind hochlukrativ, **aber:** die PV-SERP ist die am härtesten umkämpfte Nische außerhalb Strom/Gas (EchtSolar, Selfmade Energy, Wattfox, Shop-Rechner), die Gesetzes-Logik ist ein kopierbares Feature, und 7 Wochen + MaStR-Pipeline (Multi-GB-XML) ist der zweitgrößte Aufwandsposten. **Konsens:** Erst bauen, wenn die Hub-Domain Autorität hat; ggf. den Atlas-Teil (Backlink-Asset) vorziehen, den Rechner später. Phase 3.

### 9. Balkonkraftwerk-Speicher-Rechner — *vielleicht / vielleicht* (27,5)

Neutraler Rechner für die unbesetzte Folgefrage des Massenmarkts: „Speicher nachrüsten — lohnt sich das?" (Eigenverbrauch 30 % → 70 %, Amortisation 6–8 Jahre), plus Förderdatenbank. Markt riesig (1,33 Mio. Bestand, ~700.000 Neuinstallationen 2026), Affiliate belegt (Kleines Kraftwerk bis 10 %) — aber **EPV 0,40–1 € ist die schwächste Geld-Strecke der Kandidaten** (5–10× Traffic für denselben Umsatz wie die WP-Strecke nötig), die BKW-Nische ist die vollste im deutschen Energie-Web, und Akkudoktor kann das Thema jederzeit mit 431k Abonnenten besetzen. Ehrlichkeitsproblem: die korrekt gerechnete Nachrüst-Amortisation ist oft unattraktiv — drückt die eigene Conversion. Als schneller Volumen-Zubringer nach den Kern-Spokes vertretbar. Phase 3. Die Förderdatenbank ist eine Wartungsfalle — nur reduziert (Bundesländer, Top-20-Städte) führen.

### 10. Förder-Lotse — *vielleicht / vielleicht* (27,0)

PLZ + Vorhaben → alle passenden Förderprogramme. Die Lead-Kette dahinter ist die wertvollste des Netzwerks (Förder-Sucher stehen unmittelbar vor dem Kauf), **aber** die Nische ist besetzt: foerderdatenbank.de (Bund), FördermittelCheck von co2online (BMWK-gefördert, auf hunderten Partnerseiten) bieten genau das kostenlos mit Behörden-Vertrauen. Der einzige offene Winkel — kommunale Tiefe — ist ein Pflege-Fass ohne Boden; falsche Förderangaben vernichten Vertrauen und Rankings. **Konsens beider Judges: Nicht als Standalone bauen.** Stattdessen Bund+Länder-Förderlogik als Modul direkt in WP-Check und BKW-Rechner integrieren (~2 Wochen, fängt den Großteil des Lead-Werts).

### 11. CO2-Kostenaufteilungs-Tool für Kleinvermieter — *vielleicht / vielleicht* (20,5, letzter Platz)

Micro-SaaS nach dem Muster mein-nebenkostenrechner.de (Rechner gratis, PDF 12,90 €, Abo ab 7,90 €/Monat). Einziges Projekt mit bewiesener direkter Zahlungsbereitschaft und Recurring Revenue — **aber genau das ist das Problem:** Es ist ein Me-too gegen einen etablierten Incumbent plus mehrere Gratis-Rechner, ohne erkennbaren USP. Dazu Haftungsrisiko („rechtssicheres PDF" bei echtem Geld zwischen Mieter und Vermieter), teuerster Build (7 Wochen), Vermieter-Persona zahlt kaum auf die Energie-Themenautorität ein. **Zurückgestellt** — frühestens, wenn das Netzwerk steht und ein klarer USP formuliert ist.

---

## Verworfen

### 12. V2G-Cockpit — *verwerfen / verwerfen* (31,5)

„Was verdient dein E-Auto als Speicher?" Das Dossier widerlegt die eigene These: Der V2G-Markthochlauf wird **erst ab 2028** erwartet, bidirektionsfähige Hardware ist 2026 kaum kaufbar — der Rechner simuliert Erlöse, die fast niemand realisieren kann. Einzige heutige Monetarisierung ist THG-Affiliate (10–15 €), im Monetarisierungs-Bericht explizit als „Beifang im schrumpfenden Markt" eingestuft. First-Mover-SEO zwei Jahre vor dem Markt ist für einen Solo-Entwickler Opportunitätskosten-Verschwendung — der First-Mover-Vorteil einer schwachen Domain hält keine zwei Jahre gegen ADAC und Portale.

**Billige Alternative:** 2–3 gute Ratgeber-Seiten + Mini-Rechner als Unterverzeichnis der Hub-Domain halten die Keywords warm. **Neubewertung 2027/28** mit MiSpeL-Praxisdaten.
