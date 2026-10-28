# 02 – Funkcionalnosti in obseg

## Uporabniške vloge

### Uporabnik

- Uvozi zgodovino ali ročno vnese svoje 4★ in 5★ pridobitve s pityjem.
- Spremlja pity, zagotovilo, statistiko in lastništvo karakterjev s številom dvojnikov.
- Pregleduje bannerje; uporablja načrtovane funkcionalnosti kalkulatorja, wishlista, izvoza in vodenja zgradbe karakterjev.
- Nima pravic za urejanje bannerjev, kataloga ali uporabniških vlog in ne vidi zasebnih podatkov drugih uporabnikov.

### Moderator

- Ima uporabniške pravice za svoje podatke.
- Dodaja in ureja bannerje: ime, igro, vrsto, termine in izpostavljene predmete iz obstoječega kataloga.
- Nima pravic za dodajanje ali urejanje kataloških predmetov, upravljanje računov in spreminjanje vlog.
- Ne vidi zasebnih zgodovin, zbirk in valut drugih uporabnikov.

### Administrator

- Ima pravice uporabnika in moderatorja.
- Vzdržuje katalog podprtih iger, karakterjev in orožij ter njihove portrete in pravila.
- Upravlja uporabniške račune in vloge. Urejanje kataloga je njegova posebna pravica, ki je moderator nima.
- Ne more izbrisati predmeta, dokler je povezan z zgodovino ali bannerjem.
- Administratorska vloga ne omogoča vpogleda v zasebne podatke drugih uporabnikov ali v izvorna gesla.

## Predvidene funkcionalnosti

1. **Uvoz zgodovine (MVP)** – vodič in avtomatski uvoz prek URL-ja; izračun pityjev ter povzetka, shranjevanje samo 4★ in 5★ pridobitev ter preprečevanje podvojitev.
2. **Ročni vnos pridobitev (MVP)** – alternativni zavihek za vnos karakterja ali orožja, bannerja, datuma in obveznega pityja. Sistem iz pityjev oceni skupno število pullov.
3. **Pity in zagotovilo (MVP)** – spremljanje trenutnega 4★ in 5★ pityja ter samodejni izračun zagotovila iz rezultatov in pravil bannerja. Pri ročnem vodenju uporabnik dopolni trenutna pityja.
4. **Statistika sreče (MVP)** – povprečni 5★ pity, delež 5★ pridobitev, uspešnost nezagotovljenih 50/50 in osebni indeks sreče; pri ocenjenem skupnem številu so izpeljani deleži označeni kot ocene.
5. **Pregled zgodovine pridobitev (MVP)** – zadnje 5★ pridobitve s portreti in pityji, filtri igre, vrste bannerja, dogodka in redkosti ter seznam z največ 20 zapisi na stran.
6. **Pregled karakterjev (MVP)** – prikaz vseh karakterjev, sivih manjkajočih in števila dvojnikov pridobljenih karakterjev; možnost ročnega vnosa skupnega števila kopij brez ustvarjanja pullov.
7. **Koledar bannerjev (MVP)** – pregled trenutnih, prihajajočih in preteklih dogodkov s termini in izpostavljenimi predmeti.
8. **Izbira igre** – preklop med Honkai: Star Rail in Wuthering Waves v istem računu z ločenimi podatki in pravili.
9. **Kalkulator potrebnih pullov** – izračun manjkajočih pullov in valute za zagotovljeno pridobitev glede na trenutni pity, zagotovilo, valuto in vstopnice.
10. **Podatki o zgrajenih karakterjih** – vodenje levela, eidolona oziroma sequence, statistik in opreme.
11. **Ocena porabljene valute** – izračun oziroma ocena pullov v obdobju bannerja in njihove protivrednosti v igralni valuti.
12. **Wishlist in prihranki** – izračun za vse želene karakterje in skupni načrt prihrankov; vrstni red določa začetek bannerja, nato čas dodajanja, brez ročnega določanja prioritet.
13. **Upravljanje kataloga** – administrator dodaja in popravlja 4★ in 5★ karakterje in orožja za pravilno izbiro pri vnosu ter vzdrževanju bannerjev.
14. **Izvoz podatkov** – izvoz zgodovine ali lastne zbirke v JSON oziroma CSV za izbrano igro ali obe igri.
15. **Urejanje bannerjev** – moderator dodaja in popravlja bannerje ter izbira izpostavljene predmete iz kataloga; sistem preveri termine in pripadnost predmetov igri ter vrsti bannerja.

Sedem označenih funkcionalnosti predstavlja jedro prve različice. Izbira dveh iger in osnovno upravljanje kataloga ter bannerjev so podporni deli, potrebni za uporabo tega jedra. Funkcionalnosti sledijo istemu zaporedju kot uporabniške zgodbe druge naloge.

## Netrivialni delovni proces

Uporabnik izbere igro in uvozi zgodovino prek URL-ja. Sistem prebere zapise v izvorni časovni razvrstitvi, izračuna pity in stanje zagotovila ter preveri podvojitve. Shrani samo 4★ in 5★ pridobitve in povzetke, nato dopolni zbirko ter število kopij karakterjev in prikaže statistiko. Ponovljen uvoz ne poveča števila pridobitev ali dvojnikov. Ročni vnos je alternativni proces z obveznim pityjem; skupno število pullov se pri njem označi kot ocena.

## Kasnejše nadgradnje

- Podpora dodatnim gacha igram.
- Javno deljenje lastnih zbirk.
- Uvoz statistik zgrajenih karakterjev iz posnetkov zaslona.
- Obvestila pred začetkom ali koncem bannerja.
- Samodejno osveževanje kataloga in bannerjev iz zunanjih virov.

## Out of scope

- Nakup igralne valute, plačila in izvajanje ali simulacija pullov.
- Shranjevanje posameznih 3★ pridobitev.
- Polna wiki enciklopedija, novice in vodiči za igranje.
- Globalne lestvice sreče ali primerjanje zasebne zgodovine uporabnikov.
- Komentarji, družabne objave in druge skupnostne funkcije.
- Več ločenih igralnih računov iste igre v enem uporabniškem računu v MVP.
