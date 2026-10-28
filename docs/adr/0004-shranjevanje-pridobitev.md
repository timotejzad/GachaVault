# Shranjevanje 4★ in 5★ pullov ter ločenih števcev

## Context and Problem Statement

GachaVault prikazuje posamezne 4★ in 5★ pulle, skupno število pullov in trenutni pity. Tudi 3★ pulli vplivajo na te števce, zato moramo njihove učinke ohraniti, čeprav posameznih zapisov ne shranimo.

## Considered Options

* Shranjevanje vseh pullov
* Shranjevanje samo 4★ in 5★ pullov
* Shranjevanje 4★ in 5★ pullov ter ločenih števcev

## Decision Outcome

Izbrana možnost: Shranjujemo samo 4★ in 5★ pulle, skupno število pullov in trenutni pity pa hranimo ločeno, da zmanjšamo količino shranjenih podatkov.

### Consequences

* Pozitivno: Manj zapisov zmanjša porabo prostora v bazi, ločeni števci pa ohranijo skupno število pullov in trenutni pity.
* Negativno: Posameznih 3★ pullov pozneje ne moremo pregledati ali ponovno obdelati, ob ponovnem uvozu pa moramo preprečiti podvajanje pullov in napačno povečevanje števcev.
