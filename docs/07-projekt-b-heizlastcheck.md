# Projekt B: HeizlastCheck — förderkonforme Heizlast-Schnellrechnung für SHK-Betriebe

> Status: **vollständig geplantes Zweitprojekt.** Start frühestens nach Stromfazit-Studio-1.0 (dessen M5) — oder früher, falls dessen Validierungs-Gate G0 scheitert. Marktbasis: B2B-Software-Recherche August 2026 ([docs/06](06-diversifikation-software.md), Befund 1).

## 1. Warum die Lücke real ist

- Die **raumweise Heizlastberechnung nach DIN EN 12831 ist Pflichtnachweis für die BAFA/KfW-Wärmepumpen-Förderung** (seit 2023) — ohne Nachweis keine Auszahlung.
- Extern eingekauft kostet sie **150–800 € pro Gebäude** — sie wird mit echtem Geld bezahlt, nicht mit Aufmerksamkeit.
- Das günstigste Cloud-Tool startet bei **~90–98 €/Monat** (HeizNorm ab 98 €, Mepbau ab 89,99 €); in den Desktop-Suiten ist Heizlast ein **299-€-Zusatzmodul** auf einer 649-€-Jahreslizenz (EVEBI).
- **Fehlend: Pay-per-Use (19–29 €/Berechnung) bzw. 39-€/Monat-Flat** für den kleinen SHK-Betrieb mit 2–3 Berechnungen im Monat — die Preislogik, mit der iSFP-Turbo (29–69 €/Monat) gegen die Suiten gewinnt.
- Zahlungsbereitschaft ist die am besten belegte im Software-Brainstorming: Betriebe zahlen nachweislich 30–150 €/Monat für Bürosoftware (ToolTime, Plancraft, Meisterwerk, HERO).

## 2. Produktvision: Mehr als ein Formular

Der Kern ist nicht „Norm-Mathematik im Browser", sondern **der schnellste Weg vom Kundentermin zum förderfähigen Nachweis** — plus die Anschlussfragen, die im WP-Verkaufsgespräch sofort folgen:

| Baustein | Was es leistet | Warum es differenziert |
|---|---|---|
| **Heizlast-Express** | Geführte raumweise Erfassung: Gebäude → Geschosse → Räume; Maße, Außenflächen, Fenster; **Baualtersklassen-Presets** (U-Wert-Kataloge aus der frei verfügbaren IWU/TABULA-Gebäudetypologie) statt U-Wert-Recherche; Raum-Duplizieren, Vorlagen je Gebäudetyp; Live-Ergebnis pro Raum während der Eingabe | „Heizlast in 30 Minuten" — das iSFP-Turbo-Versprechen für den nächsten Pflicht-Workflow |
| **Förder-PDF** | BAFA/KfW-tauglicher Nachweis: alle Eingaben, Normbezug, Ergebnis je Raum + Gebäude, versionierte Vorlage (Reform-sicher) | Das Dokument IST das Produkt — es wird eingereicht, nicht nur angeschaut |
| **Heizkörper-Check** (R3) | Je Raum: reicht der vorhandene Heizkörper bei 55/45/35 °C Vorlauf? Tauschliste mit Leistungsdaten | Beantwortet DIE Anschlussfrage jeder WP-Beratung — kein günstiges Tool tut das heute |
| **Abgleich-Zuarbeit** (R3) | Export der Raum-Heizlasten als Grundlage für den hydraulischen Abgleich (Verfahren B) | Macht das Tool zum Standard-Schritt im WP-Prozess statt Einmal-Kauf |
| **Kunden-/Projektverwaltung** | Projekte je Endkunde, Kopieren ähnlicher Gebäude, Archiv | Wiederkehr-Anker: der Betrieb kommt für jedes Projekt zurück |

