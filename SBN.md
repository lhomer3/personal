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
- student sa moze prihlasit/odhlasit na dostupne kurzy
- admin moze vytvarat tanecne kurzy ako objekt(template) s parametrami
- kurzy maju level podla ktoreho su alebo nie su dostupne studentom
- admin moze planovat tanecne kurzy do rozvrhu
- admin moze kontrolovat dochadzku ziakov cez admin UI
- admin ma dostupne rozne typy prehladov a statistik
- teacher a admin vidia neverejnu cast profilu ziakov na zdielanie internych informacii
- pouzivatelia mozu dostavat email notifikacie
- pouzivatelia mozu dostavat push notifikacie
- pouzivatel si moze nastavit default jazyk - slovencina/anglictina
# 5. funkcne oblasti
## Student

## Admin
Admin sekcia obsahuje sekcie
- prehlady: rozne typy globalnych prehladov a statistik
- kurzy: vytvaranie a manazovanie kurzov objekt/template
- planovanie: vkladanie kurzov do kalendara - pohlad podla dna/tyzdna/mesiac
- dochadzka: prehlad prihlasenych ludi na kurzy v ten den s moznostou potvrdenia prichodu alebo vymeskania. Moznost manualne pridat studenta. Studen je automaticky "Paying/platiaci" ale je mozne zmenit studenta na "help/vypomoc"
- studenti: zoznam vsetkych registrovanych studentov. Po kliknuti na studenta sa zobrazi jeho verejny aj neverejny profil.



# NFR
dizajn musi byt responzivny - mobile first
system musi byt co najviac bezpecny a GDPR compliant
system musi byt navrhnuty, tak aby bol co najlepsi perfrormance
system musi byt strukturovany a lahko skalovatelny
# role
1. student:
prihlasovanie a odhasovanie na dostupne kurzy
editaciu svojho profilu - osobne a prihlasovacie udaje
2. ucitel:
prava ako student ale moze navyse
vstup do ucitelskej zony (zona prehladov)
vyhladavat studentov a zobrazovat si ich verejny profil
k studentovi do jeho neverejneho profilu pisat komentare a popisy a pridat fotku. Neverejny profil vidia len ucitelia a admini
mozu studentovi upravovat dostupne kurzy na zaklade jeho tanecneho levelu
v neverejnom profile vidia statistiky studenta: pocet nastivenych kurzov podla konkretneho kurzu. Rozne statsticke grafy ucasti.
3. admin:
moze vytvarat kurzy ktore sa budu studentom zobrazovat na dashboarde medzi dostupnymi kurzami na danny tyzden/mesiac
vytvarat sablonu pre kurzy, ktore sa daju kopirovat
moze odklikavat na vstup na kurzy. V danny den ma zobrazene kurzy s mennym zoznamom kurzistov a odklikne ci student prisiel alebo neprisiel
4. super admin:
zatial neurcene prava
# klucove casti systemu
planovanie kurzov: obsahuje datum a cas a dlzku, instruktorov, tanecny styl, level, salu, maximalny pocet ucastnikov, velkost cakacky
dostupne tanecnych kurzy: Styl, Level, Popis
statistika jednotlivca: kolko a akych hodin ma odchodenych, kolko hodin bol prihlaseny a neprisiel
globalne statistiky: pocty ludi na jednotlivych kurzoch
odklikavanie zucastnenych prihlasenych adminom na vstupe
moznost spristupnovat vyssi level kurzov jednotlivym studenom
mat neverejny profil pre studenta, ktori vidia len admini a ucitelia
kazdy pouzivatel prechadza standatnou sign up /sign in/ forgot password auth.
moznost exportovat vsetky emaily studentov podla roznych kriterii
monozst odosielania systemovych emailov - napriklad ked sa kurz otvori alebo neotvori





