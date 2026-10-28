# Ločen backend z Node.js in Express

## Context and Problem Statement

Frontend potrebuje dostop do uporabnikovih pullov, kataloga in bannerjev. Uvoz zahteva obdelavo zgodovine dveh iger, preverjanje podvojitev in izračune pityja.

## Considered Options

* Večina logike v brskalniku z neposrednim dostopom do podatkovnih storitev
* Ločen REST API z Node.js in Express
* Ločen API s Python in FastAPI

## Decision Outcome

Izbrana možnost: Ločen REST API z Node.js in Express, ker omogoča uporabo JavaScripta na frontendu in backendu ter centralno obdelavo podatkov in preverjanje pravic.

### Consequences

* Pozitivno: Isti jezik na frontendu in backendu olajša razvoj, ločen API pa centralizira preverjanje pravic in izračune ter omogoča neodvisno spreminjanje vmesnika.
* Negativno: Ločen API zahteva dodatno konfiguracijo, validacijo zahtevkov in obravnavo napak pri komunikaciji.
