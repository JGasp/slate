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
