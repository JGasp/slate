# Navodila za uporabo

V datoteki `includes/_user_manual.md` se bo pisalo navodila za uporabo.

## Vzdrževanje uporabnikov

Vzdrževanje uporabnikov se izvaja preko strežnika KeyCloak. Na strežnik se prijavimo preko
[URL-ja](https://kanban.smrpo7:31337/auth/admin/master/console).

Prijavimo se z računom administratorja (ob namestitvi ga kreiramo na isti strani). Projekt uporablja področje `Kis`.

### Dodajanje novega uporabnika

Novega uporabnika dodamo tako, da v levem meniju izberemo `Manage > Users` in kliknemo na gumb `Add user`. Prikažejo se
vnosna polja, kamor vnesemo podatke uporabnika. Vnos potrdimo s klikom na gumb `Save`. Nastavljanje gesla in upravljanje
pravic je opisano v nadaljnjih poglavjih.

### Pregled uporabnikov

Seznam uporabnikov lahko pregledujemo tako, da v levem meniju izberemo `Manage > Users` in kliknemo gumb
`View all users`. Prikaže se seznam vseh uporabnikov. Podrobnosti uporabnika lahko urejamo s klikom na uporabnikov ID.

### Dodajanje ali spreminjanje gesla

Geslo uporabnika lahko urejamo tako, da v pregledu uporabnika izberemo zavihek `Credentials`. Novo geslo vpišemo v
vnosna polja. Če je stikalo `Temporary` vklopljeno, bo moral uporabnik ob prvi prijavi geslo spremeniti. Spremembe
shranimo s klikom na gumb `Reset password`.

### Upravljanje s pravicami uporabnika

Sistem uporablja vloge za upravljanje s pravicami. Pravice uporabnika lahko urejamo v zavihku `Role Mappings` ob
pregledovanju uporabnika. Tu lahko uporabniku dodelimo ali odstranjujemo vloge.

Za dodelitev vloge v oknu `Available Roles` izberemo vlogo, ki jo želimo dodati uporabniku, in kliknemo gumb
`Add selected`.

Za odstranitev vloge v oknu `Assigned Roles` izberemo vlogo, ki jo želimo odstraniti, in kliknemo na gumb
`Remove selected`.

Uporabniku lahko dodelimo naslednje vloge:

Vloga | Pomen
--- | ---
ADMINISTRATOR | Skrbnik sistema
DEVELOPER | Uporabnik, usposobljen za razvijalca
KANBAN_MASTER | Uporabnik, ki je usposobljen za vlogo Kanban Master
PRODUCT_OWNER | Uporabnik, ki je usposobljen za vlogo Product Owner-ja

### Onemogočanje uporabniškega računa

Uporabniški račun lahko omogočimo tako, da v pregledu uporabnika izberemo zavihek `Details`. Stikalo `User Enabled`
izklopimo in kliknemo na gumb `Save`. Na podoben način lahko uporabnika omogočimo nazaj.

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
