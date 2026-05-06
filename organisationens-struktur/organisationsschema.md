---
description: >-
  En visuell översikt över hur distriktets organ och funktioner hänger ihop, med
  särskild vikt på mandat, rapportering och självständighet.
---

# Organisationsschema

Organisationsschemat ska visa hur distriktets delar hänger ihop på en bild.

Det ska inte förklara hela styrmodellen en gång till. Den övergripande logiken finns i [styrarkitekturen](styrarkitektur.md), rollerna beskrivs i [ansvar och roller](ansvar-och-roller.md) och konkret ansvarsfördelning hör hemma i [ansvarsmatrisen](../strategi-och-operativt-uppdrag/ansvarsmatris.md).

{% hint style="info" %}
Schemat ska visa struktur, inte skapa mandat. Om bilden och ett beslutat dokument pekar åt olika håll gäller det beslutade dokumentet enligt [normordningen](../grund-och-varden/normordning.md).
{% endhint %}

```mermaid
graph TD
  Mermaid --> Diagram

flowchart TB

%% =========================
%% Schematisk organisation
%% =========================

subgraph Demokratisk["Demokratiskt"]
    direction LR

    Valberedning["Valberedning"]
    Revision["Revision"]
    Disciplinnamnd["Disciplinnämnd"]

    Arsmote["Årsmöte"]
    Representantskap["Representantskap"]

    Valberedning --- Arsmote
    Revision --- Arsmote
    Disciplinnamnd --- Arsmote
    Arsmote --- Representantskap
end

subgraph Strategisk["Strategiskt"]
    direction TB

    Arbetsgrupper["Arbetsgrupper"]
    Distriktsstyrelse["Distriktsstyrelse"]
    Presidium["Presidium"]

    Distriktsstyrelse --- Presidium
    Arbetsgrupper -.-> Distriktsstyrelse
end

subgraph Taktisk["Taktiskt"]
    direction LR

    Tvarfunktionellt["Tvärfunktionella<br/>och övergripande<br/>utvecklingsområden<br/>och arbetssätt"]

    Kommitte1["Kommitté"]
    Kommitte2["Kommitté"]
    Kommitte3["Kommitté"]
    Kommitte4["Kommitté"]

    Tvarfunktionellt -.-> Kommitte1
    Tvarfunktionellt -.-> Kommitte2
    Tvarfunktionellt -.-> Kommitte3
    Tvarfunktionellt -.-> Kommitte4
end

subgraph Operationell["Operationellt"]
    direction TB

    Referensgrupper["Referensgrupper"]

    Ledning["Ledning"]

    Avdelning1["Avdelning"]
    Avdelning2["Avdelning"]

    Roll1["Roll/funktion"]
    Roll2["Roll/funktion"]
    Roll3["Roll/funktion"]
    Roll4["Roll/funktion"]

    Ledning --> Avdelning1
    Ledning --> Avdelning2

    Avdelning1 --> Roll1
    Avdelning1 --> Roll2

    Avdelning2 --> Roll3
    Avdelning2 --> Roll4

    Referensgrupper -.-> Ledning
end

%% Huvudlinje
Arsmote --> Distriktsstyrelse
Distriktsstyrelse --> Kommitte1
Distriktsstyrelse --> Kommitte2
Distriktsstyrelse --> Kommitte3
Distriktsstyrelse --> Kommitte4
Distriktsstyrelse --> Ledning

%% Styling
classDef demokratisk fill:#dcefd6,stroke:#b4d3aa,color:#111;
classDef strategisk fill:#b51620,stroke:#8f1118,color:#fff;
classDef presidium fill:#d96f73,stroke:#b51620,color:#fff;
classDef taktisk fill:#efe3d2,stroke:#d4c4ad,color:#111;
classDef operationell fill:#f2f2f2,stroke:#d9d9d9,color:#111;
classDef dashed fill:#fff,stroke:#111,stroke-dasharray: 6 6,color:#111;

class Valberedning,Revision,Disciplinnamnd,Arsmote,Representantskap demokratisk;
class Distriktsstyrelse strategisk;
class Presidium presidium;
class Kommitte1,Kommitte2,Kommitte3,Kommitte4 taktisk;
class Ledning,Avdelning1,Avdelning2,Roll1,Roll2,Roll3,Roll4 operationell;
class Arbetsgrupper,Referensgrupper,Tvarfunktionellt dashed;
```

