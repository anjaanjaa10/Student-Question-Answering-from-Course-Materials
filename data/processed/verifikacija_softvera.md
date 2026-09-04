# Verifikacija softvera (elektronska verzija, 2026)


<!-- pdf_page=3 printed_page=3 -->

Verifikacija softvera

<!-- pdf_page=5 printed_page=5 -->

Verifikacija softvera
Milena Vujošević Janičić
Matematički fakultet Univerzitet u Beogradu Beograd, 2026.

<!-- pdf_page=6 printed_page=6 -->

Autor: dr Milena Vujošević Janičić, vanredni profesor na Matematičkom fakultetu u Beogradu
VERIFIKACĲA SOFTVERA Prvo izdanje, 2026.
Izdavač: Matematički fakultet Univerziteta u Beogradu, Studentski trg 16, 11000 Beograd Za izdavača: prof. dr Dragoljub Kečkić, dekan
Recenzenti: dr Mirko Spasić, docent na Matematičkom fakultetu u Beogradu dr Maja Vukasović, docent na Elektrotehničkom fakultetu u Beogradu Obrada teksta i ilustracĳe: autor Štampa: Skripta internacional, Beograd Tiraž: 30
CIP - Katalogizacija u publikaciji Narodna biblioteka Srbije, Beograd
004.415.5(075.8) VUJOXEVI Janiqi, Milena, 1980Verifikacĳa softvera / Milena Vujošević Janičić ;[ilustracĳe autor]. - 1. izd. - Beograd : Univerzitet u Beogradu, Matematički fakultet, 2026 (Beograd : Skripta internacional). 392 str. : ilustr. ; 24 cm
Tiraž 30. - Napomene i bibliografske reference uz tekst. - Bibliografija uz svako poglavlje. - Register.
ISBN 978-86-7589-210-6
1. Vujoxevi Janiqi, Milena, 1980- [autor][ilustrator] a) Softver { Testirae
COBISS.SR-ID 191794697
Copyright ©Milena Vujošević Janičić Ovo delo zaštićeno je licencom Creative Commons CC BY-NC-ND 4.0 (AttributionNonCommercial-NoDerivatives 4.0 International License). Detalji licence mogu se videti na veb-adresi http://creativecommons.org/licenses/by-nc-nd/4.0/. Dozvoljeno je umnožavanje, distribucĳa i javno saopštavanje dela, pod uslovom da se navedu imena autora. Upotreba dela u komercĳalne svrhe nĳe dozvoljena. Prerada, preoblikovanje i upotreba dela u sklopu nekog drugog nĳe dozvoljena.

<!-- pdf_page=7 printed_page=7 -->

Ružici i Mihajlu

<!-- pdf_page=9 printed_page=9 -->

Predgovor
Ova knjiga nastala je kao rezultat držanja predmeta Verifikacĳa softvera koji već više od osam godina predajem studentima master studĳa na Matematičkom fakultetu Univerziteta u Beogradu. Tokom tog perioda nastavni materĳali su se postepeno razvĳali, dopunjavali i unapređivali, prateći kako razvoj oblasti verifikacĳe softvera tako i iskustva stečena u radu sa generacĳama studenata. Upravo je iz tog kontinuiranog nastavnog i naučnog rada proistekla ova knjiga.
Knjiga obuhvata sve teme koje se obrađuju u okviru kursa. Svaka oblast ilustrovana je brojnim primerima koji bi trebalo da olakšaju razumevanje osnovnih koncepata i njihove praktične primene. Na širokim marginama uz tekst nalaze se kratke napomene sa zanimljivostima i aktuelnim informacĳama iz oblasti verifikacĳe softvera. Na kraju svake tematske celine dat je spisak pitanja koja mogu poslužiti za proveru savladanog znanja. Pitanja se često sastoje iz više delova, pa je potrebno odgovoriti na svaki od njih — od najopštĳeg, kojim se proverava razumevanje šireg konteksta i osnovnih ideja, do najspecifičnĳeg, koji zahteva detaljno poznavanje obrađenog gradiva.
Tokom rada na ovoj knjizi imala sam podršku i pomoć velikog broja kolega i studenata, kojima ovom prilikom želim da izrazim svoju iskrenu zahvalnost. Zahvalnost dugujem profesorima Viktoru Kunčaku, Dušanu Tošiću i Silvĳi Gilezan čĳi su rad i ideje uticali na moja interesovanja i istraživanja u oblasti verifikacĳe softvera. Zahvaljujem se Petru Jovanoviću, kolegi iz kompanĳe Syrmia (danas HTEC Group), koji mi je pružio priliku da steknem dragoceno industrĳsko iskustvo poverivši mi razvoj i vođenje projekta zasnovanog na statičkoj analizi softvera, sa ciljem automatizacĳe provere usklađenosti koda sa standardom AUTOSAR C++14. Zahvaljujem se i Katarini Šonjić Vujić i Filipu Vujiću koji su me uključili u organizacĳu konferencĳe Belgrade Test Conference, povezali sa zajednicom koja se bavi testiranjem softvera i time doprineli proširivanju mojih znanja. Zahvaljujem se kolegi Milanu Bankoviću na zanačajnom doprinosu u početnoj verzĳi materĳala za poglavlje Proveravanje modela.
Zahvalnost dugujem asistentima na kursu, Ani Vulović i Ivanu Ristoviću, koji su kroz pripremu vežbi i rad sa studentima doprineli kvalitetu nastave i razvoju kursa. Zahvalnost dugujem studentima master studĳa koji su tokom godina, kroz svoje seminarske radove, doprineli produbljivanju i proširivanju pojedinih tema iz ove oblasti. Njihova istraživanja, pitanja i zapažanja često su ukazivala na nove uglove posmatranja i podsticala me da pojedine delove gradiva dodatno

<!-- pdf_page=10 printed_page=10 -->

razjasnim i unapredim. Svi ti seminarski radovi dostupni su na stranici kursa (https://www.verifikacijasoftvera.matf.bg.ac.rs/) i predstavljaju vredan dopunski materĳal za studente koji žele da dalje istražuju teme iz knjige.
Zahvalnost dugujem i doktorandima koji su svoja doktorska istraživanja usmerili ka temama iz oblasti verifikacĳe softvera, a čĳi su rad i diskusĳe u velikoj meri uticali na oblikovanje pojedinih delova ove knjige: Mirku Spasiću, Milanu Čuguroviću i Strahinji Stanojeviću. Zahvaljujem se i studentima koji su svoje master radove posvetili oblastima obuhvaćenim ovom knjigom. Njihov rad i rezultati značajno su doprineli razvoju i produbljivanju pojedinih tema: Veronika Marinković, Aleksandar Stefanović, Milica Kleut, Jovana Bošković, Nikola Perić, Vladimir Vuksanović, Ana Petrović, Milica Galjak, Mirko Brkušanin, Ognjen Plavišić, Irena Blagojević, Nikola Dimić, Lazar Mladenović, Strahinja Stanojević, Ivan Ristović, Ðorđe Todorović, Marina Nikolić, Nikola Vidič, Ana Mitrović, Ana Ðorđević, Aleksandra Karadžić, Nikola Prica i Branislava Živković.
Tokom pripreme rukopisa mnogi studenti i kolege su pomogle u izradi i unapređivanju ilustracĳa i dĳagrama koji prate tekst, čime su doprineli jasnĳem i preglednĳem predstavljanju pojedinih koncepata. Zahvaljujem se Petru Ðekanoviću, Vukanu Antiću, Aleksandru Šarbajiću, Milici Gnjatović, Pavlu Cvejoviću, Bojanu Bardžiću, Neveni Mĳailović, Andrĳani Bosiljčić, Milici Kleut, Dunji Čitlučanin i Tamari Ðukić. Takođe sam zahvalna studentima koji su ukazali na greške, nejasnoće i propuste u tekstu. Njihove pažljive primedbe bile su od velike pomoći u unapređenju konačne verzĳe rukopisa. Zahvaljujem se studentima Lazaru Saviću, Staši Ðorđević, Marku Lazareviću, Anđeli Jovanović i Aleksandru Ivanoviću.
Zahvalnost dugujem recenzentima, Mirku Spasiću i Maji Vukasović, na pažljivom čitanju rukopisa, korisnim savetima i konstruktivnim sugestĳama koje su znatno doprinele poboljšanju njenog sadržaja i strukture.
Na kraju, posebno se zahvaljujem svom suprugu, Predragu Janičiću, koji je pažljivo čitao rukopis, davao dragocene komentare i sugestĳe i time značajno doprineo kvalitetu ove knjige.
Beograd, 2026.
Milena Vujošević Janičić

<!-- pdf_page=11 printed_page=11 -->

Sadržaj
Ispravnost i neispravnost softvera 1
1 Kvalitet softvera 3
1.1 Upravljanje kvalitetom softvera . . . . . . . . . . . . . . . . . . . . . 4
1.2 Standardi . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 4
1.3 Atributi kvaliteta softvera . . . . . . . . . . . . . . . . . . . . . . . . 5
1.3.1 Funkcionalna podobnost . . . . . . . . . . . . . . . . . . . . 6
1.3.2 Performantnost . . . . . . . . . . . . . . . . . . . . . . . . . 6
1.3.3 Kompatibilnost . . . . . . . . . . . . . . . . . . . . . . . . . 8
1.3.4 Pouzdanost . . . . . . . . . . . . . . . . . . . . . . . . . . . . 9
1.3.5 Upotrebljivost . . . . . . . . . . . . . . . . . . . . . . . . . . 10
1.3.6 Bezbednost . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12
1.3.7 Sigurnost . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13
1.3.8 Održivost . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15
1.3.9 Prenosivost . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
2 Greške u softveru 23
2.1 Primeri poznatih grešaka . . . . . . . . . . . . . . . . . . . . . . . . 24
2.1.1 Neprĳatnosti i materĳalni gubici . . . . . . . . . . . . . . . . 24
2.1.2 Fatalne posledice . . . . . . . . . . . . . . . . . . . . . . . . 28
2.2 Troškovi usled grešaka u softveru . . . . . . . . . . . . . . . . . . . 32
3 Verifikacĳa i validacĳa softvera 37
3.1 Odnos verifikacĳe i validacĳe softvera . . . . . . . . . . . . . . . . . 38
3.2 Tehnike verifikacĳe softvera . . . . . . . . . . . . . . . . . . . . . . 40
Dinamička verifikacija softvera 45
4 Testiranje 47
4.1 Testiranje i razvoj softvera . . . . . . . . . . . . . . . . . . . . . . . . 47
4.1.1 Cena greške u kontekstu vremena otkrivanja . . . . . . . . . 48
4.1.2 Uloga testera u razvoju softvera . . . . . . . . . . . . . . . . 50
4.1.3 Faze testiranja softvera . . . . . . . . . . . . . . . . . . . . . 52

<!-- pdf_page=12 printed_page=12 -->

4.2 Vrste i nivoi testiranja . . . . . . . . . . . . . . . . . . . . . . . . . . 62
4.2.1 Testiranje jedinica koda . . . . . . . . . . . . . . . . . . . . . 63
4.2.2 Komponentno i integraciono testiranje . . . . . . . . . . . . 65
4.2.3 Sistemsko testiranje . . . . . . . . . . . . . . . . . . . . . . . 68
4.3 Tehnike testiranja . . . . . . . . . . . . . . . . . . . . . . . . . . . . 86
4.3.1 Pokrivenost testiranjem . . . . . . . . . . . . . . . . . . . . . 87
4.3.2 Podela tehnika testiranja . . . . . . . . . . . . . . . . . . . . 88
4.3.3 Testiranje crne kutĳe . . . . . . . . . . . . . . . . . . . . . . 92
4.3.4 Testiranje bele kutĳe . . . . . . . . . . . . . . . . . . . . . . . 104
4.3.5 Metamorfno testiranje . . . . . . . . . . . . . . . . . . . . . . 117
4.4 Načini sprovođenja testiranja . . . . . . . . . . . . . . . . . . . . . . 120
4.4.1 Manuelno testiranje . . . . . . . . . . . . . . . . . . . . . . . 121
4.4.2 Automatsko izvršavanje test primera . . . . . . . . . . . . . 122
4.4.3 Automatsko generisanje test primera . . . . . . . . . . . . . 124
5 Debagovanje 129
5.1 Veza izvršivog koda i debagera . . . . . . . . . . . . . . . . . . . . . 130
5.1.1 Režim prevođenja za upotrebu . . . . . . . . . . . . . . . . . 131
5.1.2 Režim prevođenja za pronalaženje grešaka . . . . . . . . . . 132
5.1.3 Kombinovani režimi prevođenja . . . . . . . . . . . . . . . . 134
5.1.4 Anti-debagovanje . . . . . . . . . . . . . . . . . . . . . . . . 136
5.2 Vrste debagovanja . . . . . . . . . . . . . . . . . . . . . . . . . . . . 136
5.2.1 Interaktivno debagovanje . . . . . . . . . . . . . . . . . . . . 137
5.2.2 Udaljeno debagovanje . . . . . . . . . . . . . . . . . . . . . . 144
5.2.3 Debagovanje nakon prekida izvršavanja programa . . . . . 145
5.3 Primeri debagera . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 147
5.4 Otvoreni problemi . . . . . . . . . . . . . . . . . . . . . . . . . . . . 152
5.5 Štampanje umesto debagera . . . . . . . . . . . . . . . . . . . . . . 153
6 Profajliranje i dinamičko detektovanje grešaka 159
6.1 Instrumentacĳa . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 160
6.2 Profajleri . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 166
6.2.1 Upotreba profila . . . . . . . . . . . . . . . . . . . . . . . . . 167
6.2.2 Kvalitet profila . . . . . . . . . . . . . . . . . . . . . . . . . . 169
6.2.3 Profajliranje uzimanjem uzoraka . . . . . . . . . . . . . . . . 170
6.2.4 Instrumentaciono profajliranje . . . . . . . . . . . . . . . . . 174
6.3 Alati za dinamičku detekcĳu grešaka . . . . . . . . . . . . . . . . . 183
6.3.1 Sanitajzeri . . . . . . . . . . . . . . . . . . . . . . . . . . . . 183

<!-- pdf_page=13 printed_page=13 -->

6.3.2 Alati platforme Valgrind . . . . . . . . . . . . . . . . . . . . 188
Statička verifikacija softvera 193
7 Semantika programskih jezika 195
7.1 Neformalna semantika . . . . . . . . . . . . . . . . . . . . . . . . . 197
7.2 Osnovne vrste formalnih semantika . . . . . . . . . . . . . . . . . . 201
7.2.1 Rezonovanje o osobinama programa . . . . . . . . . . . . . 203
7.2.2 Osnovni elementi semantike . . . . . . . . . . . . . . . . . . 205
7.3 Operaciona semantika . . . . . . . . . . . . . . . . . . . . . . . . . . 212
7.3.1 Prirodna semantika . . . . . . . . . . . . . . . . . . . . . . . 212
7.3.2 Strukturna operaciona semantika . . . . . . . . . . . . . . . 217
7.4 Denotaciona semantika . . . . . . . . . . . . . . . . . . . . . . . . . 220
7.5 Aksiomatska semantika . . . . . . . . . . . . . . . . . . . . . . . . . 226
8 Pregledi koda 235
8.1 Ciljevi pregleda koda . . . . . . . . . . . . . . . . . . . . . . . . . . 236
8.2 Efekti i značaj pregleda koda . . . . . . . . . . . . . . . . . . . . . . 240
8.3 Preporuke za efikasan pregled koda . . . . . . . . . . . . . . . . . . 241
8.4 Formalni pregledi . . . . . . . . . . . . . . . . . . . . . . . . . . . . 245
8.5 Neformalni pregledi . . . . . . . . . . . . . . . . . . . . . . . . . . . 247
9 Simboličko izvršavanje 259
9.1 Simboličko stablo izvršavanja . . . . . . . . . . . . . . . . . . . . . . 260
9.2 Principi dizajna . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 266
9.3 Konkoličko izvršavanje . . . . . . . . . . . . . . . . . . . . . . . . . 268
9.3.1 Dinamičko simboličko izvršavanje . . . . . . . . . . . . . . . 268
9.3.2 Selektivno simboličko izvršavanje . . . . . . . . . . . . . . . 271
9.4 Strategĳe obilaska putanja . . . . . . . . . . . . . . . . . . . . . . . 273
9.4.1 Jednostavne strategĳe . . . . . . . . . . . . . . . . . . . . . . 274
9.4.2 Pseudoslučajne strategĳe . . . . . . . . . . . . . . . . . . . . 275
9.4.3 Strategĳe vođene pokrivenošću koda . . . . . . . . . . . . . 276
9.4.4 Strategĳe usmerene ka dostizanju ciljne tačke . . . . . . . . 279
9.4.5 Kombinovana strategĳa . . . . . . . . . . . . . . . . . . . . . 281
9.5 Izazovi simboličkog izvršavanja . . . . . . . . . . . . . . . . . . . . 281
9.5.1 Eksplozĳa broja stanja i putanja . . . . . . . . . . . . . . . . 283
9.5.2 Modelovanje memorĳe . . . . . . . . . . . . . . . . . . . . . 290
9.5.3 Rešavanje ograničenja . . . . . . . . . . . . . . . . . . . . . . 299

<!-- pdf_page=14 printed_page=14 -->

10 Proveravanje modela 305
10.1 Osnove i motivacĳa . . . . . . . . . . . . . . . . . . . . . . . . . . . 305
10.1.1 Osnovni pojmovi . . . . . . . . . . . . . . . . . . . . . . . . 306
10.1.2 Primene proveravanja modela . . . . . . . . . . . . . . . . . 310
10.2 Pravljenje modela . . . . . . . . . . . . . . . . . . . . . . . . . . . . 312
10.2.1 Modelovanje jednostavnih sistema . . . . . . . . . . . . . . 314
10.2.2 Modelovanje hardvera . . . . . . . . . . . . . . . . . . . . . 320
10.2.3 Modelovanje softvera . . . . . . . . . . . . . . . . . . . . . . 322
10.3 Formalna specifikacĳa . . . . . . . . . . . . . . . . . . . . . . . . . . 327
10.3.1 Klase svojstava . . . . . . . . . . . . . . . . . . . . . . . . . . 327
10.3.2 Temporalne logike . . . . . . . . . . . . . . . . . . . . . . . . 330
10.3.3 Linearna temporalna logika . . . . . . . . . . . . . . . . . . 332
10.3.4 Logike CTL∗i CTL . . . . . . . . . . . . . . . . . . . . . . . . 338
10.4 Algoritmi za proveravanje modela . . . . . . . . . . . . . . . . . . . 340
10.4.1 Obilazak grafa tranzicionog sistema . . . . . . . . . . . . . . 340
10.4.2 Provera LTL svojstva putem Bihĳevih automata . . . . . . . 342
10.5 Kontrola kombinatorne eksplozĳe u proveravanju modela . . . . . 346
10.5.1 Apstrakcĳa predikata . . . . . . . . . . . . . . . . . . . . . . 347
10.5.2 Simboličko proveravanje modela . . . . . . . . . . . . . . . . 351
10.5.3 Ograničeno proveravanje modela . . . . . . . . . . . . . . . 354
11 Apstraktna interpretacĳa 365
11.1 Konkretan i apstraktan domen . . . . . . . . . . . . . . . . . . . . . 366
11.2 Konkretno izvršavanje i apstraktna interpretacĳa . . . . . . . . . . 372
11.3 Formalne osnove apstraktne interpretacĳe . . . . . . . . . . . . . . 381
11.4 Praktične primene . . . . . . . . . . . . . . . . . . . . . . . . . . . . 389
Indeks pojmova 393

<!-- pdf_page=15 printed_page=15 -->

Ispravnost i neispravnost softvera

<!-- pdf_page=17 printed_page=17 -->

Pregled
1.1 Upravljanje kvalitetom softvera . . 4
-Koji procesi su važni za kvalitet softvera? -Koji su standardi kvaliteta softvera najbitnĳi i šta oni definišu?
1.2 Standardi . . . . . 4
1.3 Atributi kvaliteta softvera . . . . . . 5
-Kojim se atributima opisuje kvalitet softvera? -Koji atributi kvaliteta softvera su važni za bankarske aplikacĳe, koji za autonomnu vožnju, koji za kalkulator, koji za onlajn prodaju karata, a koji za sisteme za razmenu poruka?
Tokom poslednjih godina, IT industrĳa se brzo razvija i predstavlja jednu od najdinamičnĳih industrĳa u svetu. Softver se razvĳa za veoma raznovrsne uređaje i svrhe. Ove namene obuhvataju oblasti poput interneta stvari, virtuelne i proširene stvarnosti, igara i zabave, pametnih okruženja i zdravstvene zaštite. Takođe, softver ima ključnu ulogu u razvoju veštačke inteligencĳe, obradi velikih podataka, poslovnim, naučnim i vojnim primenama, kao i u savremenim komunikacionim tehnologĳama.
Razvoj softvera je složen proces koji obuhvata veliki broj različitih aktivnosti, od kojih se osnovne mogu grupisati u:
-analizu sistema i specifikacĳu zahteva, -projektovanje i implementacĳu softvera, -upravljanje kvalitetom softvera i -održavanje softvera.
Slika 1.1: Softver je svuda oko nas. Počevši od malih kućnih aparata, preko telefona, prevoznih sredstava, satelita, raketa, aparata u zdravstvu — gotovo da više ne postoji elektronski uređaj koji u sebi ne sadrži nekakav softver.
Sa sve većim obimom proizvodnje softvera, raste i potreba za efikasnĳim upravljanjem procesima njegove izrade. U procesu razvoja softvera, ključno je da se dostupni resursi optimalno iskoriste kako bi se na vreme zadovoljili korisnički zahtevi i obezbedio visok kvalitet softverskog proizvoda.

<!-- pdf_page=18 printed_page=4 -->

### 1.1 Upravljanje kvalitetom softvera
Upravljanje kvalitetom softvera (eng. quality management) obuhvata principe, metode i procese koji se koriste za obezbeđivanje i unapređivanje kvaliteta softvera. Cilj upravljanja kvalitetom je da se ispune zahtevi korisnika, optimizuju poslovni procesi i smanji broj defekata.
Visok kvalitet softvera predstavlja ključni faktor njegove uspešnosti, bilo da se koristi u komercĳalne svrhe na tržištu ili u okviru specifičnih, nekomercĳalnih okruženja. Standardi kvaliteta softvera definišu smernice i propise koji omogućavaju sistematski pristup upravljanju kvalitetom. Pored toga, za postizanje visokokvalitetnog softvera neophodna je automatizovana podrška i upotreba sofisticiranih alata.
Osnovni procesi koji su vezani za kvalitet softvera su:
-planiranje kvaliteta softvera, -obezbeđivanje (eng. assurance) kvaliteta softvera, -kontrolu (eng. control) kvaliteta softvera i -poboljšanje kvaliteta softvera.
Planiranje kvaliteta je neophodno kako bi se definisao pristup razvoju softvera koji omogućava postizanje željenog nivoa kvaliteta. Na primer, različiti nivoi kvaliteta očekuju se za softver aviona i za igricu na mobilnom telefonu. Obezbeđivanje kvaliteta podrazumeva uključivanje aspekata kvaliteta u svakodnevni razvoj, dok kontrola treba da obezbedi kvalitet krajnjeg proizvoda. Na kraju, poboljšanje kvaliteta podrazumeva kontinuirano praćenje i unapređivanje procesa razvoja kroz analizu povratnih informacĳa i primenu novih metodologĳa.
### 1.2 Standardi
Željeni kvalitet softvera definiše se softverskim zahtevima, ali može biti nametnut i različitim međunarodnim standardima. Serĳa standarda ISO/IEC 25000 sadrži

<!-- pdf_page=19 printed_page=1 -->

okvir za procenu kvaliteta softvera. Najvažnĳi standard u ovoj serĳi je ISO/IEC 25010. Ovaj standard definiše devet karakteristika kvaliteta softvera, koje se obično nazivaju atributima kvaliteta softvera. Standard ISO/IEC 25023 opisuje kako se ove karakteristike kvaliteta koriste za merenje ukupnog kvaliteta proizvoda.
Postoje i važni IEEE standardi. Na primer, standard IEEE 730 daje smernice za pokretanje, planiranje, kontrolu i izvršavanje procesa obezbeđenja kvaliteta softvera, dok standard IEEE 1012-2016 definiše procese verifikacĳe i validacĳe za razvoj softvera i hardvera.
### 1.3 Atributi kvaliteta softvera
Standard ISO 25010 definiše hĳerarhĳu devet atributa kvaliteta (slika 1.2): funkcionalna podobnost, performantnost, kompatibilnost, pouzdanost, upotrebljivost, bezbednost, sigurnost, održivost i prenosivost. Svaki atribut uključuje svoje podatribute. U zavisnosti od svrhe i ciljeva softvera, svaki atribut kvaliteta softvera može imati različit nivo važnosti.
funkcionalna podobnost
ATRIBUTI KVALITETA SOFTVERA
prenosivost
performantnost (efikasnost)
održivost
kompatibilnost
sigurnost
pouzdanost
upotrebljivost
bezbednost
funkcionalna ispravnost
naučljivost
modularnost
operativna ograničenost
prilagodljivost
vremensko ponašanje
poverljivost
funkcionalna potpunost
operabilnost
iskoristivost
zrelost
instalabilnost
identifikacĳa rizika
integritet
korišćenje resursa
koegzistencĳabilnost
zaštita od korisničkih grešaka
analizabilnost
funkcionalna prikladnost
dostupnost
zamenljivost
odgovornost
izmenljivost
otporanost na greške
bezbednost kvara
kapacitet
interoperabilnost
autentifikabilnost
estetika korisničkog interfejsa
testabilnost
upozorenje na opasnost
sposobnost oporavka
neporecivost
bezbednost integracĳe
pristupačnost
prepoznatljivost svrhe aplikacĳe
Slika 1.2: Atributi softvera u skladu sa kategorizacĳom standarda ISO/IEC 25010.

<!-- pdf_page=20 printed_page=6 -->

1.3.1 Funkcionalna podobnost
Funkcionalna podobnost (eng. functional suitability) odgovara stepenu u kojem softver ispunjava funkcionalne zahteve i obuhvata naredne podatribute:
funkcionalnu ispravnost — softver treba da daje tačne rezultate,
funkcionalnu potpunost — dostupnost funkcĳa koje su očekivane specifikacĳom i
funkcionalnu prikladnost — ispunjavanje očekivane funkcionalnosti.
funkcionalna podobnost
Primer 1.3.1 (Kalkulator) Razmotrimo primer jednostavnog kalkulatora.
Funkcionalna ispravnost podrazumeva da kalkulator uvek računa ispravne vrednosti. Na primer, kalkulator treba da ne greši u sabiranju dva broja.
funkcionalna ispravnost
Funkcionalna potpunost podrazumeva da kalkulator ima dostupne sve funkcionalnosti predviđene specifikacĳom. Na primer, željene funkcionalnosti mogu da budu sabiranje, oduzimanje, množenje i deljenje.
funkcionalna potpunost
funkcionalna prikladnost
Funkcionalna prikladnost podrazumeva da se kalkulator ponaša na očekivani način. Na primer, kalkulator ne treba da ima neočekivane dodatne opcĳe kao što su skidanje sadržaja sa interneta ili puštanje filmova.
1.3.2 Performantnost
Performantnost (efikasnost) (eng. performance) odgovara stepenu u kojem softver zadovoljava vremenske i resursne zahteve. Performantnost obuhvata naredne podatribute:
vremensko ponašanje — vreme odgovora i obrade (koliko vremena je potrebno da aplikacĳa da odgovor korisniku, odnosno da obradi neke netrivĳalne

<!-- pdf_page=21 printed_page=1 -->

zahteve), stopa protoka (koliko transakcĳa je aplikacĳa u mogućnosti da obradi u jedinici vremena),
korišćenje resursa — količina i vrsta korišćenih resursa i
kapacitet — maksimalna ograničenja (npr. broj korisnika ili veličine ulaza koje aplikacĳa može da obradi).
performantnost (efikasnost)
Primer 1.3.2 (Kupovina karata) Razmotrimo primer sistema za onlajn rezervacĳu i kupovinu avionskih karata. Ponašanje ovog sistema treba razmotriti u odnosu na svakog pojedinačnog korisnika sistema, ali i u kontekstu mogućeg velikog opterećenja sistema u situacĳama kada veliki broj korisnika istovremeno želi da rezerviše ili kupi kartu.
vremensko ponašanje
Vremensko ponašanje ovog sistema uključuje i:
korišćenje resursa
vreme odgovora (odziva) aplikacĳe pri pretraživanju dostupnih karata i
kapacitet
vreme obrade potrebno za rezervacĳu ili plaćanje karte.
Na primer, očekivanja koja se postavljaju visokoefikasnom sistemu su da:
pretraga karata treba da se izvrši za manje od dve sekunde u 97% slučajeva,
prikaz rezultata pretrage (lista dostupnih karata) mora da se učita u roku od tri sekunde za 95% zahteva,
plaćanje i potvrda rezervacĳe ne smeju trajati duže od pet sekundi u 99% slučajeva.
U ovakvom sistemu često je prisutna i komunikacĳa sa spoljnim sistemima (kao što su baze podataka ili eksterni API servisi za plaćanje), te u tom kontekstu može se postaviti uslov da kašnjenje odgovora eksternih sistema ne sme biti veće od jedne sekunde. Relevantni resursi čĳu upotrebu treba pratiti za ovu aplikacĳu su procesor, memorĳa, baza podataka i

<!-- pdf_page=22 printed_page=8 -->

mrežni resursi. Na primer, očekivanja koja mogu da se postave su:
opterećenje procesora ne sme preći 70% pri normalnom radu i ne sme preći 90% pri vršnom opterećenju duže od deset sekundi,
potrošnja RAM memorĳe ne sme preći 8 GB po instanci aplikacĳe tokom normalnog rada,
upotreba baze podataka mora da omogući obradu do 500 upita u sekundi bez značajnog usporavanja i
potrošnja mrežnih resursa ne sme premašiti 1 GB po sekundi na pojedinačnim serverima, pri čemu se ne sme desiti gubitak podataka.
Kapacitet aplikacĳe definiše koliko istovremenih korisnika aplikacĳa može da podrži pre nego što performanse padnu ispod prihvatljivog nivoa. Na primer, sistem mora da podrži najmanje 10.000 istovremenih korisnika bez degradacĳe performansi.
1.3.3 Kompatibilnost
kompatibilnost
Kompatibilnost (eng. compatibility) odgovara stepenu u kojem softver može da funkcioniše na različitim platformama ili da deli podatke sa drugim proizvodima, sistemima i komponentama. Kompatibilnost obuhvata naredne podatribute:
koegzistencĳabilnost — sposobnost deljenja okruženja i resursa sa drugim softverskim proizvodima i
koegzistencĳabilnost
interoperabilnost — sposobnost sarađivanja sa drugim aplikacĳama, korišćenjem ili deljenjem podataka.
interoperabilnost
Primer 1.3.3 (Razmena poruka) Razmotrimo primer aplikacĳe za razmenu poruka (na primer, aplikacĳu nalik na WhatsApp, Viber ili Slack). Ova aplikacĳa mora da funkcioniše zajedno sa drugim aplikacĳama na uređaju (koegzistencĳabilnost) i treba da može da

<!-- pdf_page=23 printed_page=1 -->

komunicira sa drugim servisima (interoperabilnost).
Na primer, korisnik na svom telefonu koristi aplikaciju za razmenu poruka dok istovremeno sluša muziku putem aplikacĳe Spotify ili gleda video preko aplikacĳe YouTube. Koegzistencĳabilnost podrazumeva da aplikacĳa ne sme ometati druge aplikacĳe. Na primer, ako korisnik primi poziv, muzika treba da se automatski pauzira, ali i da nastavi nakon završetka poziva. Notifikacĳe koje aplikacĳa pruža ne smeju blokirati druge aplikacĳe ili ometati korisničko iskustvo sa drugim aplikacĳama.
Interoperabilnost podrazumeva da aplikacĳa treba da, na primer, omogući korisnicima da šalju slike iz galerĳe telefona ili sa Google Drive-a. To znači da ima pristup lokalnoj memorĳi ili eksternim servisima.
1.3.4 Pouzdanost
pouzdanost
Pouzdanost (eng. reliablity) označava stepen u kojem je softver pouzdan. Pouzdanost obuhvata naredne podatribute:
zrelost — stabilnost tokom svakodnevne upotrebe, dostupnost — mogućnost neprekidnog rada, tolerancĳu na greške — sposobnost funkcionisanja čak i u prisustvu određenih hardverskih i softverskih kvarova i
zrelost
dostupnost
otporanost na greške
sposobnost oporavka (povratljivost) — sposobnost vraćanja podataka i procesa u slučaju kvara sistema.
sposobnost oporavka
Primer 1.3.4 (Hitne službe) Razmotrimo primer sistema za hitne službe (kao što su pozivi policĳi ili prvoj pomoći). Za ovakve sisteme kritično je da zadovolje sve kriterĳume pouzdanosti. Pre svega, sistem mora biti dobro proveren i stabilan, a svaka nova funkcionalnost mora biti temeljno testirana i verifikovana pre uvođenja — zrelost.

<!-- pdf_page=24 printed_page=10 -->

Sistem mora biti neprekidno dostupan, što znači da nikada ne sme biti van funkcĳe — dostupnost sistema. To podrazumeva mogućnost simultanog prĳema velikog broja poziva, kao i postojanje dodatne infrastrukture u slučaju pada primarnog sistema ili njegovih delova.
Ukoliko na nekoj serverskoj lokacĳi dođe do prekida napajanja, sistem mora nastaviti sa radom bez vidljivih problema. Posao tog servera treba automatski da bude preusmeren na drugi dostupni server, čime se osigurava kontinuitet rada i sprečava gubitak podataka — tolerancĳa na greške.
Takođe, bitno je da sistem u slučaju softverskog pada može automatski da se oporavi i nastavi sa radom — sposobnost oporavka.
1.3.5 Upotrebljivost
Upotrebljivost (eng. usability) odgovara stepenu u kojem korisnici mogu koristiti softver. Upotrebljivost obuhvata naredne podatribute:
naučljivost — koliko je jednostavno naučiti kako se softver koristi,
operabilnost — koliko je lako raditi sa softverom i kontrolisati ga,
zaštitu od korisničkih grešaka — mere u okviru samog softvera koje sprečavaju pravljenje grešaka u korišćenju,
estetiku korisničkog interfejsa — vizuelnu prĳatnost i prihvatljivost dizajna,
pristupačnost — mogućnost da osobe sa različitim stepenima sposobnosti mogu da koriste softver i
prepoznatljivost svrhe aplikacĳe — jasnoću namene softvera korisnicima.
Primer 1.3.5 (Bankarska aplikacĳa) Razmotrimo pri-

<!-- pdf_page=25 printed_page=1 -->

mer bankarske aplikacĳe. Ova aplikacĳa mora biti intuitivna, jednostavna za korišćenje, sigurna i pristupačna svim korisnicima, uključujući i osobe sa posebnim potrebama. Na primer:
upotrebljivost
Naučljivost. Prilikom prvog korišćenja, korisnik bi trebalo da može samostalno da pronađe i izvrši osnovne radnje (poput slanja novca i provere stanja) za manje od 5 minuta, bez potrebe za tutorĳalom.
naučljivost
operabilnost
Operabilnost. Ključne funkcionalnosti (poput provere stanja ili prenosa sredstava između računa) treba da budu dostupne u manje od četiri klika, omogućavajući brz i lak rad sa aplikacĳom.
zaštita od korisničkih grešaka
estetika korisničkog interfejsa
Zaštita od korisničkih grešaka. Ako korisnik unese neispravan broj računa prilikom slanja novca, aplikacĳa mora automatski izvršiti validacĳu i upozoriti korisnika na grešku pre potvrde transakcĳe.
pristupačnost
prepoznatljivost svrhe aplikacĳe
Estetika korisničkog interfejsa. Aplikacĳa treba da ima profesionalan i vizuelno prĳatan dizajn. Dizajn bi trebalo da bude minimalistički, moderan i intuitivan, sa jasnim kontrastom između elemenata. Treba koristiti harmonične boje i lako čitljive fontove, dok dugmad i ikonice moraju biti vizuelno jasne i prepoznatljive.
Pristupačnost. Aplikacĳa mora biti pristupačna osobama sa različitim potrebama, uključujući korisnike sa oštećenjem vida. To znači da treba da bude kompatibilna sa alatima za čitanje ekrana, da fontovi mogu biti uvećani po potrebi i da kontrast boja omogućava čitanje osobama sa daltonizmom.
Prepoznatljivost svrhe aplikacĳe. Korisnik odmah treba da razume da je aplikacĳa namenjena bankarskim uslugama. Početni ekran treba da sadrži jasno prepoznatljive elemente, poput salda računa i dugmeta za transfer novca. Ikonice i nazivi funkcionalnosti treba da budu intuitivni i nedvosmisleni (npr. „Plaćanje“, „Kartice“, „Računi“), a brend-boje i logo banke istaknuti.

<!-- pdf_page=26 printed_page=12 -->

1.3.6 Bezbednost
Bezbednost (eng. safety) odgovara stepenu u kojem proizvod, pod definisanim uslovima, izbegava stanje u kojem su ugroženi ljudski život, zdravlje, imovina ili životna sredina. Bezbednost obuhvata naredne podatribute:
Bezbednost i sigurnost se u srpskom jeziku mogu koristiti kao sinonimi. Zbog toga je bitno napomenuti da se u kontekstu atributa kvaliteta softvera bezbednost odnosi na fizičku bezbednost/sigurnost, dok se sigurnost koristi u kontekstu informacione bezbednosti/sigurnosti.
operativnu ograničenost — stepen do kojeg proizvod ili sistem ograničava svoje funkcionisanje unutar bezbednih parametara ili stanja prilikom susreta sa operativnim opasnostima,
identifikacĳa rizika — stepen do kojeg proizvod može da identifikuje tok događaja ili operacĳa koji mogu izložiti život, imovinu ili životnu sredinu neprihvatljivom riziku,
bezbednost kvara — stepen do kojeg proizvod može automatski da se postavi u bezbedan režim rada ili da se vrati u bezbedno stanje u slučaju kvara,
bezbednost (eng. safety) = fizička bezbednost
upozorenje na opasnost — stepen do kojeg proizvod ili sistem pruža upozorenja o neprihvatljivim rizicima u operacĳama ili internim kontrolama, kako bi se omogućila pravovremena reakcĳa i održavanje bezbednog rada i
sigurnost (eng. security) = informaciona bezbednost
bezbednost integracĳe — stepen do kojeg proizvod može da održi bezbednost tokom i nakon integracĳe sa jednom ili više komponenti.
Standardi kodiranja u automobilskoj industrĳi se fokusiraju na kvalitet softvera. Primeri implementacĳe delova ovih standarda mogu se videti u master radovima Mirka Brkušanina: Implementacĳa pravila iz standarda AUTOSAR C++14 u okviru programskog prevodioca Clang i Ognjena Plavšića: Alat za statičku analizu i predlaganje izmena u C++ kodu
Primer 1.3.6 (Autonomna vožnja) U sistemu za autonomnu vožnju svi atributi sigurnosti su izuzetno važni.
Operativna ograničenost — Automobil mora ograničiti svoje manevre (npr. brzinu, skretanje) u skladu sa bezbednim parametrima, posebno pri lošim vremenskim uslovima ili oštećenjima na putu.
Identifikacĳa rizika — Sistem treba da ume da prepozna potencĳalne opasnosti kao što su pešaci koji iznenada prelaze ulicu, druga vozila koja se kreću

<!-- pdf_page=27 printed_page=1 -->

nepredvidivo ili prepreke na putu.
Bezbednost kvara — U slučaju otkaza senzora ili računarskog sistema, automobil mora automatski da se zaustavi na bezbedan način ili da preuzme minimalno funkcionalno stanje koje ne ugrožava putnike ili druge učesnike u saobraćaju.
bezbednost
operativna ograničenost
Upozorenje na opasnost — Ako se pojavi situacĳa koju sistem ne može da reši sam, mora brzo upozoriti vozača ili centralni nadzorni sistem na opasnost.
identifikacĳa rizika
bezbednost kvara
Bezbednost integracĳe — Kada se novi moduli (npr. dodatni senzori ili softverske nadogradnje) integrišu u postojeći sistem, ceo sistem mora i dalje održavati visok nivo bezbednosti i ne sme uvoditi nove rizike.
upozorenje na opasnost
bezbednost integracĳe
1.3.7 Sigurnost
Sigurnost (eng. security) odgovara stepenu u kojem softver štiti informacĳe i podatke. Sigurnost obuhvata naredne podatribute:
poverljivost — dostupnost podataka samo ovlašćenim korisnicima,
integritet — sprečavanje neovlašćenog pristupa i modifikacĳe podataka,
odgovornost — mogućnost praćenja radnji korisnika, autentifikabilnost — mogućnost dokazivanja identiteta korisnika i
neporecivost — nemogućnost osporavanja, tj. mogućnost prikupljanja informacĳa o određenim aktivnostima i događajima.
Primer 1.3.7 (Bankarska aplikacĳa — nastavak primera 1.3.5) Bankarske aplikacĳe moraju biti maksimalno sigurne, jer rukovode osetljivim finansĳskim podacima korisnika i omogućavaju transakcĳe koje ne smeju biti zloupotrebljene. Bankarska aplikacĳa je odličan primer aplikacĳe kod koje je kritična sigurnost jer je

<!-- pdf_page=28 printed_page=14 -->

potrebno:
-Održavati poverljivost — podaci korisnika
moraju biti maksimalno zaštićeni. Na primer, ukoliko korisnik može da pristupi svojoj mobilnoj banci i pregleda stanje na računu — niko drugi ne sme videti ove informacĳe. To uključuje da pristup aplikacĳi mora biti zaštićen lozinkom, PIN-om ili biometrĳom (otisak prsta, prepoznavanje lica), podaci moraju biti šifrovani tokom prenosa i skladištenja, a sama aplikacĳa ne sme dozvoliti snimanje ekrana kako bi se sprečilo curenje podataka.
sigurnost
poverljivost
integritet
odgovornost
-Garantovati integritet — transakcĳe ne smeju biti neovlašćeno menjane. Na primer, ukoliko korisnik izvrši uplatu putem aplikacĳe, transakcĳa mora biti tačna i niko ne sme neovlašćeno izmeniti iznos uplate. Banka mora da šifruje podatke tokom prenosa, svaka transakcĳa mora da ima digitalni potpis koji potvrđuje da nĳe menjana, a sistem mora da može da detektuje bilo kakve neovlašćene izmene podataka i da ih pritom odmah blokira.
autentifikabilnost
neporecivost
-Obezbediti odgovornost — sve aktivnosti se beleže i mogu se proveriti. Na primer, ukoliko se korisnik žali da neko neovlašćeno koristi njegov račun – banka mora biti u stanju da proveri ko je koristio aplikacĳu i kada.
-Osigurati autentifikabilnost — samo pravi korisnik može pristupiti svom računu. Banka mora biti sigurna da se korisnik koji pokušava da se prĳavi u aplikacĳu zaista identifikuje kao pravi vlasnik računa. Ovo se može ostvariti korišćenjem višefaktorske autentifikacĳe koja uključuje na primer lozinku, biometrĳu i jednokratne kodove. Dodatno, prĳava preko novog uređaja treba da zahteva dodatnu verifikacĳu putem elektronske pošte ili telefonskog poziva.
-Omogućiti neporecivost — korisnik ne može

<!-- pdf_page=29 printed_page=1 -->

kasnĳe tvrditi da nĳe izvršio transakcĳu. To se može ostvariti digitalnim potpisivanjem kriptografskim ključevima. Pri tome, logovi moraju biti nepromenljivi, tako da niko, pa ni administratori, ne mogu izbrisati ili izmeniti istorĳu transakcĳa.
1.3.8 Održivost
Održivost (eng. maintainability) odgovara lakoći integrisanja promena. Promene uključuju dodavanje novih funkcionalnosti, ispravljanje grešaka, poboljšanje performansi, kao i prilagođavanje promenjenim zahtevima korisnika ili izmenjenom okruženju. Izmene zahtevaju:
1. razumevanje softvera;
2. pronalaženje delova softvera koje treba izmeniti; 3. izvođenje željenih izmena; 4. proveru da izmenama nisu poremećene postojeće funkcionalnosti.
Održivost se odnosi na lakoću svih ovih koraka. Smatra se jednim od ključnih atributa kvaliteta.
Održivost je statička karakteristika softvera koja ne utiče direktno na performanse i karakteristike softvera koje su vidljive krajnjem korisniku. Iako ne utiče direktno na ponašanje sistema u radu, ima značajan uticaj na dugoročni kvalitet i održavanje softvera. Primeri metrika softvera koje su važne u kontekstu održivosti su:
veličina (eng. size) — broj linĳa koda, spregnutost (eng. coupling) — kvantitativna mera međuzavisnosti između različitih modula,
kohezĳa (eng. cohesion) — kvantitativna mera povezanosti funkcĳa ili objekata unutar istog modula,
ciklomatska složenost (eng. cyclomatic complexity) — kvantitativna mera broja linearno nezavisnih putanja kontrole toka programa. Izračunava se po formuli: 𝐶= 𝐸−𝑁+ 2𝑃, gde je:

<!-- pdf_page=30 printed_page=16 -->

-𝐸broj grana (eng. edges) u grafu kontrole toka programa,
-𝑁broj čvorova (eng. nodes), -𝑃broj povezanih komponenti.
Mala veličina, niska spregnutost, visoka kohezĳa i niska ciklomatska složenost su karakteristike održivog softvera. Kako se dizajn softvera i njegov ukupni kvalitet vremenom pogoršavaju, neophodno je primenjivati različite tehnike za očuvanje održivosti. Refaktorisanje softvera predstavlja proces poboljšanja dizajna postojećeg koda i ključni je deo održavanja tokom evolucĳe softvera. Održivost uključuje naredne podatribute: modularnost, iskoristivost, analizabilnost, izmenljivost i testabilnost.
održivost
Modularnost se odnosi na stepen u kome je softver logički podeljen na nezavisne i međusobno zamenljive module. Razbĳanje softvera na module (jedinice, komponente) omogućava skrivanje njegove ukupne složenosti kroz apstrakcĳu i definisanje interfejsa. Modularnost se obično postavlja kao jedan od ključnih ciljeva u fazi dizajna softvera.
modularnost
iskoristivost
Idealan modul treba da bude:
analizabilnost
-relativno male dimenzĳe, -niske ciklomatske složenosti, -visoke kohezĳe, -minimalno spregnut sa ostalim modulima.
izmenljivost
testabilnost
Ovakvi moduli se onda mogu nezavisno odvajati i fleksibilno kombinovati na različite načine. Modularnost podrazumeva i standardizovane interfejse između modula, što je posebno naglašeno u savremenim softverskim arhitekturama poput mikroservisa.
Iskoristivost (ponovna upotrebljivost) predstavlja stepen u kome se komponente jednog sistema mogu koristiti u drugim sistemima. Postoje različiti nivoi iskoristivosti, uključujući ponovnu upotrebu:
-specifikacĳa,

<!-- pdf_page=31 printed_page=1 -->

-dizajna, -koda, -podataka i -testova.
Umesto razvoja novih funkcionalnosti uvek treba razmotriti iskoristivost postojećih komponenti. Glavne prednosti ponovne upotrebe uključuju:
-povećanje produktivnosti, -smanjenje troškova, -poboljšanje kvaliteta, -ubrzanje razvoja i -smanjenje rizika u procesu razvoja.
Analizabilnost označava lakoću analize i razumevanja softvera, te direktno utiče na prva dva koraka unošenja izmena: (1) razumevanje softvera i (2) pronalaženje delova softvera koje je potrebno izmeniti. Direktno je povezana sa modularnošću (dobra modularnost smanjuje kompleksnost i time poboljšava analizabilnost) i iskoristivošću (korišćenje postojećih komponenti olakšava analizu koda). Analizabilnost se poboljšava i kroz postojanje dobre dokumentacĳe i kroz dosledno poštovanje kodnih standarda. Za razumevanje neispravnog ponašanja softvera, postojanje mehanizma za praćenje rada sistema i aktivnosti korisnika može značajno da poboljša analizabilnost.
Izmenljivost predstavlja lakoću implementacĳe izmena bez uvođenja grešaka. Ključni pokazatelj izmenljivosti je spregnutost, jer visoka spregnutost povlači potrebu za izmenama u različitim delovima koda što dodatno povećava i verovatnoću uvođenja grešaka. Dobra modularnost utiče pozitivno na izmenljivost jer podrazumeva smanjenje kompleksnosti i ograničava uticaj izmena na lokalne delove koda.
Testabilnost označava lakoću provere da li su izmene narušile postojeće funkcionalnosti. Prednosti visoke

<!-- pdf_page=32 printed_page=18 -->

testabilnosti uključuju bržu isporuku korisnicima i češću povratnu informacĳu o ispravnosti softvera programerima. Praktični izazovi uključuju balans između potpunosti testova i vremena njihovog izvršavanja. Za testabilnost je ključna automatizacĳa procesa testiranja, mogućnost automatskog generisanja testova kao i dostupnost test slučajeva sa unapred poznatim rezultatom izvršavanja.
Primer 1.3.8 (Razmena poruka - nastavak primera 1.3.3) Aplikacĳa za razmenu poruka mora da bude laka za održavanje jer je karakteriše često dodavanje novih funkcionalnosti u skladu sa potrebama i zahtevima korisnika.
Aplikacĳa za razmenu poruka treba da ima različite funkcionalnosti, kao što su sistem za slanje poruka, sistem za obaveštenja, korisničke postavke, lično/grupno slanje poruka i sistem za autentifikacĳu. Implementacĳa koju karakteriše lako održavanje je modularna, odnosno podeljena u različite module koje odgovaraju prethodno navedenim funkcionalnostima. Svaki od ovih modula mora da bude nezavisan, ali poveziv sa ostatkom sistema putem jasno definisanih interfejsa za komunikacĳu. Na primer, sistem za autentifikacĳu mora biti odvojen od sistema za poruke i pozive, kako bi se omogućilo lakše upravljanje bez uticaja na ostatak aplikacĳe.
Poželjno je da se aplikacĳa može koristiti na različitim platformama, na primer, na mobilnim telefonima (Android, iOS) i desktop računarima (Linux, Windows). Da bi se to ostvarilo, ključna je iskoristivost odnosno da postoji mogućnost ponovne upotrebe koda. Sve komponente i funkcionalnosti, koje nisu specifične za platformu, potrebno je dizajnirati tako da ih je moguće koristiti na različitim platformama. Na primer, sistem za prĳavu treba da bude identičan na svim platformama, omogućavajući korisnicima da se prĳave koristeći

<!-- pdf_page=33 printed_page=1 -->

isti način verifikacĳe na svakom uređaju.
Analizabilnost aplikacĳe omogućava brzo praćenje i analiziranje problema (na primer, ukoliko korisnici prĳave da se neke poruke nisu stigle ili da su stigle dva puta). Da bi se to ostvarilo, aplikacĳa treba da omogući praćenje aktivnosti korisnika i sistema (logovi grešaka, statistika korišćenja, praćenje mrežnih veza).
Usled potrebe za čestim promenama u skladu sa željama korisnika, aplikacĳa treba da je lako izmenljiva i testabilna. Posebno važna vrsta izmene je nadogradnja. Aplikacĳa treba da bude dizajnirana tako da omogući da se lako i brzo mogu dodati nove funkcionalnosti, bez uticaja na postojeće. Na primer, dodavanje video poziva mora biti odvojeno od sistema za razmenu poruka, ali se mora integrisati u postojeći korisnički interfejs. Testabilnost u kontekstu čestih promena i nadogradnja ključna je za osiguravanje da promene i novouvedene funkcionalnosti ne narušavaju postojeće funkcionalnosti. Za testabilnost je posebno značajna automatizacĳa procesa testiranja, na primer kroz pisanje jediničnih testova i upotrebu alata za pokretanje i automatsku proveru rezultata rada testova. Testiranjem je potrebno pokriti različite scenarĳe (na primer, sve vrste poruka: tekstualne, glasovne i multimedĳalne) uključujući i scenarĳe koji obuhvataju pogrešno korišćenje aplikacĳe ili nestandardne slučajeve upotrebe (na primer, korišćenje aplikacĳe u slučaju problema sa mrežom).
Atributi kvaliteta softvera nisu nezavisni, već su međusobno povezani i isprepleteni. Na primer (slika 1.3), modularnost, koja se obično postavlja kao jedan od glavnih ciljeva faze projektovanja softvera, direktno utiče na sva ostala četiri atributa održivosti, jer je dobra modularnost preduslov za iskoristivost, analizabilnost, izmenljivost i testabilnost. Slično tome, analizabilnost utiče na iskoristivost i modifikacĳu, dok testabilnost indirektno utiče na iskoristivost i izmenljivost.

<!-- pdf_page=34 printed_page=20 -->

modularnost
testabilnost
iskoristivost
izmenljivost
Slika 1.3: Veze između atributa koji utiču na održavanje softvera: strelice sa punim linĳama predstavljaju jak uticaj jednog atributa na drugi, dok isprekidane strelice odgovaraju indirektnom uticaju.
analizabilnost
1.3.9 Prenosivost
prenosivost
Prenosivost (eng. portability) odgovara stepenu u kome se softver može koristiti u različitim okruženjima. Prenosivost obuhvata naredne podatribute:
prilagodljivost — mogućnost korišćenja sa različitim hardverom, softverom ili okruženjem,
instalabilnost — mogućnost instaliranja/deinstaliranja softvera u različitim okruženjima i
prilagodljivost
zamenljivost — mogućnost zamene drugim softverskim proizvodom za iste svrhe.
instalabilnost
zamenljivost
Primer 1.3.9 (Kupovina karata — nastavak primera 1.3.2) Aplikacĳa za kupovinu avio karata treba da bude prilagodljiva različitim uređajima (mobilnim uređajima, tabletima, desktop računarima) i tržištima. Na primer, aplikacĳa treba da može da se prilagodi različitim veličinama ekrana, od malih ekrana na mobilnim telefonima do velikih ekrana na desktop računarima, pri čemu je potrebno da se automatski prilagođava vizuelni prikaz u skladu sa veličinom ekrana. Takođe, aplikacĳa treba da ponudi lokalizovane opcĳe za različite jezike i valute.

<!-- pdf_page=35 printed_page=1 -->

Aplikacĳa treba da bude jednostavna za instalacĳu na različitim uređajima. Na mobilnim uređajima, korisnici treba da mogu da preuzmu aplikacĳu sa App Store-a ili Google Play-a uz nekoliko klikova ili komandi. Za desktop verzĳu, aplikacĳa treba da bude dostupna za platforme Windows, Linux i macOS u vidu jednostavnih instalacĳa koje se pokreću sa par klikova. Za veb verzĳe, aplikacĳa mora da omogući jednostavno korišćenje u pretraživaču bez potrebe za preuzimanjem ili instalacĳom.
Prilikom ažuriranja aplikacĳe, potrebno je omogućiti laku zamenljivost starĳe verzĳe novom verzĳom. Zamenljivost znači da aplikacĳa omogućava da nova verzĳa može zameniti staru verzĳu bez gubitka podataka, kao što su starĳa putovanja, preferencĳe korisnika ili istorĳa pretrage. Takođe, zamenljivost podrazumeva lako uklanjanje prethodne verzĳe aplikacĳe prilikom instalacĳe nove. U slučaju da korisnik želi da pređe na konkurentsku aplikacĳu, zamenljivost podrazumeva da će podaci kao što su rezervacĳe ili istorĳa pretrage biti prenosivi ili lako eksportovani u druge formate.
Rezime
-Cilj upravljanja kvalitetom je da se ispune zahtevi korisnika, optimizuju poslovni procesi i smanji broj grešaka ili defekata.
-Osnovni procesi koji su vezani za kvalitet softvera uključuju planiranje, obezbeđivanje, kontrolu i poboljšanje kvaliteta softvera.
-Serĳa standarda ISO/IEC 25000 sadrži okvir za procenu kvaliteta softvera.
-U zavisnosti od svrhe i ciljeva softvera, svaki atribut kvaliteta softvera može imati različit nivo važnosti.
-Osnovni atributi kvaliteta softvera su funkcionalna podobnost, performantnost, kompatibilnost,

<!-- pdf_page=36 printed_page=22 -->

pouzdanost, upotrebljivost, bezbednost, sigurnost, održivost i prenosivost.
Literatura
[1] ISO/IEC. Systems and Software Engineering: Systems and Software Quality Requirements and Evaluation (SQuaRE) – System and Software Quality Models. ISO/IEC 25010. International Organization for Standardization, 2023.
[2] Stephen H. Kan. Metrics and Models in Software Quality Engineering. 2. izdanje. Addison-Wesley, 2002. isbn: 9780201729153.
[3] Barbara Kitchenham i Shari Lawrence Pfleeger. Software Quality: The Elusive Target. U: IEEE Software (1996.). doi: 10.1109/52.476281.
[4] Roger S. Pressman i Bruce R. Maxim. Software Engineering: A Practitioner’s Approach. 8. izdanje. McGraw-Hill, 2014. isbn: 9780078022128.
[5] Ian Sommerville. Software Engineering. 10. izdanje. Pearson, 2015. isbn: 9780133943030.
Ispitna pitanja
1. Značaj kvaliteta softvera. Procesi i standardi.
2. Značaj kvaliteta softvera. Atributi kvaliteta softvera: funkcionalna podobnost, performantnost, kompatibilnost, pouzdanost. Primeri.
3. Značaj kvaliteta softvera. Atributi kvaliteta softvera: održivost. Primeri.
4. Značaj kvaliteta softvera. Atributi kvaliteta softvera: upotrebljivost, sigurnost, bezbednost, prenosivost. Primeri.

<!-- pdf_page=37 printed_page=37 -->

2.1 Primeri poznatih grešaka . . . . . . 24
Pregled
-Na koji sve način neispravan softver utiče na svet oko nas?
2.2 Troškovi usled grešaka u softveru . . . . . . . . . . 32
-Koliko koštaju softverske greške?
Greške u softveru mogu na različite načine uticati na korisničko iskustvo. Najblaži oblik posledica jeste manja neprĳatnost, kao što je iznenadno gašenje internet pregledača (slika 2.1), muzičkog plejera ili mobilne igre, ili greška u sistemu za izgradnju softvera (slika 2.2). Ipak, te neprĳatnosti mogu biti i ozbiljnĳe — na primer, ako navigacioni softver pogrešno usmeri korisnika ka nebezbednoj lokacĳi ili ako, u hitnoj situacĳi, softverski problem onemogući uspostavljanje poziva.
Drugi nivo uticaja softverskih grešaka ogleda se u materĳalnim gubicima, koji mogu imati ozbiljne posledice po pojedince ili finansĳsko poslovanje organizacĳa. Ove greške se najčešće javljaju u poslovnom softveru i bankarskim informacionim sistema, gde mogu izazvati direktne novčane gubitke, kao i gubitak ili kompromitovanje važnih podataka. U određenim slučajevima, posledice se mogu reflektovati i na reputacĳu kompanĳe, izazivajući dugoročne finansĳske probleme.
Slika 2.1: Greška u radu Internet pregledača
Na kraju, greške u softveru mogu imati ifatalneposledice. One se javljaju u kritičnim sistemima, kao što su softver za upravljanje avionima, automobilima i vozovima, gde čak i najmanji propust može dovesti do teških saobraćajnih nesreća. Sličan rizik postoji i u medicinskim uređajima koji se koriste za dĳagnostiku, praćenje vitalnih funkcĳa i pružanje terapĳe, gde softverska greška može direktno ugroziti život pacĳenta. Greške u softveru svemirskih letelica mogu dovesti do neuspeha
Slika 2.2: Greška u sistemu za izgradnju softvera

<!-- pdf_page=38 printed_page=24 -->

misĳa vrednih više stotina miliona dolara, dok softverski problemi u nuklearnim elektranama nose potencĳal za katastrofe nesagledivih razmera. Zbog svega ovoga, razvoj softvera u ovim oblastima zahteva najviši stepen pažnje, rigorozno testiranje i stalnu proveru kvaliteta.
### 2.1 Primeri poznatih grešaka
Greška proizvodi −→
Greške koje naprave programeri, ukoliko se ne otkrĳu u procesu ispitivanja ispravnosti softvera, čine da softver nĳe u potpunosti ispravan, odnosno da sadrži defekte. Ti defekti u određenim situacĳama uzrokuju pad sistema, odnosno softver se ponaša drugačĳe od očekivanog. Pad pravi incident koji može da ima posledice.
Defekt uzrokuje −→
Pad pravi −→
Incident ima −→𝑝𝑜𝑠𝑙𝑒𝑑𝑖𝑐𝑒
2.1.1 Neprĳatnosti i materĳalni gubici
Neke od najpoznatĳih softverskih grešaka, osim što su izazvale ozbiljne neprĳatnosti korisnicima, ostavile su i duboke finansĳske posledice po kompanĳe koje su ih razvile. Njihov uticaj nĳe bio ograničen samo na korisničko iskustvo, već je često vodio ka gubicima poverenja, padu akcĳa i tržišne vrednosti, kao i značajnim materĳalnim štetama.
Aplikacĳa Apple Maps, 2012
Kompanĳa Apple je 2012. godine odlučila da ukloni aplikacĳu za mape Google Maps na svom operativnom sistemu iOS i zameni je svojom aplikacĳom — Apple Maps. Nova aplikacĳa je predstavljena uz operativni sistem iOS 6, a trebalo je da bude modernĳa, sa 3D prikazima, navigacĳom koja prati tekuće stanje u saobraćaju i glasovnim navođenjem. Međutim, aplikacĳa Apple Maps je odmah po lansiranju doživela veliku kritiku zbog brojnih grešaka, uključujući:

<!-- pdf_page=39 printed_page=2 -->

Pogrešne lokacĳe — Gradovi, znamenitosti i firme su bili loše označeni ili potpuno pogrešno locirani.
Na primer, policĳa u Australĳi je upozorila građane da ne koriste Apple Maps jer je vodič za grad Mildura ljude odvodio usred opasne pustinje.
Netačne rute — Navigacĳa je korisnike vodila pogrešnim ili nepostojećim putevima.
Izobličene mape — 3D prikazi zgrada i terena su izgledali iskrivljeno ili neprirodno. Primer lošeg prikaza dat je na slici 2.3.
Nedostajuće informacĳe — Mnoge lokacĳe i ulice nisu bile uopšte ucrtane.
Izvršni direktor kompanĳe Apple, Tim Kuk (eng. Tim Cook), uputio je javno izvinjenje i korisnicima čak preporučio da privremeno koriste konkurentske aplikacĳe. Zbog skandala, Apple je otpustio nekoliko ključnih ljudi koji su bili na visokim pozicĳama. Negativna percepcĳa kompanĳe dovela je do pada vrednosti akcĳa Apple-a za približno 4,5%, što je bilo smanjenje tržišne vrednosti za oko 30 milĳardi dolara. Kako bi ispravio početne defekte i poboljšao kvalitet svoje aplikacĳe, Apple je tokom narednih godina uložio više milĳardi dolara u razvoj Apple Maps. Ova ulaganja obuhvatala su akvizicĳe kompanĳa specĳalizovanih za pravljenje mapa, prikupljanje sopstvenih podataka, kao i razvoj novih funkcionalnosti. Iako je teško precizno kvantifikovati ukupne finansĳske gubitke, kombinacĳa pada tržišne vrednosti i višegodišnjih ulaganja u unapređenje Apple Maps sugeriše da je ova greška imala značajan ekonomski uticaj na kompanĳu.
Slika 2.3: Primer prikaza aplikacĳe Apple Maps
Knight Capital Group, 1. avgust 2012. godine
U avgustu 2012. godine, kompanĳa Knight Capital Group suočila se sa jednim od najozbiljnĳih tehnoloških incidenata u istorĳi savremenog finansĳskog tržišta. Softverska greška u sistemu za trgovanje rezultirala je gubitkom od 440 miliona dolara za svega 45 minuta — što predstavlja iznos gotovo četiri puta veći od neto profita kompanĳe ostvarenog tokom prethodne godine.

<!-- pdf_page=40 printed_page=26 -->

Dodatno, vrednost akcĳa kompanĳe je u roku od dva dana opala za čak 75%.
Knight Capital Group
Do incidenta je došlo prilikom implementacĳe novog softverskog modula, kada je nenamerno reaktiviran stari, nefunkcionalni deo koda. Aktivirani kôd je automatski generisao veliki broj netačnih naloga, izazivajući kupovinu i prodaju akcĳa po izrazito nepovoljnim cenama. Ovaj događaj ne samo da je značajno ugrozio reputacĳu kompanĳe, već je ubrzo doveo i do njenog potpunog finansĳskog kolapsa.
-Greška: (1) Programer nĳe ažurirao sve servere sa najnovĳom verzĳom softvera (2) Nepostojanje provere verzĳe koda prilikom obrade upita
-Defekt: Moguće je pokrenuti kôd koji se koristio za testiranje
-Pad: Pokrenute su pogrešne transakcĳe
Facebook Outage, 13. mart 2019. godine
-Incident: Veliki finansĳski gubitak
U martu 2019. godine, kompanĳa Facebook doživela je jedan od najznačajnĳih prekida u svojoj istorĳi koji je uticao na milĳarde korisnika širom sveta. Ovaj događaj, poznat kao Facebook Outage 2019, izazvao je ozbiljne poremećaje u funkcionisanju ne samo servisa Facebook, već i njegovih povezanih servisa kao što su Instagram, WhatsApp i Messenger.
Prema zvaničnom saopštenju kompanĳe, uzrok prekida bila je „promena konfiguracĳe servera” koja je pokrenula lanac problema u sistemu. Nakon što su servisi ponovo postali dostupni, Facebook se izvinio korisnicima i naveo da su sistemi u fazi oporavka. Međutim, kompanĳa nĳe pružila detaljnĳe informacĳe o tačnom uzroku problema, što je izazvalo kritike stručne javnosti i korisnika zbog nedostatka transparentnosti. Iako su detalji ostali oskudni, izveštaji sugerišu da je došlo do greške u internim sistemima za rutiranje podataka, što je dovelo do prekida komunikacĳe između Facebook-ovih centara podataka. Zbog toga su korisnici širom sveta imali ograničen ili nikakav pristup platformama.
Zvanično saopštenje kompanĳe Facebook: ”Juče smo izvršili promenu konfiguracĳe servera koja je pokrenula niz problema. Kao rezultat toga, mnogi korisnici su imali poteškoća u pristupu našim aplikacĳama i uslugama.”
Ovaj prekid je bio jedan od najopsežnĳih u istorĳi društvenih mreža. Pored korisničkih neugodnosti (slika 2.4), prekid je imao i finansĳske posledice. Analitičari
Slika 2.4: Poruka o nedostupnosti servisa

<!-- pdf_page=41 printed_page=2 -->

su procenili da je Facebook, sa prosečnim dnevnim prihodima od oko 189 miliona dolara, pretrpeo značajan gubitak prihoda tokom ovog perioda. Neki izvori navode da je prekid trajao 14 sati, dok drugi navode da je prekid trajao oko 24 sata. U skladu sa time se i razlikuju procene finansĳskog gubitka. Takođe, ovaj incident je uticao i na pad akcĳa kompanĳe Facebook za oko 2%.
Google Cloud Outage, 14. decembar 2020. godine
Kompanĳa Google je imala neželjeni prekid usluga 14. decembra 2020. godine u trajanju od 47 minuta. Tokom ovog perioda, korisnici širom sveta nisu mogli da pristupe uslugama koje zahtevaju Google nalog, uključujući Gmail, YouTube, Google Drive, Google Docs i druge. Ovaj događaj je imao globalni uticaj na korisnike i kompanĳe koje se oslanjaju na Google-ovu infrastrukturu.
Prema zvaničnom izveštaju kompanĳe Google (slika 2.5), uzrok prekida bio je problem u sistemu za upravljanje kvotama skladišnog prostora, koji je nenamerno smanjio kapacitet centralnog sistema za upravljanje identitetima korisnika. Ova greška je dovela do toga da se zahtevi za autentifikacĳu nisu mogli obraditi, što je rezultiralo greškama prilikom pokušaja pristupa uslugama koje zahtevaju prĳavu.
Iako je prekid trajao manje od sat vremena, njegov uticaj je bio značajan zbog široke upotrebe Google-ovih servisa u svakodnevnom poslovanju i komunikacĳi. Google se izvinio korisnicima i naveo da su preduzete mere kako bi se sprečilo ponavljanje sličnih incidenata u budućnosti.
Teško je precizno kvantifikovati direktan finansĳski gubitak izazvan ovim konkretnim prekidom. Poznato je da je Google Cloud u 2020. godini zabeležio operativni gubitak od 5,61 milĳardu dolara. Ovaj gubitak pripisuje se raznim poslovnim odlukama i nĳe vezan samo za pomenuti incident.
Slika 2.5: Deo zvaničnog izveštaja kompanĳe Google https: //status.cloud.google. com/incident/zall/20013

<!-- pdf_page=42 printed_page=28 -->

2.1.2 Fatalne posledice
Većina softverskih grešaka ne rezultira fatalnim posledicama. Ipak, kada se propusti jave u okviru kritičnih sistema, njihovi efekti mogu biti izuzetno ozbiljni — uključujući gubitke ljudskih života, teške povrede, značajne finansĳske štete i razorne sistemske havarĳe. Iako su ovakvi incidenti retki u apsolutnim brojkama, njihov uticaj na bezbednost, ekonomĳu i poverenje u tehnologĳu je nesrazmerno velik.
Uprkos kontinuiranom unapređenju programerskih praksi, uključujući primenu formalnih metoda, automatizovanog testiranja i usklađivanje sa bezbednosnim standardima, učestalost najtežih grešaka nĳe opala u meri u kojoj bi se očekivalo. Promenila se, međutim, njihova priroda: umesto pojedinačnih grešaka u kodu, sve češće se javljaju kompleksni, sistemski defekti koji proizilaze iz loše integracĳe, nejasnih zahteva ili neočekivane interakcĳe među podsistemima.
Therac 25, 1985–1987
Aparat za radioterapĳu Therac-25 je bio proizvod kanadske kompanĳe AECL (Atomic Energy of Canada Limited). Ovaj aparat je bio napredni naslednik serĳe uređaja Therac-6 i Therac-20, koji su takođe koristili sličnu tehnologĳu za primenu radioterapĳe. Therac-25 je kombinovao softversku kontrolu i hardverske komponente u cilju povećanja preciznosti zračenja.
Između 1985. i 1987. godine, aparat je uzrokovao najmanje šest slučajeva predoziranja pacĳenata radĳacĳom, od kojih su troje umrli. Ovi nesrećni slučajevi bili su rezultat softverske greške. Therac-25 je imao dva režima zračenja:
-Elektronski snop niskog intenziteta, -Fotonski snop visoke energĳe, koji mora da se dodatno filtrira.

<!-- pdf_page=43 printed_page=2 -->

Ako bi tehničar najpre uneo prvi režim, a zatim ga promenio u drugi, softver nĳe uvek uspevao da ispravno ažurira stanje uređaja. Rezultat toga je bio da uređaj misli da koristi snop niskog intenziteta i doze koje su za to predviđene, ali bi zapravo poslao visokoenergetski snop bez zaštitnog filtera. Greška je nastajala usled loše sinhronizacĳe:
Therac 25 Greška: (1) Programer je napravio grešku u promeni podataka bez adekvatne sinhronizacije, (2) Tehničar je promenio režim rada u pogrešnom trenutku Defekt: Mogućnost slanja visokoenergetskog snopa bez zaštitnog filtera Pad: Prekoračena je bezbedna doza zračenja Incident: Pacĳent je umro
-Jedan proces je ažurirao režim tretmana. -Drugi proces je proveravao spremnost uređaja za zračenje.
Ako bi se ti procesi „preklopili“ u pogrešnom trenutku, uređaj bi pogrešno zaključio da je sve spremno i poslao snop visoke energĳe bez zaštitnog filtera sa dozom zračenja koja je predviđena za snop niskog intenziteta.
Pored ove softverske greške, nesrećama su doprineli i naredni propusti:
-nedostatak hardverskih sigurnosnih sistema — Therac-25 je uklonio fizičke sigurnosne blokade koje su postojale u prethodnim uređajima, oslanjajući se isključivo na softver,
-loša dĳagnostika — interfejs aparata nĳe jasno ukazivao na probleme, tehničari su dobĳali nejasne poruke o grešci i
-zanemarivanje prethodnih incidenata — kompanĳa AECL nĳe preduzela adekvatne mere nakon inicĳalnih pritužbi i događaja.
Kao rezultat ovih nesrećnih događaja, razvĳeni su novi standardi za sigurnost medicinskih uređaja, uključujući rigoroznĳe zahteve za testiranje i formalnu verifikacĳu softvera u medicinskim sistemima.
Dahran raketa, 25. februar 1991. godine
Tokom Zalivskog rata, 25. februara 1991. godine, iračka balistička raketa pogodila je američku vojnu bazu u Dahranu (Saudĳska Arabĳa), usmrtivši 28 vojnika i ranivši

<!-- pdf_page=44 printed_page=30 -->

više od 100 vojnika. Nakon detaljne istrage, utvrđeno je da je uzrok neuspeha protivraketnog sistema Patriot bila greška u softveru koji je upravljao internim sistemskim vremenom. Naime, zbog akumulacĳe zaokruživanja decimalnih vrednosti u brojevima s pokretnim zarezom, došlo je do odstupanja od približno jedne trećine sekunde nakon 100 sati neprekidnog rada sistema. Iako se ovo odstupanje može činiti beznačajnim, u kontekstu ogromnih brzina kojima se balističke rakete kreću, ono je rezultovalo prostornim promašajem od oko 600 metara. Radar je usled toga tražio raketu na pogrešnoj lokacĳi, nĳe uspeo da je prati, i samim tim nĳe aktivirao mehanizam za presretanje.
Dahran raketa Greška: Neprecizno zaokruživanje vrednosti brojeva Defekt: Pogrešno računanje vremena Pad: Neaktiviran mehanizam za presretanje rakete Incident: Smrt 28 vojnika i povrede više od 100 vojnika
Ovaj događaj predstavlja jedan od najupečatljivĳih primera fatalnih posledica softverske greške u savremenoj vojnoj istorĳi. Osim ljudskih žrtava, incident je izazvao ozbiljnu zabrinutost u vezi sa pouzdanošću softverski vođenih odbrambenih sistema. Pentagon i američka vojska bili su izloženi javnoj i političkoj kritici, a celokupan događaj podstakao je temeljnu revizĳu načina na koji se razvĳa, testira i primenjuje softver u vojnim i drugim bezbednosno osetljivim sistemima.
Slika 2.6: Maketa rakete Ariane 5, Muzej vazduhoplovstva u Parizu, Francuska
Ariane 5, 4. jun 1996. godine
Raketa Ariane 5 Evropske svemirske agencĳe (ESA) uništila se svega 37 sekundi nakon poletanja, 4. juna 1996. godine. Pri tome su izgubljena četiri satelita namenjena proučavanju Zemljine magnetosfere. Procenjena šteta iznosila je preko 370 miliona dolara, čime je ovaj incident postao jedan od najskupljih softverskih grešaka u istorĳi svemirskih misĳa.
Ariane 5 Greška: (1) Konverzĳa iz 64-bitne u 16-bitnu vrednost (2) Nepostojanje adekvatne obrade izuzetka Defekt: Sistem neadekvatno reaguje na greške u ulaznim podacima Pad: Skretanje sa putanje i aktivacĳa sistema za samouništenje Incident: Veliki finansĳski gubitak i propuštena prilika za novim naučnim saznanjima
Uzrok nesreće bio je softverski propust. Sistem je pokušao da konvertuje 64-bitnu vrednost brzine u 16-bitnu vrednost, što je izazvalo numeričko prekoračenje i izuzetak koji nĳe bio adekvatno obrađen. To je dovelo do pogrešnih komandi, skretanja sa putanje i aktivacĳe sistema za samouništenje.

<!-- pdf_page=45 printed_page=2 -->

Ova katastrofa je istakla kritičnu važnost verifikacĳe softverskih komponenti u kompleksnim i bezbednosno osetljivim sistemima, te je podstakla reforme u ESA-inim procedurama testiranja i verifikacĳe softvera.
The Mars Climate Orbiter 23. septembar 1999. godine
Letelica Mars Climate Orbiter (NASA) nestala je prilikom ulaska u orbitu Marsa 23. septembra 1999. godine, nakon što je ušla u orbitu značajno niže od planirane putanje i najverovatnĳe izgorela u atmosferi. Istragom je utvrđeno da je uzrok nesreće bio propust u konverzĳi jedinica: deo softvera je koristio imperĳalne jedinice dok je drugi deo softvera očekivao metričke jedinice. Ova neusaglašenost dovela je do pogrešnog proračuna putanje.
Sama letelica je koštala 125 miliona dolara, dok je ukupni trošak misĳe procenjen na oko 327 miliona dolara. Incident je izazvao ozbiljnu kritiku NASA-inih programerskih i upravljačkih procedura. Kao rezultat, uvedene su strože kontrole, standardizacĳa jedinica i unapređeni protokoli testiranja softverskih komponenti.
Slika 2.7: Fotografija letelice Mars Climate Orbiter prilikom sklapanja, NASA, januar 1998. godine
Mars Climate Orbiter Greška: Deo softvera je koristio imperĳalne jedinice, dok je drugi deo softvera očekivao metričke jedinice Defekt: Pogrešno računanje putanje Pad: Ulazak u orbitu Marsa na pogrešnom rastojanju Incident: Letelica je izgorela u atmosferi Marsa
Greške u automobilskoj industrĳi
Softverske greške u automobilskoj industrĳi su ozbiljan problem koji može imati direktne posledice po bezbednost putnika. Na primer, kompanĳa General Motors je softversku grešku otkrila tek nakon saobraćajnih nesreća u kojima je bio jedan smrtni ishod i tri povrede. Ova greška je sprečavala aktivacĳu prednjih vazdušnih jastuka i zatezača sigurnosnih pojaseva tokom sudara, povećavajući rizik od povreda putnika. Kompanĳa je u septembru 2016. godine, najavila opoziv 4,3 miliona vozila.
General Motors je naveo da ovaj opoziv neće imati značajan uticaj na finansĳske rezultate kompanĳe i precizna

<!-- pdf_page=46 printed_page=32 -->

procena troškova nĳe javno objavljena. Međutim, u slučaju koji je uključivao opoziv sličnog broja vozila (opoziv zbog problema sa Takata vazdušnim jastucima) troškovi su bili procenjeni na 550 miliona dolara. S obzirom na to, može se pretpostaviti da su troškovi ovog opoziva bili značajni, ali verovatno niži od pomenute sume, jer je rešenje problema uključivalo ažuriranje softvera, što je manje skupo od fizičke zamene delova.
Sličan problem je imala i kompanĳa Fiat Chrysler koja je u maju 2017. odlučila da opozove više od 1,25 miliona kamioneta širom sveta, s ciljem otklanjanja softverske greške koja je potencĳalno povezana sa saobraćajnim nesrećama sa jednim smrtnim ishodom i dve povrede. Iako nisu postojali konačni dokazi da je softverski propust direktno uzrokovao ove nesreće, proizvođač vozila je odlučio da opoziv sprovodi preventivno, kao meru predostrožnosti.
Kako je navedeno u zvaničnom saopštenju, softverska anomalĳa je privremeno onemogućavala aktivacĳu bočnih vazdušnih jastuka, kao i mehanizama koji automatski zatežu pojas. Do takvog neispravnog ponašanja sistema je moglo da dođe u slučaju prevrtanja vozila izazvanog snažnim udarcem u donji deo automobila, na primer pri udaru u prepreke na putu ili prilikom vožnje van uređenih saobraćajnica. Verovatnoća nastanka takvog incidenta ocenjena je kao izuzetno mala, jer je za njegovu pojavu potrebna vrlo specifična i retka sekvenca događaja. U cilju otklanjanja uočene greške, bilo je neophodno izvršiti reprogramiranje računarskih modula u svim vozilima koja su obuhvaćena opozivom. Tačni troškovi ovog opoziva nisu objavljeni.
### 2.2 Troškovi usled grešaka u softveru
Najveći troškovi usled grešaka u softveru nastaju kada se greške otkrĳu nakon puštanja sistema u rad. To uključuje gubitke u prihodu, narušavanje reputacĳe, opozive

<!-- pdf_page=47 printed_page=2 -->

proizvoda, regulatorne kazne, kao i gubitke podataka ili života.
Američki nacionalni institut za standarde i tehnologĳu (eng. US National Institute of Standards and Technology, skraćeno NIST) je 2002. godine napravio opsežnu studĳu sa ciljem procene uticaja softverskih grešaka na američku ekonomĳu. Po ovoj studĳi, neispravan softver je koštao američku ekonomĳu 59.5 milĳardi dolara godišnje. Dodatno, u studĳi je naglašeno da bi rano otkrivanje grešaka moglo da uštedi 22 milĳarde dolara godišnje, dakle nešto više od trećine ukupnih troškova.
Ova studĳa značajno je uticala na ulaganje u unapređivanje procesa razvoja softvera sa ciljem poboljšanja kvaliteta softvera i smanjenja količine grešaka u softveru. Dodatno, posebna ulaganja su bila usmerena ka razvoju alata koji daju podršku i omogućavaju automatizacĳu procesa verifikacĳe softvera.
Dvadeset godina kasnĳe‗, Konzorcĳum za kvalitet informacĳa i softvera (eng. Consortium for Information and Software Quality), skraćeno CISQ) u izveštaju o ceni lošeg kvaliteta softvera (eng. Cost of Poor Software Quality) u Sjedinjenim Američkim Državama za 2022. godinu navodi da su troškovi usled lošeg kvaliteta softvera porasli na 2410 milĳardi američkih dolara. U izveštaju za 2020. godinu, navedena je procena troškova 2080 milĳardi američkih dolara. Dakle, za kratko vreme uočen je veliki porast troškova uzrokovanih softverskim greškama.
CISQ u izveštaju za 2020. godinu navodi da su najbitnĳi troškovi† proistekli iz softverskih grešaka:
Operativni softverski kvarovi: Procena je da su operativni softverski kvarovi (eng. operational software
‗ Iako najavljen, izveštaj za 2024. godinu još uvek nĳe dostupan. Poslednji javno dostupan izveštaj je iz 2022. godine.
† Ovi troškovi nisu međusobno nezavisni, tj. ima preklapanja, pa zbog toga njihov zbir nĳe 2080 već veći. Na primer, problemi sa zastarelim sistemima i operativni softverski kvarovi su usko povezani sa tehničkim dugom.

<!-- pdf_page=48 printed_page=34 -->

failures), uključujući greške u funkcionisanju sistema i nepredviđene zastoje, doveli do gubitaka od oko 1560 milĳardi dolara. Ovaj broj predstavlja povećanje od 22% u odnosu na 2018. godinu.
Neuspešni razvojni projekti: Neuspešni ili otkazani softverski projekti, često zbog lošeg upravljanja ili nedostatka kvaliteta, doveli su do gubitaka od 260 milĳardi dolara.
Problemi sa zastarelim sistemima: Održavanje i nadogradnja zastarelih sistema koštali su oko 520 milijardi dolara.
Tehnički dug: Troškovi tehničkog duga‡ (eng. technical debt), koji predstavlja nepopravljene greške i neefikasnosti u kodu, procenjeni su na 1310 milĳardi dolara.
Gubici zbog sajberkriminala: U izveštaju nĳe navedena tačna procena troškova usled sajberkriminala, osim da su ovi troškovi značajni i u porastu.
CISQ u izveštaju za 2022. godinu navodi da su najviše porasli gubici
-prouzrokovani sajber kriminalom koji su rezultat postojećih softverskih ranjivosti. Oni su između 2020. i 2021. godine porasli za 64%, a rastući trend se nastavio i u 2022. godini. Prosečan trošak jednog incidenta narušavanja podataka u SAD-u dostigao je 9,44 miliona dolara.
-nastali usled problema u komponentama softvera otvorenog koda. Broj neuspeha zbog slabosti u komponentama otvorenog koda povećao se za
‡ Tehnički dug se odnosi na posledice pravljenja brzih, kratkoročnih rešenja u razvoju softvera, umesto boljih, dugoročno održivih rešenja. To je cena koju tim mora da plati u budućnosti zbog kompromisa u kvalitetu koda napravljenih da bi se nešto brže isporučilo danas. Tehnički dug nastaje usled nejasnih i nepreciznih zahteva, zaobilaženja dobrih programerskih praksi da bi se „stigao rok“, odsustva testova i dokumentacĳe, održavanja starog koda bez značajnih refaktorisanja i nedostatka automatizacĳe i sigurnosnih provera. Posledice tehničkog duga su teži i sporĳi razvoj novih funkcionalnosti, više grešaka i kvarova, kao i povećani troškovi održavanja.

<!-- pdf_page=49 printed_page=2 -->

alarmantnih 650% između 2020. i 2021. godine.
-koji su rezultat uticaja tehničkog duga. Ovaj trošak je porastao na približno 1520 milĳardi dolara godišnje, što ukazuje na ozbiljnost problema i potrebu za njegovim rešavanjem.
Svi ovi izveštaji su vrlo konzervativni jer uzimaju u obzir samo dostupne i javno prĳavljene podatke. U većini slučajeva, oni se oslanjaju na analize izveštaja o incidentima, javno objavljenim gubicima, regulatornim dokumentima i istraživanjima sprovedenim među organizacĳama. Međutim, stvarna slika je često znatno ozbiljnĳa.
Kompanĳe, iz različitih razloga, često smanjuju i ublažavaju izveštaje o problemima koji su nastali usled grešaka u softveru. To rade kako bi zaštitile svoj ugled, izbegle pad poverenja korisnika i investitora, ili kako bi izbegle regulatorne i pravne posledice. Greške u softveru koje dovedu do curenja podataka, pada sistema, zastoja u radu ili finansĳskih gubitaka neretko se interno rešavaju i nikada ne dospeju u javnost.
Pored toga, mnoge organizacĳe nemaju razvĳen sistem za praćenje i precizno merenje posledica softverskih grešaka, pa čak i kada žele da prĳave problem – nemaju celovite podatke. Zbog toga je procena ukupnih troškova lošeg kvaliteta softvera u izveštajima poput onih koje objavljuje CISQ gotovo sigurno donji prag stvarne štete. Pritom, stvarna cena lošeg softvera uključuje i skrivene gubitke kao što su izgubljene prilike, pad produktivnosti i frustracĳe korisnika. Sve to ostaje van zvanične statistike, ali ima dugoročne posledice po poslovanje i razvoj digitalnog tržišta.
Rezime
-Uticaj neispravnog softvera: neprĳatnosti, materijalni gubici i materĳalno nemerljive posledice.

<!-- pdf_page=50 printed_page=36 -->

-Postoji veliki broj primera softverskih grešaka koje su imale značajne materĳalne i nematerĳalne posledice.
-Materĳalni troškovi neispravnog softvera se mere hiljadama milĳardi dolara na godišnjem nivou.
-Troškovi neispravnog softvera u velikoj meri su posledica tehničkog duga, odnosno pravljenja softvera bez adekvatnog kvaliteta.
Literatura
[1] Victor R. Basili i Barry T. Perricone. Software Errors and Complexity: An Empirical Investigation. U: Communications of the ACM 27.1 (1984.), str. 42– 52. doi: 10.1145/69605.2085.
[2] Albert Endres. An analysis of errors and their causes in system programs. U: Proceedings of the International Conference on Reliable Software. Los Angeles, California: ACM, 1975., str. 327–336. doi:
10.1145/800027.808455.
[3] Thomas J. Ostrand, Elaine J. Weyuker i Robert M. Bell. Predicting the Location and Number of Faults in Large Software Systems. U: IEEE Transactions on Software Engineering 31.4 (2005.), str. 340–355. doi: 10.1109/TSE.2005.49.
[4] James Reason. Human Error. Cambridge University Press, 1990. isbn: 9780521314190.
Ispitna pitanja
5. Uticaj neispravnog softvera. Primeri neprĳatnosti i materĳalnih gubitaka.
6. Uticaj neispravnog softvera. Primeri fatalnih posledica.
7. Troškovi usled grešaka u softveru.

<!-- pdf_page=51 printed_page=51 -->

Pregled
3.1 Odnos verifikacĳe i validacĳe softvera . 38
-Koji je odnos verifikacĳe i validacĳe softvera? -Kako se definišu verifikacĳa i validacĳa softvera? -Koji pristupi i problemi koji se javljaju u okviru verifikacĳe softvera?
3.2 Tehnike verifikacĳe softvera . . . . . . . 40
-Koje su specifičnosti automatske statičke verifikacĳe softvera?
Obezbeđivanje i kontrola kvaliteta softvera obuhvataju procese validacĳe i verifikacĳe.
Verifikacĳa softvera obuhvata sve procese koji su potrebni da se osigura da razvĳeni softver zadovoljava zadatu specifikacĳu, odnosno da ne sadrži defekte i da bude ispravan. Verifikacĳom se odgovara na pitanje „Da li je softver ispravno izgrađen?” i fokusira se na proveru da li sistem u potpunosti ispunjava specifikacĳu.
Validacĳa softvera obuhvata sve procese koji su potrebni da se osigura da razvĳeni softver zadovoljava korisničke potrebe. Validacĳom se odgovara na pitanje „Da li je izgrađen pravi softver?” i procenjuje da li softver ispunjava potrebe i očekivanja krajnjih korisnika.
U oba slučaja, kontrola se najčešće sprovodi testiranjem, ali postoje i druge napredne tehnike koje se mogu koristiti. Kako bi softverski proizvod bio upotrebljiv i uspešan, neophodno je da zadovolji i kriterĳume ispravnosti i kriterĳume usklađenosti sa korisničkim zahtevima.
Funkcionalna podobnost, performantnost, kompatibilnost, pouzdanost, sigurnost, bezbednost i prenosivost predstavljaju dinamička svojstva softvera i procenjuju se primarno kroz procese verifikacĳe. Upotrebljivost

<!-- pdf_page=52 printed_page=38 -->

Verifikacĳa
Potrebe i očekivanja korisnika Specifikacĳa Proces razvoja Proizvod
Validacĳa
Slika 3.1: Verifikacĳa i validacĳa softvera
se uglavnom procenjuje kroz validacĳu, iako se pojedini aspekti, poput otpornosti na korisničke greške, mogu ispitivati i verifikacĳom. Održivost je statička karakteristika koja se ocenjuje kroz verifikacĳu, najčešće pregledima koda i pomoću alata za statičku analizu.
Napomena: studentski i industrĳski projekti. Proces verifikacĳe i validacĳe studentskih projekata najčešće se sprovodi pri kraju procesa razvoja softvera, koristeći mali broj test primera. Ovaj proces obično čini veoma mali procenat ukupnog napora koji studenti ulože u razvoj softvera. S druge strane, proces verifikacĳe i validacĳe u industrĳi sprovodi se tokom celokupnog razvoja softvera i najčešće čini više od 30% ukupnog napora, pri čemu taj procenat može značajno da varira u zavisnosti od vrste projekta i nivoa kvaliteta koji je neophodno postići. Za bezbednosno kritične sisteme ovaj procenat je značajno viši. Osnovne razlike između studentskih i industrĳskih projekata su:
### 3.1 Odnos verifikacĳe i validacĳe softvera
U savremenom digitalnom okruženju, korisnici pokazuju sve manju tolerancĳu prema softverskim greškama, naročito kada je reč o mobilnim aplikacĳama. Ogromna konkurencĳa i visoka očekivanja doveli su do toga da i najmanji propust može biti presudan za uspeh proizvoda. Korisnici danas imaju širok izbor – za svaku potrebu postoji desetine alternativa, bilo da se radi o aplikacĳama za zdravlje, zabavu, hobĳe ili društvene mreže. Zbog toga, loše korisničko iskustvo se ne oprašta; prelazak na konkurentski proizvod je lak i brz. Greške u softveru nisu samo tehnički izazov — one predstavljaju direktan poslovni rizik.
Upravo zato, procesi verifikacĳe i validacĳe softvera postaju ključni u razvoju aplikacĳa. Verifikacĳa se odnosi na sve vrste provera ispravnosti rada aplikacĳe, uključujući i testiranje aplikacĳe u realnim uslovima i na različitim uređajima, kako bi se osiguralo da sistem funkcioniše bez grešaka. Ako aplikacĳa ima bagove, ruši se ili je spora, korisnici je percipiraju kao nepouzdanu i
-dužina upotrebe softvera,
-način upotrebe softvera,
-broj korisnika, -očekivanja i -cena pada.

<!-- pdf_page=53 printed_page=3 -->

deinstaliraće je često i nakon samo prve greške. Dodatno, negativne recenzĳe odvraćaju buduće korisnike.
S druge strane, validacĳa procenjuje da li aplikacĳa zaista ispunjava očekivanja korisnika. Aplikacĳa može biti tehnički ispravna, ali ako ne nudi jasnu vrednost ili ako je interfejs zbunjujući, korisnik je verovatno više neće koristiti. Upravo zbog toga, elementi kao što su dizajn korisničkog iskustva i korisničkog interfejsa, uvodno vođenje korisnika kroz aplikacĳu i prvi utisak igraju presudnu ulogu u njenom prihvatanju.
Primer 3.1.1 (Verifikacĳa i validacĳa) U komunikacĳi sa klĳentom, definisana je specifikacĳa sistema:
Aplikacĳa treba da prikazuje vreme.
U skladu sa zadatom specifikacĳom, moguće je napraviti dva rešenja.
Rešenje 1: Digitalni časovnik
Rešenje 2: Aplikacĳa za vremensku prognozu
Rešenja su fundamentalno različita jer je reč „vreme” višeznačna.
Verifikacĳom se proverava da li je sistem koji je izgrađen u skladu sa zadatom specifikacĳom, tj. da li sistem tačno prikazuje vreme.
-U slučaju digitalnog časovnika, verifikacĳa obuhvata proveru da li aplikacĳa ispravno prikazuje trenutno lokalno vreme, u skladu sa sistemskim vremenom uređaja ili referentnim vremenskim serverom. To podrazumeva ispitivanje usklađenosti prikazanog vremena sa vremenom operativnog sistema, kao i ispravnost prikaza prilikom promene vremenske zone. Takođe, proverava se da li se vreme automatski osvežava bez potrebe za dodatnom intervencĳom korisnika,

<!-- pdf_page=54 printed_page=40 -->

odnosno bez manuelnog osvežavanja stranice ili aplikacĳe.
-Kod aplikacĳa za prikaz vremenske prognoze, verifikacĳa se fokusira na tačnost i konzistentnost prikaza prognoziranih meteoroloških podataka koji se preuzimaju sa odgovarajućih vremenskih servisa, kao što su AccuWeather ili OpenWeatherMap. Neophodno je utvrditi da li se podaci, poput temperature i opisa vremenskih uslova, prikazuju u odgovarajućem i očekivanom formatu. Pored toga, proverava se i da li aplikacĳa ispravno prikazuje vremenske podatke za različite lokacĳe, bilo da su one definisane nazivima gradova ili geografskim koordinatama.
Validacĳa predstavlja postupak kojim se utvrđuje da li je razvĳeni sistem u skladu sa stvarnim potrebama i očekivanjima korisnika. Na primer, ukoliko je korisnik zahtevao digitalni časovnik, tada je rešenje koje implementira upravo tu funkcionalnost validno. Međutim, ako je korisnik očekivao aplikacĳu za vremensku prognozu, tada digitalni časovnik ne zadovoljava njegove potrebe i smatra se potpuno neodgovarajućim rešenjem.
Jasno je da i potpuno ispravan digitalni časovnik nema vrednost u kontekstu zahteva za aplikacĳom koja prikazuje vremenske uslove. S druge strane, ukoliko je korisnik zaista želeo digitalni časovnik, ali je implementacĳa neispravna, sistem takođe postaje neupotrebljiv.
### 3.2 Tehnike verifikacĳe softvera
Verifikacĳa softvera obuhvata skup sistematskih metoda i aktivnosti kojima se proverava da li softverski proizvod ispravno implementira zadatu specifikacĳu. Tehnike verifikacĳe softvera uključuju dinamičku i statič-

<!-- pdf_page=55 printed_page=3 -->

ku verifikacĳu softvera. Dinamička verifikacĳa softvera podrazumeva ispitivanje ispravnosti softvera u toku njegovog izvršavanja. Statička verifikacĳa softvera podrazumeva ispitivanje ispravnosti softvera bez njegovog izvršavanja, odnosno analizu izvornog koda.
Dinamička verifikacĳa softvera. Najčešći vid dinamičke verifikacĳe softvera je testiranje. Testiranje je izvršavanje programa sa ciljem da se pronađe što više mogućih defekata ili da se stekne dovoljno poverenja u sistem koji se testira. Pravilnim i sistematičnim testiranjem podižemo nivo pouzdanosti i smanjujemo verovatnoću da greške promaknu. Obim testiranja i aktivnosti koje su vezane za testiranje zavise od metodologĳe razvoja softvera i prilagođavaju se svakom konkretnom projektu. Moderni pristupi razvoju softvera podrazumevaju da je testiranje prisutno u svakoj fazi razvoja softvera. U okviru dinamičke verifikacĳe softvera, koriste se i alati za debagovanje kao i razne vrste profajlera.
Napomena: Testiranje se često koristi i kao sinonim za verifikacĳu i kao sinonim za validacĳu softvera. Testiranje se često koristi i kao sinonim za brigu o kvalitetu softvera. Međutim, testiranje je ipak samo važan deo verifikacĳe softvera, važan deo validacĳe softvera, a verifikacĳa i validacĳa su važan deo brige o kvalitetu softvera.
Statička verifikacĳa softvera. Postoje različite vrste statičke verifikacĳe:
Metode mašinskog učenja mogu da se koriste za predviđanje grešaka u softveru. Jedan takav primer se može videti u master radu Nikole Vidiča: Primena mašinskog učenja u verifikacĳi softvera
-Provere i pregledi koda koje rade ljudi -Formalne metode verifikacĳe softvera — uslovi ispravnosti softvera iskazuju se u terminima matematičkih tvrđenja na striktno definisanom formalnom jeziku izabrane matematičke teorĳe.
Ručne provere i pregledi koda su veoma važni i svakodnevno se primenjuju u okviru procesa razvoja softvera. Formalne metode se sve više koriste na najrazličitĳe načine. Važno mesto u oblasti formalnih metoda zauzima formalna semantika programskih jezika. Formalna semantika programskog jezika koristi matematičke modele i formalne tehnike za precizno definisanje značenja programa. Cilj formalne semantike je da na rigorozan način opiše kako se izvršavaju naredbe u programskom

<!-- pdf_page=56 printed_page=42 -->

jeziku, čime se eliminiše dvosmislenost i omogućava proverljiva interpretacĳa. Formalna semantika predstavlja temelj za razumevanje i analiziranje značenja softverskog koda na precizan, matematički način.
Upravo kroz formalnu semantiku postaje moguće:
-modelovati izvršavanje programa nezavisno od konkretne mašine ili kompajlera,
-dokazivati korektnost softverskih komponenti i -razvĳati alate za formalnu verifikacĳu.
Idealno rešenje za verifikacĳu softvera bi bio alat koji automatski analizira kôd i daje precizne informacĳe o njegovoj ispravnosti. Međutim, postoji fundamentalno ograničenje zbog kojeg tako nešto nĳe moguće napraviti. Naime, halting problem je neodlučiv.‗ Ne postoji opšti automatizovan način za proveravanje da li je neka naredba programa dostižna, pa sami tim ni da li je ispravna, odnosno da li je sam program ispravan.
Slika 3.2: Logo alata Rocq (https: //rocq-prover.org/)
Posledica teorĳskog ograničenja je da nĳe moguće napraviti program koji bi potpuno automatski u konačnom vremenu, koristeći konačne resurse mogao da utvrdi ispravnost proizvoljnog programa potpuno precizno. Međutim, ukoliko se odreknemo potpune preciznosti, možemo da napravimo program koji poptuno automatski, u konačnom vremenu, koristeći konačne resurse može da dâ veoma korisne informacĳe o ispravnosti programa, iako ne u potpunosti precizne. Preciznost može da bude narušena na dva načina. Alat može da ima
Slika 3.3: Logo alata Isabelle (https://isabelle.in. tum.de/)
Rocq je interaktivni dokazivač teorema, odnosno pomoćnik za dokazivanje. On omogućava pisanje matematičkih dokaza i formalnih specifikacĳa, tj. pisanje programa i dokaza da programi ispunjavaju svoje specifikacije. Rocq je ranĳe bio poznat kao Coq Proof Assistant. Pod tim imenom je 2013. godine dobio ACM Software System Award kao i ACM SIGPLAN Programming Languages Software Award, dve najprestižnĳe nagrade koje softver može da dobĳe.
-lažna upozorenja — da prĳavljuje problem koji u realnom izvršavanju ne može da se desi,
-propuštene greške — da ne prĳavljuje problem koji u realnom izvršavanju može da se desi.
‗ Alan Turing, On Computable Numbers With an Application to the Entscheidungsproblem, Proceedings of the London Mathematical Society, 1936.

<!-- pdf_page=57 printed_page=3 -->

Automatski pristupi obično teže da imaju ili samo lažna upozorenja, ili samo propuštene greške — kombinovanje lažnih upozorenja sa propuštenim greškama čini alat praktično nepoželjnim.
Statička verifikacĳa softvera je vremenski veoma zahtevna. Primer upotrebe paralelizacĳe sa ciljem poboljšanja efikasnosti statičke verifikacĳe može se videti u master radu Branislave Živković: Paralelizacĳa statičke verifikacĳe softvera
Takođe, prilikom izgradnje automatskog alata za ispitivanje ispravnosti često se pravi kompromis između preciznosti i efikasnosti. Efikasni alati najčešće nisu precizni, dok precizni alati nisu efikasni.
U automatsku statičku analizu se ubrajaju:
-simboličko izvršavanje, -proveravanje modela i -apstraktna interpretacĳa.
Pored alata za automatsko otkrivanje grešaka u programima, formalne metode verifikacĳe softvera obuhvataju i tehnike razvoja ispravnog softvera. Generisanje koda direktno iz specifikacĳe i formalno dokazivanje ispravnosti softvera koji se razvĳa predstavljaju najviši nivo sigurnosti u ispravnost softvera. Ovo je ujedno i najskuplji razvoj softvera i zahteva visoko stručne ljude i upotrebu posebnih alata, kao što su npr Rocq (slika 3.2) i Isabelle (slika 3.3). Iako ovakav razvoj softvera vodi najpouzdanĳem softveru, on je ujedno i najskuplji i najsporĳi pa se u industrĳi najčešće koristi samo za razvoj kritičnih delova koda.
Rezime
-Obezbeđivanje i kontrola kvaliteta softvera obuhvataju validacĳu i verifikacĳu softvera.
-Validacĳa softvera obuhvata sve procese koji su potrebni da se osigura da definisana specifikacĳa softvera zadovoljava korisničke potrebe.
-Verifikacĳa softvera obuhvata sve procese koji su potrebni da se osigura da razvĳeni softver zadovoljava zadatu specifikacĳu.
-I verifikacĳa i validacĳa su od suštinske važnosti za kvalitet softvera.

<!-- pdf_page=58 printed_page=44 -->

-Verifikacĳa softvera može da bude dinamička i statička.
-Dinamička verifikacĳa softvera se oslanja pre svega na testiranje, ali testiranje ne može da garantuje ispravnost softvera.
-Statička verifikacĳa softvera uključuje ljudske preglede koda i formalne metode.
-Automatska statička verifikacĳa: neophodni su kompromisi između preciznosti i efikasnosti.
-Razvoj direktno iz specifikacĳe i formalno dokazivanje ispravnosti softvera koristi se za razvoj kritičnih delova aplikacĳa.
Literatura
[1] Paul Ammann i Jeff Offutt. Introduction to Software Testing. Cambridge University Press, 2017. doi:
10.1017/9781316771273.
[2] Antonia Bertolino. Software Testing Research: Achievements, Challenges, Dreams. 2007., str. 85–103. doi: 10.1109/FOSE.2007.25.
[3] Edmund M. Clarke, Orna Grumberg i Doron A. Peled. Model Checking. MIT Press, 1999. isbn: 9780262032704.
[4] Glenford J. Myers, Corey Sandler i Tom Badgett. The Art of Software Testing. 3. izdanje. Wiley, 2011. isbn: 9781118031964.
[5] Doron Peled. Software Reliability Methods. Springer, 2001. doi: 10.1007/978-1-4757-3540-6.
Ispitna pitanja
8. Odnos verifikacĳe i validacĳe softvera. Primeri. 9. Tehnike verifikacĳe softvera. Osnovna podela. Mogućnosti dinamičkog i statičkog pristupa verifikacĳi softvera.

<!-- pdf_page=59 printed_page=59 -->

Dinamička verifikacija softvera

<!-- pdf_page=61 printed_page=61 -->

Pregled
4.1 Testiranje i razvoj softvera . 47
-Koja je uloga testiranja u procesu razvoja softvera? -Koje vrste testiranja postoje — šta se proverava? -Koje tehnike testiranja postoje — kako napraviti dobre test primere?
4.2 Vrste i nivoi testiranja . . . . 62
4.3 Tehnike testiranja . . . . . . . . 86
-Koji načini sprovođenja testiranja postoje — kada koristiti manuelno, a kada automatsko testiranje?
4.4 Načini sprovođenja testiranja . . 120
Dinamička verifikacĳa softvera predstavlja skup metoda i tehnika kojima se proverava ispravnost softverskog sistema tokom njegovog izvršavanja. Među tim tehnikama, najčešće primenjivana, i svakako najrasprostranjenija forma verifikacĳe uopšte, jeste testiranje. Testiranje se ogleda u kontrolisanom pokretanju softvera uz korišćenje unapred definisanih skupova ulaznih podataka, pri čemu se pažljivo prati njegovo ponašanje i upoređuje sa očekivanim ishodima.
Kada se testiranje sprovodi na pravilan i sistematičan način, ono može u velikoj meri doprineti unapređenju kvaliteta softverskog proizvoda. Razumevanje toga kako, kada i zašto testirati omogućava ne samo efikasnije otkrivanje grešaka, već i oblikovanje procesa razvoja softvera tako da se od samog početka teži visokom kvalitetu konačnog rešenja. Iz tih razloga, od suštinske je važnosti da svi koji učestvuju u razvoju softvera poseduju znanje o metodologĳi testiranja, kao i o njegovim procesima i osnovnim principima.
### 4.1 Testiranje i razvoj softvera
Softver nastaje kao odgovor na jasno definisane zahteve korisnika, koji precizno određuju šta softver treba da

<!-- pdf_page=62 printed_page=48 -->

radi, na koji način treba da funkcioniše, u kojim uslovima, koje potrebe korisnika treba da zadovolji i kako treba da ostvaruje interakcĳu sa krajnjim korisnikom. Svako odstupanje softvera od ovih zahteva smatra se defektom. Defekti su neposredna posledica ljudskih grešaka napravljenih u različitim fazama razvoja softvera — od analize i dizajna, preko implementacĳe, pa sve do testiranja i održavanja.
Testiranje softvera predstavlja sistematsku aktivnost u okviru životnog ciklusa razvoja, koja ima za cilj da otkrĳe defekte pre nego što softver dospe u ruke krajnjih korisnika. Osim što doprinosi identifikacĳi i ispravljanju defekata, testiranje takođe pomaže u proceni pouzdanosti, performansi i ukupne stabilnosti softverskog proizvoda. Na taj način, ono igra ključnu ulogu u postizanju visokog kvaliteta i korisničkog zadovoljstva.
4.1.1 Cena greške u kontekstu vremena otkrivanja
U savremenom razvoju softvera, osnovni cilj organizacĳa i razvojnih timova jeste postizanje maksimalnog profita kroz isporuku proizvoda visokog kvaliteta, ali istovremeno uz poštovanje vremenskih rokova i budžetskih ograničenja. Upravo iz tog razloga, metode i pristupi koji omogućavaju bržu, efikasnĳu i pouzdanĳu isporuku softverskih rešenja postaju sve važnĳi.
Slika 4.1: Edger Dĳkstra (eng. Edsger Dĳkstra)a, dobitnik Tjuringove nagrade 1972. godine:
”Program testing can show the presence of bugs, never their absence”
Faze razvoja softvera su organizovane prema metodologĳi koja se koristi za upravljanje razvojem softverskog projekta, a osnovne faze se javljaju u svim modelima razvoja. Osnovne faze razvoja softvera uključuju analizu zahteva, dizajn i implementacĳu softvera, razne vrste testiranja i upotrebu softvera. Najzastupljenĳe i trenutno najpopularnĳe su agilne metodologĳe razvoja softvera (npr. Scrum, Kanban, Extreme Programming). One se zasnivaju na iterativnom pristupu koji podrazumeva paralelno razvĳanje i testiranje softverskih komponenti. Umesto da se testiranje odlaže za kraj procesa (kao što je
Testiranje može da potvrdi prisustvo grešaka u softveru — testiranje ne može da dokaže ispravnost softvera.
a Fotografiju je napravio Hamilton Richards. Fotografija je dostupna pod licencom Creative Commons AttributionShare Alike 3.0

<!-- pdf_page=63 printed_page=4 -->

to slučaj u tradicionalnim pristupima razvoju softvera), ono se integriše u svaku fazu razvoja: svaka funkcionalna celina se implementira i istovremeno proverava testovima, čime se omogućava brza povratna informacija i pravovremeno otkrivanje defekata.
Savremeni pristupi razvoju softvera obuhvataju i razvoj vođen ponašanjem. Razvoj vođen ponašanjem omogućava jasnu definicĳu poslovnih zahteva, poboljšava komunikacĳu između razvojnih i poslovnih timova i doprinosi unapređenju kvaliteta i pouzdanosti softverskih sistema. Primer razvoja vođenog ponašanjem može se videti u master tezi Veronike Marinković: Razvoj vođen ponašanjem kroz primenu alata Cucumber
Kako složenost softverskih sistema raste, proporcionalno raste i značaj testiranja. Greške koje promaknu u ranim fazama razvoja mogu da izazovu lančane probleme, koji ne samo da komplikuju završne faze projekta, već u krajnjem slučaju mogu dovesti i do potpunog neuspeha proizvoda.
Zbog toga je od suštinskog značaja da se sve greške otkrĳu što ranĳe u životnom ciklusu softvera. Ispravljanje grešaka u početnim fazama razvoja je znatno brže, jednostavnĳe i jeftinĳe u poređenju sa otklanjanjem grešaka u kasnĳim fazama. To je povezano i sa brojem ljudi koje je potrebno uključiti u proces ispravljanja greške, a koji zavisi od faze razvoja softvera u kojoj se greška pronađe:
Faza analize zahteva. Greška zahteva revizĳu definisanih zahteva. Trošak uključuje dodatno vreme analitičara.
Faza dizajna softvera. Ispravka greške podrazumeva izmenu dizajna, što zahteva dodatni rad dizajnera i ažuriranje opisa implementacĳe.
Faza implementacĳe softvera. Greške otkrivene tokom kodiranja obično programer brzo ispravi. Cena zavisi od složenosti, ali je niža ako programer sam pronađe grešku. U okviru implementacĳa softvera, posebno je bitna faza integracĳe komponenti, koja obuhvata sklapanje različitih softverskih komponenti u veće celine. Greške su u ovoj fazi teže za otkrivanje jer uključuju više različitih delova softverskog sistema. Ispravka zahteva saradnju više članova tima i potencĳalno različitih razvojnih timova pa samim tim i više vremena za analizu uzroka, što utiče i na to da je ispravljanje greške skuplje.

<!-- pdf_page=64 printed_page=50 -->

Faza sistemskog testiranja. Cena greške otkrivene u ovoj fazi uključuje rad tima zaduženog za kvalitet softvera, prĳavu greške, komunikacĳu sa programerima, ponovna testiranja i praćenje kroz sistem za praćenje defekata. Ukoliko u procesu razvoja softvera postoji korak testiranja prihvatljivosti softvera, cena greške dodatno obuhvata i rad kupca odnosno korisnika koji vrši proveru da li je softver prihvatljiv. Korisnički otkrivene greške zahtevaju dodatnu koordinacĳu sa timom zaduženim za kvalitet softvera i povratnu integracĳu ispravki. Trošak uključuje vreme korisnika i produžava završne faze projekta.
Faza upotrebe. Greške u produkcĳi imaju najveću cenu. Pored tehničke ispravke, dolazi do gubitka poverenja korisnika i potencĳalne reputacione štete.
4.1.2 Uloga testera u razvoju softvera
Projekti u oblasti razvoja softvera mogu se voditi na najrazličitĳe načine. Briga o kvalitetu softvera podrazumeva primenu različitih pravila, procedura i praksi, koje zavise kako od vrste projekta, tako i od zrelosti i veličine same kompanĳe. U nekim slučajevima kvalitet softvera je odgovornost razvojnog tima, dok u drugim postoji posebno definisan tim zadužen za ovu oblast.
Tim za obezbeđenje kvaliteta softvera može postojati kao zasebna organizaciona jedinica unutar kompanĳe koja razvĳa softver (interni tim), ili može biti eksterno angažovan od strane specĳalizovane firme koja pruža usluge testiranja i kontrole kvaliteta. U nekim kompanijama, posebno u manjim i manje formalnim okruženjima, ovakav tim uopšte ne postoji, a aktivnosti testiranja programeri obavljaju ad-hoc.
Tester softvera (eng. software tester) ili jednostavno tester je stručnjak koji se bavi planiranjem, izvođenjem i dokumentovanjem aktivnosti testiranja softverskog sistema, sa ciljem da se obezbedi očekivani kvalitet proizvoda.

<!-- pdf_page=65 printed_page=4 -->

Njegov osnovni zadatak jeste sistematsko ispitivanje softvera kako bi se identifikovali defekti u funkcionisanju, performansama ili upotrebljivosti.
Raspodela obaveza između programera i testera u timovima može biti organizovana na različite načine:
-programeri su istovremeno i testeri i sami proveravaju svoj kôd,
-programeri i testeri rade zajedno u istom timu, blisko sarađujući,
-programeri i testeri čine potpuno odvojene timove sa jasnim razgraničenjem odgovornosti.
Iako je kvalitetan softver krajnji cilj i programera i testera, često postoji veliki broj problema na relacĳi programer — tester onda kada su programeri i testeri u razdvojenim timovima. Problemi su u lošoj komunikacĳi, međusobnom nerazumevanju i opštoj netrpeljivosti. Ovi problemi su najčešće posledica psihološke reakcĳe na pronalaženje greške u softveru. Pronalaženje greške u softveru testeru označava da je uspešno obavio svoj zadatak, dok programeru to znači da nĳe uspešno obavio svoj posao i da je potrebno ponovo da radi na nekom delu koda za koji je verovao da je završen (slika 4.2).
Slika 4.2: Osnovni razlog neslaganja testera i programera.
Da bi se osoba bavila testiranjem potrebno je da poseduje osnovno razumevanje programiranja i procesa razvoja softvera. Posebno, mora da detaljno poznaje procedure i proces testiranja kao i alate koji se koriste u testiranju. Za efikasnu implementacĳu i automatizaciju testiranja neophodno je i poznavanje skript jezika i skript programiranja.
Dobri testeri su kreativni i imaju potrebu za stalnim usavršavanjem, a vremenom upoznaju i česte greške i propuste kao i nesvakidašnje slučajeve upotrebe, što značajno olakšava i ubrzava proces testiranja. Za poslove testiranja još uvek je dominantna neformalna edukacija kroz kurseve, konferencĳe i sastanke profesionalnih udruženja. Za napredne poslove automatizacĳe u testiranju neophodne su napredne programerske veštine.

<!-- pdf_page=66 printed_page=52 -->

4.1.3 Faze testiranja softvera
Za početak procesa testiranja, postojanje koda nĳe neophodno. Dovoljno je imati jasno definisane zahteve korisnika jer priprema za testiranje počinje analizom tih zahteva. Dakle, da bi se započeli procesi vezani za testiranje, potrebno je da postoji specifikacĳa zahteva sistema (eng. system requirements specification) kao i specifikacĳa zahteva softvera (eng. software requirements specification).
Testiranje softvera se u opštem slučaju sastoji od narednih faza, pri čemu svaka faza obuhvata veliki broj aktivnosti.
1. Planiranje testiranja
2. Analiza, dizajn i implementacĳa testova 3. Izvršavanje testova 4. Evaluacĳa testova 5. Zatvaranje testiranja
Ove faze se usklađuju sa metodologĳom razvoja softvera tako da se u okviru iterativnih modela razvoja izvršavaju iterativno.
Planiranje testiranja
Planiranje definiše:
-potrebne vrste testova,
Planiranje testiranja (eng. test planning) predstavlja pripremu za proces testiranja. Plan testiranja se prilagođava svakom konkretnom projektu.
-tehnike testiranja koje će se koristiti,
-načine sprovođenja testiranja,
Planiranje testiranja započinje analizom zahteva, pri čemu se detaljno razmatraju svi funkcionalni i nefunkcionalni aspekti sistema. Na osnovu te analize definišu se ciljevi testiranja, odnosno šta se želi postići samim testiranjem. Sledeći korak obuhvata određivanje opsega testiranja, uključujući odluku o tome koje će komponente softvera biti testirane i koliko. Dodatno, određuju se i načini testiranja: koji će delovi testiranja biti sprovedeni ručno, a koji automatizovano, uključujući i alate koji će
-opseg testiranja, -ulazne i izlazne kriterĳume, posebno kriterĳum završetka,
-potrebne resurse, -procenu rizika, -metodologĳu praćenja defekata i
-uloge i način komunikacĳe između članova tima.

<!-- pdf_page=67 printed_page=4 -->

biti korišćeni tokom testiranja. Planiranje takođe uključuje precizno definisanje uloga i odgovornosti članova tima.
Praćenje projekata i defekata Jira https://www.
Važan deo planiranja je i procena rizika, koja uključuje identifikacĳu potencĳalnih problema i njihov uticaj na kvalitet proizvoda. Vremenski okvir testiranja se takođe detaljno planira, uz jasno definisane ulazne i izlazne kriterĳume koji određuju kada testiranje može da počne i pod kojim uslovima se smatra završenim. Konačno, planiranje uključuje pripremu test okruženja, odnosno obezbeđivanje potrebnog hardverskog i softverskog okruženja neophodnog za efikasno i pouzdano izvođenje testova.
atlassian.com/software/
jira je komercĳalna platforma za upravljanje projektima, koja se često koristi u okviru agilnog razvoja softvera. Bugzilla https://www.
bugzilla.org/ je besplatan alat otvorenog koda, specĳalizovan za praćenje grešaka i upravljanje defektima.
Neizostavan deo plana je i metodologĳa za praćenje defekata, koja precizno definiše kako se greške prĳavljuju, dokumentuju, prate tokom životnog ciklusa i na kraju zatvaraju, čime se obezbeđuje kontrola kvaliteta i transparentnost celokupnog procesa testiranja.
Analiza, dizajn i implementacĳa testova
Analiza, dizajn i implementacĳa testova (eng. test analysis, design and implementation) predstavljaju ključne faze u okviru procesa testiranja softverskih sistema. Ove aktivnosti podrazumevaju sistematski pristup u osmišljavanju načina na koji će se sprovesti testiranje, u skladu sa prethodno definisanim test planom.
Jedan od najbitnĳih rezultata ovih faza je koherentan i sveobuhvatan skup test slučajeva i procedura koji služe kao temelj za uspešno sprovođenje testiranja i verifikacĳu ispravnosti softverskog rešenja. Test slučaj (eng. test case) predstavlja formalni dokument koji opisuje određenu situacĳu testiranja kroz definisani skup ulaznih podataka i očekivane izlaze sistema. Svaki test slučaj ima za cilj da proveri konkretnu funkcionalnost softvera, njegovo ponašanje u graničnim uslovima ili otpornost na nevalidne ili neočekivane ulaze. Procedura testiranja

<!-- pdf_page=68 printed_page=54 -->

(eng. test procedure) definiše tačan redosled i način primene test slučajeva u kontrolisanom okruženju. Testni okvir, testno okruženje ili infrastruktura za testiranje (eng. test harness) je skup skripti, alata i konfiguracĳa koji omogućavaju automatsko pokretanje testova, simulacĳu realnog upotrebnog okruženja i prikupljanje rezultata. Poređenje ovih pojmova je dato u tabeli 4.1.
Tabela 4.1: Poređenje: test slučaj, procedura testiranja i testni okvir
Pojam Opis
Test slučaj (test) Konkretna situacĳa koja se testira, sa definisanim ulazima i očekivanim izlazima. Procedura testiranja Skup jasno definisanih koraka koji opisuju kako se jedan ili više test slučajeva izvršavaju u praktičnom okruženju. Testni okvir Skup alata i infrastrukture koji omogućavaju automatsko izvršavanje testova, simulacĳu delova sistema i prikupljanje rezultata testiranja.
faze testiranja
U fazi analize testova, vrši se detaljno ispitivanje mogućnosti testiranja pojedinih delova softverskog sistema i identifikacĳu zahteva koje sistem mora da ispuni. Ovaj proces podrazumeva detaljno razlaganje korisničkih priča (eng. user story), upotrebnih scenarĳa (eng. use cases) i tehničke dokumentacĳe, kako bi se identifikovali svi elementi koji mogu i treba da budu predmet testiranja. Kroz identifikacĳu zavisnosti, ograničenja i potencĳalnih rizika, analiza testova gradi detaljnu mapu puta koji vodi ka dizajnu testova i njihovom kasnĳem izvršavanju. Time se obezbeđuje sveobuhvatna pokrivenost svih relevantnih aspekata softverskog sistema.
planiranje testiranja
analiza, dizajn i implementacĳa testova
izvršavanje testova
evaluacĳa testova
zatvaranje testiranja
Primer 4.1.1 (Aplikacĳa za elektronsko bankarstvo) Razmotrimo projekat razvoja aplikacĳe za elektronsko bankarstvo. Tokom faze analize testova, testeri analiziraju funkcionalne zahteve sistema. Jedan od njih je i
Korisnici treba da mogu da prenose novac između računa.

<!-- pdf_page=69 printed_page=4 -->

Na osnovu ovog zahteva, identifikuju se različiti scenarĳi testiranja, kao što su:
-Prenos novca između računa u istoj banci -Prenos ka računima u drugim bankama -Testiranje granica – npr. minimalni i maksimalni iznos za prenos
Pored toga, identifikuju se i granični slučajevi (eng. edge cases), kao što su:
-Pokušaj prenosa novca kada korisnik nema dovoljno sredstava na računu
-Pokušaj ponovljenog prenosa usled pada mreže -Neispravno unet broj računa primaoca
Svi ovi identifikovani scenarĳi biće u narednim fazama formalizovani u test slučajeve, čime se obezbeđuje da funkcionalnost prenosa novca bude testirana u celosti — sa aspekta tačnosti, pouzdanosti i bezbednosti. Na ovaj način, analiza testova ne samo da razbĳa kompleksne zahteve na razumljive i proverljive jedinice, već i postavlja temelj za kvalitetan dizajn i izvršavanje testova, koji direktno doprinosi uspešnosti krajnjeg softverskog proizvoda.
Analiza, dizajn i implementacĳa testova: Faza analize testova daje odgovor na pitanje „šta testirati?”. Faza dizajna testova daje odgovor na pitanje „kako testirati?”. Faza implementacĳe daje sve što je potrebno da testiranje može da počne.
Faza dizajna testova sledi nakon analize i predstavlja temelj za dalji tok testiranja. U ovoj fazi definišu se ciljevi testiranja, identifikuju funkcionalnosti koje treba proveriti i preciziraju uslovi pod kojima će testovi biti sprovedeni. Identifikovani scenarĳi se razrađuju u test slučajeve i prateću dokumentacĳu (eng. testware), čime se obezbeđuje jasan i sistematičan pristup. Ključne aktivnosti u okviru dizajna testova obuhvataju:
-kreiranje i prioritizacĳu test slučajeva, -identifikacĳu potrebnih test podataka, -preciziranje testnog okruženja, uključujući potrebnu infrastrukturu i alate.
Cilj ove faze je da se obezbedi dosledna i kvalitetna osnova za kasnĳu implementacĳu i izvršavanje testo-

<!-- pdf_page=70 printed_page=56 -->

va.
Primer 4.1.2 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.1.1) Razmotrimo identifikovan scenario testiranja:
Pokušaj prenosa novca kada korisnik nema dovoljno sredstava na računu.
U fazi dizajna testova, za ovaj scenario, može se identifikovati naredni skup test slučajeva:
1. Apsolutno nedovoljno sredstava Korisnik ima 0 RSD na računu, a pokušava da prenese npr. 1000 RSD. Očekivanje: Transakcĳa odbĳena; jasna poruka o nedostatku sredstava.
2. Delimično pokrivanje iznosa Korisnik ima 500 RSD na računu, a pokušava da prenese 1000 RSD. Očekivanje: Transakcĳa odbĳena; jasna poruka o nedostatku sredstava, ali potrebno je testirati i prikaz informacĳa o preostalom saldu i sugestĳu da se izvrši prenos manjeg iznosa.
3. Nedovoljno sredstava zbog provizĳe Korisnik ima dovoljno novca na računu, ali se naplaćuje provizĳa za prenos. Očekivanje: Transakcĳa odbĳena uz poruku o dodatnoj provizĳi.
4. Nedovoljno sredstava zbog rezervacĳe sredstava Na računu piše da ima dovoljno sredstava, npr. 1000 RSD, ali je deo sredstava rezervisan, npr. 800 RSD. Očekivanje: Efektivno dostupno stanje je 200 RSD; prenos većeg iznosa treba da bude odbijen.
5. Nedovoljno sredstava u drugoj valuti Račun je u dinarima, a korisnik pokušava prenos

<!-- pdf_page=71 printed_page=4 -->

u evrima. Nakon konverzĳe, stanje nĳe dovoljno. Očekivanje: Sistem treba da prikaže da konvertovani iznos nĳe dovoljan.
6. Ponovljeni pokušaji prenosa bez sredstava Višestruki pokušaji prenosa istog iznosa bez pokrića. Očekivanje: Sistem blokira pokušaje, potencĳalno uvodi vremensko ograničenje ili detekcĳu zloupotrebe.
Dodatno, potrebno je precizirati sve identifikovane test slučajeve. Na primer, test slučaj za prenos novca u slučaju delimičnog pokrivanja iznosa je dat u okviru primera 4.2.3.
Ove test slučajeve može da izvršava tester, po zadatim koracima, a može se i napisati skript koji automatizuje njihovo izvršavanje i simulira sve korisničke korake. Ukoliko je predviđeno da se testovi izvršavaju automatizovano, u fazi implementacĳe obezbeđuje se kôd koji je potreban za njihovo izvršavanje.
U višegodišnjim projektima koje razvĳa veliki broj nezavisnih timova često se javljaju redudantni testovi. Oni otežavaju održavanje testne infrastrukture i produžavaju vreme potrebno za sprovođenje testiranja. Primer detekcĳe i uklanjanja redundantnih testova može se videti u master tezi Irene Blagojević: Automatsko uklanjanje redundantnih testova
Faza implementacĳe testova predstavlja završni korak u pripremi za izvršavanje testiranja. U ovoj fazi dolazi do konkretizacĳe prethodno dizajniranih test slučajeva kroz njihovo organizovanje u procedure testiranja, kao i pripreme potrebne testne dokumentacĳe, alata i okruženja. Cilj implementacĳe je da obezbedi doslednost, ponovljivost i tehničku spremnost za efikasno izvršavanje testova.
Ključne aktivnosti koje se sprovode tokom implementacĳe testova uključuju:
-Razvoj procedura testiranja i razvoj test okvira — omogućava strukturisano i, gde je primenljivo, automatizovano izvršavanje test slučajeva.
-Formiranje test kompleta (eng. test suites) grupisanjem povezanih procedura i skripti — radi lakše organizacĳe i povećanja efikasnosti tokom

<!-- pdf_page=72 printed_page=58 -->

izvršavanja.
-Raspoređivanje test kompleta u plan izvršavanja — u skladu sa raspoloživim resursima i prioritetima.
-Pripremu test podataka i proveru njihove integracĳe u okruženje — kako bi se obezbedila validnost ulaza i pouzdanost rezultata testiranja.
Na ovaj način, implementacĳa testova zatvara krug pripremnih aktivnosti i postavlja temelj za sledeću fazu — sâmo izvršavanje testiranja.
Primer 4.1.3 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.1.2) Naziv test procedure: Testiranje prenosa sredstava u uslovima nedovoljnog stanja na računu
Opis: Ova test procedura pokriva slučajeve kada korisnik pokušava da izvrši prenos novca, ali na računu nema dovoljno sredstava za realizacĳu transakcĳe. Cilj je da se verifikuje ispravno ponašanje sistema u različitim varĳacĳama ovog problema, uključujući osnovni nedostatak sredstava, rezervacĳe, provizĳe i valute.
Preduslovi:
-Korisnički nalog je kreiran i verifikovan. -Korisnik ima pristup elektronskom bankarstvu. -Test račun je aktivan i koristi dinarsku valutu (RSD).
-Testno okruženje koristi realne validacione mehanizme.
Koraci:
Test slučaj 1: Apsolutno nedovoljno sredstava Test slučaj 2: Delimično pokrivanje iznosa Test slučaj 3: Nedovoljno sredstava zbog provizĳe Test slučaj 4: Nedovoljno sredstava zbog rezervisanih sredstava

<!-- pdf_page=73 printed_page=4 -->

Test slučaj 5: Nedovoljno sredstava u drugoj valuti
Završni uslovi:
-Sve test transakcĳe treba da budu evidentirane u log fajlovima.
-Nĳe dozvoljena promena stvarnog salda korisnika.
-Sistem mora prikazati odgovarajuće poruke greške.
Primetimo da test slučaj vezan za ponovne uzastopne pokušaje podizanja novca kada na računu nema dovoljno sredstava može takođe da se uvrsti u ovu proceduru testiranja ili da se grupiše u drugu proceduru testiranja, na primer, u neku koja se odnosi na sigurnost sistema.
Izvršavanje testova
faze testiranja
Izvršavanje testova (eng. test execution) predstavlja fazu u kojoj se praktično primenjuju test slučajevi i test procedure razvĳene tokom prethodnih faza. Testovi se mogu sprovoditi ručno – kada tester sam prati korake iz test slučaja – ili automatski, korišćenjem specĳalizovanih alata koji omogućavaju bržu proveru funkcionalnosti.
planiranje testiranja
analiza, dizajn i implementacĳa testova
Prilikom testiranja, neophodna je organizacĳa testiranja kako bi se testovi izvršavali u skladu sa prioritetima i efikasno, bez gubljenja resursa i vremena. To uključuje raspoređivanje testova, kontrolu test okruženja i praćenje napretka test aktivnosti.
izvršavanje testova
evaluacĳa testova
zatvaranje testiranja
Izvršavanje testova predstavlja ključni korak u proverenju funkcionalnosti sistema i verifikacĳi da softver ispunjava postavljene zahteve. Tokom ove faze, testovi se sistematski sprovode kako bi se otkrile greške, ali i kako bi se pratio trenutni status svih prethodno prĳavljenih problema. Dakle, pored samog testiranja, važan deo ove aktivnosti jeste praćenje i upravljanje greškama – to podrazumeva ne samo prĳavu otkrivenih problema,

<!-- pdf_page=74 printed_page=60 -->

već i njihovo kontinuirano praćenje, proveru ispravki i konačnu potvrdu da su greške uspešno otklonjene. Svaka korekcĳa zahteva ponovno izvršavanje relevantnih testova kako bi se osiguralo da popravka nĳe dovela do novih problema ili narušila postojeću funkcionalnost.
Ova faza testiranja zahteva intenzivnu i jasnu komunikacĳu između testera i programera. Bliska saradnja i razmena informacĳa omogućavaju bržu identifikacĳu uzroka grešaka, efikasnĳe rešavanje problema i osiguranje stabilnosti sistema u završnim fazama razvoja.
Evaluacĳa testova
faze testiranja
Evaluacĳa testova (eng. test evaluation) obuhvata procenu kriterĳuma završetka testiranja i izveštavanje. Svaka izmena u kodu, čak i koja podrazumeva popravljanje grešaka, može da dovede do novih grešaka. Iz tog razloga se, za različite oblasti testiranja, definiše kriterĳum završetka testiranja u odnosu na rezultate izvršavanja testova, procenta nerešenih bagova ili preostalog vremena za testiranje. Proces evaluacĳa uključuje i pregled rezultata dobĳenih analizom izlaza test slučajeva.
planiranje testiranja
analiza, dizajn i implementacĳa testova
izvršavanje testova
Izlazni kriterĳumi (eng. exit criteria) određuju da li je testiranje kompletirano i da li je aplikacĳa spremna za korišćenje u skladu sa korisničkim zahtevima. Da bi se odredilo da li su izlazni kriterĳumi ispunjeni, potrebno je uzeti u obzir rezultate testiranja date kroz sažeti izveštaj testiranja (eng. test summary report), rezultate izračunavanja raznih metrika i izveštaj o defektima (eng. defect analysis report).
evaluacĳa testova
zatvaranje testiranja
Primer 4.1.4 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.1.3) Primer izlaznih kriterĳuma za elektronsko bankarstvo dat je u nastavku.
1. Pokrivenost testovima: 95% definisanih funkcionalnih i nefunkcionalnih zahteva mora biti po-

<!-- pdf_page=75 printed_page=4 -->

kriveno odgovarajućim test slučajevima.
2. Prolaznost test slučajeva: 100% kritičnih test slučajeva i najmanje 98% svih ostalih test slučajeva mora biti uspešno izvršeno.
3. Odsustvo kritičnih i visoko-prioritetnih grešaka:
Nisu dozvoljene greške koje utiču na osnovnu funkcionalnost sistema (npr. greške koje onemogućavaju prĳavu korisnika, pregled stanja računa, ili izvršavanje transakcĳa).
4. Potvrđena sigurnost sistema: Sigurnosne provere moraju potvrditi da sistem ne sadrži ranjivosti koje bi mogle dovesti do neautorizovanog pristupa, curenja podataka ili drugih sigurnosnih incidenata.
5. Stabilnost u test okruženju: Aplikacĳa mora stabilno funkcionisati tokom višednevnog testiranja bez rušenja, curenja memorĳe ili degradacĳe performansi.
6. Obezbeđena testna dokumentacĳa: Sva testna dokumentacĳa (test planovi, zapisnici o testiranju, rezultati testova, prĳave grešaka) mora biti ažurna i kompletna.
7. Odobrenje zainteresovanih strana: Tim za testiranje, razvoj, bezbednost i poslovni korisnici moraju formalno potvrditi da su svi zahtevi zadovoljeni i da je sistem spreman za dalji proces.
Zatvaranje testiranja
Zatvaranje testiranja označava završnu fazu test procesa, koja nastupa kada su svi planirani testovi sprovedeni i softver je isporučen krajnjem korisniku, bez daljih obaveza održavanja. Međutim, ovakva situacĳa je u praksi veoma retka, jer se nakon isporuke softvera gotovo uvek podrazumeva i njegovo održavanje, u okviru kog se testiranje i dalje sprovodi — u vidu provera ispravki, unapređenja funkcionalnosti ili novih verzĳa softvera.
Testiranje se može zatvoriti i u drugim okolnostima —

<!-- pdf_page=76 printed_page=62 -->

na primer, u slučaju da je projekat otkazan, ako su ciljevi testiranja ostvareni ranĳe nego što je planirano, ili ako nema više smisla nastavljati testiranje zbog promene poslovnih prioriteta.
faze testiranja
Tokom faze zatvaranja testiranja, vrši se arhiviranje test slučajeva, izveštaja i prateće dokumentacĳe, čime se omogućava budući uvid u realizovane aktivnosti. Istovremeno, sprovodi se analiza samog procesa testiranja, uz identifikacĳu onih praksi koje su se pokazale uspešnima i koje bi trebalo zadržati i primeniti u budućim projektima.
planiranje testiranja
analiza, dizajn i implementacĳa testova
Podjednako je važno prepoznati i aspekte koji nisu funkcionisali dobro, kako bi se greške iz prošlosti izbegle i unapredila efikasnost testiranja u narednim iteracĳama. Na taj način, zatvaranje testiranja ne označava samo kraj jedne faze, već i priliku za učenje i stalno poboljšanje procesa.
izvršavanje testova
evaluacĳa testova
zatvaranje testiranja
### 4.2 Vrste i nivoi testiranja
Testiranje softvera može se klasifikovati na više načina, u zavisnosti od cilja, obima i nivoa na kojem se testiranje sprovodi. Osnovna podela testiranja odnosi se na prirodu osobina koje se proveravaju, pa razlikujemo:
Testiranje funkcionalnih karakteristika usmereno je na proveru da li aplikacĳa pravilno izvršava funkcĳe definisane specifikacĳom zahteva. Ova vrsta testiranja ispituje ponašanje sistema u odnosu na očekivane ulaze i izlaze.
Testiranje nefunkcionalnih karakteristika usmereno je na tehničke i kvalitativne aspekte sistema, kao što su performanse, sigurnost, upotrebljivost, kompatibilnost i pouzdanost.
Druga bitna podela je podela po nivoima testiranja (slika 4.3). Mogu se testirati
-osnovne jedinice koda,

<!-- pdf_page=77 printed_page=4 -->

-pojedinačni moduli, -grupe modula (vezanih namenom, upotrebom, ponašanjem ili strukturom) ili
-ceo sistem.
U skladu sa pomenutom podelom, prema nivou testiranja, razlikujemo testove jedinice koda, komponentne, integracione i sistemske testove. Na svakom nivou mogu se testirati funkcionalne i nefunkcionalne karakteristike softvera.
Testiranje
Komponentno
Integraciono
Sistemsko
testiranje
testiranje
testiranje
jedinica koda
Slika 4.3: Nivoi testiranja
Posebna vrsta testiranja koja se može javiti u okviru svakog nivoa je regresiono testiranje. Regresiono testiranje (eng. regression testing) predstavlja proces ponovnog izvršavanja prethodno uspešno završenih test slučajeva s ciljem da se proveri da li novouvedene izmene u softveru nisu nenamerno dovele do regresĳe, tj. narušile postojeću funkcionalnost sistema ili dovele do pada performansi. Regresiono testiranje se sprovodi uvek nakon ispravki grešaka, dodavanja novih funkcionalnosti i prilikom refaktorisanja koda.
4.2.1 Testiranje jedinica koda
Primeri izazova testiranja u funkcionalnim programskim jezicima mogu se videti u master tezi Ane Petrović:
Testiranje jedinica koda (eng. unit testing) predstavlja proveru ispravnosti najmanjih delova softverskog sistema koji se mogu nezavisno testirati. U zavisnosti od programske paradigme, jedinice koda mogu biti različite: u objektno orĳentisanom programiranju to su najčešće klase, u funkcionalnom programiranju funkcĳe,
Testiranje funkcionalnih programa na primeru aplikacĳe koja koristi jezike Elm i Eliksir

<!-- pdf_page=78 printed_page=64 -->

dok se u imperativnom programiranju obično testiraju procedure i pojedinačni moduli.
Ova vrsta testiranja omogućava detaljan uvid u ponašanje svake pojedinačne jedinice, čime se osigurava stabilna osnova za kasnĳu integracĳu u veće sisteme. 1008-1987 IEEE Standard for Software Unit Testing je standard koji definiše jedinično testiranje i koji postavlja smernice i preporuke za njegovo sprovođenje.
Jedna od ključnih prednosti testiranja jedinica koda jeste snažna podrška u alatima za automatsko izvršavanje i proveru rezultata rada testova, koji su često integrisani u savremena razvojna okruženja. Automatizacĳa ovih testova omogućava brzu i čestu proveru funkcionalnosti u toku razvoja.
Testiranje
jedinica koda
Cilj jediničnih testova je da se potvrdi da izolovani delovi koda funkcionišu u skladu sa očekivanjima. Kada jedinica koda komunicira sa spoljnim resursima, kao što su standardni ulaz, mreža, baze podataka ili fajl sistemi, ta komunikacĳa se u test okruženju zamenjuje fiksiranim (eng. mock) vrednostima. Isto važi i za komunikacĳu sa drugim klasama ili komponentama – sve se apstrahuje, kako bi se test fokusirao isključivo na ponašanje posmatrane jedinice. Dozvoljena je samo interakcĳa sa memorĳom.
Ove testove najčešće pišu sami programeri tokom razvoja, što omogućava brzo otkrivanje i otklanjanje grešaka. Ukoliko postoji problem unutar same jedinice koda, upravo ova faza testiranja treba da ga otkrĳe — pre nego što dođe do složenĳih i skupljih grešaka u kasnĳim fazama razvoja.
Primer 4.2.1 (Biblioteka unittest u jeziku Python) Funkcĳa saberi(a, b) je jednostavna funkcĳa koja vraća zbir dva broja i definisana je u modulu
matematika.py.
1 def saberi(a, b):

<!-- pdf_page=79 printed_page=4 -->

2 return a + b
Naredni kôd (datoteka test_matematika.py koja je u istom direktorĳumu sa datotekom matematika.py) sadrži jednostavan jedinični test za ovu funkcĳu.
1 import unittest
2 from matematika import saberi
3
4 class TestSaberi(unittest.TestCase):
5 def test_saberi_pozitivne(self):
6 self.assertEqual(saberi(2, 3), 5)
7
8 def test_saberi_negativne(self):
9 self.assertEqual(saberi(-1, -1), -2)
10
11 if __name__ == ’__main__’:
12 unittest.main()
Klasa TestSaberi nasleđuje klasu unittest.TestCase i sadrži dva testa:
-Jedan testira sabiranje pozitivnih brojeva. -Drugi testira sabiranje negativnih brojeva.
Funkcĳa assertEqual proverava da li je rezultat funkcĳe jednak očekivanoj vrednosti. Funkcĳa
1 unittest.main()
pokreće ove testove.
Test se pokreće iz komandne linĳe narednom naredbom
1 python test_matematika.py
Ako je sve ispravno, izlaz će izgledati ovako:
1 ..
2 -------------------------------------------------
3 Ran 2 tests in 0.001s
4
5 OK
4.2.2 Komponentno i integraciono testiranje
Komponentno testiranje (eng. component testing) prove-

<!-- pdf_page=80 printed_page=66 -->

rava ispravnost komponente. Komponenta je skup funkcionalno povezanih jedinica koda koje zajedno obavljaju jednu logičku celinu i imaju jasno definisan interfejs. Komponentno testiranje se obično sprovodi izolovano od ostatka sistema i odmah nakon razvoja komponente.
Iako se po načinu izvođenja komponentno testiranje često nadovezuje na jedinično testiranje, osnovna razlika je u nivou koji obuhvataju — dok jedinično testiranje proverava pojedinačne jedinice koda, komponentno testiranje se fokusira na veće celine koje sadrže više jedinica koda i njihovu međusobnu saradnju. Sama jedinica koda je u prethodnoj fazi testiranja izolovana u potpunosti od spoljašnjeg sistema, dok se sada isti princip izolacĳe primenjuje ali na nivou komponente. To znači da jedinice koda u okviru komponente komuniciraju međusobno, ali da je sama komponenta izolovana u komunikacĳi sa drugim komponentama i sa spoljašnjim sistemima.
Komponentno
testiranje
S obzirom da se u komponentnom testiranju integrišu osnovne jedinice koda, ovo je vrsta integracionog testiranja, tako da se često i ne izdvaja kao posebna vrsta testiranja. Pošto se odnosi na direktno spajanje jedinica koda, može se shvatiti i kao integraciono testiranje na najnižem nivou. U praksi, komponentno testiranje mogu obavljati i programeri i testeri, u zavisnosti od organizacĳe projekta i kompleksnosti testiranih komponenti.
Integraciono testiranje (eng. integration testing) predstavlja fazu u procesu testiranja u kojoj se proverava saradnja između više softverskih komponenti koje zajedno čine funkcionalne celine sistema. Integraciono testiranje ispituje ispravnost interfejsa i komunikacĳe među komponentama. Cilj ovog testiranja je da se utvrdi da li su veze između komponenti pravilno definisane i implementirane, odnosno da li različiti delovi sistema međusobno komuniciraju na način koji je predviđen specifikacĳom projekta. Na taj način proverava se funkcionalna ispravnost u kontekstu saradnje, a ne samo u izolacĳi.
Slika 4.4: Brava
Pretpostavimo da imamo bravu kao na slici 4.4. Ukoliko takva brava treba da se integriše sa kliznim vratima (vratima koja se pomeraju levo-desno, a ne naprednazad), bez obzira što su i brava i vrata ispravni, njihova integracĳa neće davati željene rezultate.

<!-- pdf_page=81 printed_page=4 -->

Integracioni testovi otkrivaju razne vrste problema, uključujući:
-nekompatibilnost podataka pri razmeni između modula,
-neusklađene formate, tipove ili protokole komunikacĳe,
-pogrešno tumačenje interfejsa ili očekivanih vrednosti,
-greške u redosledu izvršavanja aktivnosti.
Ove testove obično sprovode testeri, iako je u praksi česta saradnja sa programerima, naročito u složenim sistemima. Dobra praksa je da se integraciono testiranje sprovodi inkrementalno — kako se nove komponente razvĳaju i dodaju sistemu, tako se istovremeno proverava njihova integracĳa.
Integraciono
testiranje
Primer 4.2.2 (Realni brojevi) Dve softverske komponente, Aproksimacĳa i Optimizacĳa, vrše računanja sa realnim brojevima. Međutim, zbog nedovoljno precizne specifikacĳe, jedna komponenta koristi realne brojeve jednostruke tačnosti (float), dok druga koristi realne brojeve dvostruke tačnosti (double). Iako svaka od komponenti zasebno funkcioniše ispravno u okviru svojih testova, njihova integracĳa dovodi do neočekivanih odstupanja u rezultatima. Na primer, vrednost double d = 1234567.89; kada se prebaci u float postaje 1234567.875 što doprinosi nepreciznosti izračunavanja.
Upravo kroz integraciono testiranje, takva neusklađenost u tipovima podataka treba da se otkrĳe. Testovi bi trebalo da obuhvate međusobnu razmenu podataka između komponenti i da provere konzistentnost vrednosti, preciznost proračuna i stabilnost u radu. Kada se ovakva greška otkrĳe, neophodno je uskladiti podatkovne tipove kako bi se osigurala kompatibilnost komponenti i sprečile greške u računanju.

<!-- pdf_page=82 printed_page=68 -->

4.2.3 Sistemsko testiranje
Sistemsko testiranje (eng. system testing) obuhvata proveravanje sistema kao celine. Ispituje se da li je ponašanje sistema u skladu sa specifikacĳom zadatom od strane klijenta. Ovde se zahteva i potpun pristup svim delovima sistema, uključujući bazu podataka, ukoliko se koristi, pristup mreži i svim hardverskim delovima sistema.
Sistemsko
testiranje
Sistemsko testiranje uključuje i funkcionalne i nefunkcionalne aspekte sistema. U sistemsko testiranje se ubrajaju i istraživačko testiranje, testiranje prihvatljivosti i instalaciono testiranje.
sistemsko testiranje
funkcionalno testiranje
Funkcionalno sistemsko testiranje
nefunkcionalno testiranje
Funkcionalno sistemsko testiranje predstavlja proveru funkcionalnosti sistema u uslovima koji odgovaraju stvarnom korišćenju. Cilj funkcionalnog sistemskog testiranja je da se potvrdi da su sve očekivane funkcionalnosti sistema implementirane (funkcionalna potpunost), da svaka funkcionalnost pojedinačno radi u skladu sa zahtevima korisnika (funkcionalna ispravnost) kao i da su sve funkcionalnosti sistema prikladne (funkcionalna prikladnost). Ovo testiranje obuhvata provere ulaza, obrada i izlaza za različite funkcionalne scenarĳe, uključujući tipične, granične i nesvakidašnje slučajeve upotrebe. Dodatno, potrebno je evaluirati i ponašanje sistema u slučaju pogrešnih ili neočekivanih ulaza.
istraživačko testiranje
testiranje prihvaljtljivosti
instalaciono testiranje
Primer 4.2.3 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.1.4) Primer test slučaja za funkcionalno testiranje.
Naziv test slučaja: TC-002 — Prenos novca sa nedovoljno sredstava na računu — Delimično pokrivanje iznosa
Opis: Proverava da li aplikacĳa pravilno obrađuje

<!-- pdf_page=83 printed_page=4 -->

Testiranje bezbednosti
Testiranje sigurnosti
Funkcionalno testiranje
Testiranje upotrebljivosti
Testiranje prenosivosti
Nefunkcionalno testiranje
Istraživačko testiranje
Testiranje pouzdanosti
Testiranje kompatibilnosti
Sistemsko testiranje
Testiranje performansi
Testiranje konfiguracĳa
Testiranje kapaciteta
Instalaciono testiranje
Stres testiranje
Testiranje prihvatljivosti
Paralelno testiranje
Referentno testiranje
Pilot testiranje
Slika 4.5: Vrste sistemskog testiranja
pokušaj prenosa novca kada na korisničkom računu nema dovoljno sredstava.
Preduslovi:
-Korisnik je prĳavljen u aplikacĳu -Na računu korisnika nalazi se manje sredstava od iznosa koji želi da prenese (npr. stanje: 500 RSD)
-Primalac ima validan račun u sistemu

<!-- pdf_page=84 printed_page=70 -->

Test podaci:
-Iznos za prenos: 1000 RSD -Broj računa primaoca: 170-1234567890123-45
Koraci:
1. Prĳaviti se u aplikacĳu sa validnim korisničkim nalogom
2. Otvoriti sekcĳu „Prenos sredstava“ 3. Uneti iznos prenosa: 1000 RSD 4. Uneti broj računa primaoca 5. Kliknuti na dugme „Potvrdi prenos“
sistemsko testiranje
Očekivani rezultat:
-Sistem prikazuje poruku o grešci: „Nedovoljno sredstava na računu“
funkcionalno testiranje
-Sistem sugeriše prenos manje količine novca -Prenos se ne izvršava -Stanje na računu ostaje nepromenjeno
Stvarni rezultat: (popunjava se nakon izvršavanja testa)
Status: (PASS / FAIL – popunjava se nakon testiranja)
sistemsko testiranje
Uspešno funkcionalno testiranje potvrđuje da sistem zadovoljava svoje osnovne zahteve i da je spreman za naredne faze verifikacĳe, uključujući nefunkcionalna testiranja, istraživačko testiranje i konačno prihvatanje od strane krajnjih korisnika.
nefunkcionalno testiranje
performanse
Nefunkcionalno sistemsko testiranje
kompatibilnost
pouzdanost
Nefunkcionalno sistemsko testiranje obuhvata testiranje dinamičkih nefunkcionalnih aspekata sistema: performanse, kompatibilnost, pouzdanost, upotrebljivost, bezbednost, sigurnost i prenosivost. Testovi se sprovode za one aspekte kvaliteta softvera koji su za dati sistem prepoznati kao važni i koji su stoga precizirani specifikacĳom. Na primer,
upotrebljivost
bezbednost
sigurnost
prenosivost

<!-- pdf_page=85 printed_page=4 -->

Testovima performansi proverava se vremensko ponašanje aplikacĳe i njena upotreba resursa. Ova vrsta testiranja se fokusira na metrike kao što su vreme odgovora na zahteve, broj obrađenih zahteva u jedinici vremena, vreme obrade podataka, kao i iskorišćenost memorĳe i drugih sistemskih resursa. Sastavni deo testiranja performansi su i testovi kapaciteta, stresa i konfiguracĳe.
sistemsko testiranje
Testovima kapaciteta proverava se ponašanje sistema pri obradi velikih količina podataka. Posebna pažnja posvećuje se granicama sistema, tj. kako softver funkcioniše kada se približi maksimalnim kapacitetima definisanim u zahtevima.
nefunkcionalno testiranje
performanse
Stres testovima se proverava kako se sistem ponaša kada ga izložimo zahtevima izvan njegovog projektovanog kapaciteta, odnosno šta se dogodi kada sistem preopteretimo i kako se sistem oporavlja kada se opterećenje smanji.
kapacitet
stres
Testovima konfiguracĳe proverava se rad sistema u različitim hardverskim i softverskim okruženjima. Time se obezbeđuje da aplikacĳa funkcioniše stabilno bez obzira na konkretne kombinacĳe operativnih sistema, drajvera, baza podataka ili uređaja.
konfiguracĳa
Primer 4.2.4 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.2.3) Testovi kapaciteta su ključni za planiranje infrastrukture i predviđanje kapaciteta u rastu korisničke baze. Rezultati mogu ukazati na potrebu za horizontalnim skaliranjem ili optimizacĳom baze podataka. Naziv test slučaja: TC-C003 — Test kapaciteta
Cilj testa: Proceniti ponašanje sistema pri obradi velikog

<!-- pdf_page=86 printed_page=72 -->

broja korisničkih zahteva i velikih količina podataka u periodima maksimalnog opterećenja, kako bi se utvrdili granični kapaciteti sistema.
Scenario: Simulirati rad bankarskog sistema tokom vršnog opterećenja (npr. kraj meseca, isplata plata) kada veliki broj korisnika istovremeno koristi aplikacĳu za pregled stanja, prenose sredstava i uplate računa.
Uslovi testa:
-10.000 simultanih korisničkih sesĳa. -Svaka sesĳa izvršava niz standardnih operacĳa: prĳava, pregled stanja, prenos novca, uvid u istorĳu transakcĳa.
-Korišćenje stvarnog produkcionog okruženja ili njegove precizne simulacĳe.
-Baza podataka inicĳalizovana sa velikim brojem (npr. 1.000.000) korisnika.
Metrike koje se prate:
-Prosečno i maksimalno vreme odziva za ključne operacĳe.
-Percentili vremena odziva (npr. P50, P90, P95, P99)a.
-Iskorišćenost resursa (CPU, memorĳa, baza podataka).
-Broj uspešno izvršenih zahteva u sekundi. -Broj neuspešnih ili odbĳenih zahteva (greške, prekoračenja vremena ili kapaciteta).
Kriterĳum prolaznosti: Sistem mora podržati najmanje 8.000 istovremenih korisnika sa vremenom odziva manjim od 2 sekunde za sve ključne operacĳe. Maksimalni gubitak zahteva ne sme preći 0.05%.
a : Vrednost Pk predstavlja vreme ispod koga se završava 𝑘% zahteva (npr. P95 znači da se 95% zahteva izvršava brže od te vrednosti, dok preostalih 5% traje duže).

<!-- pdf_page=87 printed_page=4 -->

Testovima kompatibilnosti proverava se način na koji sistem komunicira sa spoljnim komponentama i sistemima. Ovaj vid testiranja uključuje ispitivanje koegzistencĳe (mogućnosti rada zajedno sa drugim softverima na istom sistemu) i interoperabilnosti (sposobnosti razmene podataka i funkcionalne saradnje sa drugim sistemima). Cilj je da se osigura da sistem može uspešno da funkcioniše u širem okruženju bez konflikata ili nekompatibilnosti.
sistemsko testiranje
Primer 4.2.5 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.2.4) Aplikacĳa mora da se izvršava stabilno i kada se istovremeno izvršavaju druge aplikacĳe.
nefunkcionalno testiranje
Naziv test slučaja: TC-K009 — Koegzistencĳa sa antivirusom, VPN klĳentom i upravljanjem lozinkama.
kompatibilnost
Opis: Proveriti da li elektronska bankarska aplikacĳa može da funkcioniše ispravno kada se izvršava paralelno sa drugim softverom instaliranim na korisnikovom uređaju, bez međusobnog negativnog uticaja.
Scenario: Korisnik koristi elektronsku bankarsku aplikacĳu dok su istovremeno aktivni drugi programi koji zahtevaju mrežnu komunikaciju i bezbednosne resurse, kao što su antivirus softver, VPN klĳent i aplikacĳe za upravljanje lozinkama.
Okruženje testa:
-OS: Windows 11 -Aktivni softveri:
• Antivirus: Kaspersky Internet Security • VPN: Cisco VPN • Password manager: Bitwarden
-Aplikacĳa pokrenuta u pregledaču Chrome

<!-- pdf_page=88 printed_page=74 -->

Uslovi testa:
-Pokrenuti sve navedene programe istovremeno sa aplikacĳom.
-Izvršiti osnovne funkcĳe u aplikacĳi: prijava, pregled računa, slanje novca, pristup izvodima.
-Posmatrati eventualne konflikte: zamrzavanja, gubitak mrežne konekcĳe, bezbednosna upozorenja, itd.
Metrike koje se prate:
-Broj zabeleženih konflikata između aplikacĳe i drugih programa
-Smanjenje performansi aplikacĳe u uslovima koegzistencĳe
-Broj korisničkih funkcionalnosti koje su otežano dostupne ili onemogućene
Kriterĳum prolaznosti: Bankarska aplikacĳa mora biti funkcionalna i stabilna tokom istovremenog rada sa drugim programima. Ne sme doći do prekida funkcionalnosti, gubitka podataka, ili problema sa bezbednosnim komponentama sistema. Maksimalno dozvoljen broj manjih vizuelnih ili funkcionalnih anomalĳa: 1.
Testovima pouzdanosti proverava se stabilnost softvera i sposobnost da funkcioniše bez grešaka tokom određenog vremenskog perioda, u realnim ili simuliranim uslovima rada. Na primer, proverava se da li softver može da radi bez prekida i padova tokom dužeg vremenskog korišćenja (stabilnost u radu, zrelost i dostupnost), ispituje se sposobnost sistema da se oporavi nakon što dođe do greške, bilo automatski ili uz minimalnu intervencĳu korisnika (oporavak od grešaka), softver se izvršava neprekidno tokom više sati ili dana (dugotrajno testiranje) da bi se otkrile skrivene greške (npr. curenje memorĳe, degradacĳa performansi)
sistemsko testiranje
nefunkcionalno testiranje
pouzdanost

<!-- pdf_page=89 printed_page=4 -->

i proverava se otpornost na promene okruženja, tj. kako sistem reaguje na promene u okruženju (npr. prekid mreže, promena konfiguracĳe).
Primer 4.2.6 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.2.5) Testovi pouzdanosti su važni za kritične sisteme kao što su bankarski, gde pouzdanost direktno utiče na poverenje korisnika i bezbednost podataka.
Naziv test slučaja: TC-P006 — Pouzdanost tokom 72h Opis: Proceniti sposobnost sistema da radi stabilno i bez prekida tokom produženog vremenskog perioda, u realnim uslovima korišćenja.
Scenario: Izvršavanje aplikacĳe u trajanju od 72 sata bez prekida, tokom kojih se konstantno generišu korisnički zahtevi (prĳave, pregledi računa, transferi sredstava, uplate računa), uz periodične simulacĳe grešaka i poremećaja u mrežnom okruženju.
Uslovi testa:
-Aplikacĳa se pokreće u testnom okruženju koje odgovara produkcionom.
-Koristi se alat za automatizacĳu koji kontinuirano šalje realistične zahteve sa različitih virtuelnih korisničkih naloga.
-Na svakih 12 sati se simulira greška u komunikacĳi sa bazom podataka, zatim oporavak.
-Prati se stabilnost sistema, ponašanje memorĳe i CPU-a, kao i sposobnost aplikacĳe da se automatski oporavi.
Metrike koje se prate:
-Broj sistemskih padova ili prekida rada.

<!-- pdf_page=90 printed_page=76 -->

-Vremensko trajanje oporavka posle greške. -Prisustvo curenja memorĳe ili degradacĳe performansi.
-Očuvanost tačnosti i konzistentnosti podataka.
Kriterĳum prolaznosti: Tokom 72 sata kontinuiranog rada ne sme doći do nĳednog sistemskog pada. Nakon svake simulirane greške, sistem mora da se oporavi u roku kraćem od 60 sekundi. Potrošnja memorĳe ne sme rasti progresivno bez oslobađanja (indikator curenja memorĳe). Podaci moraju biti konzistentni i odgovarati obavljenim transakcijama.
Testovima upotrebljivosti proverava se koliko je softverski sistem lak za upotrebu krajnjim korisnicima. Ova vrsta testiranja je posebno važna za aplikacĳe sa korisničkim interfejsom, kao što su mobilne i veb aplikacĳe, jer ima direktan uticaj na korisničko iskustvo i prihvatanje proizvoda. U testovima upotrebljivosti proverava se koliko brzo novi korisnik može da nauči da koristi sistem bez pomoći ili obuke (naučljivost), da li korisnik može da izvrši zadatke u prihvatljivom broju koraka i u razumnom vremenskom okviru (efikasnost korišćenja), da li sistem omogućava korisniku da lako prepozna i ispravi greške (prevencĳa i oporavak od grešaka), pristupačnost da li su elementi korisničkog interfejsa intuitivno raspoređeni i da li korisnik lako razume njihovu svrhu (jasnoća interfejsa), da li korisnici subjektivno ocenjuju sistem kao prĳatan za korišćenje (zadovoljstvo korisnika), da li je sistem upotrebljiv za osobe sa različitim oblicima invaliditeta (pristupačnost), da li je svrha aplikacĳe jasna i lako razumljiva (prepoznatljivost). Testiranje se često sprovodi kroz posmatranje korisnika dok izvršavaju tipične zadatke, uz praćenje
sistemsko testiranje
nefunkcionalno testiranje
upotrebljivost

<!-- pdf_page=91 printed_page=4 -->

vremena, broja grešaka i nivoa frustracĳe. Cilj je da se identifikuju prepreke koje bi korisniku otežale ili onemogućile korišćenje sistema. Takođe, često se koriste upitnici i intervjui nakon testiranja kako bi se saznao subjektivni utisak korisnika.
Primer 4.2.7 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.2.6) Test naučljivosti je važan u ranim fazama dizajna korisničkog interfejsa i često se koristi za usmeravanje iterativnih poboljšanja.
Naziv test slučaja: TC-N010 — Provera naučljivosti prenosa novca sa jednog na drugi tekući račun.
Opis: Proveriti koliko brzo novi korisnik, bez prethodnog iskustva sa aplikacĳom, može samostalno da nauči kako da izvrši osnovnu funkcionalnost – prenos sredstava.
Scenario: Učesniku (koji ranĳe nĳe koristio aplikacĳu) se daje pametni telefon sa instaliranom verzĳom aplikacĳe i osnovnim uputstvom za početak (npr. kako da se prĳavi). Zadatak je sledeći:
„Prenesite 1000 RSD sa tekućeg računa na drugi račun koristeći opcĳu za internu transakcĳu.“
Parametri koji se prate:
-Vreme potrebno da korisnik pronađe opciju za prenos sredstava.
-Broj pokušaja i grešaka pre nego što se uspešno izvrši transakcĳa.
-Broj pitanja koje korisnik postavi (ako je dozvoljena asistencĳa).
-Subjektivna ocena korisnika (npr. ocena složenosti na skali od 1 do 5).
Kriterĳum prolaznosti: Korisnik bi trebalo da

<!-- pdf_page=92 printed_page=78 -->

uspešno izvrši transakcĳu bez pomoći u roku kraćem od 5 minuta, sa najviše jednom greškom (npr. pogrešan izbor opcĳe ili unos iznosa u pogrešno polje).
Napomena: Test se ponavlja sa 30 korisnika kako bi se dobila reprezentativna metrika. Ukoliko većina ispitanika ima poteškoće sa istim delovima interfejsa, to je jasan indikator za poboljšanje dizajna.
Testovima bezbednosti proverava se zaštita ljudi, opreme i okruženja od neželjenih efekata korišćenja softvera, posebno u kritičnim sistemima kao što su medicinski uređaji, automobilski sistemi, vazduhoplovstvo, industrĳska automatizacĳa i slični domeni gde greška može imati ozbiljne posledice po bezbednost.
sistemsko testiranje
nefunkcionalno testiranje
bezbednost
Primer 4.2.8 (Autonomna vožnja) Testovi bezbednosti su posebno važni u kontekstu autonomne vožnje.
Naziv test slučaja: TC-S007 — Automatsko zaustavljanje prilikom iznenadne prepreke na putu.
Opis: Proveriti kako autonomni sistem reaguje u slučaju iznenadne prepreke na putu, sa ciljem zaštite putnika i drugih učesnika u saobraćaju.
Scenario: Tokom vožnje pri brzini od 50 km/h, pešak iznenada ulazi na put na udaljenosti od 15 metara ispred vozila. Sistem za autonomnu vožnju mora da detektuje pešaka i aktivira bezbednosne mehanizme: kočenje, izbegavanje sudara i/ili upozorenje putnicima.
Uslovi testa:
-Vozilo je u režimu potpunog autonomnog upravljanja.
-Test se izvodi u zatvorenom kontrolisanom okruženju sa korišćenjem lutke kao

<!-- pdf_page=93 printed_page=4 -->

simulacĳe pešaka.
-Sistem ima pristup svim funkcionalnim senzorima.
Parametri koji se prate:
-Vreme reakcĳe sistema nakon detekcĳe prepreke.
-Efikasnost kočenja (da li je došlo do zaustavljanja pre prepreke).
-Aktivacĳa dodatnih sistema (upozorenja, sigurnosni pojasevi, naglo kočenje).
-Usklađenost sa bezbednosnim standardima.
Kriterĳum prolaznosti: Vozilo mora zaustaviti pre nego što dođe do kontakta sa preprekom u 99.9% slučajeva pri definisanoj brzini i udaljenosti, uz tolerancĳu za nepredviđene faktore kao što su vremenski uslovi ili osvetljenje.
Testovima sigurnosti proverava se da li su određene funkcionalnosti dostupne isključivo onim korisnicima kojima su namenjene. Proveravaju se dostupnost, integritet i poverljivost svih skupova podataka.
sistemsko testiranje
nefunkcionalno testiranje
Primer 4.2.9 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.2.7) Sigurnost bankarskih aplikacĳa i zaštita od neautorizovanih pristupa je izuzetno važna i zato postoji posebna kategorĳa testiranja koja se naziva penetraciono testiranje (eng. penetration testing) koja pomaže u identifikacĳi ranjivosti aplikacĳe na pokušaje neautorizovanog pristupa.
sigurnost
Naziv test slučaja: TC-SC004 — Neautorizovani pristupi grubom silom.
Opis: Proveriti da li je aplikacĳa otporna na pokušaj neautorizovanog pristupa putem napada

<!-- pdf_page=94 printed_page=80 -->

grubom silom (eng. brute force attack) na formu za logovanje.
Scenario: Napadač pokušava da pristupi korisničkom nalogu automatskim slanjem velikog broja kombinacĳa korisničkog imena i lozinke putem skripte.
Uslovi testa:
-Test se izvodi u testnom okruženju uz nadzor administratora bez pristupa stvarnim korisničkim podacima.
-Koristi se alat za automatizovani napad (npr. alat Hydra).
-Postoji korisnički nalog sa poznatim korisničkim imenom i slabom lozinkom radi simulacĳe.
Parametri koji se prate:
-Maksimalan broj dozvoljenih pokušaja unosa lozinke pre zaključavanja naloga.
-Vreme blokade naloga i mehanizam obaveštavanja korisnika.
-Evidentiranje pokušaja napada u log fajlovima i reakcĳa sistema.
-Prisustvo mehanizama CAPTCHA nakon prvog neuspešnog pokušaja.
Kriterĳum prolaznosti: Aplikacĳa mora da blokira pristup korisničkom nalogu nakon najviše 3 neuspešna pokušaja i mora da onemogući dalju automatizovanu verifikacĳu lozinki. Napad mora biti zabeležen u sistemskim logovima sa pripadajućim podacima (IP adresa, vreme napada, broj pokušaja).
sistemsko testiranje
Testovima prenosivosti proverava se sposobnost softverskog sistema da funkcioniše u različitim okruženjima. Glavni cilj ovih testova je da se potvrdi da softver može lako da se instalira, koristi i radi ispravno na više platformi, operativnih sistema, hardverskih konfiguracĳa ili pregledača (u slučaju
nefunkcionalno testiranje
prenosivost

<!-- pdf_page=95 printed_page=4 -->

veb-aplikacĳa), kao i da može da se u potpunosti ukloni sa sistema bez ostavljanja tragova ili neželjenih podataka.
Primer 4.2.10 (Aplikacĳa za elektronsko bankarstvo — nastavak primera 4.2.9) Test prenosivosti je posebno značajan za bankarske aplikacĳe jer se koristi na velikom broju različitih uređaja, a doslednost i pouzdanost korisničkog iskustva direktno utiču na poverenje korisnika.
Naziv test slučaja: TC-P003 — Prilagodljivost različitim uređajima i operativnim sistemima.
Opis: Proveriti da li mobilna bankarska aplikacĳa funkcioniše dosledno na različitim operativnim sistemima i verzĳama uređaja, bez potrebe za izmenom izvornog koda.
Scenario: Mobilna aplikacĳa razvĳena je za platforme Android i iOS. Testira se njeno ponašanje na više verzĳa operativnih sistema i različitim uređajima:
-Android 10, 11 i 13 (Samsung Galaxy, Xiaomi, Pixel)
-iOS 15 i 17 (iPhone 11, iPhone 14)
Uslovi testa:
-Instalacĳa najnovĳe verzĳe aplikacĳe sa zvanične prodavnice (Google Play / App Store).
-Test uređaji resetovani na fabrička podešavanja (čisto okruženje).
-Stabilna internet konekcĳa (Wi-Fi).
Aktivnosti testa:
-Instalacĳa i pokretanje aplikacĳe na svakom test uređaju.
-Prĳavljivanje korisnika sa validnim kredencĳalima.

<!-- pdf_page=96 printed_page=82 -->

-Provera prikaza početnog ekrana, menĳa i funkcionalnosti (pregled stanja, prenos sredstava).
-Upoređivanje vizuelne konzistentnosti interfejsa.
-Provera lokalizacĳe (prikaz na srpskom i engleskom jeziku).
Kriterĳum prolaznosti: Aplikacĳa mora da mogući korisnicima da nesmetano obave sve osnovne operacĳe na svim platformama. Ne sme doći do pada sistema, vizuelnih nepravilnosti ili funkcionalnih razlika među verzĳama.
Istraživačko testiranje
Jedna posebna forma sistemskog testiranja jeste istraživačko testiranje (eng. exploratory testing). Ova metoda testiranja oslanja se na znanje, intuicĳu i kreativnost testera, pri čemu se testiranje ne zasniva isključivo na prethodno definisanim test slučajevima, već se test slučajevi osmišljavaju i izvršavaju u hodu.
sistemsko testiranje
Istraživačko testiranje podrazumeva otkrivanje neočekivanih pravaca korišćenja softverskog sistema, kao i prepoznavanje potencĳalnih problema koji nisu bili identifikovani tokom analize i dizajna testova. Tokom ove aktivnosti tester intuitivno istražuje aplikacĳu, posmatra njeno ponašanje u različitim situacĳama i na osnovu uočenih obrazaca formuliše nove test slučajeve u realnom vremenu.
istraživačko testiranje
Ova vrsta testiranja ima najveći značaj kada je softver već funkcionalno zaokružen, odnosno kada je aplikacĳa dostupna u svom gotovo finalnom obliku. Tada tester ima mogućnost da uoči alternativne tokove korišćenja sistema koji nisu prethodno uzeti u obzir, čime se značajno povećava pokrivenost testiranjem.
Ukoliko se istraživačko testiranje zanemari, postoji rizik da određene funkcionalnosti ostanu neproverene,

<!-- pdf_page=97 printed_page=4 -->

naročito one koje se ne nalaze u primarnim ili očekivanim tokovima rada. Stoga se ova vrsta testiranja često koristi kao dopuna formalnim tehnikama, sa ciljem da se dodatno osigura kvalitet konačnog proizvoda. U okviru istraživačkog testiranja mogu se proveravati i funkcionalna i nefunkcionalna svojstva sistema.
Primer 4.2.11 (Aplikacĳa za deljenje fotografija) Tester istražuje neočekivane tokove korišćenja u aplikacĳi koja omogućava korisnicima da postavljaju, komentarišu i dele fotografije. Testiranje se sprovodi bez prethodno definisanih test slučajeva, oslanjajući se na intuicĳu, iskustvo i zapažanja testera. Na primer, tester istražuje naredne scenarĳe upotrebe
-Pokušaj postavljanja slike u formatu koji aplikacĳa formalno ne podržava (npr. format .tiff) –– proverava se reakcĳa sistema.
-Brzo višestruko postavljanje iste fotografije — provera se da li dolazi do duplikata, grešaka ili zamrzavanja aplikacĳe.
-Istovremeno korišćenje više funkcionalnosti (npr. slanje komentara dok je slika u procesu postavljanja) — provera se stabilnost aplikacĳe i ispravnost rada.
-Pokušaj učitavanja sadržaja bez dostupnog interneta, ili sa slabo propusnim internetom — provera se prisustvo adekvatne poruke o grešci.
-Promena jezičkih podešavanja tokom aktivne sesĳe — provera se uticaj na postojeći sadržaj korisničkog interfejsa.
U svakom od prethodnih situacĳa aplikacĳa bi trebalo da se ponaša stabilno, obezbedi korisniku jasne poruke o greškama i izbegne pad sistema ili gubitak podataka. Cilj ovih provera je otkrivanje potencĳalnih grešaka i nepredviđenih ponašanja sistema u realnim, kompleksnim i neobičnim scenarĳima koje standardni test slučajevi možda ne pokrivaju.

<!-- pdf_page=98 printed_page=84 -->

Testiranje prihvatljivosti
Testovi prihvatljivosti (eng. acceptance testing) treba da omoguće klĳentima i korisnicima da se sami uvere da je napravljeni softver u skladu sa njihovim potrebama i očekivanjima. Ovu vrstu testiranja izvode i procenjuju korisnici, a razvojni tim im pruža pomoć oko tehničkih pitanja, ukoliko za tim ima potrebe. Testiranje prihvatljivosti obično spada u tehnike validacĳe softvera.
Klĳent može da proceni sistem na tri načina: referentnim testiranjem, pilot testiranjem i paralelnim testiranjem.
sistemsko testiranje
Referentno testiranje izvode korisnici kako bi procenili da li je softver implementiran u skladu sa očekivanjima. Kod referentnog testiranja, klĳent generiše test slučajeve koji predstavljaju uobičajne uslove u kojima sistem treba da radi.
Testiranje prihvatljivosti
Pilot testiranje podrazumeva instalacĳu sistema na privremenoj lokacĳi i njegovu upotrebu. U ovom slučaju, testiranje se vrši simulacĳom svakodnevnog rada na sistemu.
referentno
pilot
paralelno
Paralelno testiranje se koristi tokom razvoja, kada jedna verzĳa softvera zamenjuje drugu ili kada novi sistem treba da zameni stari. Ideja je paralelno funkcionisanje oba sistema (starog i novog) čime se korisnici postepeno privikavaju i prelaze na korišćenje novog sistema.
Primer 4.2.12 Testiranje prihvatljivosti modernih aplikacĳa često se vrši na uzorku odabranih korisnika (npr. zaposlenih u kompanĳi koja proizvodi aplikacĳu ili zaposlenih u kompanĳi čĳi će korisnici da koriste tu aplikacĳu). Na primer, za bankarski softver, to mogu da budu zaposleni u banci ili manja grupa klĳenata banke.
Tokom ove faze testiranja prati se korišćenje osnovnih

<!-- pdf_page=99 printed_page=4 -->

ili novododatih funkcionalnosti. Beleže se uočeni problemi, vreme izvršavanja operacĳa i reakcĳe korisnika na interfejs i način rada sistema.
Na osnovu prikupljenih podataka identifikuju se eventualne greške, nejasnoće u korišćenju i problemi u performansama, nakon čega se sistem unapređuje pre šireg uvođenja u produkciono okruženje.
Instalaciono testiranje
Instalaciono testiranje predstavlja specifičnu vrstu testiranja u kojoj se softver instalira u klĳentskom okruženju, kako bi se proverila njegova sposobnost da se pravilno instalira i funkcioniše u realnim uslovima. Tokom ovog procesa, sistem se podešava u skladu sa tehničkim karakteristikama ciljne mašine, kao i sa specifičnostima okruženja (npr. operativni sistem, mrežne postavke, povezani uređaji). Ukoliko softver zahteva komunikacĳu sa spoljnim uređajima ili servisima, testira se i sposobnost uspostavljanja te komunikacĳe.
sistemsko testiranje
Primer 4.2.13 Kompanĳe koje obezbeđuju uslugu testiranja drugim softverskim kompanĳa često raspolažu laboratorĳama za testiranje tj. kolekcĳama uređaja i računara sa različitim softverskim konfiguracĳama. Na primer, mogu posedovati desetine modela telefona sa različitim verzĳama operativnih sistema Android i iOS. Takav pristup omogućava proveru da li se aplikacĳa ispravno instalira i pokreće na svim relevantnim uređajima i verzĳama operativnog sistema. Istovremeno, identifikuju se potencĳalni problemi koji se javljaju samo u specifičnim kombinacĳama hardvera i softvera, kao što je pad aplikacĳe na određenom modelu telefona ili verzĳi operativnog sistema. Ovakve laboratorĳe takođe štede vreme i resurse svojih klĳenata, koji oni ne moraju da poseduju sve moguće uređaje i konfiguracĳe za testiranje, dok istovremeno
instalaciono testiranje

<!-- pdf_page=100 printed_page=86 -->

omogućavaju da se testovi ponavljaju automatski ili u serĳama na više uređaja odjednom, čime se povećava ponovljivost i pouzdanost testiranja.
Instalacioni testovi se nekada sprovode i u saradnji sa krajnjim korisnicima, kako bi se osiguralo da instalacĳa teče bez grešaka i da sistem nakon instalacĳe ispravno funkcioniše. Poseban akcenat stavlja se na detekcĳu eventualnih uticaja okruženja na funkcionalne i nefunkcionalne karakteristike sistema, kao što su performanse, sigurnost ili kompatibilnost. Ovo testiranje ima za cilj da potvrdi da je softver spreman za rad u stvarnom okruženju korisnika, bez potrebe za dodatnim intervencĳama nakon instalacĳe.
### 4.3 Tehnike testiranja
Tehnike testiranja imaju za cilj da pruže sistematski odgovor na pitanje kako identifikovati reprezentativni skup test slučajeva (test primera, ili samo testova). Reprezentativni skup testova treba da obuhvati slučajeve koji najbolje odražavaju stvarne uslove rada softverskog sistema, ali i one koji imaju povećanu verovatnoću da otkrĳu potencĳalne slabosti u implementacĳi. Dodatno, treba da omogući efikasno balansiranje između obima testiranja i potrošnje resursa. Reprezentativni skup testova treba da ima naredne karakteristike:
-Visok potencĳal otkrivanja grešaka. -Relativno mala veličina. -Relativno velika brzina izvršavanja. -Pruža visok stepen poverenja u pouzdanost softvera.
Dobro definisan i pažljivo odabran skup testova predstavlja osnovu za kvalitetno, ciljno-orĳentisano testiranje koje doprinosi visokom kvalitetu softverskog rešenja.

<!-- pdf_page=101 printed_page=4 -->

4.3.1 Pokrivenost testiranjem
Pokrivenost testiranjem (eng. test coverage) je metrika koja pomaže da se proceni koliko su testovi sveobuhvatni i koliko dobro proveravaju funkcionalnost, strukturu i ponašanje sistema. Koristi se za procenu kvaliteta softvera. Takođe, može se koristiti i da ukaže na delove sistema koji nisu testirani. Pomaže u donošenju odluke da li je softver spreman za isporuku.
Pokrivenost = Broj testiranih elem.
Pokrivenost se definiše kao procenat elemenata sistema koji su obuhvaćeni testiranjem u odnosu na sve elemente te vrste. Postoje razne vrste pokrivenosti, a osnovne vrste pokrivenosti su date u nastavku.
Ukupan broj elem. × 100%
Pokrivenost zahteva (eng. requirements coverage) Mera koja pokazuje koliki je procenat zahteva proveren testiranjem u odnosu na ukupan broj zahteva korisnika koji su definisani kroz specifikacĳu. Potpuna pokrivenost podrazumeva da je svaki zahtev testiran.
Pokrivenost zahteva =
Broj testiranih zahteva
Ukupan broj zahteva × 100%
Pokrivenost funkcionalnosti (eng. functional coverage) Mera koja pokazuje koliki je procenat funkcionalnosti proveren testiranjem u odnosu na ukupan broj funkcionalnosti sistema. Potpuna pokrivenost podrazumeva da je svaka funkcionalnost testirana.
Pokrivenost funkcionalnosti =
Broj testiranih funkc.
Ukupan broj funkc. × 100%
Pokrivenost koda (eng. code coverage) Ova mera sadrži u sebi veći broj različitih pokrivenosti. Na primer, pokrivenost naredbi se definiše kao broj izvršenih naredbi u okviru testiranja podeljen sa ukupnim brojem naredbi u projektu. Pokrivenost koda se detaljno razmatra u delu 4.3.4.
Pokrivenost koda =
Broj izvršenih elem.
Ukupan broj tih elem. × 100%
Primer 4.3.1 (Veb aplikacĳa za kupovinu) Visoka pokrivenost zahteva ne znači nužno i visoku pokrivenost funkcionalnosti — mogu postojati funkcionalnosti koje nisu formalno dokumentovane zahtevima, a koje ipak treba testirati. Zato se u praksi često prate obe

<!-- pdf_page=102 printed_page=88 -->

pokrivenosti.
Na primer, za veb aplikacĳu za kupovinu, u okviru specifikacĳe mogu biti zadati naredni zahtevi:
-Korisnik može dodati proizvod u korpu. -Korisnik može obrisati proizvod iz korpe. -Korisnik može završiti kupovinu klikom na dugme Kupi.
U okviru implementacĳe, uz te zadatke, programer implementira i sledeće
-Kada je korpa prazna, dugme Kupi se automatski onemogućava.
-Ako korisnik pokuša da doda negativan broj proizvoda, sistem prikazuje poruku o grešci.
Pokrivenost zahteva u ovom slučaju ne obuhvata pokrivenost funkcionalnosti jer nedostaju testovi implementiranih funkcionalnosti za onemogućavanje dugmeta Kupi kada je korpa prazna i za prikazivanje poruke o grešci prilikom unosa negativnog broja proizvoda.
4.3.2 Podela tehnika testiranja
Većina softverskih sistema podrazumeva mogućnost relativno jasnog utvrđivanja očekivanog izlaza za zadate uslove. U takvim slučajevima, dobri test primeri se mogu naći na osnovu specifikacĳe programa (testiranje crne kutĳe), na osnovu koda programa (testiranje bele kutĳe) ili na osnovu kombinacĳe specifikacĳe i koda programa (testiranje sive kutĳe).
Odnos: Testiranje crne kutĳe je testiranje iz ugla korisnika dok je testiranje bele kutĳe testiranje iz ugla programera.
Testiranje crne kutĳe (eng. black box testing) — generisanje test primera bez razmatranja interne strukture koda već isključivo na osnovu specifikacĳe. Ovakav način testiranja se fokusira na ponašanje sistema, posmatrano iz korisničkog ugla. Drugi nazivi su i funkcionalno testiranje (eng. functional testing), testiranje ponašanja (eng. behavioural

<!-- pdf_page=103 printed_page=4 -->

testing), testiranje vođeno podacima (eng. data driven testing). Prednost ovog pristupa je mogućnost potpunog razdvajanja programera i testera i zato ovo testiranje obično obavljaju testeri. Zadatak testera je da sistemu pruži ulaze, a zatim da proveri izlaze u odnosu na datu specifikacĳu.
Crna kutĳa
Ulaz
Izlaz
Slika 4.6: Testiranje crne kutĳe: fokus na ulazu i izlazu
Testiranje bele kutĳe (eng. white box testing) — generisanje test primera na osnovu interne strukture i logike koda. Alternativni nazivi za ovaj pristup su strukturno testiranje (eng. structural testing) i testiranje vođeno logikom (eng. logic driven testing), što dodatno naglašava oslonac na logičku strukturu koda i neophodnost poznavanja implementacĳe radi pisanja testova za ovu vrstu testiranja. Zbog toga testiranje bele kutĳe obično obavljaju programeri tokom faze razvoja softvera. Primer testiranja bele kutĳe su testovi jedinica koda u kojima se proverava ispravnost najmanjih funkcionalnih delova softvera.
Bela kutĳa
Ulaz
Izlaz
Slika 4.7: Testiranje bele kutĳe: fokus na strukturi koda.

<!-- pdf_page=104 printed_page=90 -->

Testiranje sive kutĳe (eng. gray box testing) — predstavlja prelaz između tehnika crne i bele kutĳe (mešovita strategĳa). Kod ove tehnike postoji uvid u unutrašnju strukturu sistema, ali ne u toj meri kao kod tehnika bele kutĳe. Koristi se, na primer, kod komponentnog i integracionog testiranja. Ovo je tehnika koju koriste i programeri i testeri.
Siva kutĳa
Ulaz
Izlaz
?
Slika 4.8: Testiranje sive kutĳe: mešovita strategĳa.
Problem proročišta
Prethodne tehnike testiranja podrazumevaju da je za ulazne vrednosti moguće jednostavno odrediti odgovarajuće izlazne vrednosti. Međutim, to ne mora da bude slučaj za sve softverske sisteme. Preciznĳe, proročište (eng. test oracle) je mehanizam (ili znanje) koje omogućava testeru da odredi: „Očekivani rezultat za ulaz U je izlaz I“ i da uporedi stvarni izlaz sa tim očekivanim. Kada takav mehanizam ne postoji ili ga je teško definisati, dolazi do problema proročišta. Problem proročišta (eng. oracle problem) u testiranju softvera odnosi se na izazov određivanja da li je rezultat testa ispravan — tj. kako sa sigurnošću znati da je izlaz sistema za određeni ulaz tačan. Problem proročišta je izražen u oblastima kao što su računarska grafika, konstrukcĳa kompilatora i mašinsko učenje.

<!-- pdf_page=105 printed_page=4 -->

Primer 4.3.2 (C kompajler) U razvoju kompajlera za programski jezik C potrebno je da proverimo da li kompajler ispravno prevodi programe. Test bi trebalo da proveri da li je kompajler:
-ispravno generisao mašinski kôd koji odgovara očekivanom izvršavanju programa (zadržao je semantiku izvornog programa),
-ispravno optimizovao kôd (npr. eliminisao suvišne promenljive).
Međutim
-Najčešće ne postoji formalna specifikacĳa očekivanog izlaza za proizvoljan ulazni program.
-Ručna provera mašinskog koda ili ponašanja može biti izuzetno teška i podložna greškama.
-Automatizovana provera semantičke ekvivalencĳe dva programa (izvorni i prevedeni) je u opštem slučaju nerešiv problem.
Problem proročišta se rešava na različite načine.
-Korišćenje alternativnih implementacĳa kao uporednog standarda ili upotreba ranĳih verzĳa softvera kao referentnog ponašanja (onda kada su ranĳe verzĳe softvera dostupne). Ukoliko su rezultati različiti, onda bar jedna od implementacĳa ima grešku.
-Metamorfno testiranje — ne proverava se konkretan izlaz, već odnos između više izlaza koji se računa na osnovu odnosa između ulaza i osobina algoritma koji se testira.
Primer 4.3.3 (C kompajler — nastavak primera 4.3.2) Jedan praktičan pristup prevazilaženju problema proročišta kod kompajlera je tzv. diferencĳalno testiranje:
-Kôd se prevede pomoću više različitih kompajlera (ili različitih verzĳa istog kompajlera),

<!-- pdf_page=106 printed_page=92 -->

Dĳagrami stanja
Osnovne putanje
Siva kutĳa
Tabele odlučivanja
Tok podataka
Crna kutĳa
Bela kutĳa
Tehnika graničnih vrednosti
Prolasci kroz petlje
Tehnika klasa ekvivalencĳe
Tehnike testiranja
Slika 4.9: Tehnike testiranja softvera
-Izvrše se sve dobĳene verzĳe izvršivog koda u kontrolisanom okruženju,
-Ako svi rezultati izvršavanja daju isti izlaz, pretpostavlja se da su tačni.
Jasno je da se čak i tada ne može sa sigurnošću tvrditi da je rezultat ispravan, iz više razloga. Najpre, provera je urađena samo na nekim konkretnim ulazima i za te ulaze je utvrđeno da se različiti kompajleri isto ponašaju. Za neke druge ulaze možda bismo dobili razliku u ponašanju. Dodatno, moguće je i da svi kompajleri koji učestvuju u poređenju daju istu grešku.
Korišćenje različitih implementacĳa se ne može uvek primeniti pošto često ne postoji više implementacĳa istog algoritma (jer su te implementacĳe previše skupe i zahtevaju puno vremena). Takođe, ako se različite implementacĳe kreiraju od strane istih ljudi, moguće je da oni prave iste greške.
4.3.3 Testiranje crne kutĳe
Testiranje crne kutĳe teorĳski se može uraditi isprobavanjem svih mogućih ulaza (eng. exhaustive input testing).

<!-- pdf_page=107 printed_page=4 -->

Međutim, već za trivĳalne programe nĳe moguće koristiti ovu tehniku.
Primer 4.3.4 (Kvadratna jednačina) Data kvadratna jednačina 𝑎· 𝑥2 + 𝑏· 𝑥+ 𝑐= 0
ima rešenje
𝑥1,2 = −𝑏± √
𝑏2 −4 · 𝑎· 𝑐 2 · 𝑎
Ako su koeficĳenti jednačine celobrojni i tipa int32 onda je broj različitih test primera za potpuno testiranje 232 · 232 · 232 = 296
Dodatno, pored isprobavanja svih mogućih ispravnih vrednosti ulaza, potrebno je razmotriti i moguće neispravne ulaze kojih takođe može biti mnogo.
Primer 4.3.5 Neispravan ulaz za očekivanu starost osobe može da bude negativan broj ili unos neke proizvoljne reči umesto broja. Očekivano ponašanje softvera u takvim situacĳama može da bude signaliziranje greške korisniku sa mogućnošću unosa nove vrednosti ili prekid rada softvera uz odgovarajuću poruku.
Cilj tehnika testiranja crne kutĳe je da pronađu prihvatljiv broj test slučajeva (tj. kombinacĳa ulaza) koji odgovara reprezentativnom skupu testova. Test slučajevi mogu se podeliti u dve osnovne kategorĳe: test slučajevi koji odgovaraju validnim ulazima i test slučajevi koji odgovaraju nevalidnim ulazima.
Primer 4.3.6 (Kvadratna jednačina — nastavak primera 4.3.4.) Test slučaj koji odgovara ispravnom ulazu za kvadratnu jednačinu može da sadrži ulazne vred-

<!-- pdf_page=108 printed_page=94 -->

nosti {1, -3, 2} i izlazne vrednosti {1, 2}. Test slučaj koji odgovara neispravnom ulazu može da sadrži ulazne vrednosti {"I", -3, 2} i izlaznu vrednost {"Neispravan unos prvog koeficĳenta"}
Pronalaženje reprezentativnog skupa testova metodama crne kutĳe se ostvaruje postavljanjem odgovarajućih pretpostavki o softveru koji treba da se testira. Najpoznatĳi tehnike obuhvataju tehniku klasa ekvivalencĳe, tehniku graničnih vrednosti, tabele odlučivanja i dĳagrame stanja.
tehnike testiranja
testiranje crne kutĳe
klase ekvivalencĳe
Klase ekvivalencĳe
granične vrednosti
Testiranje pomoću klasa ekvivalencĳe (eng. equivalence class testing) je tehnika koja se koristi da smanji broj test slučajeva na prihvatljiv nivo, a da se pri tome zadrži zadovoljavajuća pokrivenost ulaznog prostora podataka. Klase ekvivalencĳe predstavljaju skupove ulaznih podataka koji se obrađuju na isti način od strane sistema. One se mogu podeliti na validne (ispravne) i nevalidne (neispravne) klase, u zavisnosti od toga da li bi sistem trebalo da prihvati te vrednosti za dalju obradu ili ih odbaci.
tabele odlučivanja
dĳagrami stanja
tabele stanja
Primer 4.3.7 (Validne i nevalidne klase) Ukoliko se očekuje da korisnik unese broj godina između 18 i 65, validne klase bi pokrivale sve vrednosti unutar tog opsega, dok bi nevalidne klase uključivale vrednosti ispod 18 i iznad 65.
tehnike testiranja
Ova tehnika se zasniva na pretpostavci da se sve vrednosti unutar jedne klase ponašaju identično u kontekstu testiranja, te je dovoljno izabrati po jednog predstavnika iz svake klase. Preciznĳe, pretpostavke za klase ekvivalencĳe su:
testiranje crne kutĳe
klase ekvivalencĳe
-Ukoliko jedan test slučaj iz određene klase ekvivalencĳe otkrĳe grešku, velika je verovatnoća da

<!-- pdf_page=109 printed_page=4 -->

bi i svi ostali test slučajevi iz iste klase otkrili istu tu grešku.
-Ukoliko jedan test slučaj iz određene klase ekvivalencĳe ne otkrĳe grešku, pretpostavlja se da ni ostali test slučajevi iz te klase ne bi otkrili grešku.
Na osnovu ovih pretpostavki, testiranje se može racionalizovati izborom po jednog predstavnika iz svake klase. Ključni koraci primene ove tehnike su:
1. Identifikovati sve validne klase ekvivalencĳe za ulazne vrednosti koje bi sistem trebalo da prihvati za dalju obradu.
2. Izabrati po jedan test slučaj za svaku validnu klasu.
3. Identifikovati nevalidne klase ekvivalencĳe za ulazne vrednosti koje bi sistem trebalo da odbaci.
4. Izabrati po jedan test slučaj za svaku nevalidnu klasu.
Na taj način se smanjuje broj potrebnih testova, a da se pritom zadrži visok nivo pokrivenosti funkcionalnih pravila sistema i otkrivanja potencĳalnih grešaka.
Primer 4.3.8 (Zapošljavanje na osnovu starosti) Pretpostavimo da sistem za zapošljavanje sprovodi pravila na osnovu starosti kandidata. Pravila su definisana narednom tabelom:
Godine Pravilo
0–16 Ne zaposliti 16–18 Može se zaposliti samo sa pola radnog vremena 18–55 Može se zaposliti sa punim radnim vremenom 55–99 Ne zaposliti
Validne klase ekvivalencĳe:
-V1 — Godine u opsegu 0–16 (npr. 10)

<!-- pdf_page=110 printed_page=96 -->

-V2 — Godine u opsegu 16–18 (npr. 17) -V3 — Godine u opsegu 18–55 (npr. 30) -V4 — Godine u opsegu 55–99 (npr. 70)
Nevalidne klase ekvivalencĳe:
-I1 – Vrednost ispod minimalne vrednosti (npr. −5)
-I2 – Vrednost iznad maksimalne vrednosti (npr. 105)
Test slučajevi:
ID Klasa Ulaz Očekivani rezultat
TC1 V1 10 Ne zaposliti TC2 V2 17 Zapošljavanje sa pola radnog vremena TC3 V3 30 Zapošljavanje sa punim radnim vremenom TC4 V4 70 Ne zaposliti TC5 I1 −5 Odbiti unos TC6 I2 105 Odbiti unos
Korišćenjem tehnike klasa ekvivalencĳe, broj test slučajeva za ispravne unose se smanjuje sa 100 (po jedan za svaku validnu godinu) na svega nekoliko reprezentativnih testova, uz zadržavanje pokrivenosti svih funkcionalnih pravila sistema.
Napomena: Često je lakše identifikovati validne klase ekvivalencĳe od nevalidnih. Na primer, pored nevalidnih unosa -5 i 105, potrebno je testirati i nevalidne unose kao što je unos izraza koji vodi neispravnom broju (npr. 66+35), unos slova i nenumeričkih karaktera i slično.
Granične vrednosti
Testiranje pomoću klasa ekvivalencĳe predstavlja osnovnu tehniku za oblikovanje test slučajeva. Međutim, u praksi se pokazalo da se veliki broj grešaka javlja upravo

<!-- pdf_page=111 printed_page=4 -->

na granicama definisanih klasa. Odatle potiče ideja o dodatnoj tehnici: testiranju graničnih vrednosti (eng. boundary value testing).
tehnike testiranja
Ova tehnika fokusira se na vrednosti koje se nalaze na samim granicama, neposredno ispod i neposredno iznad granica klasa ekvivalencĳe, jer upravo na tim mestima programeri najčešće prave greške. Tipična greška je pogrešno upisivanje operatora nejednakosti, na primer korišćenje znaka > umesto znaka ≥(ili obratno).
testiranje crne kutĳe
granične vrednosti
Primetimo da su termini ispod i iznad relativni pojmovi koji zavise od tipa i preciznosti vrednosti koje se testiraju. Na primer, kod celobrojnih vrednosti, to su uzastopni brojevi (𝑛−1 i 𝑛+1, ukoliko je 𝑛granica), dok kod realnih brojeva razlika može biti definisana brojem značajnih decimala. Dodatna složenost se javlja kada postoje višedimenzionalni ulazi (npr. dve povezane numeričke vrednosti) ili kada se radi sa realnim brojevima visoke preciznosti. U takvim slučajevima, identifikacĳa relevantnih granica i test tačaka zahteva dodatnu pažnju i detaljnĳu analizu.
Osnovni koraci za primenu testiranja graničnih vrednosti su sledeći:
1. Identifikovati klase ekvivalencĳe na osnovu ulaznih podataka.
2. Odrediti tačne granice svake identifikovane klase. 3. Za svaku granicu, definisati sledeće test tačke:
-tačku na samoj granici, -tačku neposredno ispod granice, -tačku neposredno iznad granice.
Važno je imati u vidu da tačke koje se nalaze ispod i iznad granice mogu da pripadaju klasama ekvivalencĳe koje su već obuhvaćene testovima. Zbog toga treba paziti da se testovi ne dupliraju kada se kombinuje testiranje graničnih vrednosti sa testiranjem klasa ekvivalencĳe.

<!-- pdf_page=112 printed_page=98 -->

Primer 4.3.9 (Zapošljavanje na osnovu starosti — nastavak primera 4.3.8) Prilikom analize graničnih vrednosti, uočava se problem u specifikacĳi sistema na granicama klasa ekvivalencĳe. Naime, vrednosti 16, 18 i 55 pojavljuju se u više klasa, što dovodi do preklapanja. Na primer, jedno pravilo navodi da osobe stare 16 godina ne treba zaposliti, dok drugo pravilo ističe da se takve osobe mogu zaposliti sa pola radnog vremena. Ovakvo preklapanje ukazuje na grešku u specifikacĳi koju je neophodno ispraviti.
Ispravna verzĳa tabele, koja eliminiše ova preklapanja, prikazana je u nastavku:
Godine Pravilo
0–15 Ne zaposliti 16–17 Može se zaposliti samo sa pola radnog vremena 18–54 Može se zaposliti sa punim radnim vremenom 55–99 Ne zaposliti
Na osnovu nje možemo da definišemo slične validne klase ekvivalencĳe i njihove predstavnike.
Validne klase ekvivalencĳe:
-V1 — Godine u opsegu 0–15 (npr. 10) -V2 — Godine u opsegu 16–17 (npr. 17) -V3 — Godine u opsegu 18–54 (npr. 30) -V4 — Godine u opsegu 55–99 (npr. 70)
Dalje, na osnovu definisanih klasa ekvivalencĳe, možemo definisati odgovarajuće vrednosti na granicama:
-Granica 0: {0, 1} -Granica 15: {14, 15, 16} -Granica 16: {15, 16, 17} -Granica 17: {16, 17, 18} -Granica 18: {17, 18, 19}

<!-- pdf_page=113 printed_page=4 -->

-Granica 54: {53, 54, 55} -Granica 55: {54, 55, 56} -Granica 99: {98, 99, 100}
Unĳa svih ovih skupova daje sledeće test vrednosti:
{0, 1, 14, 15, 16, 17, 18, 19, 53, 54, 55, 56, 98, 99, 100}
Zajedno sa vrednostima identifikovanim za same klase ekvivalencĳe, to čini skup
{0, 1, 10, 14, 15, 16, 17, 18, 19, 30, 53, 54, 55, 56, 70, 98, 99, 100}
Međutim, sada imamo preklapanja unutar istih klasa ekvivalencĳe, i neke vrednosti mogu biti redundantne. Na primer, vrednosti 0, 1, 10, 14 i 15 pripadaju istoj klasi 0–15, dok su 18, 19, 30, 53 i 54 sve iz klase 18– 54. Testove koji pripadaju istoj klasi ekvivalencĳe, a nisu granične vrednosti moguće je po potrebi ukloniti u cilju smanjivanja troškova testiranja, bez gubitka pokrivenosti.
Tabele odlučivanja
Tabela odlučivanja (eng. decision table) pruža pregled složenih poslovnih pravila u strukturisanom i lako čitljivom obliku. One predstavljaju snažno sredstvo za analizu i dizajn test scenarĳa u složenim informacionim sistemima. Često se koriste u testiranju softvera za sistematsko generisanje test slučajeva, naročito u situacijama kada postoji veći broj kombinacĳa ulaznih uslova i očekivanih akcĳa.
tehnike testiranja
Tabela odlučivanja je organizovana u redove i kolone. Redovi se dele u dve grupe: prvu grupu čine uslovi nad ulazima, dok drugu grupu čine moguće akcĳe koje sistem treba da izvrši. Kolone predstavljaju pravila — svaka kolona odgovara jedinstvenoj kombinacĳi vrednosti uslova i opisuje koje se akcĳe u tom slučaju preduzimaju.
testiranje crne kutĳe
tabele odlučivanja

<!-- pdf_page=114 printed_page=100 -->

Uslovi mogu biti binarni (na primer, da/ne, istina/laž) ili viševrednosni (na primer, malo/srednje/veliko). Kada su uslovi binarni, iz svakog pravila se obično izvodi jedan test slučaj. Kod viševrednosnih uslova može se izvesti više test slučajeva, u zavisnosti od željenog nivoa pokrivenosti.
U slučajevima kada više pravila dovode do iste akcĳe, bez obzira na vrednost nekog uslova, moguće je izvršiti objedinjavanje pravila (eng. table collapsing). U takvim slučajevima, uslov koji ne utiče na ishod označava se simbolom „—” (crtica) i naziva se nebitnim (eng. don’t care).
Test slučajevi izvedeni iz tabele odlučivanja mogu se dodatno kombinovati sa drugim tehnikama testiranja, kao što su testiranje pomoću klasa ekvivalencĳe ili testiranje graničnih vrednosti. Ova kombinacĳa povećava preciznost i efektivnost testiranja.
Primer 4.3.10 (Bankomat) Klĳent zahteva isplatu gotovine na bankomatu. Sistem treba da odluči da li će da odobri isplatu. Odlučivanje vrši pomoću podataka o sredstvima na računu i o dozvoljenom minusu. Način odlučivanja je prikazan narednom tabelom.
Pravilo 1 Pravilo 2 Pravilo 3
Uslovi Dovoljno sredstava na računu Da Ne Ne Dozvoljen minus — Da Ne Akcĳe Isplata odobrena Da Da Ne
Prvo pravilo je dobĳeno spajanjem dva pravila: kada ima dovoljno sredstava na računu, nezavisno od toga da li je minus dozvoljen ili ne, isplata se odobrava. Iz drugog pravila može se izvesti test slučaj tako što se za ulaz uzme da korisnik nema dovoljno sredstava na računu i da mu je dozvoljen minus. Zatim se izlaz iz programa poredi sa očekivanom akcĳom, a to je da je isplata odobrena. Iz trećeg pravila može se izvesti test slučaj za koji isplata nĳe odobrena.

<!-- pdf_page=115 printed_page=4 -->

Dĳagrami stanja
Sistemi koji reaguju na spoljašnje događaje i čĳe ponašanje zavisi od prethodno izvršenih akcĳa mogu se efikasno modelovati pomoću konačnih automata (eng. finite state machines). U svakom trenutku, takav sistem se nalazi u jednom od konačno mnogo mogućih stanja i pasivno čeka na neki ulazni događaj. Kada se dogodi odgovarajući događaj, sistem, u zavisnosti od trenutnog stanja, prelazi u novo stanje. Tokom ovog prelaza često se izvršava i određena akcĳa, kao što je generisanje izlaza, slanje poruke ili promena internog podatka.
Jedan od najvažnĳih načina prikaza konačnog automata u inženjerskoj praksi je dĳagram stanja (eng. statetransition diagram). Ovaj dĳagram kompaktno i pregledno opisuje složene zahteve sistema i njegov način interakcĳe sa spoljašnjim svetom. Posebno se koristi za modelovanje sistema čĳe ponašanje zavisi od sekvence prethodnih događaja.
tehnike testiranja
Osnovni elementi dĳagrama stanja prikazani su na slici 4.10 i uključuju:
testiranje crne kutĳe
Stanje — Predstavlja određeno ponašanje ili konfiguracĳu sistema; čuva informacĳu o prošlim događajima i određuje reakcĳu na buduće.
dĳagrami stanja
Prelaz — Predstavlja promenu iz jednog stanja u drugo, iniciranu događajem.
Događaj — Spoljašnji ili unutrašnji signal koji izaziva prelaz između stanja.
Akcĳa — Operacĳa koju sistem izvršava kao odgovor na prelaz, kao što su promene izlaza, logovanje ili pozivi metoda.
Dĳagram stanja omogućava vizuelizacĳu svih mogućih stanja sistema, događaja koji uzrokuju promene stanja, kao i pratećih akcĳa. Ova tehnika je široko rasprostranjena u razvoju softverskih komponenti koje zahtevaju precizno definisano ponašanje u skladu sa spoljašnjim

<!-- pdf_page=116 printed_page=102 -->

Događaj/Akcĳa
Stanje 1 Stanje 2
Slika 4.10: Prikaz prelaza u okviru dĳagrama stanja
stimulusima, kao što su korisnički interfejsi, komunikacioni protokoli i kontrolni sistemi.
Pored modelovanja ponašanja, dĳagram stanja može se koristiti i za generisanje test slučajeva. Budući da je dĳagram stanja oblik usmerenog grafa, testiranje se može zasnivati na njegovom obilasku. Na primer, možemo zahtevati da svaki prelaz u dĳagramu bude ispitan bar jednom — što predstavlja dobar kompromis između pokrivenosti i obima testova. Alternativno, može se zahtevati pokrivenost svih stanja ili čak svih mogućih putanja kroz dĳagram, u zavisnosti od ciljeva i kritičnosti sistema.
Primer 4.3.11 (Ugrađena kasa) Posmatramo softverski sistem za maloprodaju koji ima ugrađenu opcĳu za otvaranje i zatvaranje (fioke) kase prikazan na slici 4.11. Primeri test slučajeva
1. Otvori, zatvori, ugasi program
2. Otvori, otvori, zatvori, zatvori, ugasi program.
Drugi test slučaj aktivira svaki prelaz datog dĳagrama bar jednom. Pri izvršavanju navedenih naredbi proverava se da li sistem reaguje u skladu sa zadatim zahtevima.
tehnike testiranja
testiranje crne kutĳe
Tabele stanja
Konačni automat koji modeluje sistem se može prikazati i tabelama stanja (eng. state transition tables). Osnovna
tabele stanja

<!-- pdf_page=117 printed_page=4 -->

Zatvori
Otvori
Otvori/Obavesti
Zatvorena Otvorena
Zatvori/Obavesti
Ugasi program
Slika 4.11: Dĳagram stanja za ugrađenu kasu
prednost tabela stanja jeste njihov sistematični pristup jer prikazuju sve moguće kombinacĳe stanja i događaja. Takvim pristupom mogu da se uoče situacĳe u kojima ponašanje sistema nĳe definisano, što može da spreči pojavu grešaka. Kod tabela stanja, iz svakog reda se može direktno izvesti jedan test slučaj. Tabele stanja postaju nepraktične ukoliko postoji veliki broj mogućih stanja i događaja.
Primer 4.3.12 (Ugrađena kasa — nastavak primera 4.3.11) Tabela stanja za ugrađenu kasu prikazana je u narednoj tabeli.
Trenutno stanje Događaj Akcĳa Naredno stanje
Zatvorena otvori obavesti Otvorena Zatvorena zatvori - Zatvorena Zatvorena ugasi program - Zatvorena Otvorena otvori - Otvorena Otvorena zatvori obavesti Zatvorena Otvorena ugasi program - Nedefinisano
Na osnovu tabele možemo lako da uočimo da postoji test slučaj za koje stanje nĳe definisano. To je test slučaj koji odgovara situacĳi u kojoj korisnik sistema želi da ugasi program, a kasa nĳe zatvorena (poslednji red tabele). Mogućnost ostavljanja otvorene kase nĳe očigledna na dĳagramu stanja 4.11, ali jeste u tabeli

<!-- pdf_page=118 printed_page=104 -->

stanja. Moguća rešenja su da sistem upozori korisnika i spreči zatvaranje programa ili da automatski zatvori kasu.
4.3.4 Testiranje bele kutĳe
tehnike testiranja
Testiranje bele kutĳe podrazumeva detaljno poznavanje unutrašnje strukture softverskog sistema. Test slučajevi se kreiraju na osnovu analize izvornog koda, pri čemu se posebno proučava tok izvršavanja programa. Najčešće ih izrađuju sami programeri tokom razvoja, ali ih mogu pisati i iskusni test inženjeri koji imaju pristup kodu i razumevanje implementacĳe.
testiranje bele kutĳe
Zbog potrebe za dubinskim uvidom u rad sistema, testiranje bele kutĳe je zahtevnĳe i skuplje u poređenju sa tehnikama crne kutĳe. Zato se najčešće primenjuje u sistemima za koje je potrebna visoka pouzdanost i gde su softverske greške posebno skupe.
Cilj ovog testiranja je ispitivanje različitih putanja kroz kôd programa. Putanja (eng. execution path) predstavlja konkretan niz naredbi koje se izvršavaju tokom jednog prolaska kroz program, u zavisnosti od ulaznih podataka i kontrole toka programa. Ključni elementi koji utiču na formiranje putanja su:
-uslovna grananja (na primer, naredbe if i switch), -petlje (na primer, naredbe while, for i do-while), -skokovi (na primer, break, continue, return i
goto),
-pozivi funkcĳa, -izuzeci i obrada izuzetaka (na primer, naredbe
try, catch i finally).
Primer 4.3.13 (Funkcĳa pozitivni) Posmatrajmo kôd funkcĳe koja proverava da li je broj pozitivan.
1 int pozitivni(int a) {
2 if (a > 0)
3 return 1;

<!-- pdf_page=119 printed_page=4 -->

4 return 0;
5 }
Ova funkcĳa ima dve putanje. Prva putanja nakon provere uslova a > 0 (linĳa 2) izvršava naredbu return
1 (linĳa 3). Druga putanja nakon provere uslova a >
0 (linĳa 2) izvršava naredbu return 0 (linĳa 3).
Analogno ispitivanju svih kombinacĳa ulaza kod tehnika zasnovanih na modelu crne kutĳe, može se zahtevati ispitivanje svih putanja kroz program. Međutim, zbog eksponencĳalnog rasta broja mogućih putanja sa porastom složenosti programa, potpuno testiranje svih putanja je u praksi najčešće neizvodljivo.
Primer 4.3.14 (Funkcĳa pozitivni — nastavak primera 4.3.13) Posmatrajmo kôd funkcĳe koja za tri broja računa koliko njih je pozitivno.
1 int pozitivni(int a1, int a2, int a3) {
2 int brojPozitivnih = 0;
3 if (a1 > 0)
4 brojPozitivnih++;
5 if (a2 > 0)
6 pozitivan++;
7 if (a3 > 0)
8 brojPozitivnih++;
9 return brojPozitivnih;
10 }
Broj putanja kroz ovaj program je 23, jer za svaku od tri naredbe grananja imamo opcĳu izvršavanja ukoliko je uslov ispunjen i ukoliko nĳe. Konkretno, to su putanje koje prolaze kroz naredne linĳe koda:
1. 1, 2, 3, 4, 5, 6, 7, 8, 9
2. 1, 2, 3, 4, 5, 6, 7, 9
3. 1, 2, 3, 4, 5, 7, 8, 9
4. 1, 2, 3, 4, 5, 7, 9
5. 1, 2, 3, 5, 6, 7, 8, 9
6. 1, 2, 3, 5, 6, 7, 9
7. 1, 2, 3, 5, 7, 8, 9
8. 1, 2, 3, 5, 7, 9

<!-- pdf_page=120 printed_page=106 -->

Primer 4.3.15 (Funkcĳa pozitivni — nastavak primera 4.3.14) Posmatrajmo kôd funkcĳe koja za niz od 100 brojeva računa koliko njih je pozitivno.
1 int pozitivni(int a[], int n) {
2 int i = 0, brojPozitivnih = 0;
3 while (i < n) {
4 if (a[i] > 0)
5 brojPozitivnih++;
6 }
7 return brojPozitivnih;
8 }
Broj putanja kroz ovaj program je 2100, jer za svaku naredbu grananja imamo opcĳu izvršavanja ukoliko je uslov ispunjen i ukoliko nĳe. Bez pretpostavke da niz ima tačno 100 elemenata, broj putanja kroz ovu funkcĳu zavisi od veličine niza 𝑛i iznosi 2𝑛za fiksiranu vrednost 𝑛.
Primer 4.3.16 (Funkcĳa pozitivni — nastavak primera 4.3.15) Posmatrajmo kôd funkcĳe koja za vrednosti koje se unose sa standardnog ulaza (sve do unosa broja nula) računa koliko njih je pozitivno.
1 int pozitivni() {
2 int broj, brojPozitivnih = 0;
3 do {
4 scanf("%d", &broj);
5 if (broj > 0)
6 brojPozitivnih++;
7 } while (broj!=0);
8 return brojPozitivnih;
9 }
Broj putanja kroz ovaj program zavisi od broja unetih elemenata sa standardnog ulaza i nĳe ograničen.
Zbog velikog broja mogućih putanja i kroz jednostavne programe, umesto testiranja svih mogućih putanja, koriste se metrike pokrivenosti koda kako bi se obezbedio balans između kvaliteta i troškova testiranja. Pre početka testiranja, treba odrediti odgovarajući nivo i vrstu

<!-- pdf_page=121 printed_page=4 -->

pokrivenosti. Osnovni koraci u testiranju bele kutĳe su:
1. Analiza i razumevanje strukture i logike izvornog koda;
2. Kreiranje test primera na osnovu
a) identifikovanih relevantnih putanja i
b) odabranih metrika pokrivenosti;
3. Izvršavanje test primera.
Metrike pokrivenosti koda
Metrike pokrivenosti koda predstavljaju važno sredstvo za procenu kvaliteta testiranja softvera. One pomažu u identifikacĳi delova sistema koji su testirani i onih koji su ostali neprovereni, čime omogućavaju donošenje informisanih odluka o daljem razvoju i unapređenju testne infrastrukture. Metrike pokrivenosti koda koje se najčešće koriste su pokrivenost putanja, naredbi, odluka, uslova, višestrukih uslova i funkcĳa.
Pokrivenost putanja =
Izvršenih putanja
Pokrivenost putanja (eng. path coverage) Mera koja pokazuje koliki je procenat putanja u programu koje su izvršene tokom testiranja. Potpuna pokrivenost znači da je svaka moguća putanja kroz program izvršena bar jednom.
Ukupno putanja × 100%
Pokrivenost naredbi =
Izvršenih naredbi
Pokrivenost naredbi (eng. statement coverage) Mera koja pokazuje koliki je procenat naredbi u programu koje su izvršene tokom testiranja. Potpuna pokrivenost se postiže kada je svaka naredba u programu izvršena bar jednom.
Ukupno naredbi × 100%
Pokrivenost odluka =
Ispitanih odluka
Pokrivenost grana/odluka (eng. branch/decision coverage) Mera koja pokazuje koliki je procenat ishoda odluka testirano u odnosu na ukupan broj odluka u programu. Za potpunu pokrivenost, svaka odluka u kodu mora biti evaluirana bar jednom kao tačna i bar jednom kao netačna.
Ukupno odluka × 100%

<!-- pdf_page=122 printed_page=108 -->

Pokrivenost uslova (eng. condition coverage)‗ Mera koja pokazuje koliki je procenat pojedinačnih logičkih uslova unutar složenĳih izraza (npr. A && B) dobio i tačnu i netačnu vrednost tokom testiranja. Za potpunu pokrivenost, svaki uslov u svakoj odluci u kodu mora biti evaluiran bar jednom kao tačan i bar jednom kao netačan.
Pokrivenost uslova =
Ispitanih uslova
Ukupno uslova × 100%
Pokrivenost višestrukih uslova (eng. multiple condition coverage) Mera koja pokazuje koliki je procenat mogućih kombinacĳa vrednosti pojedinačnih uslova u okviru svake odluke izvršen tokom testiranja. Za potpunu pokrivenost, svaka moguća kombinacĳa vrednosti pojedinačnih uslova za svaku odluku mora biti izvršena bar jednom.
Pokrivenost višestrukih uslova =
Izvršenih kombinacĳa viš. uslova
Ukupno kombinacĳa viš. uslova
×100%
Pokrivenost funkcĳa (eng. function coverage) Mera koja pokazuje koliki je procenat funkcĳa izvršen tokom testiranja. Za potpunu pokrivenost, potrebno je obezbediti da je svaka funkcĳa bar jednom pozvana.
Pokrivenost funkcĳa =
Izvršenih funkcĳa
Ukupno funkcĳa × 100%
Pokrivenost funkcĳa je korisna za osnovnu proveru testne infrastrukture. Ukoliko neka funkcĳa nĳe nikada pozvana tokom testiranja, to znači da taj deo softvera nĳe uopšte pokriven testovima, što može ukazivati na potencĳalne rizike ili nepotrebni (mrtvi) kod.
Najčešće korišćena metrika u praksi je pokrivenost naredbi. Ova metrika je jednostavna za implementacĳu i brzo se izračunava prilikom pokretanja testova pa je njeno izračunavanje podržano u okviru većine modernih razvojnih okruženja. Međutim, pokrivenost naredbi ne odražava složenost logike programa i ne garantuje da su sve bitne situacĳe obuhvaćene testovima.
Za detaljnĳu analizu ponašanja softvera, neophodno je koristiti naprednĳe metrike, kao što je metrika pokrivenosti grana/odluka. Pokrivenost grana pruža uvid u to da li su testovi prošli kroz sve moguće logičke tokove.
‗ Za lakše razumevanje razlika između pokrivenosti odluka, uslova i višestrukih uslova, pogledati primer 4.3.18.

<!-- pdf_page=123 printed_page=4 -->

Primer 4.3.17 (Maksimalna vrednost) Razmotrimo naredni kôd
1 max = b;
2 if (a > max) {
3 max = a;
4 }
Test {a=6, b=3} pokriva sve naredbe (izvršavanje prolazi kroz naredbe 1, 2, 3 i 4), ali ne i sve putanje (nedostaje putanja 1, 2, 4) kao ni sve odluke (odluka u linĳi 2 se razmatra samo kao tačna, ne i kao netačna).
Testovi {a=6, b=3} i {a=3, b=6} pokrivaju i sve naredbe, sve putanje i sve odluke. Dodati drugi test pokriva putanju kroz linĳe 1, 2, 4. Odluka u linĳi 2 u ovom testu ima vrednost netačno.
Međutim, za visokokvalitetno testiranje kao i za kritične delove sistema, gde su greške neprihvatljive ili izuzetno skupe, prati se pokrivenost putanja, uslova i višestrukih uslova. Odabir odgovarajuće metrike treba da zavisi od konteksta upotrebe softvera, njegove složenosti i posledica potencĳalnih grešaka.
Primer 4.3.18 (Inkrementiranje pozitivnih brojeva) Razmotrimo naredni kôd i njegovu pokrivenost testovima.
1 if(a > 0 && b > 0) {
2 a++;
3 b++;
4 }
Test {a=1, b=2} pokriva sve naredbe ali
-ne pokriva sve odluke — nedostaje odluka da uslov 𝑎> 0 && 𝑏> 0 nĳe ispunjen,
-ne pokriva sve uslove — nedostaje da su vrednosti oba podizraza netačne,

<!-- pdf_page=124 printed_page=110 -->

-ne pokriva sve višestruke uslove — nedostaju još tri kombinacĳe vrednosti podrizraza, tj. testovi za koje su vrednosti podrizraza tačno-netačno, netačno-tačno i netačno-netačno,
-ne pokriva sve putanje — nedostaje putanje koja prolazi samo kroz linĳu 1.
Testovi {a=1, b=2} i {a=-1, b=2} pokrivaju sve naredbe, sve odluke i sve putanje, ali
-ne pokrivaju sve uslove — nedostaje da je vrednost podizraza 𝑏> 0 netačna,
-ne pokrivaju sve višestruke uslove — nedostaju još dve kombinacĳe vrednosti podrizraza, tj. testovi za koje su vrednosti podrizraza tačnonetačno i netačno-netačno.
Testovi {a=1, b=2}, {a=-1, b=2} i {a=-1, b=-2} pokrivaju sve naredbe, sve odluke, sve putanje i sve uslove, ali ne pokrivaju sve višestruke uslove, nedostaje kombinacĳa vrednosti podizraza koja odgovara vrednostima tačno-netačno. Testovi {a=1, b=2}, {a=-1, b=2}, {a=-1, b=-2} i {a=1, b=-2} pokrivaju sve naredbe, sve odluke, sve putanje, sve uslove i sve višestruke uslove.
Pokrivenost putanja
Pokrivenost odluka
Odnosi između različitih metrika
Pokrivenost naredbi
Potpuna pokrivenost naredbi podrazumeva potpunu pokrivenost funkcĳa. Potpuna pokrivenost odluka podrazumeva potpunu pokrivenost naredbi, dok potpuna pokrivenost putanja podrazumeva potpunu pokrivenost odluka (slika 4.12).
Pokrivenost funkcĳa
Slika 4.12: Odnosi različitih pokrivenosti počevši od pokrivenosti putanja

<!-- pdf_page=125 printed_page=4 -->

Primer 4.3.19 (Apsolutne vrednosti) Potpuna pokrivenost odluka ne podrazumeva potpunu pokrivenost putanja. Na primer, razmotrimo naredni kôd.
1 if (a < 0) {
2 a = -a;
3 }
4 if (b < 0) {
5 b = -b;
6 }
Test {a=-6, b=-3} pokriva sve naredbe, ali ne pokriva sve odluke niti sve putanje.
Testovi {a=-6, b=-3} i {a=6, b=3} pokrivaju sve naredbe i sve odluke. Međutim, ne pokrivaju sve putanje.
Testovi {a=-6, b=-3}, {a=6, b=3}, {a=-6, b=3} i {a=6, b=-3} pokrivaju sve naredbe, sve odluke i sve putanje.
Takođe, potpuna pokrivenost višestrukih uslova podrazumeva potpunu pokrivenost uslova i potpunu pokrivenost odluka (slika 4.13). Međutim, potpuna pokrivenost uslova i višestrukih uslova nisu u nužnoj vezi sa potpunom pokrivenošću putanja.
Pokrivenost višestrukih uslova
Primer 4.3.20 (Inkrementiranje pozitivnih brojeva — nastavak primera 4.3.18) Razmotrimo naredni kôd i njegovu pokrivenost testovima.
Pokrivenost uslova
1 if(a > 0 && b > 0) {
2 a++;
Pokrivenost odluka
3 b++;
4 }
Slika 4.13: Odnosi različitih pokrivenosti vezanih za uslove u grananjima
5 if(c > 0 && d > 0) {
6 c++;
7 d++;
8 }
Testovi {a=1, b=2, c=3, d=4} i {a=-1, b=2, c=-3, d=4} pokrivaju sve naredbe i sve odluke (ali ne i sve uslove,

<!-- pdf_page=126 printed_page=112 -->

sve višestruke uslove ni sve putanje).
Testovi {a=1, b=2, c=3, d=4} i {a=-1, b=-2, c=-3, d=-4} pokrivaju sve naredbe, sve odluke i sve uslove (ali ne i sve višestruke uslove ni sve putanje).
Testovi {a=1, b=2, c=3, d=4}, {a=1, b=-2, c=3, d=-4}, {a=-1, b=2, c=-3, d=4} i {a=-1, b=-2, c=-3, d=-4} pokrivaju sve naredbe, sve odluke, sve uslove i sve višestruke uslove, ali ne i sve putanje.
Testovi {a=1, b=2, c=3, d=4}, {a=1, b=2, c=-3, d=4}, {a=-1, b=2, c=3, d=4} i {a=1, b=-2, c=3, d=-4} pokrivaju sve naredbe, sve odluke, sve uslove i sve putanje, ali ne i sve višestruke uslove.
Preporučeni nivo pokrivenosti
U praksi, pitanje „Koliki nivo pokrivenosti je dovoljno dobar?“ nema univerzalni odgovor i zavisi od prirode softverskog sistema, njegovog konteksta upotrebe, kritičnosti i ciljeva testiranja. Ipak, industrĳska praksa pokazuje određene smernice koje se često koriste kao polazna tačka.
Na primer, za pokrivenost naredbi, iako se potpuna pokrivenost često postavlja kao cilj, kao preporučeni prag navodi se nivo od 80% do 90%. Ova vrednost predstavlja kompromis između efikasnosti testiranja i troškova njegove realizacĳe. Važno je napomenuti da čak i potpuna pokrivenost ne garantuje odsustvo grešaka. Ona samo znači da je sav kôd bio izvršen tokom testiranja, ali ne i da su obuhvaćeni svi logički putevi,

<!-- pdf_page=127 printed_page=4 -->

uslovi ili granični slučajevi, odnosno logički propusti i dalje mogu ostati neprimećeni. Sa druge strane, nizak nivo pokrivenosti jasno ukazuje na povišen rizik da greške mogu ostati neotkrivene i sugeriše da značajni delovi koda nisu uopšte testirani.
Pokrivenost koda testovima se menja tokom razvoja softvera i dodavanja novih funkcionalnosti. Zbog toga je potrebno redovno merenje i praćenje pokrivenosti koda testovima.
Alati za merenje pokrivenosti koda
Alati za merenje pokrivenosti koda koriste se za analizu koji delovi izvornog koda su bili izvršeni tokom testiranja. Oni predstavljaju ključnu podršku u procesu testiranja softvera, jer omogućavaju jasan uvid u to koliko je testiranje temeljno.
Razlike u pokrivenosti koda su značajne za razumevanje kako dodavanje testova utiče na pokrivenost. Master rad Nikole Perića: Alat za generisanje i prikaz razlika u pokrivenosti koda testovima
Većina alata funkcioniše na osnovu instrumentacĳe — procesa u kojem se u kôd automatski umeću dodatne instrukcĳe koje beleže rezultate izvršavanja. Instrumentacĳa može da se vrši pre ili za vreme procesa kompilacĳe, kao i nakon kompilacĳe, na nivou bajtkoda (npr. za Java programe) ili izvršivog formata (npr. za kompajlirane C/C++ binarne fajlove).
Izvršavanjem instrumentovanog koda nad ulazima koje određuju testovi, prikupljaju se podaci o tome koje su linĳe, grane, uslovi ili funkcĳe izvršeni. Na osnovu tih informacĳa generiše se izveštaj o pokrivenosti, koji pomaže programerima da identifikuju nedovoljno testirane delove sistema. Ovi izveštaji se često vizualizuju kroz procente pokrivenosti i označene delove koda (npr. bojama), kako bi se lakše uočili segmenti koji zahtevaju dodatne testove.

<!-- pdf_page=128 printed_page=114 -->

Izbor relevantnih testova i putanja kroz program
Jedan od ključnih izazova u testiranju metodama bele kutĳe jeste izbor odgovarajućih test primera. Dobar izbor testova treba da obezbedi visok nivo pokrivenosti uz minimalan broj test primera, čime se postiže efikasnost i izbegava redundantnost.
U praksi, preporučuje se korišćenje više jednostavnih i kratkih putanja koje se međusobno razlikuju u malim detaljima, umesto jedne veoma složene putanje. Takav pristup olakšava dĳagnostikovanje grešaka i održavanje testova.
Primer 4.3.21 (Petlje) Petlje u kodu mogu potencĳalno generisati beskonačan broj putanja, pa je važno odabrati reprezentativne slučajeve, kao što su:
-Petlja se preskače (nula iteracĳa). -Petlja se izvršava jednom. -Petlja se izvršava dva puta. -Ako postoji poznat gornji limit 𝑛, izvršavanje 𝑛−1 i 𝑛puta.
Testiranje osnovnih putanja (eng. basis path testing) predstavlja tehniku kojom se osigurava da su sve logičke grane u programu ispitane bar jednom. Ova tehnika se zasniva na analizi grafa toka kontrole (eng. control flow graph) i uključuje sledeće korake:
1. Izgradnja grafa kontrole toka programa iz posmatranog softverskog modula;
2. Izračunavanje ciklomatične kompleksnosti grafa†, označene sa 𝐶;
† Ciklomatična kompleksnost je broj linearno nezavisnih putanja kroz graf. Dve putanje su linearno nezavisne ako postoji bar jedna grana koja se pojavljuje u jednoj putanji, a ne pojavljuje se u drugoj. Ciklomatična kompleksnost se računa kao vrednost izraza 𝐸−𝑁+ 2𝑃gde je 𝐸broj grana u grafu, 𝑁broj čvorova grafa, a 𝑃 broj komponenti povezanosti grafa.

<!-- pdf_page=129 printed_page=4 -->

3. Odabir skupa od 𝐶linearno nezavisnih osnovnih putanja;
4. Kreiranje test primera za svaku osnovnu putanju; 5. Izvršavanje testova i analiza rezultata.
Primena testiranja osnovnih putanja garantuje pokrivenost svih naredbi i svih grana u kodu, jer je skup osnovnih putanja konstruisan tako da pokriva svaki čvor i svaku logičku odluku u grafu toka upravljanja.
Primer 4.3.22 (Osnovne putanje) Naredni graf odgovara grafu kontrole toka programa P.
A
1 2
B
D
5 6
3 4
E
7
8
C
F
9 10
G
Ciklomatična kompleksnost za dati graf je 5, jer je
𝐶= 10 −7 + 2 = 5
Primenimo naredni algoritam odabira 5 linearno nezavisnih osnovnih putanja. U svakom čvoru odluke potrebno je promeniti odluku, počevši od poslednje donete odluke. U skladu sa time, imamo naredne putanje:
1. A, B, C, G
2. A, B, C, B, C, G 3. A, B, E, F, G 4. A, D, E, F, G 5. A, D, F, G

<!-- pdf_page=130 printed_page=116 -->

Glavni izazov ove tehnike leži u pretpostavci da su sve osnovne putanje dostižne i izvodljive. U složenim programima, određene putanje mogu biti logički ili praktično nedostižne zbog međuzavisnosti uslova. Zbog toga je neophodna pažljiva analiza grafa kontrole toka i dodatna provera da izabrane putanje zaista odgovaraju realnim scenarĳima izvršavanja.
Testiranje na osnovu grafa toka podataka (eng. data flow testing) ispituje ispravnost životnog ciklusa promenljivih i upotrebe promenljivih u različitim delovima programa. Tipične anomalĳe u upotrebi podataka uključuju:
-Upotreba neinicĳalizovane promenljive – promenljiva se koristi pre nego što joj je dodeljena vrednost.
-Neiskorišćena definicĳa – promenljiva je definisana i inicĳalizovana, ali se nikada ne koristi.
-Ponovno definisanje – promenljivoj se dodeljuje nova vrednost pre nego što je prethodna upotrebljena.
-Upotreba nakon oslobađanja resursa – promenljiva (ili referenca) se koristi nakon dealokacĳe memorĳe.
-Neusaglašenost dodeljivanja i korišćenja u različitim granama izvršavanja.
Cilj testiranja je osigurati da se sve promenljive koriste na ispravan način — da su inicĳalizovane pre upotrebe, iskorišćene nakon dodeljivanja i oslobođene samo kada više nisu potrebne. Za to je potrebno u kodu identifikovati mesta gde se promenljive definišu i gde se koriste, i kreirati test primere koji pokrivaju tok izvršavanja programa koji prolazi kroz date definicĳe i korišćenja. Ova vrsta testiranja je naročito korisna za otkrivanje suptilnih grešaka koje nisu nužno vidljive kroz standardne tehnike testiranja kontrole toka i često se koristi u bezbednosno kritičnim i složenim sistemima.

<!-- pdf_page=131 printed_page=4 -->

4.3.5 Metamorfno testiranje
Metamorfno testiranje predstavlja tehniku testiranja softverskih sistema koja omogućava proveru ispravnosti bez potrebe za proročištem — komponentom koja određuje da li je rezultat testa ispravan. Umesto toga, koristi se poznavanje osobina sistema koji se testira, odnosno metamorfna svojstava (relacĳe).
Metamorfna relacĳa izražava kako bi se izlaz programa trebalo da promeni kada je ulaz izmenjen na određeni način. Osnovna ideja je da se na osnovu dva ulaza koja su u nekom specifičnom odnosu odredi odnos između odgovarajućih izlaza.
tehnike testiranja
metamorfno testiranje
Primer 4.3.23 (Standardna devĳacĳa) Ukoliko ne možemo da proverimo ispravnost rezultata za računanje standardne devĳacĳe za veoma dugačak niz brojeva, možemo da iskoristimo sledeće odnose (metamorfna svojstva):
-Permutacĳa elemenata ne utiče na standardnu devĳacĳu.
-Množenje svake vrednosti sa -1, ne utiče na standardnu devĳacĳu.
-Ako se svaki broj pomnoži sa nekom konstantom, standardna devĳacĳa novog niza brojeva bi trebalo da je srazmerna standardnoj devĳacĳi originalnog niza.
Testiranjem se proverava da li se za zadate ulaze na očekivani način menjaju izlazi. Testiranjem se detektuje greška u sistemu ukoliko se javi odstupanje u očekivanim odnosima između odgovarajućih izlaza.
Primer 4.3.24 (Standardna devĳacĳa — nastavak primera 4.3.23) Na osnovu identifikovanih metamorfnih relacĳa za algoritam standardne devĳacĳe, možemo da napravimo test primere koji su permutacĳa istog ni-

<!-- pdf_page=132 printed_page=118 -->

za brojeva i da proverimo da li svaki put dobĳemo isti rezultat. Takođe, možemo da napravimo test primere sa skaliranim vrednostima niza i da proverimo da li za dobĳenu devĳacĳu važi da je skalirana u odnosu na devĳacĳu originalnog niza. Na primer, možemo da napravimo naredne testove:
-Test 1: Proveriti za četiri permutacĳe istog niza da li daju isti rezultat.
-Test 2: Proveriti da li se dobĳa isti rezultat za početni niz i za niz u kojem su sve vrednosti pomnožene sa -1.
-Test 3: Proveriti da li su srazmerne devĳacĳe za početni niz, niz u kojem su svi elementi pomnoženi sa 2, i niz u kojem su svi elementi pomnoženi sa -5.
Metamorfno testiranje značajno doprinosi povećanju stepena automatizacĳe u testiranju i omogućava detekcĳu grešaka u situacĳama kada tradicionalne metode nisu primenljive. Za uspešnu primenu metamorfnog testiranja neophodno je:
-dobro razumevanje domena problema, -identifikacĳa relevantnih i pouzdanih metamorfnih svojstava,
-automatizacĳa generisanja izvedenih testova i njihove verifikacĳe.
Ključni korak u primeni metamorfnog testiranja jeste identifikacĳa odgovarajućih metamorfnih relacĳa. Kvalitet i snaga ovih relacĳa direktno utiču na efikasnost testiranja.
Jedan od najkorisnĳih tipova metamorfnih relacĳa je relacĳa ekvivalencĳe. Ova relacĳa podrazumeva da transformisani ulaz mora proizvesti potpuno isti izlaz kao i original, što omogućava jednostavnu i preciznu detekciju nepravilnosti u ponašanju sistema. Zbog svoje stroge prirode, relacĳa ekvivalentnosti omogućava detektovanje širokog spektra grešaka.

<!-- pdf_page=133 printed_page=4 -->

Primer 4.3.25 (Konstrukcĳa kompilatora) Veoma je teško utvrditi ekvivalencĳu između izvornog koda i izvršivog koda. Jedna alternativa je da se u dati izvorni kôd dodaju određene naredbe ili delovi naredbi koje mu ne menjaju semantiku. Na primer, to može biti dodavanje nule izrazu (time se ne menja vrednost izraza) ili dodavanje uslova koji je uvek ispunjen (uslov if (true) ... takođe ne menja semantiku programa). Za tako izmenjene izvorne programe, trebalo bi da bude generisan izvršivi kôd koji se ponaša na isti način kao i početni kôd.
Primer 4.3.26 (Mašinsko učenje — klasifikacĳa slika) Razmotrimo klasifikator slika obučen da prepoznaje kategorĳe objekata na slikama. Jedan primer metamorfnog odnosa je:
Ako se ulazna slika rotira za mali ugao (npr. do 10◦), očekuje se da klasifikacĳa ostane nepromenjena.
Na osnovu ove osobine, moguće je konstruisati sledeći postupak testiranja:
1. Izabrati originalni test primer 𝑥(sliku) za koji klasifikator daje rezultat 𝑓(𝑥).
2. Generisati transformisani primer 𝑥′ (npr. rotacija slike za 5◦).
3. Uporediti rezultate 𝑓(𝑥) i 𝑓(𝑥′); ukoliko se razlikuju, to može ukazivati na potencĳalnu grešku u modelu, ili na potrebu za dodatnim podacima u obuci.
Međutim, u praksi, relacĳa ekvivalencĳe nĳe uvek dostupna metamorfna relacĳa. U tim slučajevima koriste se slabĳe forme, kao što su relacĳe očuvanja određenih karakteristika rezultata ili relacĳe koje predviđaju smer promene izlaza. Pravilna selekcĳa metamorfnih relacĳa zahteva duboko razumevanje testiranog sistema

<!-- pdf_page=134 printed_page=120 -->

i domena primene.
Primer 4.3.27 (Predviđanje cene nekretnine) Sistem predviđa cenu nekretnine na osnovu kvadrature, lokacĳe i broja soba. U slučaju povećanja kvadrature, za isti ili veći broja soba i za nekretninu na istoj lokacĳi, očekuje se povećanje predviđene cene.
Na primer, ako imamo kao ulaz nekretninu koja ima 60m² i tri sobe, za koju sistem predviđa cenu 90.000 evra, onda možemo da kreiramo novi ulaz tako što samo povećamo kvadraturu na 80m². Za ovaj novi ulaz očekujemo da cena treba da bude veća od 90.000 evra. Izlaz se menja, ali postoji logički odnos između prvog i drugog izlaza (monotonost u predikcĳi), što se koristi za proveru ponašanja modela.
### 4.4 Načini sprovođenja testiranja
U procesu testiranja mogu se izdvojiti dve osnovne aktivnosti:
(i) definisanje test primera
(ii) sprovođenje postupka izvršavanja i evaluacĳe tih test primera.
Obe ove aktivnosti, prema načinu na koji se sprovode, mogu biti obavljane manuelno ili automatski. Iako postoje četiri moguće kombinacĳe:
(1) manuelno generisanje testova i manuelno sprovođenje testiranja,
(2) manuelno generisanje testova i automatsko sprovođenje testiranja,
(3) automatsko generisanje testova i manuelno sprovođenje testiranja i
(4) automatsko generisanje testova i automatsko sprovođenje testiranja,
u praksi se (3) obično ne koristi.

<!-- pdf_page=135 printed_page=4 -->

Automatsko generisanje testova
Automatsko izvršavanje testova
Manuelno generisanje testova
Manuelno izvršavanje testova
(2) Poluautomatsko testiranje
(3) Poluautomatsko testiranje
Automatsko generisanje testova
Manuelno izvršavanje testova
Manuelno generisanje testova
Automatsko izvršavanje testova
(4) Automatsko testiranje
(1) Manuelno testiranje
Načini sprovođenja testiranja
Slika 4.14: Načini izvođenja testiranja softvera
4.4.1 Manuelno testiranje
Termin manuelno testiranje podrazumeva da se obe aktivnosti sprovode manuelno, odnosno da testeri smišljaju test slučajeve i samostalno sprovode testiranje i ocenjuju rezultate testiranja. Manuelno testiranje je nezamenjivo u delovima verifikacĳe koji zahtevaju ljudsku percepcĳu, razumevanje konteksta i subjektivnu procenu kvaliteta. Dodatno, manuelno testiranje je ključno u domenu validacĳe softvera, gde je cilj da se utvrdi da li softver zaista zadovoljava potrebe i očekivanja krajnjih korisnika, a ne samo da li funkcioniše prema tehničkim specifikacĳama.
U kontekstu verifikacĳe softvera, primer upotrebe manuelnih tehnika testiranja je istraživačko testiranje, koje se oslanja na iskustvo i intuicĳu testera. Umesto striktno definisanih koraka, tester istražuje softver u realnom vremenu, tražeći neočekivane greške i ponašanja. Automatizacĳa ne može da zameni ovu vrstu kreativnog pristupa.
Manuelnim testiranjem često se proveravaju svojstva ko-

<!-- pdf_page=136 printed_page=122 -->

ja se nalaze na preseku validacĳe i verifikacĳe softvera. Na primer, testiranjem prihvatljivosti, koje obično sprovodi sam korisnik ili predstavnik korisnika, procenjuje se da li je softver upotrebljiv i spreman za puštanje u produkcĳu. Osim što uključuje funkcionalne provere, često podrazumeva i subjektivne ocene o korisničkom iskustvu i interfejsu.
Slično tome, aplikacĳe u realnom vremenu i interaktivne aplikacĳe, poput video igara, sistema za virtuelnu realnost ili specĳalizovanih simulacĳa, zahtevaju manuelnu evaluacĳu ponašanja sistema tokom neposredne upotrebe. U takvim slučajevima, subjektivno korisničko iskustvo ima ključnu ulogu u oceni ispravnosti i kvaliteta softvera.
U kontekstu validacĳe softvera, provera korisničkog interfejsa često zahteva manuelni pristup. Vizuelni aspekti kao što su poravnanje elemenata, čitljivost i jasnoća poruka najbolje se procenjuju ljudskim okom. Automatizovani alati mogu potvrditi prisustvo odgovarajućih elemenata, ali ne i njihovu funkcionalnu ili estetsku vrednost. Slično, testiranja vezana za ocenu naučivosti i intuitivnosti korišćenja fokusiraju se na iskustvo krajnjeg korisnika. Ona ocenjuju koliko je softver jednostavan za učenje i upotrebu, što zahteva direktno posmatranje korisnika, analizu ponašanja i prikupljanje povratnih informacĳa.
4.4.2 Automatsko izvršavanje test primera
Primeri kako automatsko izvršavanje testova ubrzava razvojni ciklus, poboljšava kvalitet koda i osigurava stabilnost aplikacĳa mogu se videti u master radovima Milice Galjak: Automatsko testiranje mobilnih aplikacĳa i Nikole Dimića: Automatsko testiranje mikroservisnih aplikacĳa
Iako manuelno testiranje omogućava uvid u korisničko iskustvo i subjektivne aspekte sistema, ono je često podložno greškama, sporo i teško skalabilno. Zbog toga je automatizacĳa testiranja od ključnog značaja, naročito kod složenih sistema i testova koji se često ponavljaju. Automatizovani testovi smanjuju potrebu za ručnim intervencĳama, ubrzavaju razvoj i unapređuju kvalitet softverskog proizvoda.

<!-- pdf_page=137 printed_page=4 -->

Najčešći oblik automatizovanog testiranja je izvršavanje testova jedinica koda. Ovakvi testovi se često automatski pokreću prilikom svake izmene u kodu, a njihova integracĳa sa alatima za merenje pokrivenosti koda omogućava praćenje kvaliteta testiranja. Postoji veliki broj okruženja za automatsko izvršavanje testova, poznatih po obrascu xxxUnit, gde xxx označava konkretni programski jezik. Na primer, za C++ postoji CppUnit, za Javu JUnit, a za Python PyUnit.
Testiranje veb aplikacĳa Selenium je softver otvorenog koda koji se dominantno koristi za automatizovano testiranje veb aplikacĳa. Selenium podržava testiranje veb aplikacĳa u gotovo svim dostupnim pretraživačima. Test skriptovi mogu biti pisani u različitim programskim jezicima, kao što su C#, Java, Ruby, Python i Perl i pokretani na operativnim sistemima Windows, macOS ili Linux.
Pored alata za izvršavanje testova, postoje i alati koji automatizuju čitav proces testiranja — uključujući upravljanje test slučajevima, integracĳu sa repozitorĳumima koda, praćenje defekata i generisanje izveštaja. Ovi alati su često deo većih razvojnih okruženja ili sistema za kontinuiranu integracĳu.
Kontinuirana integracĳa softvera
Automatizacĳa omogućava brzo, ponovljivo i pouzdano izvršavanje test primera, što je posebno važno u okruženjima kontinuirane integracĳe i isporuke softvera. Kontinuirana integracĳa (eng. continuous integration, CI) predstavlja ključni proces u razvoju softvera, posebno u timovima gde više članova svakodnevno unosi izmene u zajednički kodni repozitorĳum. Cilj kontinuirane integracĳe je da se svaka izmena odmah objedini sa trenutnim stanjem projekta, automatski izgradi i testira, kako bi se potencĳalne greške otkrile što ranĳe.
Popularni alati za kontinuiranu integracĳu su:
Prilikom svakog objedinjavanja koda, sistem prolazi kroz sledeće faze:
-Jenkins -Buildbot -Travis CI -GitLab CI -CircleCI -TeamCity (JetBrains) -Bamboo (Atlassian)
Integracĳa — sve trenutne izmene se spajaju u jedinstvenu verzĳu projekta,
Izgradnja — kôd se kompajlira i pakuje u izvršni fajl ili instalacioni paket,
Testiranje — automatski test primeri se izvršavaju kako bi se proverila ispravnost sistema,

<!-- pdf_page=138 printed_page=124 -->

Arhiviranje — rezultujući artefakti se verzionišu i čuvaju za buduću upotrebu,
Primena — sistem se učitava u okruženje za testiranje ili integracĳu, gde može biti pokrenut i dostupan za evaluacĳu.
Testiranje u okviru kontinuirane integracĳe softvera je često vremenski i memorĳski veoma zahtevno. Jedna opcĳa smanjenja troškova testiranja je selektivno testiranje. Primer selektivnog testiranja može se videti u master tezi Jovane Bošković: Optimizacĳa procesa kontinuirane integracĳe i isporuke kroz selektivno testiranje zasnovano na analizi pokrivenosti koda
Ovakav pristup značajno doprinosi:
-ranom otkrivanju grešaka, -smanjenju troškova projekta, -kraćem vremenu razvoja, -i nižem riziku prilikom isporuke novih verzĳa softvera.
4.4.3 Automatsko generisanje test primera
Generisanje test primera moguće je automatizovati samo za određene vrste testiranja, u kojima se mogu formalno definisati kriterĳumi pokrivenosti i ponašanja sistema. Tipični primeri uključuju testiranje robusnosti i testove usmerene na otkrivanje grešaka u kodu kao što su deljenje nulom, korišćenje neinicĳalizovanih promenljivih ili pristupi nedozvoljenim memorĳskim lokacĳama (vidi poglavlje 9).
Primer automatskog generisanja test primera može se videti u master tezi Ane Ðorđević: Automatsko generisanje test primera uz pomoć statičke analize i rešavača Z3
U ovim scenarĳima, automatizacĳa ima značajnu prednost jer omogućava sistematsko generisanje velikog broja ulaznih podataka uz minimalni ljudski napor. Posebno je korisna za otkrivanje ekstremnih i graničnih slučajeva koji bi lako mogli ostati neotkriveni manuelnim testiranjem. Na primer, alati za rasplinuto testiranje (eng. fuzzing) mogu nasumično, ali ciljno, generisati razne kombinacĳe ulaza, uključujući i one koji izlaze iz uobičajenih opsega, kako bi izazvali neželjeno ili nepredviđeno ponašanje softverskog sistema.
Primer implementacĳe rasplinutog testiranja može se videti u master tezi Ane Mitrović: Primena jezika Skala u paralelizacĳi rasplinutog testiranja
Slično tome, statička analiza softvera omogućava identifikacĳu potencĳalno problematičnih mesta u kodu, kao što su upotreba promenljivih pre dodeljivanja vrednosti ili dereferenciranje null pokazivača. Na osnovu tih nalaza, mogu se automatski generisati test primeri koji

<!-- pdf_page=139 printed_page=4 -->

ciljano testiraju te kritične tačke i tako povećavaju verovatnoću otkrivanja grešaka u ranim fazama razvoja.
Međutim, kada se radi o testiranju složenih funkcionalnosti koje zavise od višeslojnih uslova, konteksta upotrebe ili korisničkih odluka, automatizovano generisanje test primera postaje izuzetno izazovno, a često i neizvodljivo. U takvim situacĳama, uspešno testiranje zahteva duboko razumevanje poslovne logike, očekivanog ponašanja sistema u realnim scenarĳima, kao i interakcĳa među različitim komponentama softvera. Ove aspekte je teško formalizovati na način koji bi omogućio automatsko pouzdano i smisleno generisanje kvalitetnih test primera. Zbog toga se u praksi automatizovano generisanje testova najefikasnĳe koristi kao dopuna manuelnom procesu.
Rezime
-Testiranje softvera ima za cilj da otkrĳe defekte u softveru.
-Poželjno je ispravljanje grešaka u početnim fazama razvoja softvera.
-Testiranje mogu da obavljaju i programeri i testeri. -Proces testiranja obuhvata planiranje, analizu, dizajn, implementacĳu, evaluacĳu, izvršavanje i zatvaranje procesa testiranja
-Osnovna podela testiranja je na testiranje funkcionalnih i nefunkcionalnih karakteristika softvera.
-Prema nivou testiranja, razlikujemo testove jedinice koda, komponentne, integracione i sistemske testove.
-Nefunkcionalno sistemsko testiranje uključuje testiranje performansi, kompatibilnosti, pouzdanosti, upotrebljivosti, bezbednosti, sigurnosti i prenosivosti.
-U sistemsko testiranje se ubrajaju i istraživačko testiranje, testiranje prihvatljivosti i instalaciono testiranje.

<!-- pdf_page=140 printed_page=126 -->

-Regresiono testiranje predstavlja proces ponovnog izvršavanja prethodno uspešno završenih testova.
-Pokrivenost testiranjem je metrika koja pomaže da se proceni koliko su testovi sveobuhvatni.
-Tehnike testiranja se dele na testiranje crne kutĳe, testiranje bele kutĳe i testiranje sive kutĳe.
-Metamorfno testiranje je pristup testiranju pri postojanju problema proročišta.
-Testiranje može da bude manuelno i automatizovano.
Literatura
[1] Paul Ammann i Jeff Offutt. Introduction to Software Testing. Cambridge University Press, 2017. doi:
10.1017/9781316771273.
[2] Boris Beizer. Software Testing Techniques. 2. izdanje. Van Nostrand Reinhold, 1990.
[3] Robert Binder. Testing Object-Oriented Systems. Addison-Wesley, 1999.
[4] Koen Claessen i John Hughes. QuickCheck: A Lightweight Tool for Random Testing of Haskell Programs. U: ACM SIGPLAN Notices 35.9 (2000.), str. 268–279. doi: 10.1145/357766.351266.
[5] Gordon Fraser i Andrea Arcuri. A Large-Scale Evaluation of Automated Unit Test Generation Using EvoSuite. U: ACM Transactions on Software Engineering and Methodology 24.2 (2014.). doi:
10.1145/2685612.
[6] Barton P. Miller, Lars Fredriksen i Bryan So. An Empirical Study of the Reliability of UNIX Utilities. U: Communications of the ACM 33.12 (1990.), str. 32–44. doi: 10.1145/96267.96279.
[7] Glenford J. Myers, Corey Sandler i Tom Badgett. The Art of Software Testing. 3. izdanje. Wiley, 2011. isbn: 9781118031964.

<!-- pdf_page=141 printed_page=127 -->

Ispitna pitanja
10. Testiranje u razvoju softvera. Cena greške u kontekstu vremena otkrivanja.
11. Testiranje u razvoju softvera. Uloga testera u razvoju softvera.
12. Testiranje u razvoju softvera. Faze testiranja softvera: planiranje, analiza, dizajn i implementacĳa testova.
13. Testiranje u razvoju softvera. Faze testiranja softvera: izvršavanje i evaluacĳa testova. Zatvaranje testiranja.
14. Vrste testiranja. Testiranje jedinica koda. Primeri. 15. Vrste testiranja. Komponentno i integraciono testiranje. Primeri.
16. Vrste testiranja. Sistemsko testiranje. Funkcionalno sistemsko testiranje. Regresiono testiranje. Primeri.
17. Vrste testiranja. Sistemsko testiranje. Istraživačko testiranje. Testovi prihvatljivosti. Instalaciono testiranje. Primeri.
18. Vrste testiranja. Nefunkcionalno testiranje. Testovi performansi. Testovi kompatibilnosti. Testovi pouzdanosti. Primeri.
19. Vrste testiranja. Nefunkcionalno testiranje. Testovi upotrebljivosti. Testovi bezbednosti. Testovi sigurnosti. Testovi prenosivosti. Primeri.
20. Tehnike testiranja. Karakteristike dobrog skupa testova. Pokrivenost testiranjem. Podela na tehnike testiranja.
21. Tehnike testiranja. Testiranje metodama crne kutije. Isprobavanja svih mogućih ulaza. Metod klasa ekvivalencĳe. Primeri.
22. Tehnike testiranja. Testiranje metodama crne kutĳe. Metod klasa ekvivalencĳe. Metod graničnih vrednosti. Primeri.
23. Tehnike testiranja. Karakteristike dobrog skupa testova. Tabele odlučivanja. Primeri.
24. Tehnike testiranja. Karakteristike dobrog skupa testova. Dĳagrami stanja. Tabele stanja. Primeri.

<!-- pdf_page=142 printed_page=128 -->

25. Tehnike testiranja. Testiranje metodama bele kutĳe. Putanja i broj putanja u programu. Pojam i vrste pokrivenosti. Njihovi odnosi. Primeri.
26. Tehnike testiranja. Testiranje metodama bele kutĳe. Pojam i vrste pokrivenosti. Preporučen nivo pokrivenosti. Alati za merenje pokrivenosti. Primeri.
27. Tehnike testiranja. Testiranje metodama bele kutije. Izbor relevantnih testova i putanja. Testiranje osnovnih putanja. Testiranje na osnovu grafa toka podataka. Primeri.
28. Tehnike testiranja. Problem proročišta. Metamorfno testiranje. Primeri.
29. Načini testiranja. Manuelno testiranje. 30. Načini testiranja. Automatsko izvršavanje i evaluacĳa testova. Kontinuirana integracĳa.
31. Načini testiranja. Automatsko generisanje test primera.

<!-- pdf_page=143 printed_page=143 -->

— If Broken it is, Fix it You Should — (Yoda, Star Wars)
5.1 Veza izvršivog koda i debagera 130
5.2 Vrste debagovanja . . . . . . . . 136
Pregled
5.3 Primeri debagera . . . . . . . . . 147
-Kada se u okviru testiranja otkrĳe da postoji defekt u radu softvera, kako pronaći grešku koja je uzrokovala taj defekt?
5.4 Otvoreni problemi . . . . . . . . 152
5.5 Štampanje umesto debagera153
-Koja je uloga debagovanja u procesu razvoja softvera?
-Zašto je debager sistemski alat? -Koje vrste debagovanja postoje? -Koje alternative debagovanju postoje?
Debagovanje je proces u razvoju softvera koji ima za cilj pronalaženje greške odnosno uzroka defekta u programu. Debager (eng. debugger) je alat koji se koristi za praćenje izvršavanja programa radi boljeg razumevanja ponašanja programa i lakšeg pronalaženja greške u programu.
Kako bi informacĳe koje debager pruža programeru bile precizne i razumljive, neophodna je podrška kompajlera i linkera, koji obezbeđuju povezivanje izvršivog koda sa izvornim kodom, kao i razne druge korisne podatke. Funkcionalnost debagera takođe zavisi od podrške operativnog sistema, a u određenim slučajevima i samog hardvera.
Poznati debager GDB, koji se razvĳa u okviru projekta GNU, se može koristiti kroz veliki broj razvojnih okruženja, uključujući QtCreator, Visual Studio Code, Eclipse, NetBeans, CLion i IntelliJ.
Debageri se često integrišu u razvojna okruženja koja im obezbeđuju grafički korisnički interfejs. Iako grafički interfejs može znatno olakšati upotrebu i unaprediti korisničko iskustvo, važno je imati na umu da je ono samo sredstvo interakcĳe sa debagerom, a ne njegov suštinski deo. Sama funkcionalnost debagera ostaje nezavisna od načina na koji se korisniku prikazuje.

<!-- pdf_page=144 printed_page=130 -->

### 5.1 Veza izvršivog koda i debagera
Tokom kompilacĳe softverskog projekta dostupne su brojne opcĳe i podešavanja koja omogućavaju precizno upravljanje načinom prevođenja izvornog koda u izvršivi program. Ova podešavanja se često koriste za optimizacĳu performansi, lakše pronalaženje grešaka, ili prilagođavanje ciljnim platformama.
Režim kompilacĳe je skup opcĳa kompilacĳe koje se često zajedno koriste sa određenim ciljem. Postoje:
režim prevođenja za upotrebu (eng. release mode), skraćeno režim riliz — to je svaki režim koji ima za cilj dobĳanje optimizovane izvršive verzĳe namenjene krajnjem korisniku,
režim prevođenja za pronalaženje grešaka (eng. debug mode), skraćeno režim debag — to je režim prevođenja koji ima za cilj dobĳanje izvršive verzĳe programa namenjene programeru radi lakšeg otkrivanja grešaka u kodu i
kombinovani režim koji odgovara kombinacĳi odabranih opcĳa režima za prevođenje za upotrebu i režima za pronalaženje grešaka — ovaj režim se koristi u situacĳama kada je potrebno naći grešku u programu, a režim prevođenja za pronalaženje grešaka ne daje željene rezultate.
Na program koji se dobĳa prevođenjem za upotrebu često se referiše sa riliz verzĳa programa, dok se na program koji se dobĳa prevođenjem za pronalaženje grešaka referiše sa debag verzĳa programa.
Nakon generisanja izvršive verzĳe programa, moguće je primeniti specĳalizovane alate koji modifikuju izvršivi kôd sa ciljem otežavanja i ometanja debagovanja‗. Ovakve tehnike se nazivaju anti-debagovanje (eng. antidebugging) i koriste se radi zaštite intelektualne svojine,
‗ Iako anti-debagovanje može da se koristi na svakoj izvršivoj verzĳi programa, ima ga smisla koristiti samo nad programima koji su prevedeni u riliz režimu.

<!-- pdf_page=145 printed_page=5 -->

kako bi se sprečilo analiziranje logike programa i krađa koda, ili pak u zlonamernom softveru, kako bi se onemogućilo prepoznavanje i analiziranje malicioznog ponašanja.
Debager se može koristiti za svaku izvršivu verzĳu programa. Mogućnosti i informacĳe koje se dobĳaju za debag verzĳu su povezane sa izvornim kodom i olakšavaju programeru da poveže stanje izvršavanja sa izvornim kodom. S druge strane, informacĳe koje debager može da pruži za riliz verzĳu su često samo uvid u asemblerski kôd, na isti način kao što ih vidi i procesor. U slučaju primene anti-debagovanja, mogućnosti debagera su dodatno ograničene.
5.1.1 Režim prevođenja za upotrebu
Primarni cilj prevođenja u režimu za upotrebu jeste postizanje visoke efikasnosti izvršavanja kroz različite strategĳe optimizacĳa koje sprovodi kompajler. Ove optimizacĳe mogu uključivati uklanjanje nepotrebnog koda, preuređivanje instrukcĳa radi boljeg iskorišćenja procesora, zamenu složenĳih konstrukcĳa bržim ekvivalentima, kao i umetanje funkcĳa. Kao rezultat, generisani izvršivi kôd je kompaktnĳi i brži u odnosu na verzĳu prevedenu u režimu za uklanjanje grešaka.
Režim prevođenja za upotrebu podrazumeva optimizacĳe koje kao primarni cilj imaju optimizacĳu brzine izvršavanja programa. Međutim, za neke aplikacĳe, na primer za one koje se izvršavaju na uređajima sa malom količinom memorĳe, neophodne su optimizacĳe koje se odnose na smanjivanje veličine izvršive datoteke kao i upotrebe memorĳe u fazi izvršavanja. Režim prevođenja za upotrebu u ovom slučaju se naziva režim prevođenja za upotrebu sa minimalnom veličinom (eng. minimum size release mode).
Sprovedene optimizacĳe smanjuju mogućnost povezivanja izvršivog koda sa izvornim datotekama. Neki delovi

<!-- pdf_page=146 printed_page=132 -->

koda se mogu potpuno izostaviti, promeniti redosled ili transformisati do neprepoznatljivosti, što značajno otežava proces razumevanja izvršavanja koda i traženja greške u kodu. Zbog toga se ova verzĳa prevođenja gotovo nikada ne koristi za analizu i dĳagnostiku grešaka.
Primer 5.1.1 (Prevođenje za upotrebu) Prilikom prevođenja programa pomoću kompajlera gcc, ne postoji jedinstvena opcĳa za režim prevođenja za upotrebu, već se to postiže kombinovanjem odgovarajućih kompajlerskih opcĳa. Ove opcĳe uključuju korišćenje visokog nivoa optimizacĳe, na primer -O2 ili -O3, dok se za režim za upotrebu sa minimalnom veličinom koristi opcĳa optimizacĳe -Os. Dodatno, druga bitna opcĳa je -DNDEBUG. Ova opcĳa definiše makro
NDEBUG, koji onemogućava izvršavanje poziva funkcĳe assert(), čĳa je upotreba karakteristična u fazi otklanjanja grešaka.
S druge strane, u mnogim sistemima za izgradnju koda, izbor režima može da se uključi jedinstvenom opcĳom. Na primer, u sistemu CMake, koristi se opcĳa
-DCMAKE_BUILD_TYPE koja se za režim prevođenja za upotrebu postavlja na vrednost Release, a za režim prevođenja za upotrebu sa minimalnom veličinom postavlja na vrednost MinSizeRel.
5.1.2 Režim prevođenja za pronalaženje grešaka
Primarni cilj prevođenja u režimu za pronalaženje grešaka je pravljenje izvršive verzĳe koda koja za svaku instrukcĳu u fazi izvršavanja omogućava preciznu povezanost sa odgovarajućim linĳama izvornog koda. Kompajler u ovom režimu generiše dodatne informacĳe koje omogućavaju debageru da poveže izvršavane instrukcĳe sa odgovarajućim linĳama izvornog koda.
Za razliku od režima riliz, gde su uključene optimizacĳe radi postizanja što efikasnĳeg izvršavanja, u režimu

<!-- pdf_page=147 printed_page=5 -->

debag su te optimizacĳe isključene ili svedene na minimum kako bi se očuvala što preciznĳa veza između izvornog i izvršivog koda. Zbog odsustva optimizacĳa, izvršiva datoteka generisana u režimu debag najčešće je znatno veća od datoteke prevedene u režimu riliz†. Takođe, izvršavanje programa prevedenog u ovom režimu može biti primetno sporĳe i manje efikasno u pogledu iskorišćenja memorĳe. Međutim, ta neefikasnost je prihvatljiva u fazi razvoja, jer omogućava precizno praćenje toka izvršavanja i stanja promenljivih.
Primer 5.1.2 (Prevođenje za pronalaženje grešaka) Prilikom prevođenja programa pomoću kompajlera
gcc, ne postoji jedinstvena opcĳa za režim prevođenja za pronalaženje grešaka, ali se to postiže kombinovanjem opcĳe koja uključuje korišćenje najnižeg nivoa optimizacĳe -O0 i opcĳe -g koja uključuje upisivanje informacĳa za debagovanje u izvršivu datoteku.
Kao što je pomenuto, u mnogim sistemima za izgradnju koda, izbor režima može da se uključi jedinstvenom opcĳom. U sistemu CMake, opcĳa -DCMAKE_-
BUILD_TYPE se za režim prevođenja za pronalaženje grešaka postavlja na vrednost Debug.
Formati za predstavljanje pomoćnih informacĳa
Formati za predstavljanje pomoćnih informacĳa potrebnih za debagovanje preciziraju način na koji kompajler može da zapiše podatke kao što su nazivi funkcĳa, nazivi promenljivih, tipovi podataka, odgovarajuće linĳe iz izvorne datoteke i slično. Najpoznatĳi formati za predstavljanje pomoćnih informacĳa potrebnih za debagovanje su format DWARF i format Microsoft CodeView. Ovi formati nisu kompatibilni.
† Izvršiva datoteka može biti značajno veća i iz drugih razloga. Na primer, informacĳe u formatu DWARF se upisuju direktno u izvršivu datoteku.

<!-- pdf_page=148 printed_page=134 -->

Iako je format DWARF nezavisan od formata izvršive datoteke, najčešće se koristi uz format za izvršive i povezane datoteke ELF (eng. Executable and Linkable Format) u okviru UNIX-olikih operativnih sistema, kao što su Linux i macOS. Format DWARF se može koristiti prilikom prevođenja programa koji su napisani u različitim programskim jezicima — npr. C, C++ i Fortran, a karakteristike formata omogućavaju i proširenja za dodatne jezike i njihove specifične konstrukte, ukoliko je to potrebno. Za format DWARF je karakteristično da se metapodaci koje on definiše umeću direktno u izvršivi kôd, što čini debag verzĳu programa dodatno većom u odnosu na riliz verzĳu koja te podatke ne sadrži.
DWARF je dizajniran kao nezavisan format, ali u slično vreme sa formatom za izvršive i povezane datoteke ELF. ELF na engleskom znači vilenjak, dok DWARF znači patuljak. Nazivi DWARF i ELF su uklopljeni kao skladni delovi epske fantastike. Ipak, kasnĳe je predložen odgovarajući akronim i za format DWARF — Debugging With Arbitrary Record Formats (debagovanje sa proizvoljnim formatima zapisa).
Primer 5.1.3 (Format DWARF) Kompajleri kao što su GCC i Clang generišu informacĳe u formatu DWARF i njih mogu da koriste debageri GDB i LLDB.
Operativni sistem Windows koristi sopstveni format za pomoćne informacĳe Microsoft CodeView, koji je integrisan u Majkrosoftove razvojne alate. Ovaj format koristi se prilikom prevođenja programa koji su napisani u programskim jezicima C, C++ i jezicima .NET platforme. Metapodaci u formatu CodeView se distribuiraju odvojeno od izvršivog koda (u okviru datoteka sa ekstenzĳom pdb). Oni se koriste po potrebi, ne opterećuju izvršivi kôd, ali se učitavaju u debager prilikom debagovanja.
Primer 5.1.4 (Format Microsoft CodeView) Kompajler MSVC (kompajler Microsoft Visual Studio C++) generiše podatke u formatu Microsoft CodeView i njih mogu da koriste debageri WinDbg i Visual Studio Debugger.
5.1.3 Kombinovani režimi prevođenja
Moguće je da ponašanje programa dobĳenih u režimima debag i riliz bude različito, što može značajno otežati

<!-- pdf_page=149 printed_page=5 -->

proces otklanjanja grešaka. Na primer, može se desiti da se određene greške ispoljavaju isključivo u riliz verzĳi, dok se u debag verzĳi program izvršava ispravno. Ovakva situacĳa može imati više uzroka.
Poboljšavanju korisničkog iskustva prilikom korišćenja debagera nad optimizovanom verzĳom programa aktivno doprinose Ðorđe Todorović & Nikola Prica, diplomirani master studenti Matematičkog fakulteta:
Jedan od mogućih razloga je to što debag verzĳa sadrži dodatne informacĳe, kao i inicĳalizacĳu memorĳe koju riliz verzĳa ne poseduje. Time se greška može privremeno „zamaskirati“, iako je prisutna u izvornom kodu. S druge strane, uzrok može biti i greška u kompajleru, koja se manifestuje tokom optimizacĳe prilikom generisanja riliz verzĳe. Iako su ovakve greške izuzetno retke, one i dalje predstavljaju ozbiljan problem jer zahtevaju pronalaženje zaobilaznog rešenja kako bi se dobila ispravna optimizovana verzĳa programa.
-Debug info in optimized code - how far can we go? Improving LLVM debug info with function entry values
https://www.
youtube.com/watch?
v=1cWAmLMF1eI
-Improving Debug Information in LLVM to Recover Optimized-out Function Parameters
U oba opisana slučaja, debagovanje debag verzĳe programa ne može otkriti uzrok problema, dok je debagovanje riliz verzĳe otežano zbog nepostojanja veze između izvornog i izvršivog koda. Zbog toga se u savremenom razvoju softvera sve više ulaže u unapređenje mogućnosti za debagovanje optimizovanog koda, a problemu se pristupa upotrebom hibridnog režima kompilacĳe, u kojem se optimizacĳe kombinuju sa zadržavanjem debag informacĳa (onoliko koliko to optimizacĳe dozvoljavaju).
https://www.
youtube.com/watch?
v=ih5v65K10M8
Doprinos unapređenju korisničkog iskustva pri debagovanju dao je i Vladimir Vuksanović, diplomirani master student Matematičkog fakulteta. Njegov master rad: Unapređenje infrastrukture LLVM čuvanjem originalne lokacĳe pri debagovanju izdvojenog koda
Primer 5.1.5 (Kombinovani režim prevođenja) Kombinovani režim prevođenja, za kompajler gcc, podrazumeva viši stepen optimizacĳe, na primer -O2 kao i opcĳu koja uključuje informacĳe za debagovanje
-g. Dodatno, uključuje se i opcĳa -DNDEBUG kako bi izvršavanje bilo više nalik izvršavanju koje se dobĳa sa režimom prevođenja za upotrebu.
Ovakav režim prevođenja u sistemu CMake može se postići postavljanjem opcĳe -DCMAKE_BUILD_TYPE na vrednost RelWithDebInfo.

<!-- pdf_page=150 printed_page=136 -->

5.1.4 Anti-debagovanje
Mogućnost debagovanja izvršive verzĳe programa nije uvek poželjna osobina, naročito u kontekstu zaštite intelektualne svojine, bilo radi zaštite od neovlašćenog kopiranja (eng. software copy protection) ili radi sprečavanja obrnutog inženjeringa (eng. reverse engineering). U takvim slučajevima, primenjuju se različite tehnike poznate pod nazivom anti-debagovanje. Tehnike antidebagovanja se koriste i u malicioznim programima, gde služe kao sredstvo za izbegavanje analize i prepoznavanje od strane antivirusnih alata i sistema za detekcĳu pretnji.
Anti-debagovanje obuhvata implementacĳu jedne ili više metoda čĳi je cilj da ometaju ili potpuno onemoguće pokušaje debagovanja ciljanog procesa. Ove tehnike mogu uključivati detekcĳu prisustva debagera, izmenu toka izvršavanja u slučaju da je debager prisutan, korišćenje specifičnih instrukcĳa koje se ponašaju drugačĳe u prisustvu nadgledanja, kao i tehnike obfuskacĳe‡.
Iako tehnički sofisticirano, anti-debagovanje uvek predstavlja balans između zaštite i funkcionalnosti. Prekomerna zaštita može negativno uticati na stabilnost, efikasnost i održivost softverskog proizvoda.
### 5.2 Vrste debagovanja
Debagovanje možemo podeliti na interaktivno debagovanje, udaljeno debagovanje i debagovanje nakon prekida izvršavanja programa (post-mortem debagovanje). Debager može da započne proces i da prati njegovo izvršavanje, može da prati izvršavanje procesa koji je
‡ Obfuskacĳa ne menja funkcionalnost programa, već samo način na koji je on predstavljen i uključuje preimenovanje simbola, dodavanje beskorisnog (mrtvog) koda, dinamičko generisanje koda i šifrovanje delova koda ili podataka (kôd se generiše ili dešifruje tokom izvršavanja, umesto da bude prisutan u izvršivoj datoteci, kako bi se sprečila statička analiza koda).

<!-- pdf_page=151 printed_page=5 -->

već započeo sa radom kao i da analizira stanje programa nakon što je program završio sa radom.
5.2.1 Interaktivno debagovanje
Interaktivnodebagovanje podrazumeva dinamičku analizu programa u realnom vremenu uz aktivno učešće programera, koji koristi debager da bi pratio i kontrolisao tok izvršavanja aplikacĳe. Ovaj način debagovanja omogućava dvosmernu komunikacĳu sa debagerom, putem komandne linĳe ili grafičkog korisničkog interfejsa.
Osnovni mehanizam interaktivnog debagovanja zasniva se na tačkama prekida (eng. breakpoints), koje omogućavaju da se izvršavanje programa automatski pauzira na odabranoj linĳi koda. Kada izvršavanje programa dođe do linĳe koda na kojoj je postavljena tačka prekida, debager omogućava inspekcĳu promenljivih, sadržaja steka, registara i drugih komponenti stanja programa. Nakon analize, izvršavanje može biti nastavljeno, korak po korak (naredbe koje se nazivaju na engleskom step i next) ili do sledeće tačke prekida.
Primer 5.2.1 (Funkcĳa ptrace) Debageri su sistemski zavisni alati. Za razumevanje funkcionisanja debagera potrebno je razumeti procese i sistem prekida na odgovarajućem operativnom sistemu.
Pod operativnim sistemom Linux, za rad debagera od suštinske važnosti je sistemska funkcĳa ptracea. Korišćenjem sistemskog poziva ptrace, jedan proces, upravljački proces, najčešće debager, može da kontroliše drugi, ciljni proces, i da upravlja njegovim unutrašnjim stanjem. Debageri koriste funkcĳu ptrace kako bi mogli da zaustavljaju program, da posmatraju memorĳu zaustavljenog programa i da je menjaju.
a ptrace je skraćeno od „pratilac procesa” (eng. process trace).

<!-- pdf_page=152 printed_page=138 -->

Pored običnih tačaka prekida, moguće je postavljati i uslovne tačke prekida koje se aktiviraju samo kada je ispunjen određeni logički uslov. Na taj način se izvršavanje ne zaustavlja pri svakom prolazu, već samo kada je stanje sistema relevantno za otkrivanje greške.
Primer 5.2.2 (Implementacĳa tačaka prekida) Kada se postavi prekidna tačka u programu sa željom da se na tom mestu zaustavi program, debager zameni odgovarajuću instrukcĳu instrukcĳom prekida, pri čemu sačuva i originalnu instrukcĳu. Kada se prilikom izvršavanja programa naiđe na instrukcĳu prekida, desi se hardverski izuzetak, operativni sistem zaustavlja rad procesa i obaveštava o tome debager.
Debager najpre proverava da li je prekid u listi očekivanih prekida koje je postavio debager (tj. da li je u pitanju namerno zaustavljanje ili greška u originalnom kodu). Ukoliko je greška u originalnom kodu, onda se dopusti da se ta greška i izvrši.
Ukoliko je u pitanju tačka prekida koju je postavio debager, onda debager na tom mestu omogući uvid u sve vrednosti fizičkih registara procesa kao i u stanje memorĳe. Debager prikazuje pročitane informacĳe o procesu povezane sa informacĳama o izvornom kodu koje su generisali kompajler i/ili linker prilikom prevođenja programa.
Kada korisnik želi da nastavi sa izvršavanjem,
1. debager zameni instrukcĳu prekida originalnom instrukcĳom,
2. izvrši je, 3. zameni ponovo originalnu instrukcĳu instrukcĳom prekida,
4. prepusti dalje kontrolu programu.
Ukoliko je u pitanju uslovna prekidna tačka, debager proverava uslov i u slučaju da uslov nĳe ispunjen, preskače se zaustavljanje i prikaz stanja memorĳe

<!-- pdf_page=153 printed_page=5 -->

već se samo nastavlja dalje sa izvršavanjem procesa. Ukoliko uslov jeste ispunjen, debager zaustavlja rad procesa i prikazuje relevantne informacĳe, kao i za obične tačke prekida.
Savremeni debageri omogućavaju i postavljanje tačaka posmatranja (eng. watchpoint) nad određenim lokacĳama u memorĳi. Kada se sadržaj označene memorĳske lokacĳe promeni, debager automatski pauzira izvršavanje programa, čime se olakšava praćenje neželjenih ili neočekivanih promena podataka u toku rada aplikacĳe. Ova tehnika se naročito koristi kod analize grešaka izazvanih nepredviđenim upisima u memorĳu, kao što su prekoračenje bafera (eng. buffer overflow) ili konkurentni pristupi deljenim resursima.
Primer 5.2.3 (Hardver — specĳalni registri za debagovanje) Za efikasno funkcionisanje, debager može da koristi i direktno neke funkcionalnosti hardvera, ukoliko su dostupne. Na primer, tačke posmatranja omogućavaju praćenje vrednosti neke promenljive u memorĳi, tj. da li se neka vrednost u memorĳi menja ili se sa nje nešto čita. Ukoliko postoji podrška hardvera (specĳalni registri koji pamte i proveravaju odgovarajuće adrese), biće podignut izuzetak koji će debager da obradi. Ukoliko to nĳe dostupno ili se zahteva praćenje većeg broja vrednosti nego što je to dostupno podrškom hardvera, onda debager mora da izvršava instrukcĳu po instrukcĳu i da za svaku proverava šta se dešava na traženim memorĳskim lokacĳama, što značajno usporava izvršavanje.
Interaktivno debagovanje omogućava precizno i fleksibilno praćenje toka izvršavanja, što je od izuzetne važnosti u složenim programima gde je ponašanje teško predvideti. Kroz kombinacĳu pauziranja, ispitivanja i nastavljanja rada, programer stiče detaljan uvid u ponašanje softverskog sistema i može efikasno identifikovati greške.

<!-- pdf_page=154 printed_page=140 -->

Primer 5.2.4 (Interaktivno debagovanje: gdb iz komandne linĳe) Analizirajmo program maksimum_niza.c interaktivnim debagerom gdb.
1 #include <stdio.h>
2
3 int maksimum_niza(int* niz, size_t velicina_niza
) {
4 int max = niz[0];
5 for (size_t i = 1; i < velicina_niza; i++) {
6 int tekuci = niz[i];
7 if (tekuci > max) {
8 max = tekuci;
9 }
10 }
11 return max;
12 }
13
14 int main() {
15 int niz[] = {8,1,16,0,256,5};
16 int max = maksimum_niza(niz, sizeof(niz)/
sizeof(int));
17
18 printf("maksimum = %i\n", max);
19 return 0;
20 }
Najpre je potrebno prevesti program (nivo optimizacĳe -O0 je podrazumevan pa se može i izostaviti) i pokrenuti debager.
1 gcc -g -O0 maksimum_niza.c -o maksimum_niza
2 gdb maksimum_niza
Nakon toga, pokreće se debager gdb koji štampa svoju pozdravnu poruku. Nakon toga je dostupan prompt za komunikacĳu.
1 ...
2 Reading symbols from maksimum_niza...
3 (gdb)
Osnovna komanda je komanda run koja će pokrenuti i izvršiti program
1 (gdb) run

<!-- pdf_page=155 printed_page=5 -->

2 Starting program: /home/matf/Desktop/
maksimum_niza
3 maksimum = 256
4 [Inferior 1 (process 42904) exited normally]
5 (gdb)
Komandom
1 break
možemo postaviti tačku prekida na željeni broj linĳe koda ili na željenu funkcĳu. Na primer,
1 break maksimum_niza
će postaviti tačku prekida na početak izvršavanja funkcĳe maksimum_niza. Naredba
1 run
će pokrenuti izvršavanje programa i zaustaviti se na linĳi 3 (jer je tu postavljena tačka prekida, tj. tu je početak funkcĳe maksimum_niza). Komandom
1 next
prelazimo na narednu naredbu programa, linĳu 4. Komandom
1 info locals
možemo videti vrednost svih lokalnih promenljivih. Komandom
1 info args
možemo videti vrednost argumenata funkcĳe.
1 (gdb) break maksimum_niza
2 Breakpoint 1 at 0x1169: file maksimum_niza.c,
line 3.
3 (gdb) run
4 Starting program: /home/matf/Desktop/
maksimum_niza
5
6 Breakpoint 1, maksimum_niza (niz=0xf0,
velicina_niza=93824992231488) at
maksimum_niza.c:3
7 3 int maksimum_niza(int* niz, size_t
velicina_niza) {
8 (gdb) next
9 4 int max = niz[0];

<!-- pdf_page=156 printed_page=142 -->

10 (gdb) next
11 5 for (size_t i = 1; i < velicina_niza; i
++) {
12 (gdb) info locals
13 i = 140737488346839
14 max = 8
15 (gdb) next
16 6 int tekuci = niz[i];
17 (gdb) info locals
18 tekuci = 0
19 i = 1
20 max = 8
21 (gdb) info args
22 niz = 0x7fffffffded0
23 velicina_niza = 6
Uslovne tačke prekida postavljaju se dodavanjem uslova prekida. Na primer, komandom
1 break 6 if i==3
prekidamo izvršavanje na linĳi 6 ukoliko je vrednost promenljive i jednaka 3. Slično, komandom
1 watch max
možemo da prekinemo izvršavanje svaki put kada se promeni vrednost promenljive max. Komandom
1 info break
možemo da vidimo koje su sve prekidne tačke trenutno postavljene u programu.
1 (gdb) break 6 if i==3
2 Breakpoint 2 at 0x55555555518c: file
maksimum_niza.c, line 6.
3 (gdb) watch max
4 Hardware watchpoint 3: max
5 (gdb) info break
6 Num Type Disp Enb Address
What
7 1 breakpoint keep y 0
x0000555555555169 in maksimum_niza at
maksimum_niza.c:3
8 breakpoint already hit 1 time

<!-- pdf_page=157 printed_page=5 -->

9 2 breakpoint keep y 0
x000055555555518c in maksimum_niza at
maksimum_niza.c:6
10 stop only if i==3
11 3 hw watchpoint keep y
max
Komandom
1 continue
nastavljamo izvršavanje programa do prve naredne prekidne tačke.
1 (gdb) continue
2 Continuing.
3
4 Hardware watchpoint 3: max
5
6 Old value = 8
7 New value = 16
8 maksimum_niza (niz=0x7fffffffded0, velicina_niza
=6) at maksimum_niza.c:5
9 5 for (size_t i = 1; i < velicina_niza; i
++) {
10 (gdb) continue
11 Continuing.
12
13 Breakpoint 2, maksimum_niza (niz=0x7fffffffded0,
velicina_niza=6) at maksimum_niza.c:6
14 6 int tekuci = niz[i];
15 (gdb) info locals
16 tekuci = 16
17 i = 3
18 max = 16
Dodatno, savremeni debageri pružaju i niz naprednih mogućnosti koje prevazilaze klasično postavljanje tačaka prekida i izvršavanje koda korak po korak. Jedna od značajnih funkcionalnosti jeste mogućnost izmene koda u toku izvršavanja (eng. hot code replacement), što omogućava programeru da prilagodi ili ispravi deo programa bez potpunog zaustavljanja i ponovnog pokretanja izvršavanja. Ova osobina značajno ubrzava razvoj i testiranje, naročito u kompleksnim sistemima sa dugim vremenom pokretanja. Još jedna napredna

<!-- pdf_page=158 printed_page=144 -->

tehnika jeste debagovanje unazad (eng. reverse debugging), koje omogućava programeru da prati izvršavanje koda unazad, analizirajući operacĳe koje su dovele do određenog stanja.
5.2.2 Udaljeno debagovanje
Pored interaktivnog debagovanja koje se sprovodi na lokalnoj mašini, često se koristi i udaljeno debagovanje (eng. remote debugging). Ova tehnika podrazumeva interaktivno debagovanje pri čemu se aplikacĳa izvršava na jednom sistemu — ciljnom sistemu, dok se proces debagovanja obavlja sa drugog sistema — udaljenog sistema. Povezivanje se ostvaruje preko mreže koristeći odgovarajuće protokole i servise.
Udaljeno debagovanje omogućava da debager sa udaljenog računara upravlja izvršavanjem programa na ciljnom sistemu, postavlja tačke prekida, ispituje vrednosti promenljivih i dobĳa informacĳe o stanju memorĳe i registara ciljne aplikacĳe. Ova tehnika je naročito korisna u scenarĳima kada ciljni sistem ima ograničene resurse i ne može lokalno izvršavati debager, što je čest slučaj kod uređaja sa ugrađenim računarom (eng. embedded systems), kao i prilikom razvoja sistema za koje nĳe lako obezbediti direktni fizički pristup, kao što su IoT (eng. internet of things) platforme ili sistemi u produkcionom okruženju.
Primer 5.2.5 (Udaljeno debagovanje korišćenjem debagera gdb) Korišćenjem alata gdb na udaljenom sistemu i servisa gdbserver na ciljnom sistemu, moguće je uspostaviti vezu između razvojne stanice i ciljnog sistema, čime se omogućava upravljanje izvršavanjem programa sa udaljene lokacĳe. Da bi udaljeno debagovanje bilo moguće, potrebno je da ciljna i udaljena arhitektura budu iste, ili da debager na udaljenom sistemu ima podršku za arhitekturu ciljnog sistema

<!-- pdf_page=159 printed_page=5 -->

(npr. multiarch podrška za debager gdb). Dodatno, mrežna povezanost između dva sistema treba da bude stabilna i odgovarajuće konfigurisana (na primer, često se koristi protokol TCP/IP).
5.2.3 Debagovanje nakon prekida izvršavanja programa
Doprinos unapređenju debagovanja nakon prekida izvršavanja programa alatom gdb dao je Ðorđe Todorović, diplomirani master student Matematičkog fakultata. Njegov master rad: Podrška za naprednu analizu promenljivih lokalnih za niti pomoću alata GNU GDB
Debagovanje nakon prekida izvršavanja programa ili post-mortem debagovanje je tehnika analize ponašanja programa nakon što je njegovo izvršavanje već prekinuto, najčešće usled greške kao što su pristup nevažećoj memorĳi ili neobrađen izuzetak. Za razliku od interaktivnog debagovanja, koje se sprovodi tokom izvršavanja programa, post-mortem debagovanje se oslanja na informacĳe koje su zabeležene u trenutku prekida, bez mogućnosti ponovnog pokretanja aplikacĳe u istom stanju. Post-mortem debagovanje je posebno važno u produkcionim okruženjima, gde se greške moraju analizirati bez direktnog ponovnog izvršavanja programa u identičnim uslovima.
Za post-mortem debagovanje ključnu ulogu imaju tzv. core dump datoteke, koje sadrže snimak memorĳe procesa u trenutku njegovog pada, uključujući relevantne informacĳe kao što su sadržaj steka, registra, segmenta podataka i koda. Da bi se generisala core dump datoteka prilikom prekida rada programa usled kritične greške, potrebna su dodatna podešavanja u okviru operativnog sistema pošto je najčešće opcĳa generisanja ove datoteke podrazumevano isključena.
Tehnike post-mortem analize uključuju:
-pregled sadržaja memorĳe i registara, -rekonstrukcĳu steka poziva funkcĳa (eng. backtrace),
-utvrđivanje poslednjih instrukcĳa koje su se izvršile,
-uvid u vrednosti promenljivih u trenutku prekida,

<!-- pdf_page=160 printed_page=146 -->

-analizu sistemskih logova i izlaznih datoteka.
Debageri kao što su GDB, LLDB i WinDbg podržavaju post-mortem debagovanje.
Primer 5.2.6 (Datoteka core dump) Naredni jednostavan program izaziva grešku Segmentation fault zbog derefernciranja NULL pokazivača u linĳi 6.
1 // crash.c
2 #include <stdio.h>
3
4 int main() {
5 int *p = NULL;
6 *p = 42;
7 return 0;
8 }
Ukoliko se program prevede sa
1 gcc -g crash.c -o crash
i pokrena sa
1 ./crash
dobĳa se poruka
1 Segmentation fault (core dumped)
Standardna podešavanja većine Linux distribucĳa podrazumevaju da se core dump datoteka ne generiše, ali se to može promeniti podešavanjima sistema koja zavise od distribucĳe i verzĳe same distribucĳe. Pored ostalog, potrebno je podesiti da veličina core dump datoteke ne bude ograničena. Na primer, u okviru Linux distribucĳe Ubuntu, to se radi komandom ulimit -c
unlimited. Takođe, potrebno je pokrenuti odgvarajući sistemski servis za generisanje core dump datoteka kao i pronaći lokacĳu gde se core dump datoteka smešta (ili namestiti da se on smesti u isti direktorĳum kao i izvršiva datoteka).
Ime core dump datoteke može da bude u različitim formatima. Na primer, ako se generisana datoteka zove
core.24122.crash.1750685973 i ako se nalazi u istom direktorĳumu, onda se deba-

<!-- pdf_page=161 printed_page=5 -->

gerom gdb post-mortem debagovanje može pokrenuti na sledeći način
1 gdb ./crash core.24122.crash.1750685973
Debager gdb će, nakon standardne uvodne poruke, odštampati sledeće
1 Reading symbols from ./crash...
2 [New LWP 24122]
3 Core was generated by ‘./crash’.
4 Program terminated with signal SIGSEGV,
Segmentation fault.
5 #0 0x0000562e1631313d in main () at crash.c:6
6 6 *p = 42;
7 (gdb)
Ova poruka govori da je do greške došlo u linĳi broj 6 programa crash i prikazuje nam sadržaj te linĳe (*p = 42;). Takođe, saznajemo i da je program završen sa signalom SIGSEGV koji odgovara grešci tipa Segmentation fault. Dalje u okviru prompta debagera možemo da koristimo standardne komande, na primer štampanje vrednosti promenljivih (print p) ili tekućih registara (info registers) u trenutku kada je došlo do greške.
1 (gdb) print p
2 $1 = (int *) 0x0
3 (gdb) info registers
4 rax 0x0 0
5 rbx 0x562e16313150
94755940806992
6 ...
### 5.3 Primeri debagera
Debagovanje se najčešće dovodi u vezu sa tradicionalnim sistemskim i imperativnim programskim jezicima kao što su C i C++. Međutim, odgovarajući alati postoje i za druge programske jezike i paradigme.
Upotreba debagera u različitim jezicima ima mnogo zajedničkih osobina: uobičajene funkcionalnosti uključuju postavljanje i uklanjanje tačaka prekida, koračanje

<!-- pdf_page=162 printed_page=148 -->

naredbu po naredbu, ispitivanje vrednosti promenljivih i stanja memorĳe, kao i praćenje kontrole toka izvršavanja. Iako se sintaksa i interfejs mogu razlikovati, osnovni principi debagovanja ostaju isti i čine sastavni deo efikasnog procesa razvoja softvera.
Primer 5.3.1 (Debager gdb) Debager gdb je jedan od najpoznatĳih i najmoćnĳih alata za debagovanje. On omogućava interaktivno debagovanje, udaljeno debagovanje i debagovanje nakon prekida rada programa. Dodatno, multiarch gdb omogućava pokretanje i analizu izvršivih datoteka namenjenih procesorskim arhitekturama koje su različite od one na kojoj se debagovanje izvršava.
Gdb je napisan u programskom jeziku C i kontinuirano se razvĳa kao deo GNU projekta. Podržava debagovanje programa napisanih u više programskih jezika, uključujući Ada, C, C++, Objective-C, Pascal, Fortran, Go, Rust i Java. GDB se može integrisati u veliki broj različitih razvojnih okruženja, kao što su Eclipse, Visual Studio, Qt Creator i CLion. Takođe, gdb je dostupan na velikom broju operativnih sistema, uključujući razne Unix i GNU/Linux distribucĳe, kao i Microsoft Windows platforme.
Primer 5.3.2 (Debager LLDB) Debager LLDB je savremeni debager koji se razvĳa kao deo projekta LLVM, sa ciljem da ponudi efikasnu, modularnu i proširivu alternativu tradicionalnim alatima za debagovanje. LLDB omogućava interaktivno debagovanje. U dizajniranju ovog debagera, fokus je bio na ostvarivanje brzine, lake nadogradivosti i mogućnosti integracĳe sa modernim alatima.
LLDB je implementiran u programskom jeziku C++ i kontinuirano se razvĳa u okviru razvoja kompajlerske infrastrukture LLVM, odakle i koristi veliki broj

<!-- pdf_page=163 printed_page=5 -->

komponenti. Podržani programski jezici uključuju C, C++, Objective-C i Swift. LLDB se može integrisati u različita razvojna okruženja, kao što su Xcode, CLion, Qt creator i Visual Studio Code.
Debager je prvenstveno razvĳan za Unix-olike operativne sisteme, uključujući macOS i Linux, ali je u poslednjim verzĳama proširena i podrška za Microsoft Windows, iako još uvek u nešto manjoj meri nego kod debagera GDB. LLDB ima poseban značaj u ekosistemu Apple platformi, gde predstavlja podrazumevani debager u razvoju aplikacĳa za macOS, iOS i srodne sisteme.
Primer 5.3.3 (Debageri Visual Studio Debugger i WinDbg) Debagere Visual Studio Debugger i WinDbg razvĳa kompanĳa Microsoft. Oba su namenjena za rad u okviru Windows operativnih sistema i pored podrške za jezike C i C++, imaju podršku i za programske jezike zasnovane na .NET platformi (uključujući, na primer, C#, Visual Basic i F#). Oba alata podržavaju interaktivno debagovanje i post-mortem analizu.
Visual Studio Debugger je duboko integrisan u grafičko razvojno okruženje Visual Studio i prvenstveno je namenjen razvoju korisničkih aplikacĳa, pri čemu nudi intuitivni korisnički interfejs, automatsku inspekciju vrednosti, vizuelno upravljanje tačkama prekida i druge udobnosti grafičkog korisničkog interfejsa koje ga čine pogodnim za svakodnevni razvoj aplikacĳa.
Debager WinDbg je manje poznat u širem krugu programera u poređenju sa debagerom Visual Studio Debugger, ali predstavlja naprednĳi alat sa širim spektrom mogućnosti, posebno u kontekstu sistemskog debagovanja. WinDbg nudi preciznĳu kontrolu i detaljnĳi uvid u sistemski kontekst, što ga čini pogodnim za analizu modula kernela, drajvera, sistemskih komponenti i složenih grešaka koje se ne mogu lako otkriti

<!-- pdf_page=164 printed_page=150 -->

putem standardnog razvojnog okruženja. Koristi se kao samostalna aplikacĳa, često iz komandne linĳe, i zahteva viši nivo tehničkog znanja.
Primer 5.3.4 (Debageri za programski jezik Java) Za programski jezik Java dostupan je debager jdb koji je deo standardne Java distribucĳe. Debager jdb se može koristiti iz komandne linĳe na sličan način kao i gdb, omogućavajući interaktivno debagovanje (postavljanje tačaka prekida, koračanje kroz kôd i ispitivanje vrednosti promenljivih). Takođe, može se integrisati u razvojna okruženja poput Eclipse i IntelliJ IDEA, što omogućava grafički interfejs i lakšu upotrebu. Iako je jdb namenski alat za Javu, moguće je koristiti za Javu i druge debagere u kombinacĳi sa specifičnim podešavanjima i prevodiocima koji generišu izvršivi kôd. Na primer, debager gdb može da se koristi u kombinacĳi sa kompajlerom Native Image koji je sastavni deo kompajlerske infrastrukture GraalVM.
Primer 5.3.5 (Debageri za programski jezik Python) Za skript jezike takođe postoje odgovarajući debageri. Na primer, programski jezik Python ima standardni modul pdb, koji omogućava interaktivno debagovanje direktno iz terminala ili integracĳu u razvojne alate. Modul pdb podržava osnovne debagerske funkcĳe: postavljanje tačaka prekida, koračanje kroz kôd i inspekcĳu stanja programa.
Primer 5.3.6 (Debageri za programski jezik Go) Standardno okruženje za razvoj u jeziku Go ne dolazi sa ugrađenim interaktivnim debagerom. Programi napisani u programskom jeziku Go mogu se debagovati debagerom gdb, ali uz ograničene mogućnosti zbog modela konkurentnosti koji jezik Go koristi. Najzna-

<!-- pdf_page=165 printed_page=5 -->

čajnĳi i najrasprostranjenĳi alat za debagovanje Go programa je Delve koji omogućava standardne funkcionalnosti interaktivnih debagera. Delve se može integrisati sa mnogim popularnim razvojnim okruženjima i editorima, uključujući Visual Studio Code (preko ekstenzĳe za Go) i GoLand, koji razvĳa kompanĳa JetBrains.
Primer 5.3.7 (Debageri za programski jezik JavaScript) Debagovanje JavaScript koda podržano je kroz širok spektar alata, kako integrisanih u same veb pregledače, tako i kroz zasebna razvojna okruženja i pomoćne biblioteke. Najrasprostranjenĳi i najčešće korišćeni debagerski alati za JavaScript su ugrađeni direktno u moderne veb pregledače kao što su Google Chrome, FireFox, Safari i Microsoft Edge.
Primer 5.3.8 (Debageri za programski jezik Haskell) Debagovanje Haskell programa razlikuje se od debagovanja u imperativnim jezicima zbog njegove funkcionalne prirode i podrške lenjom izračunavanju. U ovom jeziku prioritet ima razumevanje evaluacĳe izraza i praćenje toka podataka kroz čiste funkcĳe, pa su alati za debagovanje posebno prilagođeni tim konceptima.
Najpoznatĳi i najčešće korišćeni alat za debagovanje Haskell programa jeste GHCi Debugger, koji dolazi kao deo standardnog kompajlera GHCi i koji omogućava standardno interaktivno debagovanje: postavljanje tačaka prekida u funkcĳama i praćenje evaluacĳe izraza korak po korak.
Pored GHCi debagera, programeri se često oslanjaju i na alate Haskell Tracer Hat i Hoed koji se najviše koriste za post-mortem analizu izvršavanja Haskell programa.

<!-- pdf_page=166 printed_page=152 -->

### 5.4 Otvoreni problemi
Protivnici debagera Iako velika većina programera koristi debagere, postoji izvesan broj značajnih programera koji ne vole debagere i glasno se izjašnjavaju protiv njihove upotrebe:
Iako je debagovanje ključna tehnika za analizu izvršavanja programa, primenljivost debagera je ograničena. Jedan od najizraženĳih problema upotrebe debagera javlja se kod debagovanja višenitnih aplikacĳa. Zbog konkurentnog izvršavanja više niti, greške mogu zavisiti od redosleda izvršavanja koji se teško reprodukuje. Debageri često ne uspevaju da precizno upravljaju svim nitima istovremeno, a samo pokretanje aplikacĳe u debageru može promeniti ponašanje programa i redosled izvršavanja niti, prikrivajući probleme poput trke za resursima i međusobnog blokiranja. Iako savremeni debageri podržavaju praćenje pojedinačnih niti, njihova primena u kompleksnim višenitnim sistemima ostaje nepraktična, neprecizna i često nedovoljna. Zbog toga se pronalaženje grešaka u ovakvim aplikacĳama uglavnom oslanja na kombinovanje više tehnika. Tehnike uključuju dinamičke pristupe: logovanje, profajliranje, upotrebu specĳalizovanih sanitajzera za otkrivanje konkurentnih grešaka ali i statičku analizu (na primer, tehniku proveravanje modela).
Rob Pike, jedan od autora programskog jezika Go, kaže sledeće If you dive into the bug, you tend to fix the local issue in the code, but if you think about the bug first, how the bug came to be, you often find and correct a higher-level problem in the code that will improve the design and prevent further bugs.
Linus Torvalds, kreator operativnog sistema Linux, ne koristi debager.
Robert C. Martin, jedan od autora agilnog programiranja, kaže sledeće Debuggers are a wasteful timesink.
Distribuirane aplikacĳe predstavljaju dodatni izazov, jer njihovo izvršavanje uključuje više nezavisnih komponenti koje rade na različitim fizičkim mašinama. Tradicionalni debageri nisu dizajnirani za takav kontekst i ne omogućavaju jedinstveno praćenje toka izvršavanja u svim delovima sistema.
Debagovanje je takođe problematično u sistemima sa ugrađenim računarom i aplikacĳama koje rade u realnom vremenu, gde ograničenja resursa i strogi vremenski zahtevi ne dozvoljavaju pauziranje programa ili umetanje dodatnog koda za analizu. U takvim okruženjima debager može biti nepristupačan, a njegovo korišćenje može dovesti do narušavanja funkcionalnosti sistema.
Važno ograničenje odnosi se i na debagovanje aplikacĳa koje su prevedene u režimu za upotrebu. Optimizacĳe

<!-- pdf_page=167 printed_page=5 -->

koje vrši kompajler menjaju strukturu izvršivog koda: uklanjaju se delovi koda, funkcĳe se spajaju ili reorganizuju, čime se narušava mogućnost jasnog povezivanja sa izvornim kodom što čini debagovanje značajno otežanim.
Na kraju, kod veoma velikih i kompleksnih sistema, količina podataka i broj međusobno povezanih komponenti često prevazilaze mogućnosti praćenja putem debagera. U takvim slučajevima, debagovanje postaje sporo, nepregledno i nedovoljno skalabilno.
Zbog svega navedenog, debagovanje se u praksi često kombinuje sa drugim tehnikama: logovanjem, automatskim testiranjem, statičkom analizom i specĳalizovanim alatima za otkrivanje specifičnih vrsta grešaka. Razumevanje ograničenja debagovanja je ključno kako bi se odabrala odgovarajuća strategĳa za ispitivanje i ispravljanje softverskih problema.
### 5.5 Štampanje umesto debagera
Štampanje vrednosti promenljivih pomoću funkcĳe
Print umesto debagera
print (odnosno funkcĳe koja vrši štampanje) predstavlja jednu od prvih tehnika debagovanja koju većina programera usvaja. Razlog za to je jednostavnost — tehnika je intuitivna, lako primenljiva i ne zahteva poznavanje dodatnih alata.
Brian W. Kernighan,
koautor knjige Programski jezik C i pionir u razvoju operativnog sistema Unix, čĳi su radovi oblikovali savremeno sistemsko programiranje, tvrdi: The most effective debugging tool is still careful thought, coupled with judiciously placed print statements.
Ova metoda podrazumeva umetanje naredbe za štampanje u ključne delove programa, kako bi se:
-prikazale trenutne vrednosti promenljivih, -pratila kontrola toka (npr. ulazak u funkcĳu, izvršavanje određenih grana uslova, izlazak iz petlji),
-uočili neočekivani rezultati tokom izvršavanja.
Guido van Rossum, autor programskog jezika Python, koristi poziv funkcĳe print za 90% svog debagovanja.
Na primer, ako program proizvodi netačan rezultat, programer može umetnuti štampanje unutar petlje ili grane uslova kako bi ispratio kako se vrednosti promenljivih menjaju. Ovo omogućava osnovni uvid u ponašanje

<!-- pdf_page=168 printed_page=154 -->

programa bez potrebe za korišćenjem spoljašnjih alata za debagovanje.
Primer 5.5.1 (Print za debagovanje) Funkcĳa suma_-
niza dopunjena je sa pozivom funkcĳe printf unutar petlje koji služi za praćenje trenutnog indeksa, vrednosti elementa niza i trenutne sume. Ovo pomaže da se uoče greške, npr. ako petlja ide van granica ili ako se neka vrednost ne sabira kako treba.
1 int suma_niza(int niz[], int duzina) {
2 int suma = 0;
3 for (int i = 0; i < duzina; i++) {
4 printf("niz[%d]=%d, suma=%d\n", i, niz[i],
suma);
5 suma += niz[i];
6 }
7 return suma;
8 }
Uprkos dostupnosti savremenih i veoma moćnih alata za debagovanje, upotreba štampanja za praćenje toka izvršavanja programa i dalje je široko rasprostranjena. Jedan od osnovnih razloga za to jeste jednostavnost umetanja funkcĳe print nasuprot nepoznavanja upotrebe alata za debagovanje.
Oslanjanje na štampanje kao zamenu za debager danas se smatra prevaziđenim pristupom iz više razloga:
-Svaka izmena u vidu umetanja poziva funkcĳe za štampanje zahteva ponovno prevođenje programa, što je kod većih projekata vremenski zahtevno.
-Umetanje poziva funkcĳe za štampanje može promeniti raspored memorĳe programa i time prikriti ili izmeniti ponašanje greške.
-Štampanjem se ne mogu lako ispratiti svi relevantni aspekti stanja programa, kao što su sadržaji registara, vrednosti pokazivača ili stanja steka.
-Štampanje ne omogućava zaustavljanje programa, niti interaktivno ispitivanje stanja promenljivih.

<!-- pdf_page=169 printed_page=5 -->

Uprkos tim nedostacima, štampanje ostaje važna dopunska tehnika jer mogu postojati i opravdani razlozi za upotrebu štampanja umesto debagera. To su, na primer:
-nepostojanje debagera za određenu platformu ili arhitekturu, i
-slučajevi kada i sam debager svojim prisustvom menja ponašanje programa i time otežava detekcĳu greške.
U takvim situacĳama, štampanje može predstavljati poslednje dostupno sredstvo za ispitivanje izvršavanja programa.
Primer 5.5.2 (Štampanje u programskom jeziku Haskell) Iako postoje specĳalizovani alati za debagovanje Haskell programa, programeri često pribegavaju i osnovnim tehnikama poput umetanja funkcĳa za ispis (trace) iz paketa Debug.Trace kako bi pratili tok evaluacĳe izraza prilikom izvršavanja programa.
Uporedna analiza korišćenja debagera i štampanja data je u tabeli 5.1. Iako korisna, tehnika štampanja ne može zameniti funkcionalnosti modernih debagera i trebalo bi je koristiti kao dopunu, tj. kao pragmatičnu i ponekad neizbežnu pomoćnu tehniku, ali nikako kao osnovnu metodu za analizu ponašanja programa.

<!-- pdf_page=170 printed_page=156 -->

Tabela 5.1: Poređenje pristupa: print i debager
Print Debager
Zahteva izmene u izvornom kodu i ponovno prevođenje
Omogućava analizu bez izmena izvornog koda
Statičan — unapred definisano šta se prikazuje
Dinamičan — moguće je menjati prikazane informacĳe u realnom vremenu
Može prikriti greške ili uticati na izvršavanje programa
Može prikriti greške ili uticati na izvršavanje programa, ali ređe i manje
Uvek moguće koristiti Nekada debager nĳe dostupan
Pruža delimičan uvid u stanje programa
Pruža kompletan uvid u stanje programa
Jednostavno za upotrebu Kompleksno za upotrebu za početnike
Pogodno za jednostavne analize izvršavanja programa
Pogodno za kompleksne analize izvršavanja programa
Rezime
-Debager je sistemski alat koji se koristi za praćenje izvršavanja programa u kojem je potrebno identifikovati greške.
-Rad debagera se oslanja na operativni sistem, hardver i kompajler.
-Tri osnovna režima prevođenja su režim prevođenja za upotrebu, režim prevođenja za pronalaženje grešaka i kombinovani režim.
-Tehnike anti-debagovanja se koriste radi ometanja ili otežavanja procesa debagovanja.
-Interaktivno debagovanje je osnovni pristup debagovanju koji obuhvata postavljanje tačaka prekida i tačaka posmatranja, i izvršavanje programa korak po korak.
-Udaljeno debagovanje podrazumeva interaktivno debagovanje pri čemu se aplikacĳa koja se debaguje izvršava na jednom, a debager na drugom

<!-- pdf_page=171 printed_page=157 -->

sistemu.
-Debagovanje nakon prekida izvršavanja programa omogućava uvid u stanje memorĳe nakon prekida izvršavanja programa u situacĳama kada se greške moraju analizirati bez direktnog ponovnog izvršavanja programa u identičnim uslovima.
-Najpoznatĳi debageri su gdb, lldb, Visual Studio Debugger i WinDbg.
-Debagovanje ima niz ograničenja i ne može se uvek primeniti.
-Štampanje umesto debagovanja je tehnika koja se smatra prevaziđenom i koju treba koristiti samo kada ne postoji alternativa.
Literatura
[1] David J. Agans. Debugging. Amacom, 2002. isbn: 9780814471685.
[2] Holger Cleve i Andreas Zeller. Locating causes of program failures. U: Proceedings of the 27th International Conference on Software Engineering. ICSE ’05. St. Louis, MO, USA: ACM, 2005., str. 342– 351. doi: 10.1145/1062455.1062522.
[3] James A. Jones i Mary Jean Harrold. Empirical evaluation of the tarantula automatic fault-localization technique. U: Proceedings of the 20th IEEE/ACM International Conference on Automated Software Engineering. ASE ’05. Long Beach, CA, USA: ACM, 2005., str. 273–282. doi: 10.1145/1101908.
1101949.
[4] Andreas Zeller. Why Programs Fail. Morgan Kaufmann, 2009. isbn: 978-0-12-374515-6. doi: 10.1016/
B978-0-12-374515-6.X0000-7.
[5] Andreas Zeller i Ralf Hildebrandt. Simplifying and Isolating Failure-Inducing Input. U: IEEE Transactions on Software Engineering 28.2 (2002.), str. 183– 200. doi: 10.1109/32.988498.

<!-- pdf_page=172 printed_page=158 -->

Ispitna pitanja
32. Debagovanje. Veza izvršivog koda i debagera. Režim prevođenja za upotrebu. Primeri.
33. Debagovanje. Veza izvršivog koda i debagera. Režim prevođenja za pronalaženje grešaka. Formati za predstavljanje pomoćnih informacĳa. Primeri.
34. Debagovanje. Veza izvršivog koda i debagera. Kombinovani režimi prevođenja. Primeri.
35. Debagovanje. Veza izvršivog koda i debagera. Anti-debagovanje.
36. Debagovanje. Vrste debagovanja. Interaktivno debagovanje. Implementacĳa interaktivnog debagovanja, tačaka prekida i tačaka posmatranja. Primeri.
37. Debagovanje. Vrste debagovanja. Udaljeno debagovanje. Debagovanje nakon prekida izvršavanja programa. Primeri.
38. Debagovanje. Primeri debagera. 39. Debagovanje. Otvoreni problemi. 40. Debagovanje. Štampanje umesto debagera. Primeri.

<!-- pdf_page=173 printed_page=173 -->

Pregled
6.1 Instrumentacĳa 160
6.2 Profajleri . . . . 166
-Šta je instrumentacĳa i kako se ona koristi? -Koja je uloga profajliranja, a koja sanitiziranja u procesu razvoja softvera?
6.3 Alati za dinamičku detekcĳu grešaka . . . . . 183
-Koje vrste profajlera postoje? -Koji su najpoznatĳi sanitajzeri i šta oni omogućavaju?
U procesu razvoja softvera, naročito složenih i zahtevnih sistema, neophodno je osigurati efikasnost i pouzdanost krajnjeg proizvoda. Za postizanje ovih ciljeva koriste se različiti alati za dinamičku analizu programa i detekcĳu grešaka, od kojih se izdvajaju profajleri i sanitajzeri. Ovi alati omogućavaju detaljno praćenje ponašanja softvera tokom njegovog izvršavanja, ali na drugačĳi način u odnosu na debagere.
Profajleri prikupljaju informacĳe o performansama programa — na primer, koliko često se izvršavaju određene funkcĳe, koliko vremena se troši u različitim delovima koda i koliko se memorĳe i ostalih resursa koristi. Profajleri se koriste kada postoje problemi sa performansama i kada je potrebno optimizovati kôd, najčešće u kasnijim fazama razvoja, kada su osnovne funkcionalnosti sistema implementirane.
Sanitajzeri, s druge strane, fokusirani su na automatsku detekcĳu grešaka koje mogu dovesti do nestabilnosti, kvarova ili sigurnosnih propusta. Oni identifikuju probleme kao što su pristupi neinicĳalizovanoj ili nealociranoj memorĳi, curenje memorĳe ili greške u pristupu podacima kod višenitnih aplikacĳa. Sanitajzeri se mogu koristiti da olakšaju pronalaženje uzroka uočenog defekta u kodu, ali i za proveru da li kôd sadrži greške čak i onda kada nema uočenih defekata. Sanitajzeri mogu

<!-- pdf_page=174 printed_page=160 -->

da se koriste i u ranĳim fazama razvoja, odnosno nĳe neophodno čekati na potpunu implementacĳu funkcionalnosti sistema. Naziv sanitajzer vezuje se za porodicu alata koji rade u fazi kompilacĳe. Pored sanitajzera, postoji i veliki broj drugih alata koji imaju za cilj otkrivanje sličnih vrsta grešaka. Većina tih alata je komercĳalne prirode.
U tabeli 6.1 data je uporedna analiza profajlera i alata za dinamičku detekcĳu grešaka. Razumevanje rada i primene profajlera i alata za dinamičku detekcĳu grešaka predstavlja osnovu za efikasno testiranje, analizu i unapređenje softverskih sistema.
Tabela 6.1: Poređenje profajlera i detektora grešaka
Karakteristika Profajleri Dinamička detekcĳa grešaka
Cilj upotrebe Za odabir delova koda koji treba optimizovati
Za otkrivanje grešaka u kodu
Šta meri ili prati Vreme izvršavanja, broj poziva funkcĳa, memorĳska potrošnja, promašaji u keš memorĳi...
Neispravni pristupi memorĳi, curenja memorĳe, nesinhronizovan pristup podacima u višenitnim aplikacĳama, neinicijalizovane promenljive...
Vrsta analize Kvantitativna: koliko se šta koristi?
Kvalitativna: da li postoje greške, koje i gde?
Faza razvoja U kasnim fazama, kada je funkcionalnost implementirana
U ranim fazama
Primeri alata gprof, perf, VTune, Callgrind, Cachegrind, Java Flight Recorder, Visual Studio Profiler, Instruments, dotTrace, cProfile, JProfiler, YourKit
Sanitajzeri: ASan, MSan, TSan, UBSan. Alati: Memcheck, Massif, Helgrind, DRD, BoundsChecker, Purifier, Insure++, Intel Inspector, Go race detector
### 6.1 Instrumentacĳa
Instrumentacĳa (eng. instrumentation) je proces dodava-

<!-- pdf_page=175 printed_page=6 -->

nja instrukcĳa u program kako bi se tokom njegovog izvršavanja, pratile određene pojave i prikupljali podaci o njegovom ponašanju. Instrumentacĳa se koristi u jednoj vrsti profajlera kao i u sanitajzerima i drugim alatima za dinamičko otkrivanje grešaka.
Najvažnĳe osobine koje dobra instrumentacĳa treba da zadovolji su:
1. Ne utiče na funkcionalnost programa.
2. Prikuplja sve neophodne podatke i samo njih. 3. Ne usporava previše rad programa. 4. Ne povećava previše upotrebu memorĳe.
Prvi uslov ističe da ukoliko dodata instrumentacĳa utiče na funkcionalnost programa onda prikupljeni podaci neće oslikavati pravi način njegovog rada. Drugi uslov je važan jer prikupljanje nepotrebnih podataka dodatno usporava program i samu njihovu obradu, dok premalo informacĳa može biti beznačajno.
Preterano usporavanje rada programa može da vodi do praktične neupotrebljivosti programa zbog instrumentacĳe. Na primer, ako izvršavanje programa traje jedan sat, a usporenje koje instrumentacĳa nameće izvršavanju je sto puta, onda izvršavanje instrumentovanog programa traje 100 sati što je prilično nepraktično. Slično, ako program već zahteva upotrebu velike količine memorĳe, onda povećanje potrošnje memorĳe može da utiče na to da instrumentovan program ne može da stane na uređaj na kojem treba da se izvršava. Usporavanje i povećavanje upotrebe memorĳe zavise od tipa aplikacĳe i mogu se kontrolisati izborom delova programa koji se instrumentuju.
Primer 6.1.1 (Uređaji koji rade u realnom vremenu) Usporavanje rada programa koje je posledica instrumentacĳe je posebno važno u kontekstu sistema koji treba da rade u realnom vremenu. Ovi sistemi često imaju vrlo stroga vremenska ograničenja koja se in-

<!-- pdf_page=176 printed_page=162 -->

strumentacĳom mogu poremetiti (prekršiti) i time onemogućiti relevantnu smislenu analizu rada uređaja. Dodatno, problem mogu da budu i memorĳska ograničenja uređaja jer dodatni kôd za instrumentaciju i njeno rukovanje može uvećati program tako da on ne može da stane na uređaj.
Instrumentacĳa se može klasifikovati prema načinu na koji se nove instrukcĳe dodaju u program: može je vršiti programer ili se može vršiti automatski. Programer može izvršiti instrumentacĳu dodavanjem i inkrementiranjem brojača na željenim mestima u kodu. Automatsku instrumentacĳu može da sprovodi:
-kompajler i/ili linker tokom prevođenja i linkovanja programa,
-specĳalizovani alat na već prevedenom (izvršivom) programu i
-specĳalizovani alat tokom samog izvršavanja programa.
Instrumentacĳa se može vršiti prilikom proizvoljne vrste prevođenja kao i nad proizvoljnom izvršivom verzĳom programa. Za dinamičku analizu koja ima za cilj otkrivanje grešaka, obično je poželjno debag prevođenje (ili verzĳa) programa, dok je za praćenje performansi najčešće neophodno koristiti riliz prevođenje (verzĳu) programa, odnosno onu verzĳu programa koja će biti isporučena korisniku (jer je za tu verzĳu ključno izmeriti performanse).
Primer 6.1.2 (Manuelna instrumentacĳa) Dodavanjem globalne promenljive brojac_saberi i njenim inkrementiranjem unutar funkcĳe saberi moguće je izbrojati pozive ove funkcĳe tokom izvršavanja programa. Na kraju rada programa potrebno je odštampati vrednost ove promenljive kako bi se prikazao rezultat brojanja, ili sačuvati tu vrednost u nekoj datoteci.
1 int brojac_saberi = 0;
2 int saberi(int a, int b) {

<!-- pdf_page=177 printed_page=6 -->

3 brojac_saberi++;
Ime alata Valgrind (izgovara se Velgrind, između a i e) potiče iz nordĳske mitologĳe, gde Valgrind označava glavnu kapĳu koja vodi u Valhalu (eng. Valhalla) — Odinovu dvoranu u koju ulaze duše palih ratnika. Odin je vrhovni bog u nordĳskoj mitologĳi, bog mudrosti, poezĳe, rata i smrti. Valgrind je simbolično opisan kao široka, čvrsta kapĳa kroz koju prolaze samo oni koji su dostojni Odinove časti i poziva.
4 return a + b;
5 }
Manuelna instrumentacĳa se u praksi gotovo nikada ne primenjuje. Ovde se koristi kao ilustracĳa, jer se sličan kôd automatski ubacuje, bilo putem kompajlera, bilo putem specĳalizovanih alata.
Instrumentacĳa u fazi izvršavanja
Valgrind je platforma koja omogućava izvršavanje programa, njegovu instrumentacĳu u fazi izvršavanja i snimanje izveštaja koji nastaju prilikom analize izvršavanja programa. Valgrind se koristi kao osnova za pravljenje alata za dinamičku analizu programa: profajlera i alata za dinamičku detekcĳu grešaka u programima.
Autori alata su ovo ime odabrali kako bi dočarali ideju ulaska u „unutrašnjost“ programa: kao što Valgrind u mitologĳi otvara put u svet hrabrih ratnika, tako i softverski Valgrind omogućava programerima da zavire u unutrašnje stanje svojih aplikacĳa, otkrivajući greške i nedostatke koje inače ne bi mogli da vide. Ovo ime ističe ulogu alata kao „čuvara kapĳe“ između uobičajenog izvršavanja programa i njegove detaljne analize na nivou memorĳe i performansi.
Svi Valgrind alati rade na istoj osnovi koja obuhvata podršku za izvršavanje i snimanje rezultata analize, kao i interfejs ka definisanju instrumentacĳe. Informacĳe koje se emituju variraju u zavisnosti od zadate instrumentacĳe koja je specifična za svaki pojedinačni alat:
Valgrind + Instrumentacĳa = Alat za dinamičku analizu
Izazovi uspešnog rada alata zasnovanog na platformi Valgrind sastoje se, pre svega, u sklapanju dva procesa u jedan: program koji se analizira i program alata se sklapaju u jedan proces. Mnogi resursi se dele između ova dva programa, kao što su registri ili memorĳa, i potrebno ih je pravilno uskladiti.
Dostupnost Valgrinda Valgrind je sistemski i arhitekturalno zavisni alat koji radi na sledećim platformama:
Prilikom analize izvršavanja programa nĳedan deo programa koji se analizira se ne izvršava u svom izvornom obliku. Valgrind deli originalni kôd u sekvence koje se nazivaju osnovni blokovi. Osnovni blok je linearna sekvenca mašinskog koda, na čĳi se početak dolazi nekom naredbom skoka, koja u sebi ne sadrži grananja, pozive funkcĳa ili skokove, i koja se završava sa skokom, pozivom funkcĳe ili naredbom povratka u funkcĳu
Linux - x86, AMD64, ARM, ARM64, PPC32, PPC64, S390X, MIPS32, MIPS64
Solaris - x86, AMD64 Android - ARM, ARM64, x86, MIPS32
Darwin - x86, AMD64 (Mac OS X 10.12)

<!-- pdf_page=178 printed_page=164 -->

pozivaoca. Veličina osnovnog bloka je ograničena na maksimalno šezdeset mašinskih instrukcĳa. Valgrind dopunjava mašinski kôd programa kodom koji vrši instrumentacĳu. Dopunjavanje se vrši pojedinačno po osnovnim blokovima, neposredno pre prvog izvršavanja samog bloka.
Proces transformisanja koda se sastoji iz podizanja originalnog mašinskog koda u odgovarajuću međureprezentacĳu (eng. intermediate representation) koja se zatim instrumentuje i ponovo prevodi u novi mašinski kôd.
disasembliranje
Izgradnja optimizovane međureprezentacĳe sastoji se od disasembliranja (Valgrind vrši podizanje mašinskog koda programa u internu međureprezentacĳu) i standardnih optimizacĳa programskih prevodilaca (kao što su uklanjanje redundantnog koda i eliminacĳa zajedničkih podizraza). Disasembliranje je arhitekturalno zavisno.
optimizacĳa 1
instrumentacĳa
Instrumentacĳa se vrši nad generisanom međureprezentacĳom. Blok koda u međureprezentacĳi se prosleđuje alatu, koji može proizvoljno da ga transformiše. Alat u zadati blok dodaje novi međukod, kojim proverava ispravnost ili prati i skuplja informacĳe o radu programa.
optimizacĳa 2
izgradnja grafa
Prevođenje u izvršivi kôd obuhvata optimizacĳe, izgradnju grafa, odabir instrukcĳa, alokacĳu registara i asembliranje. Druga faza optimizacĳe je jednostavnĳa od prve i uključuje samo izračunavanje vrednosti izraza koji se mogu izračunati pre faze izvršavanja i uklanjanje mrtvog koda. Zatim se od međureprezentacĳe kreira stablo radi lakšeg odabira instrukcĳa. Prilikom odabira instrukcĳa, koriste se virtuelni registri koji se određuju u fazi alokacĳe registara. Na kraju, u fazi asembliranja, kôd se prevodi u mašinski i smešta se u odgovarajući blok memorĳe. Odabir instrukcĳa, alokacĳa registara i asembliranje su arhitekturalno zavisni.
odabir instrukcĳa
alokacĳa registara
asembliranje
Razvoju platforme Valgrind doprinela je Aleksandra Karadžić, diplomirani master student Matematičkog fakultata. Njena master teza: Alat Valgrind — Implementacĳa konvencĳe FPXX za arhitekturu MIPS
Sve faze procesa transformacĳe koda obavlja Valgrind, osim instrumentacĳe koju obavlja odgovarajući alat. Re-

<!-- pdf_page=179 printed_page=6 -->

Mašinski kôd
0110001010 1010110101 0110101011
Disasembliranje
Međukod
Originalni međukôd
Optimizacĳa 1
Redundantan originalni međukôd, podizrazi...
Dodatni međukôd Mrtav međukôd, izrazi koji se mogu izračunati pre izvršavanja
Instrumentacĳa
Optimizacĳa 2
Izgradnja grafa
Instrukcĳe, virtuelni registri
Instrukcĳe, izabrani registri
Odabir instrukcĳa
Virtuelni registri
Alokacĳa registara
Registri
Asembliranje
0111000101 0010101010 1101010101 0101110010 1110100010
Slika 6.1: Faze transformacĳe koda koje su neophodne radi instrumentacĳe koda u fazi izvršavanja (platforma Valgrind)

<!-- pdf_page=180 printed_page=166 -->

zultat procesa transformacĳe koda se čuva u memorĳi i izvršava se po potrebi. Valgrind troši najviše vremena na sam proces transformacĳe koda, kao i na pronalaženje i izvršavanje transformisanog koda. Usporenje koje Valgrind nameće izvršavanju programa je od 5 do 100 puta, u zavisnosti od konkretnog alata.
Najpoznatĳi Valgrind alati su:
Kako Valgrind i njegovi alati ne analiziraju izvorni kôd već mašinski kôd programa, to znači da ih je moguće koristiti za analizu programa napisanih u bilo kom programskom jeziku. Ipak, najčešće se koriste za analizu programa napisanih u jezicima C i C++ jer su i greške koje se analiziraju i prate karakteristične za te jezike.
-Memcheck — detektor memorĳskih grešaka, -Massif — detektor memorĳskih grešaka praćenjem upotrebe dinamičke memorĳe,
-Cachegrind — profajler keš memorĳe, -Callgrind — profajler funkcĳa, -Helgrind i DRD — detektori grešaka višenitnog izvršavanja.
### 6.2 Profajleri
Važan deo testiranja performansi odnosi se na merenje vremenske i memorĳske efikasnosti programa. Ukoliko program ne zadovoljava postavljene kriterĳume performansi, neophodno je identifikovati uzroke i sprovesti odgovarajuće optimizacĳe. Proces optimizacĳe predstavlja sastavni i neizostavan deo razvoja softverskih sistema, jer obezbeđuje da implementacĳa ispunjava zahteve u pogledu brzine izvršavanja i potrošnje resursa.
Kako bi se precizno identifikovali delovi koda koji zahtevaju poboljšanje, u praksi se koriste specĳalizovani pomoćni alati — profajleri — koji generišu detaljne informacĳe o ponašanju programa tokom izvršavanja. Na osnovu ovih informacĳa donose se odluke o prioritetima i načinima optimizacĳe.
Profajliranje je vid dinamičke analize programa. Profajliranjem se tokom izvršavanja programa nad unapred definisanim skupom ulaznih podataka prikupljaju detaljni

<!-- pdf_page=181 printed_page=6 -->

podaci o ponašanju programa u realnim uslovima. Rezultat ovog procesa je skup podataka poznat kao profil programa. Profil može da obuhvata različite informacije, uključujući frekvencĳe poziva funkcĳa i izvršavanja osnovnih blokova koda, procenat ukupnog vremena utrošenog u pojedinačnim delovima koda, informacĳe o korišćenju memorĳe — uključujući alokacĳe i dealokacĳe — zatim učestalost promašaja u kešu procesora, kao i redosled zaključavanja i otključavanja katanaca prilikom višenitnog izvršavanja.
Profajliranje može biti implementirano softverski, oslonjeno na podršku hardvera ili kao kombinacĳa oba pristupa. Kada se koristi hardverska podrška, profajliranje postaje efikasnĳe i omogućava prikupljanje šireg spektra podataka. Za određene vrste merenja, poput broja promašaja u keš memorĳi ili vremena utrošenog zbog čekanja u protočnoj obradi instrukcĳa (eng. pipeline stall), hardverska podrška je neophodna.
Profajliranje se može zasnivati na instrumentacĳi, tj. ubacivanju dodatnih instrukcĳa u kôd radi preciznog praćenja ponašanja programa tokom izvršavanja, ili na uzorkovanju (eng. sampling), gde se povremeno beleže karakteristični podaci o stanju sistema. Obe tehnike imaju svoje prednosti i ograničenja, a izbor tehnike, tj. odgovarajućeg alata, treba načiniti u skladu sa zahtevima za preciznošću i dozvoljenim opterećenjem sistema.
6.2.1 Upotreba profila
Profil programa se može upotrebljavati na različite načine, u zavisnosti od informacĳa koje on sadrži. Najčešća upotreba je identifikacĳa tzv. vrućih delova koda (eng. hot spots). To su delovi koda koji se najčešće izvršavaju ili koji najviše doprinose ukupnom vremenu izvršavanja, što je od suštinskog značaja za optimizacĳu performansi. Takođe, profil može da posluži za procenu pokrivenosti koda datim skupom testova, čime se dobĳa

<!-- pdf_page=182 printed_page=168 -->

uvid na koji način dalje proširiti skup testova sa ciljem da se dobĳe veća pokrivenost koda. Pored toga, profil se može koristiti i za detektovanje curenja memorĳe i raznih grešaka u kodu.
Optimizacĳu na osnovu profila može da izvrši programer, a može je automatski sprovesti i programski prevodilac. Samo programer može da suštinski izmeni algoritam koji se koristi u implementacĳi ali i automatska optimizacĳa može da napravi važna poboljšanja u efikasnosti koda.
Primer 6.2.1 Razmotrimo aplikacĳu koja obrađuje tekst i broji koliko puta se svaka reč pojavljuje u datoteci.
Profajliranjem je utvrđeno da se najviše vremena troši na ponovljeno pretraživanje liste reči kako bi se proverilo da li se neka reč već pojavila. Kako lista raste, ova operacĳa postaje sve sporĳa.
Na osnovu toga, programer može optimizovati kod zamenom liste odgovarajućom heš mapom, gde se provera postojanja i ažuriranje broja pojavljivanja obavlja u konstantnom vremenu. Ova izmena značajno poboljšava performanse, posebno za velike ulazne tekstove.
Automatska optimizacĳa može da se sprovodi u fazi kompilacĳe pre izvršavanja programa ili u fazi kompilacĳe tokom izvršavanja programa. U oba slučaja, optimizacĳe koje se sprovode na osnovu profila programa nazivaju se optimizacĳe vođene profilom (eng. profile guided optimizations). Ove optimizacĳe značajno poboljšavaju performanse i prevazilaze domete standardnih kompajlerskih optimizacĳa.
Optimizacĳa u fazi kompilacĳe pre izvršavanja programa, da bi mogla da se sprovede, zahteva da je profil programa dostupan, što znači da toj kompilacĳi prethodi jedna kompilacĳa i izvršavanje

<!-- pdf_page=183 printed_page=6 -->

programa sa ciljem prikupljanja profila. Prikupljanje profila koji je potreban za optimizacĳu je često veoma zahtevan posao koji značajno troši memorĳske i vremenske resurse. Zbog toga se umesto prikupljanja profila, nekada koriste statički profajleri, odnosno predviđanje profila metodama mašinskog učenja na osnovu karakteristika koda. Na primer, obrada grešaka i izuzetaka odgovaraju putanjama programa koje se ređe izvršavaju u odnosu na glavne funkcionalnosti programa. Modeli mašinskog učenja mogu da nauče takve i kompleksnĳe zakonitosti i da na osnovu statičkih osobina koda predvide koji će se delovi programa najčešće izvršavati.
Razvoju statičkih profajlera modelima mašinskog učenja aktivno doprinosi i dr Milan Čugurović, sa Matematičkog fakulteta: GraalSP: Polyglot, efficient, and robust machine learning-based static profiler Njegova doktorska teza: Predviđanje profila izvršavanja programa tehnikama mašinskog učenja
Optimizacĳa u fazi kompilacĳe tokom izvršavanja pro-
grama je karakteristična za kompilacĳu u toku izvršavanja‗ (eng. Just-In-Time compilation, JIT). Kompilacĳa u toku izvršavanja koristi profil koji se dobĳa tokom izvršavanja da bi se donele odluke o tome da se neki delovi koda kompiliraju, umesto interpretiraju, i da se dodatno optimizuju.
6.2.2 Kvalitet profila
Na izvršavanje programa utiču konkretni ulazi i različiti ulazi daju različite rezultate profajliranja. Da bi se donosile odluke o optimizacĳi na osnovu profajliranja, važno je da izvršavanje u okviru kojeg se vrši profajliranje reflektuje realnu upotrebu programa, odnosno da su skupljeni podaci na osnovu relevantnih ulaznih podataka ili da su skupljeni podaci na osnovu više različitih skupova ulaznih podataka. U suprotnom, mogu se propustiti prilike za optimizacĳu programa ili se mogu doneti pogrešne odluke.
‗ Kompilacĳa u toku izvršavanja je karakteristična za sve jezike koji se izvršavaju na Javinoj virtuelnoj mašini, na primer Java, Scala i Kotlin.

<!-- pdf_page=184 printed_page=170 -->

Primer 6.2.2 (Propuštena prilika) Razmotrimo funkciju koja vrši obradu elemenata niza algoritmom kubne složenosti i pretpostavimo da se ta funkcĳa u praksi koristi nad velikim nizovima. Ukoliko se program profajlira sa ulazom koji funkcĳi prosleđuje niz sa malim brojem elemenata, onda se profajliranjem ne može uočiti problem koji će nastati u praksi, jer kubna složenost za mali niz može i dalje da daje zadovoljavajuće performanse.
Primer 6.2.3 (Pogrešne odluke) Razmotrimo funkcĳu 𝑓koja ima naredbu grananja u okviru koje se u then grani poziva funkcĳa 𝑓𝑡ℎ𝑒𝑛, a u else grani funkcĳa 𝑓𝑒𝑙𝑠𝑒. Pretpostavimo da se u praksi then grana izvršava 20 puta češće nego else grana ali da su ulazni podaci za profajliranje izabrani tako da nas vode u
else granu. Na osnovu takvog profajliranja, može da se donese pogrešan zaključak, tj. da je potrebno optimizovati funkcĳu 𝑓𝑒𝑙𝑠𝑒. Optimizacĳa te funkcĳe u praksi neće davati vidljive rezultate, s obzirom na to da se ona retko izvršava.
Prilikom optimizacĳe na osnovu dobĳenih profila važno je pronaći ravnotežu između vremena utrošenog na prikupljanje podataka i koristi od dobĳenih informacĳa. U početnim fazama optimizacĳe mogu se koristiti jednostavnĳe i manje precizne metode kako bi se identifikovali najveći problemi. Kako optimizacĳa napreduje, preostale prilike za unapređenje postaju suptilnĳe, što zahteva preciznĳe tehnike profajliranja.
6.2.3 Profajliranje uzimanjem uzoraka
Profajler zasnovan na uzorkovanju (eng. sample based profiler) periodično prekida izvršavanje programa, najčešće u fiksnim vremenskim intervalima, koristeći prekide operativnog sistema. Prilikom svakog prekida, profajler

<!-- pdf_page=185 printed_page=6 -->

snima stek poziva (eng. call stack) svake niti, beležeći niz aktivnih funkcĳskih poziva u tom trenutku. Prikupljeni podaci se zatim agregiraju tako da budu pogodni za analizu.
Na osnovu dovoljno velikog broja uzoraka i za dobro izabrane intervale merenja, moguće je napraviti preciznu statističku procenu koji delovi koda se najčešće izvršavaju ili gde se troši najviše vremena. Uzorkovanje pruža statističku aproksimacĳu, a ne precizno merenje broja poziva ili vremena izvršavanja. Ako se funkcĳa izvršava vrlo brzo i retko, moguće je da neće biti obuhvaćena uzorkovanjem.
Ovaj pristup omogućava programu da se izvršava gotovo punom brzinom, što ga čini pogodnim za velike i složene aplikacĳe, dugotrajne aplikacĳe i sisteme u realnom vremenu. Dodatno, nĳe potrebno ponovno prevođenje izvornog koda već se profajliranje uzimanjem uzoraka može vršiti nad proizvoljnim izvršivim datotekama (ali prisustvo debag simbola može da poboljša analizu i interpretacĳu rezultata).
Najpoznatĳi alati koji vrše profajliranje uzorkovanjem su perf, oprofile, gprof (kombinacĳa uzorkovanja i instrumentacĳe), Visual Studio Profiler (ima podršku i za instrumentaciono profajliranje), Intel VTune Profiler, Google CPU Profiler i Instruments (Xcode).
Primer 6.2.4 (perf) Alat perf uveden je kao deo Linux kernela verzĳe 2.6.31, objavljene u septembru 2009. godine. Cilj alata bio je da zameni starĳe i manje fleksibilne alate za profajliranje uzorkovanjem, poput alata oprofile, kao i da pruži moderan interfejs za korišćenje savremenih ugrađenih hardverskih brojača za performanse (eng. performance monitoring units). Od tada se perf aktivno razvĳa zajedno sa Linux kernelom i održava ga Linux kernel zajednica, uz značajan doprinos programera iz kompanĳa kao što su Red Hat, Intel, Google u IBM.

<!-- pdf_page=186 printed_page=172 -->

Perf pruža statistički pregled vremena izvršavanja i resursa koje program koristi. Zahvaljujući malim troškovima upotrebe i visokoj preciznosti, perf je postao standardni alat za profajliranje na Linux platformama. Njegova fleksibilnost omogućava primenu kako na nivou pojedinačnih procesa, tako i na nivou celog sistema, a rezultati mogu biti prikazani tekstualno ili vizuelno.
Primer 6.2.5 (Plameni graf u Javi) Plameni graf (eng. flame graph) je vizuelizacĳa koji se koristi za analizu performansi softvera, posebno za identifikovanje uskih grla i razumevanje upotrebe resursa. Plameni graf se generiše na osnovu rezultata rada profajlera.
Primer dela plamenog grafa za program Game of Life u Javi čĳi je deo koda prikazan u listingu 6.1 dat je na slici 6.2. Primer pokazuje da se u programu najviše vremena troši redom u metodama koje pozivaju metod main, koja zatim poziva metod run u okviru koje se najviše vremena troši u metodama nextGeneration i printGrid. Histogram u dnu slike pokazuje sortirano koliko najviše vremena se troši u pojedinačnim metodama isključujući vreme koje troše funkcĳe koje su iz njih pozvane. Dakle, najviše vremena se troši u funkciji koja preuzima karaktere getChars, a zatim i u funkcĳi koja računa narednu generacĳu nextGeneration.
Listing 6.1: Deo koda aplikacije Game of Life 1 import java.io.FileWriter;
2
3 // A simple Java program to implement Game of
Life
4 // Modified from https://www.geeksforgeeks.org/
program-for-conways-game-of-life/
5 public class GameOfLife {
6 ...
7 public static void main(String[] args) {
8 new GameOfLife().run();
9 }
10 private void run() {

<!-- pdf_page=187 printed_page=6 -->

11 // Initializing the grid.
12 int[][] grid = newGrid();
13 printGrid(grid);
14 for (int i = 0; i < GENERATIONS; i++) {
15 grid = nextGeneration(grid);
16 printGrid(grid);
17 }
18 }
19 ...
20 static int[][] nextGeneration(int[][] grid) {
21 int[][] future = new int[M][N];
22 // Loop through every cell
23 for (int l = 0; l < M; l++) {
24 for (int m = 0; m < N; m++) {
25 ...
26 }
27 }
28 return future;
29 }
30
31 private static void printGrid(int[][] grid) {
32 try (FileWriter myWriter = new FileWriter("f
")) {
33 for (int i = 0; i < M; i++) {
34 for (int j = 0; j < N; j++) {
35 if (grid[i][j] == 0)
36 myWriter.write(".");
37 else
38 myWriter.write("*");
39 }
40 myWriter.write(System.lineSeparator
());
41 }
42 } catch (Exception e) {
43 throw new IllegalStateException();
44 }
45 }
46 ...
Plameni graf je obično interaktivan prikaz poziva metoda tokom izvršavanja programa. Svaka traka (pravougaonik) odgovara pozivu jedne metode, a svaki „plamen“ odgovara jednom nizu poziva metoda.

<!-- pdf_page=188 printed_page=174 -->

Slika 6.2: Deo plamenog grafa za izvršavanje programa Game of Life u Javi
Širina svake trake proporcionalna je vremenu koje je program proveo u tom metodu i metodama koje su iz njega pozvane.
Plameni graf na pregledan način prikazuje veliki broj uzoraka i pomaže u donošenju odluka o prioritetima u optimizacĳi performansi. Vizuelni prikaz putanja poziva olakšava i otkrivanje neočekivanih redosleda izvršavanja ili neefikasnih rekurzivnih poziva.
6.2.4 Instrumentaciono profajliranje
Informacĳe o pokrivenosti koda se generišu nakon završetka rada programa. Međutim, specifičnosti nekih programa, poput servera, operativnih sistema ili sistema za rad u realnom vremenu, zahtevaju uvid u pokrivenost i pre završetka rada programa. Jedno rešenje za prikazivanje podataka o pokrivenosti koda u fazi izvršavanja može se videti u master radu Marine Nikolić: Prikupljanje i prikaz podataka o izvršavanju programa
Instrumentacĳom se mogu pratiti najrazličitĳe karakteristike izvršavanja programa. Profili koji se koriste za određivanje delova koda koji se najčešće izvršavaju kao i tačni udeli učestalosti izvršavanja različitih delova koda, za kompajlerski zasnovane optimizacĳe i za utvrđivanje pokrivenosti koda testovima, dobĳaju se na osnovu sledećih vrsta profajliranja:
1. profajliranje putanja,
2. profajliranje grana i 3. profajliranje blokova.

<!-- pdf_page=189 printed_page=6 -->

Instrumentacĳa se može vršiti u fazi kompilacĳe, kada je na raspolaganju graf kontrole toka izvršavanja programa i u tom slučaju se profajliranje sprovodi izvršavanjem instrumentovanog programa. Instrumentacĳa se može vršiti i u kasnĳim fazama, pa čak i u fazi samog izvršavanja programa. Tada je, pored izvršive verzĳe programa, neophodno pokrenuti i profajler, koji dinamički ubacuje dodatne instrukcĳe i prati ponašanje programa u realnom vremenu.
Doprinos razvoju kompajlerski zasnovanog profajliranja u okviru kompajlerske infrastrukture LLVM dao je Nikola Prica, diplomirani master student Matematičkog fakultata. Njegova master teza: Podrška za profajliranje softvera uređaja sa ugrađenim računarom
Profajliranje putanja i blokova
Profajliranje putanja (eng. path profiling) je složen vid profajliranja kojim se dobĳaju informacĳe o najčešće korišćenim putanjama kroz program. Ova vrsta profila u sebi sadrži i informacĳe o profilima grana i blokova. Profajliranje putanja zahteva kompleksne algoritme i najviše utiče na performanse izvršavanja prilikom profajliranja.
Profajliranjem blokova (eng. basic-block profiling) utvrđuje se ukupan broj izvršavanja svakog bloka u programu. Blok može biti funkcĳa ili deo koda u kome se ne nalaze instrukcĳe grananja ili skokova. Naivni algoritam može se ostvariti tako što se u svaki blok umeće brojač, čime se dobĳaju precizne informacĳe o broju izvršavanja blokova, ali se i prilično usporava sistem i opterećuje memorĳa. Ovaj način profajliranja ne daje informacĳe o tome koje su putanje kroz program najčešće kao ni koji su prelazi između blokova česti. Primer grafa kontrole toka i odgovarajućih profila blokova dat je na slici 6.3a.
Profajliranje grana
Profajliranjem grana (eng. edge profiling) dobĳaju se podaci o prelascima koji se ostvaruju instrukcĳama grananja ili skoka kojom se prebacuje tok izvršavanja programa iz jednog bloka u drugi. Profajliranjem grana mogu

<!-- pdf_page=190 printed_page=176 -->

A
𝐴65
50 15
B C
𝐵50 𝐶15
12 13
48
38
D
17
𝐷25
10
2
E
15
𝐸48
F
𝐹17
(a) Profili blokova su upisani uz oznaku bloka (npr. blok A je izvršen 65 puta)
(b) Profili grana su su označeni uz svaku granu (npr. grana A-B je izvršena 50 puta)
Slika 6.3: Profili dobĳeni profajliranjem blokova (levo) i profajliranjem grana (desno)
se dobiti i podaci koji se dobĳaju profajliranjem blokova. Broj izvršavanja svakog bloka može se izračunati pomoću brojača grana tako što se sumiraju sve grane koje ulaze u blok. Primer profila grana dat je na slici 6.3b.
Naivni algoritam profajliranja grana podrazumeva da se za svaku naredbu skoka umeće po jedan brojač. Međutim, takvo rešenje previše opterećuje program. Profajliranje grana, ukoliko se instrumentacĳa radi u fazi kompilacĳe, može da se implementira značajno efikasnije. Rešenje koje podrazumeva minimalni broj umetnutih brojača predložio je Donald Knut (eng. Donald Knuth). Osnovni koraci Knutovog algoritma profajliranja grana su:
Podsetnik Razapinjuće stablo je podskup grafa G koji sadrži sve čvorove pokrivene sa minimalnim mogućim brojem grana. Razapinjuće stablo ne sadrži cikluse i ne može biti nepovezano. Po definicĳi, svaki povezan neusmeren graf G ima najmanje jedno razapinjuće stablo. Broj grana u razapinjućem stablu je 𝑣−1, gde je 𝑣broj čvorova grafa.
1. Konstruisati graf kontrole toka (eng. control flow graph) programa, u kojem svaki čvor predstavlja blok instrukcĳa, a grana naredbu skoka ili grananja.

<!-- pdf_page=191 printed_page=6 -->

𝐵1
a
k
𝐵2
b c
j
𝐵3 𝐵4
d e
𝐵6 𝐵5
f g h
𝐵7
i
𝐵8
(a) Graf kontrole toka
𝐵1
𝐵1
𝐵1
𝐵1
a
a
a
a
k
k
k
k
𝐵2
𝐵2
𝐵2
𝐵2
b c
b c
b c
b c
j
𝐵3 𝐵4
j
𝐵3 𝐵4
j
𝐵3 𝐵4
j
𝐵3 𝐵4
d e
d e
d e
d e
𝐵6 𝐵5
𝐵6 𝐵5
𝐵6 𝐵5
𝐵6 𝐵5
g f
h
g f
h
g
h f
g
h f
𝐵7
𝐵7
𝐵7
𝐵7
i
i
i
i
𝐵8
𝐵8
𝐵8
𝐵8
(b) Brojači: f, g, j, k
(c) Brojači: h, i, j, k
(d) Brojači: f, h, j, k
(e) Brojači: g, i, j, k
Slika 6.4: Za četiri različita razapinjuća stabla (obeležena crnom isprekidanom linĳom) instrumentuju se različite grane (obeležene punom plavom linĳom)
2. Za dati graf kontrole toka izračunati odgovarajuće razapinjuće stablo (eng. spanning tree).
3. Granama koje ne pripadaju dobĳenom stablu treba dodati brojač.
Knutovim algoritmom se umesto svake grane u programu instrumentuje 𝑒−𝑣+ 1 grana, gde je 𝑣broj čvorova grafa, a 𝑒broj grana grafa. Knutovo rešenje može instrumentovati isti broj grana ali na različite načine, jer standardni algoritam računanja razapinjućeg stabla može vratiti različita stabla u zavisnosti od redosleda obrade grana (slika 6.4).

<!-- pdf_page=192 printed_page=178 -->

i
i
𝐵1
𝐵1
a b
a b
𝐵2
𝐵2
k
k
c d
𝐵3
c d
𝐵3
j
j
𝐵4 𝐵5
e
𝐵4 𝐵5
e
f g
f g
𝐵6
𝐵6
h
h
(a) Broj izvršavanja neinstrumentovanih grana se može izračunati u narednom redosledu: 𝑓= 𝑐 𝑔= 𝑑 𝑎= 𝑐+ 𝑑 𝑏= 𝑒+ 𝑘 𝑗= 𝑎+ 𝑏−𝑖 ℎ= 𝑒+ 𝑓+ 𝑔−𝑗
(b) Broj izvršavanja neinstrumentovanih grana se može izračunati u narednom redosledu: 𝑐= 𝑓 𝑑= 𝑔 𝑎= 𝑐+ 𝑑 𝑏= 𝑒+ 𝑘 𝑗= 𝑎+ 𝑏−𝑖 ℎ= 𝑒+ 𝑓+ 𝑔−𝑗
Slika 6.5: Profajliranje grana: dve mogućnosti grana za instrumentacĳu. Plavom bojom i punom linĳom obeležene su grane koje se instrumentuju, dok su isprekidane crne grane deo razapinjućeg stabla. Na osnovu instrumentovanih grana je moguće rekonstruisati brojeve izvršavanja preostalih grana. Razlika u izračunavanju za ova dva primera je samo u prva dva koraka.
Broj izvršavanja grana koje ne sadrže brojač se može izračunati na osnovu profajliranih vrednosti jer je zbir izlaznih vrednosti grana iz jednog bloka jednak zbiru ulaznih vrednosti grana u taj blok. Primer izračunavanja je dat na slici 6.5.
Optimalno razapinjuće stablo grafa izvršavanja programa je ono stablo kod kojeg se grane najveći broj puta izvršavaju, jer ako se te grane ne instrumentuju, onda se izvršavanje programa najmanje opterećuje. Međutim, to je upravo informacĳa koja se profajliranjem i traži i zbog koje se instrumentacĳa i radi, tako da je veoma teško izabrati baš to stablo. Tomas Bal (eng. Tomas Ball) i Džejms Larus (eng. James R. Larus) su osmislili heuristike izbora onih grana za koje se predviđa, na osnovu statičke analize koda, da će se najmanje puta izvršiti.

<!-- pdf_page=193 printed_page=6 -->

Smanjivanje troškova instrumentacĳe
Instrumentacĳa omogućava dobĳanje preciznog profila izvršavanja programa. Međutim, instrumentacĳa povlači značajno veću potrošnju vremenskih i memorĳskih resursa. Zbog toga postoje razni pristupi smanjivanju troškova instrumentacĳe uz smanjivanje preciznosti dobĳenih profila.
Jedan od načina smanjivanja vremena izvršavanja je naizmenično izvršavanje instrumentovanog i originalnog koda. U kôd se umeću provere na osnovu koji se odlučuje da li se izvršava instrumentovan kôd ili se ostaje u originalnom kodu. Za ovaj pristup potrebno je da postoje dve verzĳe koda (slika 6.6):
-instrumentovani kôd, koji se naziva još i duplirani kôd i
-originalni kôd, koji se naziva još proveravajući zato što se u njemu ispituje uslov koji, ukoliko je ispunjen, omogućava kontrolisan prelazak u duplirani kôd.
Kada izvršavanje pređe u duplirani kôd ono tu ostaje ograničeno vreme, a zatim se vraća u proveravajući kôd. Uslov prelaska iz proveravajućeg u duplirani kôd kontroliše koliko vremena će se izvršavati svaki od ova dva koda. Trenutak prelaska iz proveravajućeg u duplirani kôd se može inicirati hardverski, putem operativnog sistema ili softverski.
Prelazak iz proveravajućeg u duplirani kôd može da se vrši na osnovu fiksiranih vremenskih intervala ili na osnovu vrednosti brojača. U prvom slučaju, kada istekne odgovarajući vremenski period, sledeći prelazak u duplirajući kôd će se desiti tek kada se ponovo ispita uslov prelaska. U drugom slučaju, čuva se brojač za prelaske koji se dekrementira. Kada brojač dođe do nule, prelazi se u duplirajući kôd i resetuje se brojač. Najčešće je profajliranje na osnovu brojača preciznĳe u

<!-- pdf_page=194 printed_page=180 -->

Proveravajući kôd Duplirani kôd Legenda
Neinstrumentovan blok
Instrumentovan blok
Provera uslova
Postojeće ivice
Ivice dodate između proveravajućeg i dupliranog koda
Slika 6.6: Dupliranje koda radi periodičnog izvršavanja instrumentovanog koda
odnosu na profajliranje na osnovu fiksiranih vremenskih intervala.
Predložen pristup smanjuje vreme izvršavanja ali povećava potrebnu memorĳu kao i vreme kompilacĳe. Postoje proširene verzĳe ovog pristupa koje ne prave celu kopĳu koda već samo onih delova koji su vezani za instrumentacĳu, jer, za rekonstrukcĳu profila nĳe potrebno instrumentovati svaki blok ili svaku granu. Delimičnim dupliranjem (slika 6.7) može se smanjiti upotreba memorĳe i vreme kompilacĳe sa potpunim zadržavanjem preciznosti dobĳenih informacĳa (u odnosu na potpuno dupliranje koda).
Primer 6.2.6 (Profajler keš memorĳe Cachegrind) Cachegrind je alat platforme Valgrind namenjen softverskom profajliranju keš memorĳe i izvršavanja grana. On simulira memorĳski podsistem procesora i prati

<!-- pdf_page=195 printed_page=6 -->

𝐵1 𝐵1𝑑
𝐵1
𝐵2 𝐵2𝑑
𝐵2 𝐵2𝑑
𝐵3 𝐵4 𝐵3𝑑 𝐵4𝑑
𝐵3 𝐵4 𝐵3𝑑
𝐵5 𝐵5𝑑
𝐵5
(a) Potpuno dupliranje koda
(b) Delimično dupliranje koda
Slika 6.7: Potpuno i delimično dupliranje koda: blokove 𝐵1, 𝐵4 i 𝐵5 nĳe potrebno duplirati jer je za njihove duplikate moguća rekonstrukcĳa vrednosti na osnovu instrumentovanih blokova. Ako se izvršio dupliran blok 𝐵2𝑑, onda se tačno jednom izvršio i blok 𝐵1𝑑. Blok 𝐵5𝑑se izvršio onoliko puta koliko i blok 𝐵2𝑑, a broj izvršavanja bloka 𝐵4𝑑je jednak razlici broja izvršavanja blokova 𝐵2𝑑i 𝐵3𝑑. Slično se mogu rekonstruisati i profili grana. Zbog toga je dovoljno duplirati samo blokove 𝐵2 i 𝐵3.
pristupe softverskom kešu tokom izvršavanja analiziranog programa. Simulacĳa uključuje keš prvog nivoa (L1) podeljen na dve nezavisne sekcĳe: I1 za instrukcĳe i D1 za podatke, kao i objedinjeni drugi nivo keša (L2), što odgovara konfiguracĳi mnogih modernih procesora. Na mašinama sa tri ili više nivoa keša, Cachegrind modeluje prvi i poslednji nivo, odnosno sekcĳe I1, D1 i LL (poslednji nivo keša).
Alat prikuplja detaljnu statistiku o pristupima memorĳi i kešu, kako na nivou celog programa, tako i pojedinačno za svaku funkcĳu. Prate se ukupni brojevi izvršenih instrukcĳa, čitanja i upisa u memorĳu, kao i broj promašaja prilikom čitanja i upisa u različite nivoe keš memorĳe — posebno za instrukcĳe i

<!-- pdf_page=196 printed_page=182 -->

za podatke u prvom i poslednjem nivou keša. Na savremenim procesorima promašaj u kešu L1 ima približnu cenu od 10 procesorskih ciklusa, dok promašaj u poslednjem nivou keša (LL) može koštati i do 200 ciklusa. Cachegrind tako omogućava identifikacĳu uskih grla u performansama vezanim za efikasnost upotrebe keš memorĳe.
Primer 6.2.7 (Profajler funkcĳa Callgrind) Callgrind je alat platforme Valgrind koji profajlira pozive funkcĳa i generiše graf poziva funkcĳa korisničkog programa, prikazujući odnos između pozivaoca i pozvanih funkcĳa, broj izvršenih instrukcĳa i broj poziva. U osnovnim podešavanjima prikupljeni podaci uključuju mapiranje instrukcĳa na linĳe izvornog koda, kao i statistiku poziva između funkcĳa. Dodatno, Callgrind može da analizira upotrebu keš memorĳe i grananja u programu na način sličan alatu Cachegrind.
Cachegrind meri isključivo događaje koji nastaju unutar same funkcĳe, takozvane ekskluzivne troškove. S druge strane, Callgrind propagira troškove funkcĳa kroz sve njene pozive, računajući inkluzivne troškove — ukupnu cenu funkcĳe zajedno sa svim funkcĳama koje ona poziva, direktno ili indirektno. Tako je, na primer, cena funkcĳe bar uključena u cenu funkcĳe
foo ako je bar pozvana iz foo.
Zahvaljujući prikazu grafa poziva, moguće je pratiti putanje od početka rada programa i identifikovati funkcĳe sa najvećim ukupnim troškovima. Statistika odnosa pozivaoca i pozvane funkcĳe posebno je korisna kada funkcĳa ima više poziva iz različitih mesta u kodu, jer omogućava konteksno osetljive optimizacĳe.

<!-- pdf_page=197 printed_page=6 -->

### 6.3 Alati za dinamičku detekcĳu grešaka
Alati za dinamičku detekcĳu grešaka koriste instrumentacĳu kako bi omogućili automatsku detekcĳu grešaka u kodu, najčešće u radu sa memorĳom i nitima. Postali su neizostavan deo modernih razvojnih alata, jer značajno doprinose stabilnosti, bezbednosti i pouzdanosti softverskih sistema. Njihova glavna prednost je u tome što automatizuju proveru velikog broja potencĳalno problematičnih situacĳa, čime programeru omogućavaju da se fokusira na otklanjanje grešaka umesto na njihovo traženje. Ovi alati se obično primenjuju u ranim fazama razvoja i testiranja, često i kao dodatni stepen sigurnosti da kôd ne sadrži greške.
6.3.1 Sanitajzeri
Sanitajzeri se razvĳaju u okviru kompajlerskih infrastruktura. U fazi kompilacĳe, oni vrše automatsku instrumentacĳu kao i drugačĳu organizacĳu memorĳe tako da se u fazi izvršavanja omogućava automatska detekcĳa grešaka. Primena sanitajzera značajno povećava vreme izvršavanja programa i potrošnju memorĳe, zbog čega se obično koriste samo u testnom, a ne u produkcionom okruženju.
Najpoznatĳi sanitajzeri su adresni sanitajzer AddressSanitizer, sanitajzer memorĳe MemorySanitizer, sanitajzer niti ThreadSanitizer i sanitajzer nedefinisanog ponašanja UndefinedBehaviorSanitizer. U tabeli 6.2 dat je uporedni pregled karakteristika ovih sanitajzera, dok su detalji za svaki sanitajzer dati u nastavku.
Adresni sanitajzer
Adresni sanitajzer AddressSanitizer (ASan) je jedan od najčešće korišćenih sanitajzera, namenjen dinamičkoj

<!-- pdf_page=198 printed_page=184 -->

Tabela 6.2: Poređenje sanitajzera
Sanitajzer Otkriva greške Podržani kompajleri
Uticaj na performanse
AddressSanitizer (ASan)
Pristup memorĳi izvan granica, korišćenje nakon oslobađanja, dvostruko oslobađanje, curenje memorĳe
Clang/LLVM, GCC, XCode, MSVC
Umeren
MemorySanitizer (MSan)
Korišćenje neinicĳalizovanih vrednosti
Clang/LLVM Visok
ThreadSanitizer (TSan)
Nesinhronizovan pristup podacima
Clang/LLVM, GCC
Veoma visok
UndefinedBehaviorSanitizer (UBSan)
Nedefinisano ponašanje prema standardu jezika
Clang/LLVM, GCC
Mali do umeren
detekcĳi grešaka u upravljanju memorĳom. On instrumentuje program tokom kompilacĳe, ubacujući dodatne provere pri svakom pristupu memorĳi, i preuređuje način organizacĳe memorĳskog prostora tokom izvršavanja kako bi omogućio precizno otkrivanje čitavog spektra grešaka. AddressSantizer je dostupan u okviru kompajlera GCC, Clang/LLVM, XCode i MSVC.
AddressSanitizer detektuje nepravilne pristupe memorĳi kao što su čitanje ili pisanje izvan granica alocirane memorĳe, korišćenje memorĳe nakon njenog oslobađanja, dvostruko oslobađanje memorĳe i curenje memorĳe. Ove greške su uobičajene u programima napisanim u jezicima poput C i C++, a često su uzrok padova programa, oštećenja podataka ili sigurnosnih propusta.
Osnovni princip rada alata ASan zasniva se na instrumentacĳi svih pristupa memorĳi i uvođenju provera validnosti na svaku operacĳu čitanja i pisanja. Pored toga, alokacĳe memorĳe proširuju se dodatnim tzv. „crvenim zonama” (eng. red zones), koje okružuju svaki blok memorĳe i služe za otkrivanje prekoračenja granica. Status svakog bajta memorĳe čuva se u posebnoj do-

<!-- pdf_page=199 printed_page=6 -->

datnoj memorĳi (eng. shadow memory), koja omogućava efikasnu detekcĳu grešaka.
Glavne prednosti upotrebe alata ASan su njegova pouzdanost i jednostavnost upotrebe. Program je potrebno prevesti uz dodatak odgovarajuće opcĳe pri kompilacĳi kako bi proveravanje bilo omogućeno. Greške u pristupu memorĳi otkrivaju se odmah prilikom prvog nepravilnog pristupa. Zahvaljujući tome, ASan je postao standardni deo alata za razvoj i testiranje modernih softverskih sistema.
Sa druge strane, njegova primena nosi i određene probleme. Programi instrumentovani ovim sanitajzerom zahtevaju značajno više memorĳe (često dva do tri puta više od neinstrumentovanog programa) i značajno sporĳe se izvršavaju (takođe dva do tri puta sporĳe u poređenju sa odgovarajućim neinstrumentovanim programom).
Memorĳski sanitajzer
Memorĳski sanitajzer MemorySanitizer (MSan) je specĳalizovan za otkrivanje korišćenja promenljivih kojima nisu inicĳalizovane vrednosti† u programima napisanima u jezicima poput C i C++. Korišćenje neinicĳalizovanih podataka može dovesti do nepredvidljivog ponašanja programa, uključujući pogrešne rezultate izračunavanja, oštećenja podataka ili sigurnosne ranjivosti. Takve greške su često teške za detekcĳu, jer se program može činiti ispravnim u nekim slučajevima, dok u drugim generiše neočekivane rezultate. MSan se razvĳa u okviru kompajlerske infrastrukture LLVM i može se koristiti kao opcĳa kompajlera Clang/LLVM.
MSan instrumentuje program tokom kompilacĳe, ubacujući dodatne provere koje prate inicĳalizovanost svake
† Neke jednostavne slučajeve korišćenja neinicĳalizovanih promenljivih može da prĳavi kompajler u fazi prevođenja programa.

<!-- pdf_page=200 printed_page=186 -->

promenljive u memorĳi. On održava poseban deo memorĳe (eng. shadow memory) u kojoj pamti status svakog bajta korisničke memorĳe, označavajući da li je njegova vrednost inicĳalizovana. Svaki pristup memorĳi tokom izvršavanja se dodatno proverava korišćenjem ove memorĳe, i čim se otkrĳe čitanje neinicĳalizovane vrednosti, program prekida izvršavanje i prĳavljuje grešku sa tačnom lokacĳom.
Prednost MSan-a je njegova sposobnost da pouzdano i precizno otkrĳe ovu klasu grešaka koja je inače izuzetno teško uočljiva običnim testiranjem ili debagovanjem. Međutim, ovaj sanitajzer ima i određena ograničenja: njegova primena značajno povećava potrošnju memorĳe i usporava izvršavanje programa, često još više nego ASan. Dodatno, MSan zahteva da sve biblioteke sa kojima se program linkuje budu takođe kompajlirane sa podrškom za ovaj sanitajzer, jer u suprotnom može generisati lažno pozitivne rezultate.
Sanitajzer niti
Sanitajzer niti ThreadSanitizer (TSan) je namenjen otkrivanju grešaka u višenitnim programima, odnosno detekcĳi nesinhronizovanog pristupa podacima (eng. data race). Greške izazvane nekorektnim pristupom deljenim podacima iz različitih niti bez odgovarajuće sinhronizacĳe spadaju među najteže za pronalaženje i reprodukovanje, jer se često ispoljavaju samo u specifičnim, teško ponovljivim scenarĳima. TSan je dostupan u okviru kompajlera GCC i Clang/LLVM. Sastoji se od modula za instrumentacĳu u fazi kompilacĳe i od posebne biblioteke koja se koristi u fazi izvršavanja (eng. run-time library).
TSan instrumentuje program tokom kompilacĳe i prati sve pristupe deljenim promenljivama tokom izvršavanja. Pomoću dodatnih provera u kodu vodi evidencĳu o tome koje niti pristupaju kojim memorĳskim lokacĳama i na koji način, kao i o sinhronizacionim primitivima koje

<!-- pdf_page=201 printed_page=6 -->

se koriste. Kada otkrĳe da dve ili više niti pristupaju istoj promenljivoj, a bar jedna od njih vrši upis, bez adekvatne sinhronizacĳe, sanitajzer prĳavljuje grešku, navodeći tačne lokacĳe problematičnih pristupa.
Osnovna prednost ovog sanitajzera je u tome što otkriva nesinhronizovan pristup podacima, grešku koja je veoma opasna i teška za otkrivanje. Međutim, programi instrumentovani ovim sanitajzerom izvršavaju se znatno sporĳe, a potrošnja memorĳe je značajno veća u poređenju sa neinstrumentovanom verzĳom. Tipično uspori izvršavanje od 5 do 15 puta, a memorĳsko dodatno opterećenje je od 5 do 10 puta.
Sanitajzer nedefinisanog ponašanja
Sanitajzer nedefinisanog ponašanja UndefinedBehaviorSanitizer (UBSan) namenjen je otkrivanju ponašanja koja su nedozvoljena ili nedefinisana prema standardu programskog jezika. Nedefinisana ponašanja u jezicima kao što su C i C++ često su izvor suptilnih grešaka koje mogu dovesti do ozbiljnih problema uključujući padove programa i oštećenja podataka. UndefinedBehaviorSanitizer je dostupan u okviru kompajlera GCC i Clang/LLVM.
UBSan instrumentuje kôd tokom kompilacĳe i dodaje provere za razne vrste operacĳa koje mogu izazvati nedefinisano ponašanje. Među najčešćim problemima koje UBSan detektuje su:
-prekoračenje opsega celobrojnih tipova (eng. integer overflow),
-konverzĳe između tipova koje nisu dozvoljene (koje vode prekoračenju),
-pristup nepravilno poravnatim memorĳskim lokacĳama (eng. unaligned access),
-dereferenciranje null pokazivača, -operacĳa šiftovanja koja vodi do prekoračenja tipa.

<!-- pdf_page=202 printed_page=188 -->

UBSan omogućava programeru da identifikuje i otkloni greške koje često na određenim arhitekturama i u određenim uslovima prolaze bez vidljivih posledica. Na taj način, UBSan doprinosi pisanju prenosivĳeg i pouzdanijeg koda, koji neće zavisiti od specifičnih karakteristika platforme. Sa druge strane, UBSan ima minimalni uticaj na performanse u poređenju sa drugim sanitajzerima. Preporučuje se njegovo korišćenje zajedno sa drugim sanitajzerima kako bi se obuhvatio što širi spektar grešaka.
6.3.2 Alati platforme Valgrind
Većina alata za dinamičku detekcĳu grešaka je komercĳalne prirode i zatvorenog koda. Platforma Valgrind i njeni alati su besplatni i otvorenog koda.
Alati za dinamičku detekcĳu grešaka platforme Valgrind otkrivaju slične vrste grešaka kao sanitajzeri, ali, za razliku od sanitajzera, instrumentacĳu rade u fazi izvršavanja. Zbog toga su performanse ovih alata lošĳe od performansi sanitajzera. Detektori grešaka višenitnog izvršavanja Helgrind i DRD pokrivaju značajno veći spektar grešaka u odnosu na sanitajzere niti.
Primer 6.3.1 (Detektor memorĳskih grešaka Memcheck)
Memcheck je najpoznatĳi i najčešće korišćeni alat platforme Valgrind. Njegova osnovna uloga je detekcĳa memorĳskih grešaka u korisničkom programu. Program koji se izvršava pod kontrolom alata Memcheck u proseku je od dvadeset do sto puta sporĳi u odnosu na samostalno izvršavanje, što je posledica dinamičke transformacĳe koda. Izlaz programa dopunjen je izveštajima koje generiše sam Memcheck i koji se ispisuju na standardni izlaz za greške.
Primer automatizacĳe ispravljanja grešaka koje se otkriju profajliranjem može se videti u master tezi Lazara Mladenovića: Automatsko ispravljanje grešaka detektovanih pomoću alata Memcheck
Za programe pisane u jezicima C i C++ Memcheck otkriva najčešće greške u radu sa memorĳom, kao što su:

<!-- pdf_page=203 printed_page=6 -->

-upisivanje podataka van opsega hipa ili steka, -pristupanje memorĳi koja je već oslobođena, -neispravno oslobađanje memorĳe, uključujući duplo oslobađanje ili neupareno korišćenje funkcĳa malloc/new/new[] i free/delete/
delete[],
-curenje memorĳe, -korišćenje neinicĳalizovanih vrednosti ili vrednosti izvedenih iz drugih neinicĳalizovanih podataka,
-preklapanje parametara prosleđenih funkcĳama, na primer preklapanje pokazivača src i dst kod funkcĳe memcpy.
Primer 6.3.2 (Detektor memorĳskih grešaka Massif) Massif je alat platforme Valgrind namenjen analizi korišćenja memorĳe u hip segmentu korisničkog programa. Postoje određeni scenarĳi curenja memorĳe koji ne spadaju u klasične slučajeve i koje Memcheck ne može da detektuje. Do ovakvih problema dolazi kada memorĳa formalno nĳe izgubljena — pokazivač na nju i dalje postoji — ali se više nikada ne koristi tokom izvršavanja. Programi koji imaju ovakvu vrstu „prikrivenog“ curenja memorĳe bespotrebno zauzimaju dodatne resurse. Massif pomaže upravo u identifikacĳi takvih slučajeva. Massif pruža detaljne informacĳe o tome koji delovi programa su odgovorni za alokacĳu memorĳe, olakšavajući pronalaženje uzroka neefikasnog upravljanja memorĳom.
Primer 6.3.3 (Detektori grešaka višenitnog izvršavanja Helgrind i DRD) Helgrind je alat namenjen otkrivanju grešaka u sinhronizacĳi pri korišćenju POSIX modela niti. DRD je takođe alat za detekcĳu grešaka u višenitnim programima, namenjen programima koji koriste niti u skladu sa POSIX standardom ili konceptima koji su na njemu zasnovani. Iako oba alata imaju

<!-- pdf_page=204 printed_page=190 -->

sličnu namenu i značajan broj preklapajućih detekcĳa, koriste različite algoritme za analizu izvršavanja i otkrivaju delimično različite tipove grešaka.
Greške u višenitnom izvršavanju koje alati detektuju uključuju mrtvo blokiranje (eng. deadlock) kao posledica pogrešnog redosleda zaključavanja i pristup zajedničkoj memorĳi bez adekvatne sinhronizacĳe i zaključavanja. Alat DRD može da detektuje i zadržavanje katanca (eng. lock-holding) i lažno deljenje (eng. false sharing). Greške u korišćenju POSIX niti koje ovi alati mogu da otkrĳu su:
pogrešno otključavanje muteksa — kada je muteks nevažeći, nĳe prethodno zaključan ili je zaključan od strane druge niti,
nepravilno rukovanje zaključanim muteksom — uništavanje nevažećeg ili zaključanog muteksa, kao i dealokacĳa memorĳe koja sadrži zaključan muteks,
pogrešno korišćenje funkcĳe pthread_cond_wait — prosleđivanje nezaključanog, nevažećeg ili muteksa koji je zaključala druga nit,
greške u radu sa barĳerama pthread_barrier — nevažeća ili dvostruka inicĳalizacĳa, kao i čekanje na objekat koji nikada nĳe inicĳalizovan.
Rezime
-Profajleri i sanitajzeri su alati koji vrše dinamičku analizu programa.
-Instrumentacĳa je proces dodavanja instrukcĳa u program kako bi se, tokom njegovog izvršavanja, pratile određene pojave i prikupljali podaci o njegovom ponašanju.
-Instrumentacĳom se značajno utiče na performanse instrumentovanog programa i postoje različiti algoritmi koji imaju za cilj smanjivanje troškova instrumentacĳe.
-Profajliranje može biti implementirano softverski,
