# MongoDB in Mongoose za shranjevanje podatkov

## Context and Problem Statement

Podatkovni model vključuje uporabnike, igre, bannerje, predmete, pulle, povzetke in lastništvo karakterjev. Nekateri podatki, kot so statistike karakterjev in pravila bannerjev, se med igrami razlikujejo. Hkrati morajo biti osebni zapisi povezani s pravilnim uporabnikom, igro in predmetom, ponovljen uvoz pa ne sme ustvariti podvojitev.

## Considered Options

* MongoDB z Mongoose
* PostgreSQL
* Datoteke JSON

## Decision Outcome

Izbrana možnost: MongoDB z Mongoose, ker omogoča shranjevanje različnih pravil iger in podatkov karakterjev v dokumentih.

### Consequences

* Pozitivno: Dokumenti omogočajo shranjevanje različnih podatkov za vsako igro, sheme preverjajo njihovo obliko, unikatni indeksi pa preprečujejo podvojitve izbranih zapisov.
* Negativno: Aplikacija mora preverjati povezave med dokumenti in usklajevati spremembe povezanih zapisov; ob spremembi strukture podatkov bo morda treba posodobiti tudi obstoječe zapise.
