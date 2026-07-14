# Deploy-guide — website + repo

## Repo-struktur (GitHub = filmaster)

```
<reponavn>/
├── index.html                  ← websitet (fra Website/)
├── medhold_fuld.md             ← FULD SAMLING — hovedknappen kopierer denne. GENERERES: regenerér ved enhver modulændring (se nederst)
├── moduler/
│   ├── M_START.md
│   ├── M0_Grundinstruktion.md
│   ├── M1_Sagslog.md
│   ├── M3_Forstaa_situationen.md
│   ├── M4_Svar_paa_partshoering.md
│   ├── M5_Klage.md
│   ├── M6_Aktindsigt.md
│   └── M9_Aktgennemgang.md
├── bibliotek/
│   ├── B1_Klagevejskort.md
│   ├── B3_Eskalationskort.md
│   └── B4_Videnskilder.md
├── D1_Kom_i_gang.md
├── Eksempel_Kirsten.md
├── LICENSE                     ← afventer licensvalg (åbent punkt i roadmap)
└── README.md                   ← kort projektbeskrivelse + link til websitet
```

## Trin

1. Opret offentligt GitHub-repo, læg filerne som ovenfor (index.html i roden).
2. Settings → Pages → "Deploy from branch" → main → root. Siden er live på `<bruger>.github.io/<repo>` få minutter efter.
3. Eget domæne: opret CNAME-record hos din DNS-udbyder, der peger (sub)domænet på `<bruger>.github.io`, og skriv domænet i Pages-indstillingerne (GitHub laver selv HTTPS). Virker med både `harness.nexiuslab.com` og et selvstændigt domæne.
4. Udfyld pladsholderne i `index.html` og `D1_Kom_i_gang.md`: **FEEDBACK@DOMÆNE.dk**, **buymeacoffee.com/BRUGERNAVN**, **DOMÆNE.dk** i light-fallbackens URL (index.html-scriptet), og [CLAUDE-PROJEKT-LINK]. Navn: **Medhold** (valgt 2026-07-14).
5. Opdatér [STED]-henvisningerne i `M_START.md` til de rigtige URL'er (fx `https://<domæne>/moduler/M5_Klage.md`).

## Vigtige detaljer

- **Kopiér-knapperne** på siden henter modulteksten fra de relative stier — derfor SKAL .md-filerne ligge i samme repo/host som index.html. Fallback: kan teksten ikke hentes, åbnes filen i stedet.
- **R2-links (til AI'er):** brug de rene fil-URL'er (`https://<domæne>/moduler/M_START.md`) — GitHub Pages serverer .md som ren tekst, hvilket AI'er kan læse direkte. Raw-URL'er fra github.com virker også.
- **Versionering:** bump versionsnummer + dato i filens topbanner ved hver ændring; annoncér i Facebook-gruppen.
- **Feedback-mail:** opret fx `feedback@<domæne>` eller et alias — skal ikke være Jacobs personlige.
- **`medhold_fuld.md` regenereres** ved enhver ændring i moduler/bibliotek (rækkefølge: M_START, M0, M1, M3, M4, M5, M6, M9, B1, B3, B4 med topbanner). Læg genererings-scriptet i repoet (`scripts/build_fuld.sh`) og kør det før hvert commit — eller som GitHub Action. Hovedknappen på sitet kopierer den fulde samling; "Medhold Light"-linket kopierer M_START alene (til små/gratis kontekstvinduer).
- **[REPO-ZIP-LINK]:** GitHub giver gratis zip af hele repoet på `https://github.com/<bruger>/<repo>/archive/refs/heads/main.zip` — brug den som "Download alle filer".
