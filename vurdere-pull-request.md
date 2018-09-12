# Vurdere pull request

1. Les gjennom akseptansekriteriene og se om de er oppfylt i koden
2. Sjekk kodekvalitet, lesbarhet og forståelse, og at ting forstås funksjonelt
3. Sjekk koden mot relevante kriterier under (og alt annet du kan komme på)
4. Kommenter mangler og ting som er bra
5. Godkjenn hvis alt ser bra ut
6. **Uansett:** Si fra på slack (i #team-aasmund-pr / #team-tuan-pr) at pull requesten har kommentarer eller er godkjent

## Endepunkter

Sjekk at

- Endringer i APIer er bakoverkompatible
- Endepunkter er tilstrekkelig beskyttet
- Endepunkter ikke eksponerer for mye/sensitiv data til brukere som ikke skal ha tilgang til det

## Database

- Ved opprettelse av tabeller eller nye kolonner, se etter potensielle behov for indekser
- Se etter manglende parametrisering av SQL. (SQL-injection)
- Sjekk at evt. endringer i migreringsscript er bakoverkompatible
- Sjekk at migreringen enten skjer fullstendig eller ikke i det hele tatt. Pass på at migreringen er wrappet inn i en transaction. Delvis migreringer er vanskelig å komme seg ut av.

## Universell utforming

- Se etter semantisk korrekt bruk av h1, h2, h3? Korrekt rekkefølge h1,h2,h3 i stedet for h6,h7,h8.
- Alle input, links, images og andre synlige elementer bør ha alt tekst.
- Input felter må ha placeholder og label.
- Alle elementer nås med tastatur. F.eks.: lenker, knapper, radioknapper, checkboxer, nedtrekksmenyer og funksjoner kan styres ved tastatur. At man kan navigere seg vekk/videre vha tastatur.
