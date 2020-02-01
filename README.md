# hello-world
testni repozitorij

A: Metodološki del
Izbira tehnologije
Linux, Debian 10+, Linux kernel: , PostgresSQL 9.5+, Python 3.8.1+
+ pomeni praviloma zadnja verzija oziroma najmanj toliko, kot je napisana.
Django dependecies so v datoteki: »requirements.txt«

Postavitev komunikacijskih kanalov med sodelujočimi moduli
Osnovni moduli so Uporabniški vmesnik (spletna aplikacija - UI), baza, poljubno število testerjev in če je potrebno še skripte za komunikacijo med bazo in testerji.
Poleg tega so še standardni moduli, npr. spletni in poštni strežnik, statične strani  za uporabniške priročnike, strežnik za dokumentacijo vzdrževalcev, ki je lahko tudi integriran na strani ali nekje zunaj

Izbira protokolov za podatkovni tok
Središče vseh podatkovnih tokov je v bazi. Vsi moduli neposredno komunicirajo z bazo. Na bazi so tudi triggerji (prožilci), ki prožijo naslednja dejanja. Komunikacija testerjev z bazo je izvedena glede na to, kaj tester zmore (direktna, preko skript, preko spletnih storitev).

Izbira okolja za delovanje aplikacije (vključno z dependenciji)
Uporabniški vmesnik (UI) ima dependecies v datoteki: »requirements.txt«. Ostali deli sistema imajo podobno datoteko in s skripto se kadarkoli preveri ustreznost okolja.

Razvojno okolje (individualno in skupinsko, hierarhija strežnikov)
Aplikacija teče v virtualnem okolju. Vsak sodelavec ima pri sebi razvojno okolje, ki ga posodablja iz odložišča. Skupno razvojno okolje je na naslovu:

Dokumentacija (način vodenja, pravila, orodje)
Funkcionalni opis in druga celovita informacija o aplikacijo naj bo zapisana na repozitoriju ali skupinskem orodju. Aplikacija vezana na posamezne module, naj bo skupaj s kodo.

Planiranje testiranja
Postopek testiranja je obvezni del dokumentacije in napisane programske kode. Vsak modul ima v dokumentaciji napisan okvirni postopek testiranja. Večina testiranja poteka preko skript. Kjer pa to ni možno, je podroben opis testiranja. Na podlagi zapaženih težav se dopolnjujejo postopki testiranja. Testiranje se izvaja pretežno s skriptami in pa v debug načinu. Postopki testiranja komunikacij so izvedeni na način, da se potrdi ali ovrže vsak korak na komunikacijski poti.

Sklapljanje modulov – uploadi in verzioniranje
Vsak modul ima svojo oznako in oznako verzije. Postopek je dokumentiran in vsak modul mora imeti podpis, ki ga je možno preveriti (na primer s skripto ali pa ukazom v debug načinu..

Pregled in potrjevanje dokumentacije
Dokumentacija ima naslednje vidike: funkcionalni opis (opis vsebine za celotno aplikacijo in okvirno razdelitev in grobi opis po modulih), arhitekturni opis (tehnološki opis po modulih, protokoli za pretok informacije), dokumentacije za namestitev in sistemsko vzdrževanje (vključno s skriptami za namestitev in nadzor delovanja, testiranjem ustreznosti dependencies). Dokumentacijo vodijo skrbniki posameznih delov aplikacije in jo pregledujejo pregledovalci. Dokumentacija je živa in se sproti dopolnjuje in se evidentirajo verzije in spremembe med verzijami.

Testiranje (postopek in priprava skript za testiranje)
Postopek testiranja je obvezni del pisanja programske kode. Vsak modul ima v dokumentaciji napisan okvirni postopek testiranja, ki je v programu implementiran in je sestavni del programske kode

Potrjevanje verzij
Vsak sodelavec na projektu skrbi za del programske kode (skrbnik). Pred oddajo v repozitorij, kodo pregleda drugi sodelavec (pregledovalec) in opozori na morebitne pomanjkljivosti, ki jih skrbnik odpravi in tako pregledano kodo naloži v repozitorij

Avtorske pravice
V času zasnove projekta, je projekt namenjen izključno kot neprofitna aplikacija, ki jo uporabljata Zavod za računalniško izobraževanje in Sinel, d.o.o. Vsi sodelavci materialne avtorske pravice predajo obema organizacijama, zadržijo pa moralne pravice in so navedeni kot sodelavci na projektu, razen če želijo biti neimenovani.
Če bi se iz aplikacije kdaj v prihodnosti razvila komercialna aplikacija, se o tem napravi pogodba o vrednotenju avtorskih prispevkov.

Osebni podatki
Aplikacijo se zasnuje tako, da v osnovi potrebuje le tiste podatke, ki so dejansko potrebni za vodenje dejavnosti in tako, da so zakriti osebni podatki osebam, ki podatkov ne potrebujejo in tako, da je s strani pooblaščenih oseb možen nadzor delovanja, administracija in vzdrževanje ob minimalnem razkrivanju podatkov oseb.

B: Vsebinski in operativni del
1.	Big picture / funkcionalni opis
2.	Podatkovni model
3.	Arhitekturni opis (s stičnimi točkami med moduli)
4.	Podrobni opis aplikacije po modulih (dokumentacija, vsebina, podatkovni tok, načrt testiranja)
5.	Podrobni opis sistemskega vzdrževanja (dokumentacija in skripte za instalacijo, čiščenje in monitoring)
6.	Implementacija v skladu z gornjimi točkami

