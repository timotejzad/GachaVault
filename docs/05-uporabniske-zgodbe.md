# 05 – Uporabniške zgodbe: GachaVault

## US-01 – Uvoz zgodovine

**Povezana funkcionalnost:** Uvoz zgodovine  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim uvoziti zgodovino prek URL-ja, da mi pridobitev ni treba vnašati posamično.

**Pogoji sprejema:**

1. Uporabnik izbere igro in enega od zavihkov »Avtomatsko (URL)« ali »Ročno«. Vodič pojasni oba načina kot alternativi.
2. Avtomatski zavihek vsebuje polje za URL in gumb za uvoz. Ob neveljavnem ali pretečenem URL-ju se prikaže napaka.
3. Sistem iz uvožene zgodovine izračuna pity ob pridobitvah in trenutno stanje števcev, nato shrani samo 4★ in 5★ pridobitve ter izračunano stanje; zapisov 3★ ne shranjuje.
4. Ponoven uvoz iste pridobitve ne ustvari podvojitve; po uspehu se izpiše število dodanih in preskočenih pridobitev.

## US-02 – Ročni vnos pridobitev

**Povezana funkcionalnost:** Ročni vnos pridobitev  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim vnesti 4★ ali 5★ karakter oziroma orožje s pityjem ob pridobitvi, da lahko zgodovino vodim brez URL-ja.

**Pogoji sprejema:**

1. Ročni zavihek omogoča izbor igre, bannerja, predmeta redkosti 4★ ali 5★, datuma in obveznega pityja ob pridobitvi.
2. Pity je celo število od 1 do dovoljene meje izbrane redkosti, če je meja določena; predmet in banner morata pripadati izbrani igri.
3. Sistem shrani vneseni pity in pridobitev prikaže v zgodovini; na podlagi zaporedja pityjev izračuna oceno skupnega števila pullov.
4. Stanje zagotovila izračuna sistem iz zaporedja 5★ pridobitev in izpostavljenih predmetov bannerja; uporabnik ga ne izbira ročno.

## US-03 – Pity in zagotovilo

**Povezana funkcionalnost:** Pity in zagotovilo  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim spremljati trenutni pity in zagotovilo naslednje izpostavljene pridobitve, da vem, kako blizu sem naslednji pomembni pridobitvi.

**Pogoji sprejema:**

1. Povzetek za izbrano igro in skupino bannerjev pokaže trenutni 4★ in 5★ pity ter stanje zagotovila, kadar ga pravila uporabljajo.
2. Avtomatski uvoz šteje pulle od zadnje pridobitve posamezne redkosti. Če so po zadnji 5★ pridobitvi sledili trije pulli brez nove 5★, je trenutni 5★ pity 3.
3. Pri omejenem karakter bannerju s pravilom 50/50 standardni, neizpostavljeni 5★ karakter pomeni poraz in zagotovljeno naslednjo izpostavljeno pridobitev. Izpostavljena 5★ pridobitev zagotovilo porabi; standardni banner sam ne ustvarja tega zagotovila.
4. Pri ročnem vodenju sistem izračuna zagotovilo iz vnesenega zaporedja, uporabnik pa vnese le trenutni 4★ in 5★ pity, ker iz zadnje pridobitve ni mogoče ugotoviti poznejših pullov.

## US-04 – Statistika sreče

**Povezana funkcionalnost:** Statistika sreče  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim videti povprečni pity, delež 5★ pridobitev in uspešnost 50/50, da lahko ocenim svoje rezultate.

**Pogoji sprejema:**

1. Statistika za izbrano igro in skupino bannerjev prikaže povprečni 5★ pity ter delež 5★ pridobitev glede na izračunano skupno število pullov.
2. Pityji 20, 40 in 60 dajo povprečje 40. Osebni indeks sreče je 100 × (H − povprečje) / (H − 1), kjer je H meja 5★ pityja; ni globalni percentil.
3. Delež dobljenih 50/50 upošteva samo nezagotovljene poskuse: dve zmagi in en poraz pomenijo 66,7 %. Pri bannerjih brez tega pravila se ta podatek ne prikaže.
4. Če izračun skupnih pullov temelji na ročnih pityjih, sta skupno število in iz njega izpeljani delež označena kot ocena; pri prazni zgodovini se prikaže poziv k uvozu.

## US-05 – Pregled zgodovine pridobitev

**Povezana funkcionalnost:** Pregled zgodovine pridobitev  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim pregledovati svoje 4★ in 5★ pridobitve ter zadnje 5★ rezultate, da hitro najdem pomembne rezultate svojih pullov.

