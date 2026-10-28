# Uporaba Reacta za uporabniški vmesnik

## Context and Problem Statement

GachaVault podpira Honkai: Star Rail in Wuthering Waves v istem uporabniškem vmesniku. Obe igri uporabljata podobne prikaze zgodovine, filtre, statistiko, obrazce in mrežo karakterjev. Ob preklopu igre se morajo prikazani podatki in trenutno stanje vmesnika uskladiti. Potrebujemo način razvoja, ki omogoča ponovno uporabo teh delov in omeji podvajanje.

## Considered Options

* HTML, CSS in JavaScript brez ogrodja
* React z Vite
* Vue z Vite

## Decision Outcome

Izbrana možnost: React z Vite, ker skupne komponente omogočajo ponovno uporabo prikazov obeh iger in usklajevanje interaktivnega vmesnika.

### Consequences

* Pozitivno: Skupne komponente zmanjšajo podvajanje vmesnikov obeh iger, poenotijo prikaz in olajšajo dodajanje podobnih strani.
* Negativno: Nepravilna uporaba komponent in stanja lahko povzroči nepotrebno ponovno izrisovanje ter upočasni dolge sezname pullov.
