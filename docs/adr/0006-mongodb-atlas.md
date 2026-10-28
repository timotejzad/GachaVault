# Gostovanje MongoDB v oblaku z MongoDB Atlas

## Context and Problem Statement

Aplikacija potrebuje trajno podatkovno bazo, dostopno backendu. Bazo želimo uporabljati brez lokalne namestitve MongoDB ali Dockerja.

## Considered Options

* Lokalna namestitev MongoDB
* MongoDB v Dockerju
* MongoDB Atlas

## Decision Outcome

Izbrana možnost: MongoDB Atlas, ker omogoča uporabo MongoDB v oblaku brez lokalnega nameščanja in zaganjanja baze.

### Consequences

* Pozitivno: Baze ni treba lokalno nameščati ali zaganjati, dostop do iste baze iz različnih razvojnih okolij pa je preprostejši.
* Negativno: Dostop je odvisen od internetne povezave in razpoložljivosti storitve ter zahteva urejene dostopne pravice in upoštevanje omejitev izbranega paketa.
