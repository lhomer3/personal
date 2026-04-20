# SBN
# 1. Ciel aplikacie 
Webova aplikacia pre manazovanie kurzov a prihlasovanie sa na kurzy tanecnej skoly.
# 2. tech stack
- lovable
- supabase
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
- user si moze menit heslo aj email
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
- kurz musi mat samostatnu URL alebo moznost poslat nan link
# 5. funkcne oblasti

## podsekcie dotupne iba pre admina ucitela - nesmie byt viditelne studentom
- prehlady (admin/teacher): rozne typy globalnych prehladov a statistik. Rozne podsekcie prehladov budu pristupne podla role
- kurzy (admin): vytvaranie a manazovanie kurzov objekt/template
- planovanie (admin): vkladanie kurzov do kalendara - pohlad podla dna/tyzdna/mesiac
- dochadzka (admin): prehlad prihlasenych ludi na kurzy v ten den s moznostou potvrdenia prichodu alebo vymeskania. Moznost manualne pridat studenta. Student je automaticky "default" ale je mozne zmenit studenta na "help/vypomoc"
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
Parametre kurzu - otvorena hodina:
- Nazov
- tanecny styl
- level
- typ: partnerwork, muzi, zeny, unisex neparove /mandatory
- Popis
- trvanie v minutach

## Kurzy - planovanie
- Sluzi na planovanie kurzov do kalendara. Admin si vyberie z prednastevenych kurzov a kurz naplanuje do casu
- Naplanovany kurz musi byt doplneny o
-- sala (sala 1/ sala 2) /default empty
-- instruktori (zoznam teachers + moznost pridat manualne ine meno)
-- Maximalna kapacita per pohlavie /default empty
- Popis a trvanie v minutach je editovatelne pre konkretnu naplanovanu hodinu

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

# 8. Funkcnosti do buducna
- moznost mesacneho kurzu, ktory obsahuje viacero hodin hodin ale da sa prihlasit len cely kurz





