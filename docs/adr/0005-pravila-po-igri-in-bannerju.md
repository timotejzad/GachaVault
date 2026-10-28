# Ločena pravila po igri in skupini bannerjev

## Context and Problem Statement

Podprti igri in vrste bannerjev nimajo nujno enakih meja pityja ali pravil zagotovila. Nekateri zaporedni dogodki si delijo pity, druge skupine pa so neodvisne. Skupni števec za vse bannerje bi zato povzročil napačne rezultate, popolnoma ločen števec za vsak dogodek pa bi izgubil prenos stanja znotraj iste skupine.

## Considered Options

* Enotna pravila in števci za vse bannerje
* Ločeno stanje za vsak posamezni dogodek
* Pravila po igri in vrsti bannerja ter stanje po uporabniku, igri in skupini bannerjev

## Decision Outcome

Izbrana možnost: Ločena pravila za vsako igro in vrsto bannerja ter ločeni števci za vsakega uporabnika, igro in skupino bannerjev, da se pity in zagotovilo prenašata samo med bannerji, ki si ju delijo.

### Consequences

* Pozitivno: Ločena pravila preprečujejo mešanje števcev med igrami, omogočajo prenos pityja med povezanimi bannerji in olajšajo podporo dodatnim igram.
* Negativno: Različna pravila zahtevajo dodatno konfiguracijo in preverjanje, napačna razvrstitev bannerja ali sprememba pravil pa lahko vpliva na zgodovinske izračune.