**Pogoji sprejema:**

1. Uporabnik izbere igro, vrsto bannerja in po želji dogodek; filter redkosti ponudi 4★, 5★ ali obe.
2. Nad seznamom je prikazanih največ 20 zadnjih 5★ pridobitev s portretom in pityjem, od najnovejše naprej.
3. Povzetek vsebuje pity, zagotovilo, izračunano skupno število pullov, števili 4★ in 5★ pridobitev ter statistiko sreče.
4. Seznam prikazuje datum, predmet, redkost in pity; prikazanih je največ 20 zapisov na stran. Ročni vnos brez pityja ni mogoč, pri uvozu pa se pity izračuna pred shranjevanjem.
5. Če ni pridobitev za izbrani filter, se prikaže obvestilo in povezava do uvoza.

## US-06 – Pregled karakterjev

**Povezana funkcionalnost:** Pregled karakterjev  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim videti vse karakterje in število njihovih dvojnikov, da vem, katere že imam in katere še zbiram.

**Pogoji sprejema:**

1. Prikaz vsebuje vse karakterje izbrane igre: 5★ na vrhu in 4★ pod njimi.
2. Pridobljeni karakterji imajo običajen prikaz, nepridobljeni so sivi, brez besedila »Ni pridobljen«.
3. V kotu pridobljenega karakterja je število dvojnikov: ena pridobljena kopija pomeni 0, tri kopije pa 2 dvojnika. Število se izračuna iz zgodovine pullov, razen če uporabnik ročno vnese skupno število kopij.
4. Uporabnik lahko vnese skupno število kopij karakterja, tudi 0. Vnesena vrednost nadomesti število iz zgodovine in ne doda pullov. Odstranitev ročne vrednosti znova uporabi število iz zgodovine.

## US-07 – Koledar bannerjev

**Povezana funkcionalnost:** Koledar bannerjev  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim pregledovati trenutne, prihajajoče in pretekle bannerje, da lahko načrtujem pridobivanje želenih karakterjev.

**Pogoji sprejema:**

1. Koledar omogoča izbiro igre ter filtrov »Trenutni«, »Prihajajoči« in »Pretekli«.
2. Vsak banner prikaže ime, vrsto, začetek, konec in izpostavljene predmete.
3. Banner je prihajajoč pred začetkom, trenutni od začetka do konca in pretekli od konca naprej; čas je prikazan v navedenem lokalnem časovnem pasu.

## US-08 – Izbira igre

**Povezana funkcionalnost:** Izbira igre  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim preklapljati med Honkai: Star Rail in Wuthering Waves, da lahko obe igri spremljam v istem računu.

**Pogoji sprejema:**

1. Začetni zaslon vsebuje izbiro obeh iger; izbrano igro je mogoče zamenjati tudi v glavi aplikacije.
2. Preklop pokaže zgodovino, karakterje in bannerje izbrane igre ter ohrani podatke druge igre.
3. Izračuni uporabljajo pravila izbrane igre in skupine bannerjev; podatki ene igre ne vplivajo na drugo.

## US-09 – Kalkulator potrebnih pullov

**Povezana funkcionalnost:** Kalkulator potrebnih pullov  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim izračunati manjkajoče pulle za želeni karakter, da vem, koliko valute moram še prihraniti.

**Pogoji sprejema:**

1. Uporabnik izbere karakter, vnese stanje valute in razpoložljivih vstopnic; sistem uporabi trenutni pity in izračunano zagotovilo.
2. Pri meji H in pityju P je največje potrebno število pullov H − P z zagotovilom oziroma 2 × H − P brez zagotovila pri pravilu 50/50.
3. Pri H = 90, P = 30 in zagotovilu je potrebnih 60 pullov. Pri 20 vstopnicah, 1600 valute in ceni 160 manjka 30 pullov oziroma 4800 valute.
4. Rezultat predstavlja zagotovljeno pridobitev v najslabšem primeru.

## US-10 – Podatki o zgrajenih karakterjih

**Povezana funkcionalnost:** Podatki o zgrajenih karakterjih  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim shraniti level, nadgradnje, statistike in opremo karakterja, da spremljam njegovo trenutno zgradbo.

**Pogoji sprejema:**

