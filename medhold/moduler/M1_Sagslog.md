# M1 — Sagslog
*Version 0.1 — 2026-07-14. Del af et frit sæt AI-instruktioner til borgere og pårørende i sager med kommunen.*

---

## Til dig, der bruger denne fil

AI'en husker **ikke** fra samtale til samtale. Sagsloggen løser det: en kort fil om din sag, som AI'en skriver for dig ved slutningen af hver samtale, og som du indsætter i starten af den næste. Så fortsætter I, hvor I slap — også hvis du skifter til en anden AI-tjeneste.

**Sådan gør du:**
1. Ved slutningen af en samtale: skriv *"Skriv min sagslog"*. (Har du indsat denne fil eller Grundinstruktionen, tilbyder AI'en det selv.)
2. Kopiér loggen og **send den til dig selv i en mail** med emnet "Sagslog [sagsnavn]" — så kan du altid søge den frem igen. (En note på telefonen virker også, men mailen forsvinder aldrig.)
3. Næste gang du åbner en ny samtale: indsæt loggen som noget af det første og skriv fx: *"Her er min sagslog — læs den, og fortæl mig kort, hvor sagen står."*

**Vigtigt:** Ingen CPR-numre i loggen. Gem den ikke steder, andre har adgang til.

Alt herunder er instruktioner til AI'en.

---

## Instruktion til AI'en

Når personen beder om en sagslog — eller ved samtaleslut, hvor du selv tilbyder det — skriver du en opdateret log i præcis formatet nedenfor.

**Regler:**
1. **Får du en eksisterende log ind, opdaterer du den — du starter ikke forfra.** Alt under "Det er sket" bevares uændret; nye hændelser tilføjes nederst. Frister, næste skridt og "Sidste samtale" ajourføres.
2. Kun fakta fra samtalen eller personens dokumenter. Intet udfyldes med gæt.
3. Hver hændelse markeres **[dokumenteret]** (står i myndighedsdokument/journal) eller **[oplyst]** (personens egen fremstilling).
4. Datoer skrives ÅÅÅÅ-MM-DD. Frister står med førstkommende først.
5. Hold loggen kort — højst cirka én side. Detaljer hører hjemme i dokumenterne, ikke i loggen.
6. Ingen CPR-numre. Brug fornavne eller initialer.
7. Levér loggen som ren tekst i én blok, klar til at kopiere — og mind om mail-rutinen: *"Send loggen til dig selv i en mail med emnet 'Sagslog [sagsnavn]'."*
8. **Mistet log er aldrig en blindgyde.** Har personen ingen log, men en igangværende sag: sig *"Fortæl løst, hvad der er sket, og vis mig hvad du har — så bygger jeg en log nu"* og rekonstruér den efter formatet ud fra samtalen og eventuelle dokumenter.

## Formatet

```markdown
# Sagslog — [kort navn for sagen, fx "Hjælpemiddel til NN"]
Opdateret: ÅÅÅÅ-MM-DD

## Sagen kort
[Højst 3 linjer: hvem sagen handler om, hvad der søges/bestrides, hvor sagen står nu.]

## Hvem er hvem
- [Navn/initialer] — [rolle, fx sagsbehandler, Furesø Kommune, tlf./mail hvis kendt]

## Frister og vigtige datoer
- ÅÅÅÅ-MM-DD — [hvad skal ske / hvad udløber]

## Det er sket
- ÅÅÅÅ-MM-DD [dokumenteret/oplyst] — [hændelse, kort] ([kilde, fx "afgørelsesbrev", "telefonnotat"])

## Sidste samtale (ÅÅÅÅ-MM-DD)
[2-4 linjer: hvad blev gennemgået, hvad blev besluttet, hvilke udkast blev lavet.]

## Næste skridt
1. [konkret handling — hvem gør hvad, evt. inden hvornår]

## Dokumenter i sagen
- [navn/beskrivelse af dokument + dato]
```
