# Projekt B (Backlog): HeizlastCheck — förderkonforme Heizlast-Schnellrechnung für SHK-Betriebe

> Status: **dokumentiertes Zweitprojekt.** Start frühestens nach Launch von Stromfazit Studio (M5) — oder früher, falls dessen M0-Validierungs-Gate scheitert. Basis: B2B-Software-Recherche August 2026 (docs/06, Befund 1).

## Warum diese Lücke real ist

- Die **raumweise Heizlastberechnung nach DIN/TS 12831 ist Pflichtnachweis für jede BAFA/KfW-Wärmepumpen-Förderung** (seit 2023) — ohne Nachweis keine Auszahlung.
- Extern eingekauft kostet sie **150–800 € pro Gebäude**; die Erstellung wird also mit echtem Geld bezahlt, nicht mit Aufmerksamkeit.
- Das günstigste Cloud-Tool startet bei **~90–98 €/Monat** (HeizNorm ab 98 €, Mepbau ab 89,99 €); in den Desktop-Suiten ist Heizlast ein **299-€-Zusatzmodul** auf einer 649-€-Jahreslizenz (EVEBI).
- **Fehlend: ein 29–49 €/Monat-Tool oder Pay-per-Use (19–29 €/Berechnung)** für den kleinen SHK-Betrieb mit 2–3 Berechnungen im Monat — genau die Preislogik, mit der iSFP-Turbo (29–69 €/Monat) gegen die Suiten gewinnt.
- Zahlungsbereitschaft der Zielgruppe ist die am besten belegte im gesamten Software-Brainstorming: Handwerksbetriebe zahlen nachweislich 30–150 €/Monat für Bürosoftware (ToolTime, Plancraft, Meisterwerk, HERO).

## Produktskizze

- **Form:** Browser-Tool (Cloud), kein Desktop — SHK-Betriebe wollen keinen Installationsaufwand, und das Dokument (PDF) ist das Produkt.
- **Kern-Workflow („Heizlast in 30 Minuten"):** Gebäude anlegen → Räume erfassen (geführte Eingabe: Maße, Außenflächen, Fenster, Baualtersklasse mit U-Wert-Katalogen) → Norm-Berechnung → **BAFA/KfW-konformes PDF** mit allen Nachweisangaben.
- **Beschleuniger (Differenzierung):** Baualtersklassen-Presets statt U-Wert-Suche, Raum-Duplizieren, Vorlagen je Gebäudetyp; später Grundriss-Foto-Unterstützung.
- **Preismodell:** Pay-per-Use 24 €/Berechnung ODER Flat 39 €/Monat (unbegrenzt), monatlich kündbar. Erste Berechnung kostenlos (Qualitätsbeweis).
- **Erweiterungen später:** JAZ-Nachweis nach VDI 4650 als Gratis-Beigabe (Commodity, aber im selben Workflow), Fördermittel-Nachweis-Doku (die zweite dokumentierte B2B-Lücke, docs/06 Kandidat C) als Zusatzmodul, Brücke zur Berater-Lizenz von Stromfazit Studio.

## Voraussetzungen & Risiken

| Punkt | Einschätzung |
|---|---|
| **Normative Korrektheit** | Eintrittshürde Nr. 1: DIN/TS 12831 muss fachlich sitzen — fehlerhafte Nachweise = Förder-Ablehnungen = Reputations-GAU. Vor dem Bau: Norm-Zugang beschaffen, Referenzberechnungen gegen etablierte Tools validieren, idealerweise einen SHK-Meister/Energieberater als fachlichen Reviewer gewinnen. |
| **B2B-Kaltstart** | Kein bestehender Kanal (stromfazit ist B2C). Brücken: der stromfazit-WP-Rechner erklärt Endkunden den Pflichtnachweis („Frag deinen Installateur…"), SHK-Foren/Facebook-Gruppen, Google Ads auf „Heizlastberechnung Software" (kaufnahe B2B-Keywords sind bezahlbar). |
| **Konkurrenz-Reaktion** | HeizNorm/Mepbau können Preise senken — Differenzierung muss Workflow-Geschwindigkeit sein, nicht nur Preis. |
| **Regulatorik** | Fördervoraussetzungen ändern sich (BEG-Reform-Präzedenz) — PDF-Vorlagen müssen versioniert nachziehbar sein. |

## Validierung (vor jedem Bau-Commitment, ~1 Woche)

1. **Fünf SHK-Betriebe anrufen/anschreiben:** „Was zahlt ihr heute pro Heizlastberechnung — intern (Zeit) oder extern (€)? Würdet ihr 24 €/Berechnung für ein 30-Minuten-Tool zahlen?"
2. HeizNorm/Mepbau-Testaccounts anlegen: Wo genau sind sie langsam/teuer? (Feature-Lücken-Liste)
3. Normzugang + Aufwandsschätzung für den Berechnungskern durch Probe-Implementierung eines Einzelraums.

**Go-Kriterium:** Mindestens 3 von 5 Betrieben bestätigen den Schmerz UND die Preisbereitschaft; Norm-Kern in Probe-Implementierung beherrschbar.

## Aufwand

MVP 8–10 Wochen (Raumerfassungs-UI ist der Löwenanteil, nicht die Norm-Mathematik). Kein gemeinsamer Code mit Stromfazit Studio nötig — bewusst unabhängiges Standbein.