1. Uporabnik izbere svoj karakter in vnese level, eidolon oziroma sequence, statistike ter opremo.
2. Po shranitvi in ponovnem odprtju so prikazane shranjene vrednosti.
3. Level in nadgradnje so cela števila v dovoljenem razponu izbrane igre; neveljaven vnos se zavrne z navedbo razpona.

## US-11 – Ocena porabljene valute

**Povezana funkcionalnost:** Ocena porabljene valute  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim videti oceno valute, porabljene med bannerjem, da lažje primerjam svojo porabo.

**Pogoji sprejema:**

1. Sistem izračuna število pullov v obdobju izbranega bannerja iz uvoznega povzetka oziroma oceni iz ročno vnesenih pityjev ter ga pomnoži s ceno pulla.
2. Pri izračunanih 25 pullih in ceni 160 enot znaša ocena 4000 enot igralne valute.
3. Prikaz je označen kot protivrednost v igralni valuti, vključno z vstopnicami, ne kot poraba denarja.

## US-12 – Wishlist in prihranki

**Povezana funkcionalnost:** Wishlist in prihranki  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim dodati želene karakterje na wishlist in izračunati njihove stroške, da vem, koliko moram prihraniti za vse svoje cilje.

**Pogoji sprejema:**

1. Uporabnik lahko na wishlist doda več karakterjev iz prihajajočih bannerjev; istega karakterja na istem bannerju ne more podvojiti.
2. Sistem za vse vnose prikaže izračun potrebnih pullov za vsakega karakterja in skupno potrebno količino. Za zaporedne cilje upošteva porabo trenutnega pityja in zagotovila samo pri prvem cilju iste skupine.
3. Začetni cilj določi datum začetka bannerja, pri istem datumu pa vrstni red dodajanja; uporabniku ni treba določati prioritet.
4. Skupni izračun prihrankov obstoječo valuto in vstopnice odšteje samo enkrat; odstranitev cilja spremeni skupni načrt.

## US-13 – Upravljanje kataloga

**Povezana funkcionalnost:** Upravljanje kataloga  
**Uporabniška vloga:** Administrator

**Uporabniška zgodba:** Kot administrator želim vzdrževati katalog karakterjev in orožij, da lahko uporabniki in moderatorji izbirajo pravilne predmete.

**Pogoji sprejema:**

1. Administrator doda karakter ali orožje z imenom, igro, vrsto, redkostjo 4★ ali 5★ in portretom.
2. Administrator lahko popravi podatke obstoječega predmeta, sprememba pa je vidna v katalogu za izbiro pri vnosu in urejanju bannerjev.
3. Urejanje kataloga je dovoljeno samo administratorju; uporabnik in moderator nimata tega dostopa.
4. Predmeta, povezanega z zgodovino ali bannerjem, ni mogoče izbrisati, dokler te povezave obstajajo.

## US-14 – Izvoz podatkov

**Povezana funkcionalnost:** Izvoz podatkov  
**Uporabniška vloga:** Uporabnik

**Uporabniška zgodba:** Kot uporabnik želim izvoziti zgodovino in svojo zbirko, da imam lokalno kopijo podatkov.

**Pogoji sprejema:**

1. Uporabnik izbere zgodovino ali zbirko, igro oziroma vse igre ter format JSON ali CSV.
2. Izvoz zgodovine vsebuje igro, banner, predmet, redkost, datum in pity. Izvoz zbirke vsebuje lastne karakterje, število kopij ter shranjene podatke o zgradbi.
3. Pri prazni izbiri JSON vsebuje prazen seznam, CSV pa samo glavo stolpcev.

## US-15 – Urejanje bannerjev

**Povezana funkcionalnost:** Urejanje bannerjev  
**Uporabniška vloga:** Moderator

**Uporabniška zgodba:** Kot moderator želim dodajati in popravljati bannerje, da uporabniki vidijo pravilne termine in izpostavljene predmete.

**Pogoji sprejema:**

1. Moderator odpre obrazec za nov banner ali urejanje obstoječega; običajni uporabnik nima pravice shranjevanja bannerjev.
2. Obrazec zahteva igro, ime, vrsto, začetek in konec ter vsaj en izpostavljen predmet pri omejenih bannerjih; konec mora biti po začetku.
3. Izpostavljeni predmeti morajo pripadati izbrani igri in ustrezati vrsti bannerja; neveljavna kombinacija se zavrne.
4. Po shranjevanju se prikaže potrditev in banner s shranjenimi podatki; pri napaki se obstoječi banner ne spremeni.
5. Moderator ne more dodajati ali urejati kataloških predmetov in spreminjati uporabniških vlog.