## Bilden ska visa relationerna

Ett bra organisationsschema visar inte bara rutor. Det visar relationer.

För Smålands Fotbollförbund är fyra relationer särskilt viktiga: mandat, rapportering, samverkan och granskning. De bör visas med olika linjer eller annan tydlig markering, så att läsaren ser skillnad på vem som ger uppdrag, vem som rapporterar, vem som samverkar och vem som granskar.

<table data-view="cards"><thead><tr><th></th></tr></thead><tbody><tr><td><strong>Mandat</strong><br>Vem som ger uppdrag eller beslutanderätt.</td></tr><tr><td><strong>Rapportering</strong><br>Vem som återrapporterar till vem.</td></tr><tr><td><strong>Samverkan</strong><br>Vilka som behöver arbeta tillsammans utan att vara över- eller underordnade.</td></tr><tr><td><strong>Granskning</strong><br>Vilka funktioner som ska kunna pröva, granska eller bereda självständigt.</td></tr></tbody></table>

## Grundstrukturen i bilden

Bilden bör vara enkel nog att förstå snabbt. Den behöver samtidigt vara korrekt nog för att inte skapa fel förväntningar.

{% columns %}
{% column %}
#### Det ska synas

Medlemsföreningarnas demokratiska mandat.

Årsmötet som högsta beslutande organ.

Representantskapet som medlemsorgan för tävlingsfrågor.

Distriktsstyrelsen som strategisk ledning mellan de demokratiska mötena.

Distriktschef och kansli som operativ ledning och genomförande.
{% endcolumn %}

{% column %}
#### Det ska hållas isär

Granskande funktioner rapporterar till årsmötet.

Arbetsgrupper rapporterar till distriktsstyrelsen om inte annat beslutats.

Referensgrupper rapporterar till kansliet om inte annat beslutats.

Kommittéer är inte egna styrelser.

Presidiet är inte ett parallellt beslutsorgan.
{% endcolumn %}
{% endcolumns %}

## En skiss för hur det kan ritas

```
Medlemsföreningar
        │
        ▼
Årsmöte
   │        ▲
   │        │ rapportering / granskning
   │        │
   │   Valberedning
   │   Revision
   │   Lekmannarevision
   │   Disciplinnämnd
   │
   ├── Representantskap
   │
   ▼
Distriktsstyrelse ── Presidium
        │
        ├── Kommittéer
        │
        ├── Arbetsgrupper
        │       └── rapporterar till distriktsstyrelsen
        │
        ▼
Distriktschef
        │
        ▼
Kansli
        │
        └── Referensgrupper
                └── rapporterar till kansliet
```

Skissen är inte färdig formgivning. Den visar huvudlogiken: medlemsföreningarna bär mandatet, årsmötet är den högsta demokratiska nivån, distriktsstyrelsen leder mellan de demokratiska mötena, kansliet genomför i vardagen och granskande funktioner står vid sidan av den operativa linjen.

## Rita inte in mer än bilden klarar

Organisationsschemat ska inte bära all information. Om varje projekt, roll, kontaktperson och arbetsflöde ritas in blir bilden svår att använda.

{% hint style="warning" %}
Om schemat kräver långa förklaringar har det blivit för detaljerat. Flytta då detaljer till arbetsordningar, instruktioner, processer, bilagor eller andra dokument i [dokumentarkivet](https://app.gitbook.com/o/TR51rgBV2VcNfsavrrCR/s/ENOAH9wAe9WidINWNBqc/).
{% endhint %}

Ett bra schema ska hjälpa läsaren att hitta rätt nästa steg. Inte svara på varje fråga själv.
