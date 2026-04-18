# SBN
# 1. Ciel aplikacie 
Webova aplikacia pre manazovanie kurzov a prihlasovanie sa na kurzy tanecnej skoly.
# 2. tech stack
- lovable (+lovable cloud: subapase)
- resend - email
- onesignal - push notifikacie
- github
- claude code
# 3. user roles
- student
- teacher
- admin
- superadmin
# 4. core features
- users si mozu vytvarat a manazovat svoje pouzivatelske ucty
- user si moze menit heslo
- student sa moze prihlasit/odhlasit na dostupne kurzy
- admin moze vytvarat tanecne kurzy ako objekt(template) s parametrami (nemoze mazat)
- kurzy maju level podla ktoreho su alebo nie su dostupne studentom
- admin moze planovat tanecne kurzy do rozvrhu
- admin moze kontrolovat dochadzku ziakov cez admin UI
- admin ma dostupne rozne typy prehladov a statistik
- teacher a admin vidia neverejnu cast profilu ziakov na zdielanie internych informacii
- pouzivatelia mozu dostavat email notifikacie
- pouzivatelia mozu dostavat push notifikacie
- automaticky trigerovane notifikacie (napriklad neotvoreny kurz, posunutie cakacky)
- pouzivatel si moze nastavit default jazyk - slovencina/anglictina
- kurzy maju svoje limity a je mozne sa prihlasit na cakacku podla poradia. Cakacka sa automaticky posuva v pripade odhlasenia prihlaseneho studenta
# 5. funkcne oblasti
## home page
- menu, ktore obsahuje ine sekcie
- pouzivatelsky profil
- notifikacne centrum (zvoncek)
- zoznam dostupnych kurzov na prihlasenie

## podsekcie dotupne iba pre admina ucitela - nesmie byt viditelne studentom
- prehlady (admin/teacher): rozne typy globalnych prehladov a statistik. Rozne podsekcie prehladov budu pristupne podla role
- kurzy (admin): vytvaranie a manazovanie kurzov objekt/template
- planovanie (admin): vkladanie kurzov do kalendara - pohlad podla dna/tyzdna/mesiac
- dochadzka (admin): prehlad prihlasenych ludi na kurzy v ten den s moznostou potvrdenia prichodu alebo vymeskania. Moznost manualne pridat studenta. Student je automaticky "Paying/platiaci" ale je mozne zmenit studenta na "help/vypomoc"
- studenti (admin/teacher): zoznam vsetkych registrovanych studentov. Po kliknuti na studenta sa zobrazi jeho verejny aj neverejny profil.

# 6. Detailna specifikacia klucovych funkcnych oblasti
## Vytvorenie profilu pouzivatela
polia
- prve meno /mandatory
- druhe meno / mandatory
- muz(leader) alebo zena(follower) /mandatory
- email /mandatory
- heslo /mandatory
- potvrdenie hesla /mandatory
- profilova fotka /optional

## Kurzy - manazovanie
Kurzy sluzia ako objekt alebo ako template aby mohol byt pouzity pri planovani harmonogramu kurzov
Parametre kurzu:
- Nazov /mandatory
- tanecny styl /mandatory
- level /optional, default empty
- sala (sala 1/ sala 2) /default empty
- instruktori (zoznam teachers + moznost pridat manualne ine meno) / default empty
- Partnerwork/styling / default empty
- Maximalna kapacita per pohlavie /default empty

## Kurzy - planovanie
Sluzi na planovanie kurzov do kalendara

## Prehlady a reporty
- pocet kurzov za casovy interval
- pocet ucastnikov za casovy interval
- pocet pouzivatelov v systeme
- rozlozenie ludi na kurzoch casovy interval (kolacovy graf) - podla typov kurzov
- ludia s vysmeskanou dochadzkou podla poctu zmeskanych hodin
- prehlad ziakov
- statistiky nastevnosti kurzov pre zvoleneho ziaka

# 6. NFR
- system musi byt co najviac bezpecny a GDPR compliant
- system musi byt navrhnuty, tak aby bol co najlepsi perfrormance
- system musi byt strukturovany a lahko skalovatelny

# 7. Dizajn a vizual
- dizajn musi byt responzivny - mobile first pre rolu ucitel a ziak. Web desktop first pre admin.
- dizajn musi byt moderny/cool - mladeznicky, sviezy ale zaroven prehladny




