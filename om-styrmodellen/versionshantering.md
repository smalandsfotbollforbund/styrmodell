# Versionshantering

## Syfte

Detta dokument beskriver hur versionshanteringen av styrmodellen fungerar.

-----

## GitHub som versionshanteringssystem

Styrmodellen förvaltas i ett GitHub-repo. GitHub:s inbyggda versionshistorik ger automatisk teknisk spårbarhet för alla ändringar:

- varje ändring (commit) är daterad och kopplad till den som gjort ändringen
- det går att se exakt vad som ändrats, när och av vem
- tidigare versioner kan alltid återställas vid behov
- ändringshistoriken är ett permanent arkiv över styrmodellens utveckling

Det innebär att varje gång en fil uppdateras i repot skapas automatiskt ett spår.

-----

## Commit-kommentarer

För att versionshistoriken ska vara användbar ska varje commit ha en beskrivande kommentar. Kommentaren ska kortfattat ange vad som ändrats och varför. Exempel:

- “Uppdaterar kommittémodellen efter styrelsebeslut 2026-03-15”
- “Rättar stavfel och uppdaterar länk till attestordning”
- “Lägger till nytt avsnitt om riskhantering”

Vaga kommentarer som “uppdatering” eller “fix” ska undvikas.

-----

## Ändringslogg i dokumenten

Vid väsentliga revideringar av ett dokument — dvs. förändringar som påverkar innehållet, inte bara formateringen — ska en ändringslogg läggas till längst ned i dokumentet. Loggen ska ange:

- datum för ändringen
- vad som ändrades
- vilket organ som beslutade om ändringen (om relevant)

Exempel på format:

```
---
## Ändringshistorik
- 2026-03-15: Avsnittet om delegering uppdaterat efter styrelsebeslut. Ny text om brådskande beslut tillagd.
- 2025-11-01: Ursprunglig version publicerad.
```

-----

## Versionsmärkning

Styrmodellen som helhet versionsmärks inte med versionsnummer — det skulle kräva onödig administration när enskilda sidor uppdateras löpande. Istället används:

- GitHub-repots commit-historik för teknisk versionsspårning
- Datum i dokumentens ändringslogg för innehållsmässig spårning
- Datummärkning i de styrande dokumenten på [dokument.smaland.football](https://dokument.smaland.football) för de formella styrdokumenten

-----

## Externa bärande dokument

Externa dokument — RF:s stadgar, SvFF:s stadgar och RF-SISU Smålands stadgar — uppdateras av respektive organisation. SmFF sparar lokala PDF-kopior med tydlig versionsmärkning (datum och antagen version). När en ny version publiceras uppdateras länken och den gamla kopian arkiveras. Se [Dokumentarkitektur](../styrande-dokument/dokumentarkitektur.md) för mer om hanteringen av externa dokument.
