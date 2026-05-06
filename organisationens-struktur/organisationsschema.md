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
flowchart TB

%% =========================
%% ORGANISATIONSSTRUKTUR
%% Layout styrd efter originalets ordning
%% =========================

%% --- ÖVERSTA RADEN ---
subgraph DemokratiskRad[" "]
    direction LR

    subgraph GranskandeFunktioner[" "]
        direction TB
        Valberedning["Valberedning"]
        Revision["Revision"]
        Disciplinnamnd["Disciplinnämnd"]
    end

    Arsmote["Årsmöte"]
    Representantskap["Representantskap"]
end


%% --- STRATEGISK RAD ---
subgraph StrategiskRad[" "]
    direction LR

    Arbetsgrupper["Arbetsgrupper"]

    subgraph Styrelseblock[" "]
        direction LR
        Distriktsstyrelse["Distriktsstyrelse"]
        Presidium["Presidium"]
    end

    StrategiskSlut[" "]
end


%% --- TAKTISK RAD ---
subgraph TaktiskRad[" "]
    direction LR

    Tvarfunktionella["Tvärfunktionella<br/>och övergripande<br/>utvecklingsområden<br/>och arbetssätt"]

    subgraph Kommitteblock[" "]
        direction LR
        Kommitte1["Kommitté"]
        Kommitte2["Kommitté"]
        Kommitte3["Kommitté"]
        Kommitte4["Kommitté"]
    end

    TaktiskSlut[" "]
end


%% --- OPERATIONELL RAD ---
subgraph OperationellRad[" "]
    direction LR

    Referensgrupper["Referensgrupper"]

    subgraph Kansliblock[" "]
        direction TB

        Ledning["Ledning"]

        subgraph Avdelningsrad[" "]
            direction LR
            Avdelning1["Avdelning"]
            Avdelning2["Avdelning"]
        end

        subgraph Rollrad[" "]
            direction LR
            Roll1["Roll/funktion"]
            Roll2["Roll/funktion"]
            Roll3["Roll/funktion"]
            Roll4["Roll/funktion"]
        end
    end

    OperationellSlut[" "]
end


%% =========================
%% FORMELLA LINJER
%% =========================

Valberedning --- Arsmote
Revision --- Arsmote
Disciplinnamnd --- Arsmote

Arsmote --- Representantskap
Arsmote --> Distriktsstyrelse

Distriktsstyrelse --- Presidium

Distriktsstyrelse --> Kommitte1
Distriktsstyrelse --> Kommitte2
Distriktsstyrelse --> Kommitte3
Distriktsstyrelse --> Kommitte4

Distriktsstyrelse --> Ledning

Ledning --> Avdelning1
Ledning --> Avdelning2

Avdelning1 --> Roll1
Avdelning1 --> Roll2

Avdelning2 --> Roll3
Avdelning2 --> Roll4


%% =========================
%% STÖDJANDE / TVÄRFUNKTIONELLA LINJER
%% =========================

Arbetsgrupper -.-> Distriktsstyrelse

Tvarfunktionella -.-> Kommitte1
Tvarfunktionella -.-> Kommitte2
Tvarfunktionella -.-> Kommitte3
Tvarfunktionella -.-> Kommitte4

Referensgrupper -.-> Ledning


%% =========================
%% OSYNLIGA LAYOUT-LÄNKAR
%% De hjälper Mermaid att hålla ordningen
%% =========================

Arbetsgrupper ~~~ Styrelseblock
Styrelseblock ~~~ StrategiskSlut

Tvarfunktionella ~~~ Kommitteblock
Kommitteblock ~~~ TaktiskSlut

Referensgrupper ~~~ Kansliblock
Kansliblock ~~~ OperationellSlut


%% =========================
%% STYLING
%% =========================

classDef green fill:#b9d7ae,stroke:#b9d7ae,color:#111;
classDef red fill:#b51620,stroke:#b51620,color:#fff;
classDef lightred fill:#da7073,stroke:#da7073,color:#fff;
classDef beige fill:#efe3d2,stroke:#efe3d2,color:#111;
classDef white fill:#f7f7f7,stroke:#f7f7f7,color:#111;
classDef dashed fill:#ffffff,stroke:#111,stroke-dasharray: 6 6,color:#111;
classDef invisible fill:transparent,stroke:transparent,color:transparent;

class Valberedning,Revision,Disciplinnamnd,Arsmote,Representantskap green;
class Distriktsstyrelse red;
class Presidium lightred;
class Kommitte1,Kommitte2,Kommitte3,Kommitte4 beige;
class Ledning,Avdelning1,Avdelning2,Roll1,Roll2,Roll3,Roll4 white;
class Arbetsgrupper,Tvarfunktionella,Referensgrupper dashed;
class StrategiskSlut,TaktiskSlut,OperationellSlut invisible;

style DemokratiskRad fill:#dcefd6,stroke:#dcefd6
style StrategiskRad fill:#efb8b8,stroke:#efb8b8
style TaktiskRad fill:#f3eee8,stroke:#f3eee8
style OperationellRad fill:#f4f4f4,stroke:#f4f4f4

style GranskandeFunktioner fill:transparent,stroke:transparent
style Styrelseblock fill:#b51620,stroke:#b51620
style Kommitteblock fill:#e8dcc9,stroke:#e8dcc9
style Kansliblock fill:#eeeeee,stroke:#eeeeee
style Avdelningsrad fill:transparent,stroke:transparent
style Rollrad fill:transparent,stroke:transparent
```

## Bilden ska visa relationerna

Ett bra organisationsschema visar inte bara rutor. Det visar relationer.

För Smålands Fotbollförbund är fyra relationer särskilt viktiga: mandat, rapportering, samverkan och granskning. De bör visas med olika linjer eller annan tydlig markering, så att läsaren ser skillnad på vem som ger uppdrag, vem som rapporterar, vem som samverkar och vem som granskar.

<table data-view="cards"><thead><tr><th></th></tr></thead><tbody><tr><td><strong>Mandat</strong><br>Vem som ger uppdrag eller beslutanderätt.</td></tr><tr><td><strong>Rapportering</strong><br>Vem som återrapporterar till vem.</td></tr><tr><td><strong>Samverkan</strong><br>Vilka som behöver arbeta tillsammans utan att vara över- eller underordnade.</td></tr><tr><td><strong>Granskning</strong><br>Vilka funktioner som ska kunna pröva, granska eller bereda självständigt.</td></tr></tbody></table>

## Grundstrukturen i bilden

Bilden bör vara enkel nog att förstå snabbt. Den behöver samtidigt vara korrekt nog för att inte skapa fel förväntningar.

{% columns %}
{% column %}
**Det ska synas**

Medlemsföreningarnas demokratiska mandat.

Årsmötet som högsta beslutande organ.

Representantskapet som medlemsorgan för tävlingsfrågor.

Distriktsstyrelsen som strategisk ledning mellan de demokratiska mötena.

Distriktschef och kansli som operativ ledning och genomförande.
{% endcolumn %}

{% column %}
**Det ska hållas isär**

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