**Nicht-Ziele:** kein CAD/3D, keine Wohnungslüftungs-Auslegung, keine GEG-Bilanzierung (Suite-Territorium), keine Endkunden-Version (Kanal-Konflikt mit stromfazit vermeiden — Endkunden bekommen dort höchstens den Grob-Check mit Verweis „dein Installateur braucht die Norm-Berechnung").

## 3. Tech-Stack (Cloud, bewusst nicht Desktop)

SHK-Betriebe wollen keinen Installationsaufwand; das PDF ist das Produkt; Projekte müssen im Büro UND beim Kunden (Tablet) erreichbar sein.

- **Frontend:** SvelteKit (oder Next.js) als PWA — tablet-tauglich für die Vor-Ort-Erfassung, offline-fähige Eingabe mit Sync
- **Backend:** Supabase (Auth, Postgres mit Row-Level-Security, EU-Region) — Solo-tauglich, DSGVO-sauber; alternativ Cloudflare Workers + D1
- **Rechenkern:** reines TypeScript-Modul mit Golden-Tests (identische Disziplin wie Studio-`core/`) — läuft client- UND serverseitig
- **PDF:** serverseitiges Rendering (HTML→PDF, z. B. Typst/Chromium-Worker) mit versionierten Vorlagen
- **Zahlung:** Merchant of Record (Paddle/Lemon Squeezy) oder Stripe (B2B-Rechnungen); Entscheidung in B-M4
- **DSGVO-Besonderheit:** Das Tool verarbeitet Endkunden-Daten der Betriebe (Adressen, Gebäudedaten) → **AVV-Muster erforderlich**, EU-Hosting Pflicht, Löschkonzept

## 4. Preis & Packaging

| Stufe | Preis | Enthält |
|---|---|---|
| **Erste Berechnung** | 0 € | voller Workflow inkl. PDF mit Wasserzeichen „Muster" → Qualitätsbeweis |
| **Pay-per-Use** | 24 €/Berechnung | finales PDF, Projekt bleibt gespeichert |
| **Flat** | 39 €/Monat, monatlich kündbar | unbegrenzte Berechnungen, Vorlagen, Kundenarchiv |
| **Team** (später) | 79 €/Monat | 3 Nutzer, gemeinsames Archiv |

Anker-Argumentation im Marketing: „Eine externe Berechnung kostet 150–800 €. Eine Flat kostet 39 €."

## 5. Releases & Meilensteine mit Arbeitspaketen

Aufwände = Netto-Arbeitstage (Solo + KI). Akzeptanzkriterium entscheidet über „fertig".

### B-M0 — Validierung (1–2 Wochen Laufzeit, ~4 d) → Gate B-G0

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP0.1 | **5–8 SHK-Betriebe interviewen** (Anruf/Besuch): Was zahlt ihr heute pro Heizlast (Zeit intern / € extern)? Wie läuft die Erfassung? Würdet ihr 24 €/Berechnung zahlen? | 2 d | ≥5 geführte Gespräche, protokolliert |
| B-AP0.2 | **Wettbewerbs-Teardown:** Testaccounts HeizNorm + Mepbau, Workflow stoppen (Minuten pro Gebäude), Schwächenliste | 1 d | Dokument mit konkreten Zeit-/Feature-Lücken |
| B-AP0.3 | **Norm-Machbarkeit:** DIN EN 12831 + DIN/TS 12831-1 beschaffen (Lizenzkosten einplanen — Normtext ist kostenpflichtig, Formeln implementieren ist zulässig, Normtext-Weitergabe nicht); Probe-Implementierung EIN Raum gegen ein Referenzbeispiel | 1,5 d | Proberaum-Ergebnis stimmt mit publiziertem Referenzbeispiel überein |

**🚦 Gate B-G0:** ≥3 von 5 Betrieben bestätigen Schmerz UND Preisbereitschaft; Norm-Kern beherrschbar. Sonst: dokumentieren, stoppen.

### B-M1 — Rechenkern (3 Wochen) → Gate B-G1

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP1.1 | Datenmodell: Gebäude/Geschoss/Raum/Bauteil (Wand, Fenster, Decke, Boden) mit Orientierung, Nachbarraum-Temperaturen | 2 d | Modell bildet 3 reale Referenzgebäude ab |
| B-AP1.2 | **Normkern Transmission + Lüftung** nach DIN EN 12831 (Norm-Außentemperatur je PLZ-Klimazone, Wärmebrücken-Pauschalen, Aufheizzuschlag) | 4 d | 2 vollständige Referenzgebäude auf ±2 % gegen etabliertes Tool (EVEBI-Test/BKI-Beispiel) |
| B-AP1.3 | **U-Wert-Kataloge:** IWU/TABULA-Baualtersklassen als Presets + manueller Override + Bauteil-Bibliothek | 2 d | Für jedes Baujahr 1919–2025 sinnvolle Defaults; Quellen dokumentiert |
| B-AP1.4 | Golden-Test-Suite + METHODIK-Doku (öffentlich, Vertrauens-Asset wie bei Studio) | 2 d | CI grün; Methodik von 1 externem Energieberater gegengelesen |
| B-AP1.5 | **Fachlicher Reviewer gewinnen** (SHK-Meister/Energieberater, gegen Honorar/Beteiligung) | 1 d (+laufend) | Reviewer benannt, hat B-AP1.2-Fälle abgenommen |

**🚦 Gate B-G1:** Referenzgebäude-Abweichung ≤2 %, Reviewer-Abnahme liegt vor. **Ohne B-G1 kein UI-Bau** — normative Korrektheit ist die Existenzfrage dieses Produkts.

### B-M2 — Erfassungs-UI (3 Wochen) → R0 „intern"

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP2.1 | Projekt-Setup: SvelteKit + Supabase (Auth, RLS, EU), CI | 1,5 d | Login → leeres Projekt → gespeichert |
| B-AP2.2 | **Geführte Raumerfassung:** Geschoss-/Raumliste, Bauteile mit Presets, Duplizieren, Tablet-Layout | 5 d | Testgebäude (6 Räume) in ≤30 Min ab Grundriss erfassbar |
| B-AP2.3 | Live-Ergebnis je Raum + Gebäudesumme, Plausibilitäts-Warnungen (W/m² außerhalb üblicher Spannen) | 2 d | Eingabefehler (z. B. Fensterfläche > Wandfläche) werden abgefangen |
| B-AP2.4 | Kunden-/Projektverwaltung, Projekt kopieren | 2 d | Zweites ähnliches Gebäude in <10 Min durch Kopieren+Anpassen |

**🚦 Gate B-G2 (= R0):** Der fachliche Reviewer erfasst ein echtes Kundenprojekt selbstständig in ≤45 Min mit korrektem Ergebnis.

### B-M3 — Nachweis-PDF & Kommerz (2 Wochen) → Gate B-G3

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP3.1 | **Förder-PDF:** versionierte Vorlage mit allen BAFA/KfW-relevanten Angaben; Muster-Wasserzeichen im Gratis-Modus | 2,5 d | Reviewer bestätigt: „würde ich so einreichen"; ein Pilotbetrieb reicht es real ein (spätestens in B-M5) |
| B-AP3.2 | Zahlung: Pay-per-Use + Flat (MoR/Stripe), Rechnungsstellung B2B | 2 d | Testkauf beider Modelle Ende-zu-Ende |
| B-AP3.3 | Recht: AGB (B2B), **AVV-Muster**, Datenschutz, Impressum, Löschkonzept | 1,5 d | Dokumente live; AVV im Registrierungs-Flow abschließbar |
| B-AP3.4 | Landingpage mit Anker-Argument (150–800 € extern vs. 39 € Flat) + Demo-Video | 1,5 d | Seite live, Gratis-Berechnung ohne Zahlungsdaten startbar |

### B-M4 — Pilot (3 Wochen Laufzeit) → **Release R1 „Pilot"**, Gate B-G4

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP4.1 | Die 5–8 Interview-Betriebe als Piloten aktivieren (3 Monate Flat gratis gegen Feedback + Referenz) | 1 d | ≥3 Betriebe rechnen echte Projekte |
| B-AP4.2 | Wöchentliche Feedback-Zyklen, Erfassungs-UI härten | 4 d | Top-5-Hürden behoben; Erfassungszeit im Feld ≤45 Min |
| B-AP4.3 | **Förder-Praxistest:** mind. 1 PDF wird real bei BAFA/KfW eingereicht und akzeptiert | — (Laufzeit) | Bewilligung ohne Nachweis-Beanstandung |

**🚦 Gate B-G4 (= R1-DoD):** ≥3 aktive Pilotbetriebe, ≥1 akzeptierter Fördernachweis, ≥2 Betriebe sagen zu, nach der Gratisphase zu zahlen.

### B-M5 — Public Launch (2 Wochen) → **Release R2**

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP5.1 | Onboarding-Politur, Beispielprojekt, Hilfe-Videos je Erfassungsschritt | 2 d | Neuer Betrieb kommt ohne Support zum ersten PDF |
| B-AP5.2 | Vertrieb: Google Ads auf „Heizlastberechnung Software/online" (kaufnahe B2B-Keywords), SHK-Foren/Facebook-Gruppen, Pilot-Referenzen als Testimonials | 2 d | Kampagne live, CPA-Messung steht |
| B-AP5.3 | stromfazit-Brücke: WP-Rechner-Seite erklärt Endkunden den Pflichtnachweis („Frag deinen Installateur — er kann ihn hier erstellen") | 0,5 d | Verweis live (B2C→B2B-Signal, bewusst klein) |

**🚦 R2-DoD:** Self-Service-Registrierung → Gratis-Berechnung → Kauf ohne manuelle Schritte; Support-FAQ deckt Pilot-Top-10 ab; Monitoring/Backups aktiv.

### B-M6 — Ausbau (3 Wochen) → **Release R3**

| AP | Inhalt | Aufwand | Akzeptanzkriterium |
|---|---|---|---|
| B-AP6.1 | **Heizkörper-Check:** Bestandsheizkörper je Raum erfassen (Typ/Maße → Leistungstabellen), Ampel bei 55/45/35 °C Vorlauf, Tauschliste | 4 d | Reviewer-Abnahme an 2 realen Projekten |
| B-AP6.2 | **Abgleich-Zuarbeit:** Export der Raumlasten (CSV/PDF) als Verfahren-B-Grundlage | 1,5 d | Ein Pilotbetrieb nutzt den Export real |
| B-AP6.3 | Team-Tarif (Mehrbenutzer, Rollen) | 2 d | 79-€-Tarif buchbar |

**Gesamtdauer ab positivem B-G0: ~14 Wochen bis R2, ~17 Wochen bis R3.**

## 6. Risiken

| Risiko | Gegenmaßnahme |
|---|---|
| **Normative Fehler → Förder-Ablehnung → Reputations-GAU** | Gate B-G1 (±2 % + Reviewer) vor jedem UI-Bau; realer Förder-Praxistest in der Pilotphase; öffentliche Methodik |
| Norm-Lizenzkosten/Urheberrecht | Norm kaufen, nur Formeln implementieren, keine Normtexte im Produkt zitieren |
| B2B-Kaltstart | Piloten aus B-M0-Interviews; kaufnahe Google-Ads-Keywords; Anker-Preisargument |
| HeizNorm/Mepbau senken Preise | Differenzierung über Erfassungs-Geschwindigkeit + Heizkörper-Check, nicht nur Preis |
| Fördervoraussetzungen ändern sich (BEG-Präzedenz) | versionierte PDF-Vorlagen, Regulatorik-Watch (gemeinsam mit stromfazit-Pflege) |
| Endkunden-Datenschutz | AVV, EU-Hosting, RLS, Löschkonzept ab B-M3 |

## 7. Startbedingung

Projekt B startet, wenn **eine** der Bedingungen eintritt:
1. Stromfazit Studio hat R2 („1.0") erreicht und läuft im Wartungsmodus, **oder**
2. Studios Gate G0 (Validierung) ist gescheitert, **oder**
3. Ein B-M0-Pilotpartner drängt mit konkreter Zahlungszusage (opportunistischer Vorzug — dann B-M0 sofort).
