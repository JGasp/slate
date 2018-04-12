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
