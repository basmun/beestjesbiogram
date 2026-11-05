# Antibiogram-naslag

Een interactief, Nederlandstalig overzicht van welke antibiotica doorgaans werken tegen welke bacteriën, en vooral **waarom**. Het overzicht is bedoeld als leermiddel en is toegespitst op de Nederlandse situatie.

> [!WARNING]
> **Alleen voor educatief gebruik, niet voor klinische besluitvorming.**
> Dit overzicht is een vereenvoudigde, gegeneraliseerde inschatting van de verwachte activiteit van antibiotica. Het is niet gevalideerd voor de behandeling van individuele patiënten en vervangt geen kweek met gevoeligheidsbepaling, geen lokaal antibiogram, geen actuele SWAB-richtlijn of SWAB-ID en geen overleg met de arts-microbioloog of ziekenhuisapotheker. Resistentie verschilt per ziekenhuis, afdeling en patiënt. Er worden bewust **geen doseringen** genoemd. Gebruik in de kliniek altijd de officiële bronnen.

## Doelgroep

(Senior) geneeskundestudenten, bijvoorbeeld tijdens de coschappen of de voorbereiding daarop, die het verband willen leren zien tussen micro-organisme, werkingsmechanisme, resistentie en de plek van de infectie. Het overzicht is een studiehulp en geen behandelprotocol.

## Inhoud

| Bestand | Beschrijving |
|---|---|
| `index.html` | Interactieve naslag (één losstaand bestand, werkt offline in elke browser) |
| `antibiogram-print.html` | Printversie op A4 liggend (2 pagina's) |

**Interactieve naslag (`index.html`)**

- **Antibiogram:** 29 middelen × 25 verwekkers. Klik op een verwekker om te zien welke middelen werken, of op een cel voor de toelichting.
- **Waarom het werkt:** per middelgroep het werkingsmechanisme, de logica achter het spectrum, resistentiemechanismen, farmacokinetiek en Nederlandse aandachtspunten.
- **Resistentiemechanismen:** β-lactamasen, MRSA (PBP2a), ESBL, AmpC, carbapenemasen, porineverlies/efflux, MLSB en VRE.
- **Intrinsieke resistentie:** per regel staat of die uit EUCAST komt of uit het werkingsmechanisme volgt.
- **Weefselpenetratie:** liquor, long, urine, bot, prostaat, gal, abces en intracellulair.
- **Infectiehaard → verwekkers.**
- **Nederlandse resistentiecijfers** uit NethMap 2025.

**Printversie (`antibiogram-print.html`)**

- Pagina 1 is de volledige tabel.
- Pagina 2 bevat intrinsieke resistentie, weefselpenetratie, NethMap-cijfers, β-lactamasen en vuistregels.
- Zet bij het printen "Achtergrondafbeeldingen" aan, anders vallen de kleuren weg.

## Gebruik

Open `index.html` in een browser, of bekijk de online versie via GitHub Pages (`https://<gebruikersnaam>.github.io/<repo-naam>/`; de printversie staat op `.../antibiogram-print.html`). Lokaal is geen installatie of internetverbinding nodig. Beide bestanden werken los van elkaar.

## Legenda

| Teken | Betekenis |
|---|---|
| **+** | Doorgaans actief (in Nederland meestal < ~10% resistent) |
| **±** | Wisselend: verworven resistentie is relevant of het middel is alleen in specifieke situaties geschikt |
| **−** | Niet betrouwbaar of niet gebruiken. Dit omvat ook combinaties waarvoor EUCAST "–" geeft (testen niet aanbevolen) en functioneel intrinsieke resistentie die EUCAST niet als fenotype vermeldt |
| **IR** | Verwacht resistent fenotype volgens EUCAST (Expected Resistant Phenotypes v1.2) |
| **·** | Niet van toepassing |

## Methode

- **Basis:** de indeling is opgesteld vanuit algemene microbiologische kennis en Nederlandse richtlijnen.
- **Controle tegen EUCAST:** daarna is de tabel cel voor cel gecontroleerd tegen de **EUCAST Clinical Breakpoint Tables v16.1 (2026)** en de **EUCAST Expected Resistant Phenotypes v1.2**. Daarvoor is de machineleesbare versie van deze tabellen uit het AMR-pakket voor R gebruikt.
  - "IR" staat alleen bij combinaties die EUCAST als verwacht resistent noemt.
  - Waar EUCAST "–", onvoldoende bewijs (IE) of alleen een UWI-breekpunt geeft, staat dat in de toelichting bij de cel.
- **Nederlandse context:** resistentiepercentages zijn afgeronde waarden uit de samenvatting van NethMap 2025 (data 2024).

**Beperkingen**

- Anaeroben en atypische verwekkers vallen grotendeels buiten de EUCAST-fenotypelijst. Voor deze kolommen berust de indeling op het werkingsmechanisme.
- De indeling in +/± is een didactische vereenvoudiging en geen officiële categorie.

## Bronnen

1. EUCAST. Clinical Breakpoint Tables v16.1 (2026). https://www.eucast.org/clinical_breakpoints
2. EUCAST. Expected Resistant Phenotypes v1.2 (2023). https://www.eucast.org/expert_rules_and_expected_phenotypes/expected_phenotypes
3. SWAB – Stichting Werkgroep Antibioticabeleid. Richtlijnen. https://swab.nl
4. SWAB-ID – Nationaal Antibioticaboekje. https://swabid.nl
5. RIVM/SWAB. NethMap 2025 (data 2024). https://www.rivm.nl/publicaties/nethmap-one-health-2025
6. NHG-Standaarden. https://richtlijnen.nhg.org
7. Harris PNA et al. Piperacillin-tazobactam vs meropenem for E. coli or K. pneumoniae bloodstream infection with ceftriaxone resistance (MERINO). *JAMA* 2018;320:984–994.
8. Berends MS et al. AMR – An R package for working with antimicrobial resistance data. *J Stat Softw* 2022;104(3). https://github.com/msberends/AMR
9. Inspiratie voor de opzet: [aetherist/antibiogram](https://github.com/aetherist/antibiogram) (Engelstalig, VS-georiënteerd).

## Bijdragen en fouten melden

Zie je een fout of een verouderde bewering? Open een issue met de bron (bij voorkeur EUCAST, SWAB of NethMap). Wijzigingen in de tabel moeten met een bron onderbouwd worden.
