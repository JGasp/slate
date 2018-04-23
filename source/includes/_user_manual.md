# Navodila za uporabo

V datoteki `includes/_user_manual.md` se bo pisalo navodila za uporabo.

## Vzdrževanje uporabnikov

Vzdrževanje uporabnikov se izvaja preko administratorske [/admin](https://www.kanban.smrpo7/admin), ki je na voljo le uporabnikom v vlogi administratorja.

### Dodajanje novega uporabnika

Na administrativni strani `/admin` s klikom na gumb create administrator lahko ustvari novega uporabnika.

### Pregled uporabnikov

Administratorju je omogočeno pregledovanje in iskanje vseh uporabnikov. 
Išče lahko po ključni besedi z iskalnim poljem, hkrati lahko išče tudi po statusu aktivnosti z klikom na okno Deleted.

### Dodajanje ali spreminjanje gesla

Administrator lahko ponastavi geslo z klikom na gumb `Set password`, ki se nahaja v oknu s podrobnostmi uporabnika.

### Upravljanje s pravicami uporabnika

Administrator ob ustvarjanju ali ob urejanju uporabniškega profila lahko nastavlja vloge v katerih uporabnik nastopa.

Vloga | Pomen
--- | ---
ADMINISTRATOR | Skrbnik sistema
DEVELOPER | Uporabnik, usposobljen za razvijalca
KANBAN_MASTER | Uporabnik, ki je usposobljen za vlogo Kanban Master
PRODUCT_OWNER | Uporabnik, ki je usposobljen za vlogo Product Owner-ja

### Onemogočanje uporabniškega računa

Administrator lahko s klikom na gumb `Deactivate` na oknu z uporabniškimi podrobnostmi onemogoči uporabniški račun. 
Ponovno ga nato lahko aktivira s klikom na gumb `Activate`.

### Vpis uporabnikov v sistem

Uporabniki se lahko vpisujejo v sistem preko uporabniškega imena ali elektronske pošte. Če uporabnik napačno vnese geslo 3 krat zapored se račun začasno blokira za 10 sekund, kar se nato povečuje z dodatnimi poskusi vnosa napačnega gesla.

## Vzdrževanje projektov

Omogoča kreiranje, urejanje in brisanje projektov. Te funkcije so na voljo le uporabnikom z vlogo `Kanban Master`. 

### Kreiranje novega projekta

Do obrazca za kreiranje projektov pridemo tako, da v orodni vrstici izberemo `Projects` in nato kliknemo gumb `Create project`. 
V obrazec moramo vnesti ime projekta, naročnika, datum začetka in konca ter iz seznama izbrati razvojno ekipo. 
Pri izpolnjevanju moramo upoštevati naslednje omejitve:

- datum pričetka mora biti manjši ali enak trenutnemu
- datum zaključka mora biti večji od trenutnega datuma
- predvideni datum zaključka mora biti večji od datuma pričetka

Po končanem vnosu podatkov, kliknemo gumb `Submit`. Če so bili vsi podatki pravilno vnešeni in omejitve upoštevane, se projekt ustvari. V nasprotnem primeru se nam prikaže opozorilo, ki nam pove, katera polja so bila napačno vnešena.

### Urejanje projekta

Projekte lahko po kreiranju tudi urejamo. V orodni vrstici moramo izbrati `Projects` in nato klikniti na projekt, ki ga želimo urediti. Odprejo se nam podrobne informacije, pod katerimi se nahaja gumb `Edit`. Ob kliku na ta gumb se nam odpre obrazec za urejanje. Uredimo lahko enaka polja kot pri kreiranju, pri čemer moramo upoštevati zgoraj omenjene omejitve. V primeru, da smo na projektu že začeli z delom in smo mu že določili kartice, datuma začetka ne moramo več spreminjati.

### Brisanje projekta

Če želimo projekt izbrisati, moramo v orodni vrstici izbrati `Projects`, klikniti na projekt, ki ga želimo izbrisati in klikniti na gumb `Delete`. Pojavi se nam potrditveno okno, kjer ponovno kliknemo `Delete` in s tem izbrišemo projekt.

## Vzdrževanje in ustvarjanje novih razvojnih skupin

Omogoča kreiranje, urejanje in vpogled v razvojne skupine. Ustvarjanje in urejanje je omogočeno le uporabniku z vlogo `Kanban Master`. Do strani z pregledom nad razvojnimi skupinami [/dev-team] pridemo tako, da v orodoni vrstici kliknemo na gumb `Dev team`

### Kreiranje novege razvojne skupine

Do obrazca za kreiranje razvojne skupine pridemo tako, da kliknemo gumb `Create project`, ki se nahaja na strani [/dev-team]. V obrazec moramo vnesti ime razvojne skupine, naročnika, ter iz seznama izbrati razvijalce. Pri izpolnjevanju moramo upoštevati naslednje omejitve:

- `Kanban Master` je vedno uporabnik ki ustvarja razvojno skupino (Kasneje lahko v vlogo povabi drugega uporabnika).
- Povabiti mora enega ali več razvijalcev

Po končanem vnosu podatkov, kliknemo gumb `Submit`. Če so bili vsi podatki pravilno vnešeni in omejitve upoštevane, se razvojna skupina ustvari. V nasprotnem primeru se nam prikaže opozorilo, ki nam pove, katera polja so bila napačno vnešena.

### Urejanje razvojne skupine

Razvojne skupine lahko po kreiranju tudi urejamo. V orodni vrstici moramo izbrati `Dev team` in nato klikniti na razvojno skupino, katero želimo urejati. Odprejo se nam opis izbrane razvojne skupine. Na desni strani se nahajata gumba za urejanje razvojne skupine in povabitev novega kanban mastra.

### Urejanje imena in vlog v razvojni skupini

Z klikom na gumb `Edit development team` se nam odpre obrazec, v katerem lahko spremenimo ime skupine, product ownerja in dodajamo ali odstranjamo razvijalce. Razvojno skupino je mozno urejati le v okvirju kriterijev, ki so enaki kot ob ustvarjanju nove razvojne skupine. Treba je poskrbeti, da so vse vloge pravilno zastopane. Ob nepravilnem izboru, nas sistem opozori in ne dopusti dokončanja urejanja.
Urejanje končamo z klikom na gumb `SUBMIT`.

### Urejanje vloge `Kanban Master`

Z klikom na gumb `Invite new Kanban Master` lahko v razvojno skupino povabimo novega `Kanban Mastra`. Ob kliku se nam odpre seznam z možnimi uporabniki, ki so vsposobljeni prevzeti to vlogo. Ko z klikom na gumb `Select` svojo izbiro potrdimo, se izbranemu uporabniku poslje povabilo v razvojno skupino.


## Urejanje table

Omogoča kreiranje, urejanje in brisanje table. Te funkcije so na voljo le uporabnikom z vlogo `Kanban Master`.

### Ustvarjanje table

Z obiskom strani `/board` se prikažejo vse table do katerih uporabnik lahko dostopa. Če je uporabnik v vlogi `Kanban Master`, lahko ustvari novo tablo s klikom na gumb `Create`.
To ga bo preusmerilo na stran `/board-edit`, kjer se bo prikazal seznam z lokalno shranjenimi tabelami. Te tabele se še niso ustvarile v bazi in se hranijo lokalo izključno za urejanje. Ko imamo željeno obliko tabele, s klikom gumb `Create` ustvarimo tabelo.

### Urejanje table

Ustvarjeno tabelo naknadno lahko tudi spreminjamo. Z na strani `/board` klikom na tabelo obiščemo stran `/board/{id_tabele}`, ki vsebuje podrobnosti tabele in hkrati tudi gumb `Edit`, ki je dovoljen uporabniku v vlogi Kanban Mastra. Z klikom na gumb `Edit` obiščemo stran `/board/{id_tabele}/edit`, kjer lahko spreminjamo tabelo. Možno je dodajanje in odvzemanje obstoječih projektov. Dodajamo in spreminjamo lahko tudi stolpce, ki ne vsebujejo kartic.

### Prikaz tabele

Na strani `/board` so prikazane vse tabele dostopne vpisanemu uporabniku. Za bolj podroben pogled lahko uporabnik klikne na željeno tablo, kar ga preusmeri na stran `/board/{id_table}` z podrobnostmi tabela.

### Kopiranje tabele

Ustvarjene tabelo lahko na strani za urejanje `/board/{id_tabele}/edit` kopiramo z klikom na gumb `Copy`, kar bo ustvarilo in preusmerilo uporabnika na novo lokalno tabelo, ki je strukturno enaka.