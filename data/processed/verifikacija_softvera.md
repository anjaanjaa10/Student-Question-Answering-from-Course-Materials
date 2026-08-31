# Verifikacija softvera (elektronska verzija, 2026)


<!-- pdf_page=3 printed_page=3 -->

Verifikacija softvera

<!-- pdf_page=5 printed_page=5 -->

Verifikacija softvera

Milena Vujošević Janičić

Matematički fakultet
Univerzitet u Beogradu
Beograd, 2026.

<!-- pdf_page=6 printed_page=6 -->

Autor:
dr Milena Vujošević Janičić, vanredni profesor na Matematičkom fakultetu u Beogradu

VERIFIKACĲA SOFTVERA
Prvo izdanje, 2026.

Izdavač:
Matematički fakultet Univerziteta u Beogradu, Studentski trg 16, 11000 Beograd
Za izdavača: prof. dr Dragoljub Kečkić, dekan

Recenzenti:
dr Mirko Spasić, docent na Matematičkom fakultetu u Beogradu
dr Maja Vukasović, docent na Elektrotehničkom fakultetu u Beogradu
Obrada teksta i ilustracĳe: autor
Štampa: Skripta internacional, Beograd
Tiraž: 30

CIP - Katalogizacija u publikaciji
Narodna biblioteka Srbije, Beograd

004.415.5(075.8)
VUJOXEVI Janiqi, Milena, 1980-
Verifikacĳa softvera / Milena Vujošević Janičić ;[ilustracĳe autor]. - 1. izd.
- Beograd : Univerzitet u Beogradu, Matematički fakultet, 2026 (Beograd :
Skripta internacional). 392 str. : ilustr. ; 24 cm

Tiraž 30. - Napomene i bibliografske reference uz tekst. - Bibliografija uz
svako poglavlje. - Register.

ISBN 978-86-7589-210-6

1. Vujoxevi Janiqi, Milena, 1980- [autor][ilustrator]
a) Softver { Testirae

COBISS.SR-ID 191794697

Copyright ©Milena Vujošević Janičić
Ovo delo zaštićeno je licencom Creative Commons CC BY-NC-ND 4.0 (Attribution-
NonCommercial-NoDerivatives 4.0 International License). Detalji licence mogu se videti
na veb-adresi http://creativecommons.org/licenses/by-nc-nd/4.0/. Dozvoljeno je
umnožavanje, distribucĳa i javno saopštavanje dela, pod uslovom da se navedu imena
autora. Upotreba dela u komercĳalne svrhe nĳe dozvoljena. Prerada, preoblikovanje i
upotreba dela u sklopu nekog drugog nĳe dozvoljena.

<!-- pdf_page=7 printed_page=7 -->

Ružici i Mihajlu

<!-- pdf_page=9 printed_page=9 -->

Predgovor

Ova knjiga nastala je kao rezultat držanja predmeta Verifikacĳa softvera koji već više
od osam godina predajem studentima master studĳa na Matematičkom fakultetu
Univerziteta u Beogradu. Tokom tog perioda nastavni materĳali su se postepeno
razvĳali, dopunjavali i unapređivali, prateći kako razvoj oblasti verifikacĳe sof-
tvera tako i iskustva stečena u radu sa generacĳama studenata. Upravo je iz tog
kontinuiranog nastavnog i naučnog rada proistekla ova knjiga.

Knjiga obuhvata sve teme koje se obrađuju u okviru kursa. Svaka oblast ilustrovana
je brojnim primerima koji bi trebalo da olakšaju razumevanje osnovnih koncepata
i njihove praktične primene. Na širokim marginama uz tekst nalaze se kratke
napomene sa zanimljivostima i aktuelnim informacĳama iz oblasti verifikacĳe
softvera. Na kraju svake tematske celine dat je spisak pitanja koja mogu poslužiti za
proveru savladanog znanja. Pitanja se često sastoje iz više delova, pa je potrebno
odgovoriti na svaki od njih — od najopštĳeg, kojim se proverava razumevanje šireg
konteksta i osnovnih ideja, do najspecifičnĳeg, koji zahteva detaljno poznavanje
obrađenog gradiva.

Tokom rada na ovoj knjizi imala sam podršku i pomoć velikog broja kolega
i studenata, kojima ovom prilikom želim da izrazim svoju iskrenu zahvalnost.
Zahvalnost dugujem profesorima Viktoru Kunčaku, Dušanu Tošiću i Silvĳi Gilezan
čĳi su rad i ideje uticali na moja interesovanja i istraživanja u oblasti verifikacĳe
softvera. Zahvaljujem se Petru Jovanoviću, kolegi iz kompanĳe Syrmia (danas
HTEC Group), koji mi je pružio priliku da steknem dragoceno industrĳsko iskustvo
poverivši mi razvoj i vođenje projekta zasnovanog na statičkoj analizi softvera,
sa ciljem automatizacĳe provere usklađenosti koda sa standardom AUTOSAR
C++14. Zahvaljujem se i Katarini Šonjić Vujić i Filipu Vujiću koji su me uključili u
organizacĳu konferencĳe Belgrade Test Conference, povezali sa zajednicom koja se
bavi testiranjem softvera i time doprineli proširivanju mojih znanja. Zahvaljujem se
kolegi Milanu Bankoviću na zanačajnom doprinosu u početnoj verzĳi materĳala za
poglavlje Proveravanje modela.

Zahvalnost dugujem asistentima na kursu, Ani Vulović i Ivanu Ristoviću, koji
su kroz pripremu vežbi i rad sa studentima doprineli kvalitetu nastave i razvoju
kursa. Zahvalnost dugujem studentima master studĳa koji su tokom godina, kroz
svoje seminarske radove, doprineli produbljivanju i proširivanju pojedinih tema
iz ove oblasti. Njihova istraživanja, pitanja i zapažanja često su ukazivala na
nove uglove posmatranja i podsticala me da pojedine delove gradiva dodatno

<!-- pdf_page=10 printed_page=10 -->

razjasnim i unapredim. Svi ti seminarski radovi dostupni su na stranici kursa
(https://www.verifikacijasoftvera.matf.bg.ac.rs/) i predstavljaju vredan
dopunski materĳal za studente koji žele da dalje istražuju teme iz knjige.

Zahvalnost dugujem i doktorandima koji su svoja doktorska istraživanja usmerili ka
temama iz oblasti verifikacĳe softvera, a čĳi su rad i diskusĳe u velikoj meri uticali
na oblikovanje pojedinih delova ove knjige: Mirku Spasiću, Milanu Čuguroviću
i Strahinji Stanojeviću. Zahvaljujem se i studentima koji su svoje master radove
posvetili oblastima obuhvaćenim ovom knjigom. Njihov rad i rezultati značajno su
doprineli razvoju i produbljivanju pojedinih tema: Veronika Marinković, Aleksandar
Stefanović, Milica Kleut, Jovana Bošković, Nikola Perić, Vladimir Vuksanović, Ana
Petrović, Milica Galjak, Mirko Brkušanin, Ognjen Plavišić, Irena Blagojević, Nikola
Dimić, Lazar Mladenović, Strahinja Stanojević, Ivan Ristović, Ðorđe Todorović,
Marina Nikolić, Nikola Vidič, Ana Mitrović, Ana Ðorđević, Aleksandra Karadžić,
Nikola Prica i Branislava Živković.

Tokom pripreme rukopisa mnogi studenti i kolege su pomogle u izradi i unapređiva-
nju ilustracĳa i dĳagrama koji prate tekst, čime su doprineli jasnĳem i preglednĳem
predstavljanju pojedinih koncepata. Zahvaljujem se Petru Ðekanoviću, Vukanu
Antiću, Aleksandru Šarbajiću, Milici Gnjatović, Pavlu Cvejoviću, Bojanu Bardžiću,
Neveni Mĳailović, Andrĳani Bosiljčić, Milici Kleut, Dunji Čitlučanin i Tamari Ðukić.
Takođe sam zahvalna studentima koji su ukazali na greške, nejasnoće i propuste u
tekstu. Njihove pažljive primedbe bile su od velike pomoći u unapređenju konačne
verzĳe rukopisa. Zahvaljujem se studentima Lazaru Saviću, Staši Ðorđević, Marku
Lazareviću, Anđeli Jovanović i Aleksandru Ivanoviću.

Zahvalnost dugujem recenzentima, Mirku Spasiću i Maji Vukasović, na pažljivom
čitanju rukopisa, korisnim savetima i konstruktivnim sugestĳama koje su znatno
doprinele poboljšanju njenog sadržaja i strukture.

Na kraju, posebno se zahvaljujem svom suprugu, Predragu Janičiću, koji je pažljivo
čitao rukopis, davao dragocene komentare i sugestĳe i time značajno doprineo
kvalitetu ove knjige.

Beograd, 2026.

Milena Vujošević Janičić

<!-- pdf_page=11 printed_page=11 -->

Sadržaj

Ispravnost i neispravnost softvera
1

1
Kvalitet softvera
3

1.1
Upravljanje kvalitetom softvera . . . . . . . . . . . . . . . . . . . . .
4

1.2
Standardi . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
4

1.3
Atributi kvaliteta softvera . . . . . . . . . . . . . . . . . . . . . . . .
5

1.3.1
Funkcionalna podobnost . . . . . . . . . . . . . . . . . . . .
6

1.3.2
Performantnost
. . . . . . . . . . . . . . . . . . . . . . . . .
6

1.3.3
Kompatibilnost
. . . . . . . . . . . . . . . . . . . . . . . . .
8

1.3.4
Pouzdanost . . . . . . . . . . . . . . . . . . . . . . . . . . . .
9

1.3.5
Upotrebljivost . . . . . . . . . . . . . . . . . . . . . . . . . .
10

1.3.6
Bezbednost . . . . . . . . . . . . . . . . . . . . . . . . . . . .
12

1.3.7
Sigurnost . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
13

1.3.8
Održivost . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
15

1.3.9
Prenosivost . . . . . . . . . . . . . . . . . . . . . . . . . . . .
20

2
Greške u softveru
23

2.1
Primeri poznatih grešaka . . . . . . . . . . . . . . . . . . . . . . . .
24

2.1.1
Neprĳatnosti i materĳalni gubici . . . . . . . . . . . . . . . .
24

2.1.2
Fatalne posledice
. . . . . . . . . . . . . . . . . . . . . . . .
28

2.2
Troškovi usled grešaka u softveru . . . . . . . . . . . . . . . . . . .
32

3
Verifikacĳa i validacĳa softvera
37

3.1
Odnos verifikacĳe i validacĳe softvera . . . . . . . . . . . . . . . . .
38

3.2
Tehnike verifikacĳe softvera
. . . . . . . . . . . . . . . . . . . . . .
40

Dinamička verifikacija softvera
45

4
Testiranje
47

4.1
Testiranje i razvoj softvera . . . . . . . . . . . . . . . . . . . . . . . .
47

4.1.1
Cena greške u kontekstu vremena otkrivanja . . . . . . . . .
48

4.1.2
Uloga testera u razvoju softvera . . . . . . . . . . . . . . . .
50

4.1.3
Faze testiranja softvera
. . . . . . . . . . . . . . . . . . . . .
52

<!-- pdf_page=12 printed_page=12 -->

4.2
Vrste i nivoi testiranja . . . . . . . . . . . . . . . . . . . . . . . . . .
62

4.2.1
Testiranje jedinica koda . . . . . . . . . . . . . . . . . . . . .
63

4.2.2
Komponentno i integraciono testiranje
. . . . . . . . . . . .
65

4.2.3
Sistemsko testiranje . . . . . . . . . . . . . . . . . . . . . . .
68

4.3
Tehnike testiranja
. . . . . . . . . . . . . . . . . . . . . . . . . . . .
86

4.3.1
Pokrivenost testiranjem . . . . . . . . . . . . . . . . . . . . .
87

4.3.2
Podela tehnika testiranja
. . . . . . . . . . . . . . . . . . . .
88

4.3.3
Testiranje crne kutĳe
. . . . . . . . . . . . . . . . . . . . . .
92

4.3.4
Testiranje bele kutĳe . . . . . . . . . . . . . . . . . . . . . . .
104

4.3.5
Metamorfno testiranje . . . . . . . . . . . . . . . . . . . . . .
117

4.4
Načini sprovođenja testiranja . . . . . . . . . . . . . . . . . . . . . .
120

4.4.1
Manuelno testiranje . . . . . . . . . . . . . . . . . . . . . . .
121

4.4.2
Automatsko izvršavanje test primera . . . . . . . . . . . . .
122

4.4.3
Automatsko generisanje test primera . . . . . . . . . . . . .
124

5
Debagovanje
129

5.1
Veza izvršivog koda i debagera . . . . . . . . . . . . . . . . . . . . .
130

5.1.1
Režim prevođenja za upotrebu . . . . . . . . . . . . . . . . .
131

5.1.2
Režim prevođenja za pronalaženje grešaka . . . . . . . . . .
132

5.1.3
Kombinovani režimi prevođenja . . . . . . . . . . . . . . . .
134

5.1.4
Anti-debagovanje . . . . . . . . . . . . . . . . . . . . . . . .
136

5.2
Vrste debagovanja . . . . . . . . . . . . . . . . . . . . . . . . . . . .
136

5.2.1
Interaktivno debagovanje . . . . . . . . . . . . . . . . . . . .
137

5.2.2
Udaljeno debagovanje . . . . . . . . . . . . . . . . . . . . . .
144

5.2.3
Debagovanje nakon prekida izvršavanja programa
. . . . .
145

5.3
Primeri debagera . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
147

5.4
Otvoreni problemi . . . . . . . . . . . . . . . . . . . . . . . . . . . .
152

5.5
Štampanje umesto debagera
. . . . . . . . . . . . . . . . . . . . . .
153

6
Profajliranje i dinamičko detektovanje grešaka
159

6.1
Instrumentacĳa . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
160

6.2
Profajleri
. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .
166

6.2.1
Upotreba profila . . . . . . . . . . . . . . . . . . . . . . . . .
167

6.2.2
Kvalitet profila . . . . . . . . . . . . . . . . . . . . . . . . . .
169

6.2.3
Profajliranje uzimanjem uzoraka . . . . . . . . . . . . . . . .
170

6.2.4
Instrumentaciono profajliranje . . . . . . . . . . . . . . . . .
174

6.3
Alati za dinamičku detekcĳu grešaka . . . . . . . . . . . . . . . . .
183

6.3.1
Sanitajzeri
. . . . . . . . . . . . . . . . . . . . . . . . . . . .
183

<!-- pdf_page=13 printed_page=13 -->

6.3.2
Alati platforme Valgrind
. . . . . . . . . . . . . . . . . . . .
188

Statička verifikacija softvera
193

7
Semantika programskih jezika
195

7.1
Neformalna semantika
. . . . . . . . . . . . . . . . . . . . . . . . .
197

7.2
Osnovne vrste formalnih semantika . . . . . . . . . . . . . . . . . .
201

7.2.1
Rezonovanje o osobinama programa
. . . . . . . . . . . . .
203

7.2.2
Osnovni elementi semantike . . . . . . . . . . . . . . . . . .
205

7.3
Operaciona semantika . . . . . . . . . . . . . . . . . . . . . . . . . .
212

7.3.1
Prirodna semantika . . . . . . . . . . . . . . . . . . . . . . .
212

7.3.2
Strukturna operaciona semantika . . . . . . . . . . . . . . .
217

7.4
Denotaciona semantika . . . . . . . . . . . . . . . . . . . . . . . . .
220

7.5
Aksiomatska semantika . . . . . . . . . . . . . . . . . . . . . . . . .
226

8
Pregledi koda
235

8.1
Ciljevi pregleda koda . . . . . . . . . . . . . . . . . . . . . . . . . .
236

8.2
Efekti i značaj pregleda koda . . . . . . . . . . . . . . . . . . . . . .
240

8.3
Preporuke za efikasan pregled koda . . . . . . . . . . . . . . . . . .
241

8.4
Formalni pregledi . . . . . . . . . . . . . . . . . . . . . . . . . . . .
245

8.5
Neformalni pregledi . . . . . . . . . . . . . . . . . . . . . . . . . . .
247

9
Simboličko izvršavanje
259

9.1
Simboličko stablo izvršavanja . . . . . . . . . . . . . . . . . . . . . .
260

9.2
Principi dizajna
. . . . . . . . . . . . . . . . . . . . . . . . . . . . .
266

9.3
Konkoličko izvršavanje . . . . . . . . . . . . . . . . . . . . . . . . .
268

9.3.1
Dinamičko simboličko izvršavanje . . . . . . . . . . . . . . .
268

9.3.2
Selektivno simboličko izvršavanje . . . . . . . . . . . . . . .
271

9.4
Strategĳe obilaska putanja
. . . . . . . . . . . . . . . . . . . . . . .
273

9.4.1
Jednostavne strategĳe . . . . . . . . . . . . . . . . . . . . . .
274

9.4.2
Pseudoslučajne strategĳe . . . . . . . . . . . . . . . . . . . .
275

9.4.3
Strategĳe vođene pokrivenošću koda . . . . . . . . . . . . .
276

9.4.4
Strategĳe usmerene ka dostizanju ciljne tačke
. . . . . . . .
279

9.4.5
Kombinovana strategĳa . . . . . . . . . . . . . . . . . . . . .
281

9.5
Izazovi simboličkog izvršavanja . . . . . . . . . . . . . . . . . . . .
281

9.5.1
Eksplozĳa broja stanja i putanja . . . . . . . . . . . . . . . .
283

9.5.2
Modelovanje memorĳe . . . . . . . . . . . . . . . . . . . . .
290

9.5.3
Rešavanje ograničenja . . . . . . . . . . . . . . . . . . . . . .
299

<!-- pdf_page=14 printed_page=14 -->

10 Proveravanje modela
305

10.1 Osnove i motivacĳa
. . . . . . . . . . . . . . . . . . . . . . . . . . .
305

10.1.1
Osnovni pojmovi
. . . . . . . . . . . . . . . . . . . . . . . .
306

10.1.2
Primene proveravanja modela . . . . . . . . . . . . . . . . .
310

10.2 Pravljenje modela
. . . . . . . . . . . . . . . . . . . . . . . . . . . .
312

10.2.1
Modelovanje jednostavnih sistema
. . . . . . . . . . . . . .
314

10.2.2 Modelovanje hardvera
. . . . . . . . . . . . . . . . . . . . .
320

10.2.3 Modelovanje softvera . . . . . . . . . . . . . . . . . . . . . .
322

10.3 Formalna specifikacĳa . . . . . . . . . . . . . . . . . . . . . . . . . .
327

10.3.1
Klase svojstava . . . . . . . . . . . . . . . . . . . . . . . . . .
327

10.3.2 Temporalne logike . . . . . . . . . . . . . . . . . . . . . . . .
330

10.3.3 Linearna temporalna logika
. . . . . . . . . . . . . . . . . .
332

10.3.4 Logike CTL∗i CTL . . . . . . . . . . . . . . . . . . . . . . . .
338

10.4 Algoritmi za proveravanje modela . . . . . . . . . . . . . . . . . . .
340

10.4.1
Obilazak grafa tranzicionog sistema . . . . . . . . . . . . . .
340

10.4.2 Provera LTL svojstva putem Bihĳevih automata . . . . . . .
342

10.5 Kontrola kombinatorne eksplozĳe u proveravanju modela
. . . . .
346

10.5.1
Apstrakcĳa predikata . . . . . . . . . . . . . . . . . . . . . .
347

10.5.2 Simboličko proveravanje modela . . . . . . . . . . . . . . . .
351

10.5.3 Ograničeno proveravanje modela . . . . . . . . . . . . . . .
354

11 Apstraktna interpretacĳa
365

11.1
Konkretan i apstraktan domen . . . . . . . . . . . . . . . . . . . . .
366

11.2 Konkretno izvršavanje i apstraktna interpretacĳa
. . . . . . . . . .
372

11.3 Formalne osnove apstraktne interpretacĳe
. . . . . . . . . . . . . .
381

11.4 Praktične primene . . . . . . . . . . . . . . . . . . . . . . . . . . . .
389

Indeks pojmova
393

<!-- pdf_page=15 printed_page=15 -->

Ispravnost i neispravnost
softvera

<!-- pdf_page=17 printed_page=17 -->

Pregled

1.1
Upravljanje kvali-
tetom softvera . .
4

▶Koji procesi su važni za kvalitet softvera?
▶Koji su standardi kvaliteta softvera najbitnĳi i šta
oni definišu?

1.2
Standardi . . . . .
4

1.3
Atributi kvaliteta
softvera . . . . . .
5

▶Kojim se atributima opisuje kvalitet softvera?
▶Koji atributi kvaliteta softvera su važni za bankar-
ske aplikacĳe, koji za autonomnu vožnju, koji za
kalkulator, koji za onlajn prodaju karata, a koji za
sisteme za razmenu poruka?

Tokom poslednjih godina, IT industrĳa se brzo razvi-
ja i predstavlja jednu od najdinamičnĳih industrĳa u
svetu. Softver se razvĳa za veoma raznovrsne uređaje i
svrhe. Ove namene obuhvataju oblasti poput interneta
stvari, virtuelne i proširene stvarnosti, igara i zabave,
pametnih okruženja i zdravstvene zaštite. Takođe, sof-
tver ima ključnu ulogu u razvoju veštačke inteligencĳe,
obradi velikih podataka, poslovnim, naučnim i vojnim
primenama, kao i u savremenim komunikacionim teh-
nologĳama.

Razvoj softvera je složen proces koji obuhvata veliki broj
različitih aktivnosti, od kojih se osnovne mogu grupisati
u:

▶analizu sistema i specifikacĳu zahteva,
▶projektovanje i implementacĳu softvera,
▶upravljanje kvalitetom softvera i
▶održavanje softvera.

Slika 1.1: Softver je svuda oko
nas. Počevši od malih kućnih
aparata, preko telefona, prevo-
znih sredstava, satelita, raketa,
aparata u zdravstvu — gotovo
da više ne postoji elektronski
uređaj koji u sebi ne sadrži ne-
kakav softver.

Sa sve većim obimom proizvodnje softvera, raste i po-
treba za efikasnĳim upravljanjem procesima njegove
izrade. U procesu razvoja softvera, ključno je da se do-
stupni resursi optimalno iskoriste kako bi se na vreme
zadovoljili korisnički zahtevi i obezbedio visok kvalitet
softverskog proizvoda.

<!-- pdf_page=18 printed_page=4 -->

### 1.1 Upravljanje kvalitetom softvera

Upravljanje kvalitetom softvera (eng. quality management)
obuhvata principe, metode i procese koji se koriste za
obezbeđivanje i unapređivanje kvaliteta softvera. Cilj
upravljanja kvalitetom je da se ispune zahtevi korisnika,
optimizuju poslovni procesi i smanji broj defekata.

Visok kvalitet softvera predstavlja ključni faktor njegove
uspešnosti, bilo da se koristi u komercĳalne svrhe na tr-
žištu ili u okviru specifičnih, nekomercĳalnih okruženja.
Standardi kvaliteta softvera definišu smernice i pro-
pise koji omogućavaju sistematski pristup upravljanju
kvalitetom. Pored toga, za postizanje visokokvalitet-
nog softvera neophodna je automatizovana podrška i
upotreba sofisticiranih alata.

Osnovni procesi koji su vezani za kvalitet softvera su:

▶planiranje kvaliteta softvera,
▶obezbeđivanje (eng. assurance) kvaliteta softvera,
▶kontrolu (eng. control) kvaliteta softvera i
▶poboljšanje kvaliteta softvera.

Planiranje kvaliteta je neophodno kako bi se definisao
pristup razvoju softvera koji omogućava postizanje že-
ljenog nivoa kvaliteta. Na primer, različiti nivoi kvaliteta
očekuju se za softver aviona i za igricu na mobilnom
telefonu. Obezbeđivanje kvaliteta podrazumeva uklju-
čivanje aspekata kvaliteta u svakodnevni razvoj, dok
kontrola treba da obezbedi kvalitet krajnjeg proizvoda.
Na kraju, poboljšanje kvaliteta podrazumeva kontinuira-
no praćenje i unapređivanje procesa razvoja kroz analizu
povratnih informacĳa i primenu novih metodologĳa.

### 1.2 Standardi

Željeni kvalitet softvera definiše se softverskim zahtevi-
ma, ali može biti nametnut i različitim međunarodnim
standardima. Serĳa standarda ISO/IEC 25000 sadrži

<!-- pdf_page=19 printed_page=1 -->

okvir za procenu kvaliteta softvera. Najvažnĳi standard
u ovoj serĳi je ISO/IEC 25010. Ovaj standard definiše
devet karakteristika kvaliteta softvera, koje se obično
nazivaju atributima kvaliteta softvera. Standard ISO/I-
EC 25023 opisuje kako se ove karakteristike kvaliteta
koriste za merenje ukupnog kvaliteta proizvoda.

Postoje i važni IEEE standardi. Na primer, standard IEEE
730 daje smernice za pokretanje, planiranje, kontrolu i
izvršavanje procesa obezbeđenja kvaliteta softvera, dok
standard IEEE 1012-2016 definiše procese verifikacĳe i
validacĳe za razvoj softvera i hardvera.

### 1.3 Atributi kvaliteta softvera

Standard ISO 25010 definiše hĳerarhĳu devet atributa
kvaliteta (slika 1.2): funkcionalna podobnost, perfor-
mantnost, kompatibilnost, pouzdanost, upotrebljivost,
bezbednost, sigurnost, održivost i prenosivost. Svaki
atribut uključuje svoje podatribute. U zavisnosti od svr-
he i ciljeva softvera, svaki atribut kvaliteta softvera može
imati različit nivo važnosti.

funkcionalna
podobnost

ATRIBUTI
KVALITETA
SOFTVERA

prenosivost

performantnost
(efikasnost)

održivost

kompatibilnost

sigurnost

pouzdanost

upotrebljivost

bezbednost

funkcionalna
ispravnost

naučljivost

modularnost

operativna
ograničenost

prilagodljivost

vremensko
ponašanje

poverljivost

funkcionalna
potpunost

operabilnost

iskoristivost

zrelost

instalabilnost

identifikacĳa
rizika

integritet

korišćenje
resursa

koegzistencĳabil-
nost

zaštita od
korisničkih
grešaka

analizabilnost

funkcionalna
prikladnost

dostupnost

zamenljivost

odgovornost

izmenljivost

otporanost
na greške

bezbednost kvara

kapacitet

interoperabilnost

autentifikabilnost

estetika ko-
risničkog
interfejsa

testabilnost

upozorenje
na opasnost

sposobnost
oporavka

neporecivost

bezbednost
integracĳe

pristupačnost

prepoznatljivost
svrhe aplikacĳe

Slika 1.2: Atributi softvera u skladu sa kategorizacĳom standarda ISO/IEC 25010.

<!-- pdf_page=20 printed_page=6 -->

1.3.1 Funkcionalna podobnost

Funkcionalna podobnost (eng. functional suitability) od-
govara stepenu u kojem softver ispunjava funkcionalne
zahteve i obuhvata naredne podatribute:

funkcionalnu ispravnost — softver treba da daje tačne
rezultate,

funkcionalnu potpunost — dostupnost funkcĳa koje
su očekivane specifikacĳom i

funkcionalnu prikladnost — ispunjavanje očekivane
funkcionalnosti.

funkcionalna
podobnost

Primer 1.3.1 (Kalkulator) Razmotrimo primer jedno-
stavnog kalkulatora.

Funkcionalna ispravnost podrazumeva da kalkulator
uvek računa ispravne vrednosti. Na primer, kalkulator
treba da ne greši u sabiranju dva broja.

funkcionalna
ispravnost

Funkcionalna potpunost podrazumeva da kalkulator
ima dostupne sve funkcionalnosti predviđene specifi-
kacĳom. Na primer, željene funkcionalnosti mogu da
budu sabiranje, oduzimanje, množenje i deljenje.

funkcionalna
potpunost

funkcionalna
prikladnost

Funkcionalna prikladnost podrazumeva da se kalku-
lator ponaša na očekivani način. Na primer, kalkulator
ne treba da ima neočekivane dodatne opcĳe kao što
su skidanje sadržaja sa interneta ili puštanje filmova.

1.3.2 Performantnost

Performantnost (efikasnost) (eng. performance) odgo-
vara stepenu u kojem softver zadovoljava vremenske
i resursne zahteve. Performantnost obuhvata naredne
podatribute:

vremensko ponašanje — vreme odgovora i obrade (ko-
liko vremena je potrebno da aplikacĳa da odgovor
korisniku, odnosno da obradi neke netrivĳalne

<!-- pdf_page=21 printed_page=1 -->

zahteve), stopa protoka (koliko transakcĳa je apli-
kacĳa u mogućnosti da obradi u jedinici vremena),

korišćenje resursa — količina i vrsta korišćenih resursa
i

kapacitet — maksimalna ograničenja (npr. broj kori-
snika ili veličine ulaza koje aplikacĳa može da
obradi).

performantnost
(efikasnost)

Primer 1.3.2 (Kupovina karata) Razmotrimo primer
sistema za onlajn rezervacĳu i kupovinu avionskih
karata. Ponašanje ovog sistema treba razmotriti u
odnosu na svakog pojedinačnog korisnika sistema, ali
i u kontekstu mogućeg velikog opterećenja sistema
u situacĳama kada veliki broj korisnika istovremeno
želi da rezerviše ili kupi kartu.

vremensko
ponašanje

Vremensko ponašanje ovog sistema uključuje i:

korišćenje
resursa

vreme odgovora (odziva) aplikacĳe pri pretraživa-
nju dostupnih karata i

kapacitet

vreme obrade potrebno za rezervacĳu ili plaćanje
karte.

Na primer, očekivanja koja se postavljaju visokoefika-
snom sistemu su da:

pretraga karata treba da se izvrši za manje od dve
sekunde u 97% slučajeva,

prikaz rezultata pretrage (lista dostupnih karata) mo-
ra da se učita u roku od tri sekunde za 95%
zahteva,

plaćanje i potvrda rezervacĳe ne smeju trajati duže
od pet sekundi u 99% slučajeva.

U ovakvom sistemu često je prisutna i komunikacĳa
sa spoljnim sistemima (kao što su baze podataka ili
eksterni API servisi za plaćanje), te u tom kontekstu
može se postaviti uslov da kašnjenje odgovora ek-
sternih sistema ne sme biti veće od jedne sekunde.
Relevantni resursi čĳu upotrebu treba pratiti za ovu
aplikacĳu su procesor, memorĳa, baza podataka i

<!-- pdf_page=22 printed_page=8 -->

mrežni resursi. Na primer, očekivanja koja mogu da
se postave su:

opterećenje procesora ne sme preći 70% pri normal-
nom radu i ne sme preći 90% pri vršnom opte-
rećenju duže od deset sekundi,

potrošnja RAM memorĳe ne sme preći 8 GB po in-
stanci aplikacĳe tokom normalnog rada,

upotreba baze podataka mora da omogući obradu
do 500 upita u sekundi bez značajnog uspora-
vanja i

potrošnja mrežnih resursa ne sme premašiti 1 GB po
sekundi na pojedinačnim serverima, pri čemu
se ne sme desiti gubitak podataka.

Kapacitet aplikacĳe definiše koliko istovremenih kori-
snika aplikacĳa može da podrži pre nego što perfor-
manse padnu ispod prihvatljivog nivoa. Na primer,
sistem mora da podrži najmanje 10.000 istovremenih
korisnika bez degradacĳe performansi.

1.3.3 Kompatibilnost

kompatibilnost

Kompatibilnost (eng. compatibility) odgovara stepenu u
kojem softver može da funkcioniše na različitim plat-
formama ili da deli podatke sa drugim proizvodima,
sistemima i komponentama. Kompatibilnost obuhvata
naredne podatribute:

koegzistencĳabilnost — sposobnost deljenja okruženja
i resursa sa drugim softverskim proizvodima i

koegzistencĳabil-
nost

interoperabilnost — sposobnost sarađivanja sa drugim
aplikacĳama, korišćenjem ili deljenjem podataka.

interoperabilnost

Primer 1.3.3 (Razmena poruka) Razmotrimo primer
aplikacĳe za razmenu poruka (na primer, aplikacĳu
nalik na WhatsApp, Viber ili Slack). Ova aplikacĳa mora
da funkcioniše zajedno sa drugim aplikacĳama na
uređaju (koegzistencĳabilnost) i treba da može da

<!-- pdf_page=23 printed_page=1 -->

komunicira sa drugim servisima (interoperabilnost).

Na primer, korisnik na svom telefonu koristi aplikaci-
ju za razmenu poruka dok istovremeno sluša muziku
putem aplikacĳe Spotify ili gleda video preko aplika-
cĳe YouTube. Koegzistencĳabilnost podrazumeva da
aplikacĳa ne sme ometati druge aplikacĳe. Na primer,
ako korisnik primi poziv, muzika treba da se automat-
ski pauzira, ali i da nastavi nakon završetka poziva.
Notifikacĳe koje aplikacĳa pruža ne smeju blokirati
druge aplikacĳe ili ometati korisničko iskustvo sa
drugim aplikacĳama.

Interoperabilnost podrazumeva da aplikacĳa treba
da, na primer, omogući korisnicima da šalju slike iz
galerĳe telefona ili sa Google Drive-a. To znači da ima
pristup lokalnoj memorĳi ili eksternim servisima.

1.3.4 Pouzdanost

pouzdanost

Pouzdanost (eng. reliablity) označava stepen u kojem je
softver pouzdan. Pouzdanost obuhvata naredne poda-
tribute:

zrelost — stabilnost tokom svakodnevne upotrebe,
dostupnost — mogućnost neprekidnog rada,
tolerancĳu na greške — sposobnost funkcionisanja čak
i u prisustvu određenih hardverskih i softverskih
kvarova i

zrelost

dostupnost

otporanost
na greške

sposobnost oporavka (povratljivost) — sposobnost vra-
ćanja podataka i procesa u slučaju kvara sistema.

sposobnost
oporavka

Primer 1.3.4 (Hitne službe) Razmotrimo primer siste-
ma za hitne službe (kao što su pozivi policĳi ili prvoj
pomoći). Za ovakve sisteme kritično je da zadovolje
sve kriterĳume pouzdanosti. Pre svega, sistem mora
biti dobro proveren i stabilan, a svaka nova funkcio-
nalnost mora biti temeljno testirana i verifikovana pre
uvođenja — zrelost.

<!-- pdf_page=24 printed_page=10 -->

Sistem mora biti neprekidno dostupan, što znači da
nikada ne sme biti van funkcĳe — dostupnost siste-
ma. To podrazumeva mogućnost simultanog prĳema
velikog broja poziva, kao i postojanje dodatne in-
frastrukture u slučaju pada primarnog sistema ili
njegovih delova.

Ukoliko na nekoj serverskoj lokacĳi dođe do prekida
napajanja, sistem mora nastaviti sa radom bez vidlji-
vih problema. Posao tog servera treba automatski
da bude preusmeren na drugi dostupni server, či-
me se osigurava kontinuitet rada i sprečava gubitak
podataka — tolerancĳa na greške.

Takođe, bitno je da sistem u slučaju softverskog pada
može automatski da se oporavi i nastavi sa radom —
sposobnost oporavka.

1.3.5 Upotrebljivost

Upotrebljivost (eng. usability) odgovara stepenu u kojem
korisnici mogu koristiti softver. Upotrebljivost obuhvata
naredne podatribute:

naučljivost — koliko je jednostavno naučiti kako se
softver koristi,

operabilnost — koliko je lako raditi sa softverom i kon-
trolisati ga,

zaštitu od korisničkih grešaka — mere u okviru sa-
mog softvera koje sprečavaju pravljenje grešaka u
korišćenju,

estetiku korisničkog interfejsa — vizuelnu prĳatnost
i prihvatljivost dizajna,

pristupačnost — mogućnost da osobe sa različitim ste-
penima sposobnosti mogu da koriste softver i

prepoznatljivost svrhe aplikacĳe — jasnoću namene
softvera korisnicima.

Primer 1.3.5 (Bankarska aplikacĳa) Razmotrimo pri-

<!-- pdf_page=25 printed_page=1 -->

mer bankarske aplikacĳe. Ova aplikacĳa mora biti
intuitivna, jednostavna za korišćenje, sigurna i pri-
stupačna svim korisnicima, uključujući i osobe sa
posebnim potrebama. Na primer:

upotrebljivost

Naučljivost. Prilikom prvog korišćenja, korisnik bi tre-
balo da može samostalno da pronađe i izvrši osnovne
radnje (poput slanja novca i provere stanja) za manje
od 5 minuta, bez potrebe za tutorĳalom.

naučljivost

operabilnost

Operabilnost. Ključne funkcionalnosti (poput provere
stanja ili prenosa sredstava između računa) treba da
budu dostupne u manje od četiri klika, omogućavajući
brz i lak rad sa aplikacĳom.

zaštita od
korisničkih
grešaka

estetika ko-
risničkog
interfejsa

Zaštita od korisničkih grešaka. Ako korisnik unese
neispravan broj računa prilikom slanja novca, apli-
kacĳa mora automatski izvršiti validacĳu i upozoriti
korisnika na grešku pre potvrde transakcĳe.

pristupačnost

prepoznatljivost
svrhe aplikacĳe

Estetika korisničkog interfejsa. Aplikacĳa treba da
ima profesionalan i vizuelno prĳatan dizajn. Dizajn bi
trebalo da bude minimalistički, moderan i intuitivan,
sa jasnim kontrastom između elemenata. Treba koristi-
ti harmonične boje i lako čitljive fontove, dok dugmad
i ikonice moraju biti vizuelno jasne i prepoznatljive.

Pristupačnost. Aplikacĳa mora biti pristupačna oso-
bama sa različitim potrebama, uključujući korisnike
sa oštećenjem vida. To znači da treba da bude kompa-
tibilna sa alatima za čitanje ekrana, da fontovi mogu
biti uvećani po potrebi i da kontrast boja omogućava
čitanje osobama sa daltonizmom.

Prepoznatljivost svrhe aplikacĳe. Korisnik odmah tre-
ba da razume da je aplikacĳa namenjena bankarskim
uslugama. Početni ekran treba da sadrži jasno pre-
poznatljive elemente, poput salda računa i dugmeta
za transfer novca. Ikonice i nazivi funkcionalnosti
treba da budu intuitivni i nedvosmisleni (npr. „Plaća-
nje“, „Kartice“, „Računi“), a brend-boje i logo banke
istaknuti.

<!-- pdf_page=26 printed_page=12 -->

1.3.6 Bezbednost

Bezbednost (eng. safety) odgovara stepenu u kojem pro-
izvod, pod definisanim uslovima, izbegava stanje u
kojem su ugroženi ljudski život, zdravlje, imovina ili
životna sredina. Bezbednost obuhvata naredne podatri-
bute:

Bezbednost i sigurnost se u
srpskom jeziku mogu kori-
stiti kao sinonimi. Zbog toga
je bitno napomenuti da se u
kontekstu atributa kvaliteta
softvera bezbednost odnosi
na fizičku bezbednost/si-
gurnost, dok se sigurnost
koristi u kontekstu informa-
cione bezbednosti/sigurno-
sti.

operativnu ograničenost — stepen do kojeg proizvod
ili sistem ograničava svoje funkcionisanje unutar
bezbednih parametara ili stanja prilikom susreta
sa operativnim opasnostima,

identifikacĳa rizika — stepen do kojeg proizvod mo-
že da identifikuje tok događaja ili operacĳa koji
mogu izložiti život, imovinu ili životnu sredinu
neprihvatljivom riziku,

bezbednost kvara — stepen do kojeg proizvod može
automatski da se postavi u bezbedan režim rada
ili da se vrati u bezbedno stanje u slučaju kvara,

bezbednost (eng. safety)
=
fizička bezbednost

upozorenje na opasnost — stepen do kojeg proizvod ili
sistem pruža upozorenja o neprihvatljivim rizici-
ma u operacĳama ili internim kontrolama, kako bi
se omogućila pravovremena reakcĳa i održavanje
bezbednog rada i

sigurnost (eng. security)
=
informaciona bezbednost

bezbednost integracĳe — stepen do kojeg proizvod
može da održi bezbednost tokom i nakon integra-
cĳe sa jednom ili više komponenti.

Standardi kodiranja u auto-
mobilskoj industrĳi se foku-
siraju na kvalitet softvera.
Primeri implementacĳe de-
lova ovih standarda mogu
se videti u master radovima
Mirka Brkušanina:
Implementacĳa pravila iz stan-
darda AUTOSAR C++14 u
okviru programskog prevodioca
Clang
i Ognjena Plavšića:
Alat za statičku analizu i
predlaganje izmena u C++ kodu

Primer 1.3.6 (Autonomna vožnja) U sistemu za au-
tonomnu vožnju svi atributi sigurnosti su izuzetno
važni.

Operativna ograničenost — Automobil mora ograni-
čiti svoje manevre (npr. brzinu, skretanje) u skladu sa
bezbednim parametrima, posebno pri lošim vremen-
skim uslovima ili oštećenjima na putu.

Identifikacĳa rizika — Sistem treba da ume da pre-
pozna potencĳalne opasnosti kao što su pešaci koji
iznenada prelaze ulicu, druga vozila koja se kreću

<!-- pdf_page=27 printed_page=1 -->

nepredvidivo ili prepreke na putu.

Bezbednost kvara — U slučaju otkaza senzora ili ra-
čunarskog sistema, automobil mora automatski da se
zaustavi na bezbedan način ili da preuzme minimal-
no funkcionalno stanje koje ne ugrožava putnike ili
druge učesnike u saobraćaju.

bezbednost

operativna
ograničenost

Upozorenje na opasnost — Ako se pojavi situacĳa
koju sistem ne može da reši sam, mora brzo upozoriti
vozača ili centralni nadzorni sistem na opasnost.

identifikacĳa
rizika

bezbednost kvara

Bezbednost integracĳe — Kada se novi moduli (npr.
dodatni senzori ili softverske nadogradnje) integrišu
u postojeći sistem, ceo sistem mora i dalje održavati
visok nivo bezbednosti i ne sme uvoditi nove rizike.

upozorenje
na opasnost

bezbednost
integracĳe

1.3.7 Sigurnost

Sigurnost (eng. security) odgovara stepenu u kojem sof-
tver štiti informacĳe i podatke. Sigurnost obuhvata
naredne podatribute:

poverljivost — dostupnost podataka samo ovlašćenim
korisnicima,

integritet — sprečavanje neovlašćenog pristupa i modi-
fikacĳe podataka,

odgovornost — mogućnost praćenja radnji korisnika,
autentifikabilnost — mogućnost dokazivanja identite-
ta korisnika i

neporecivost — nemogućnost osporavanja, tj. moguć-
nost prikupljanja informacĳa o određenim aktiv-
nostima i događajima.

Primer 1.3.7 (Bankarska aplikacĳa — nastavak prime-
ra 1.3.5) Bankarske aplikacĳe moraju biti maksimalno
sigurne, jer rukovode osetljivim finansĳskim podaci-
ma korisnika i omogućavaju transakcĳe koje ne smeju
biti zloupotrebljene. Bankarska aplikacĳa je odličan
primer aplikacĳe kod koje je kritična sigurnost jer je

<!-- pdf_page=28 printed_page=14 -->

potrebno:

▶Održavati poverljivost — podaci korisnika

mo-
raju biti maksimalno zaštićeni. Na primer, uko-
liko korisnik može da pristupi svojoj mobilnoj
banci i pregleda stanje na računu — niko drugi
ne sme videti ove informacĳe. To uključuje da
pristup aplikacĳi mora biti zaštićen lozinkom,
PIN-om ili biometrĳom (otisak prsta, prepozna-
vanje lica), podaci moraju biti šifrovani tokom
prenosa i skladištenja, a sama aplikacĳa ne sme
dozvoliti snimanje ekrana kako bi se sprečilo
curenje podataka.

sigurnost

poverljivost

integritet

odgovornost

▶Garantovati integritet — transakcĳe ne smeju
biti neovlašćeno menjane. Na primer, ukoliko
korisnik izvrši uplatu putem aplikacĳe, transak-
cĳa mora biti tačna i niko ne sme neovlašćeno
izmeniti iznos uplate. Banka mora da šifruje
podatke tokom prenosa, svaka transakcĳa mora
da ima digitalni potpis koji potvrđuje da nĳe
menjana, a sistem mora da može da detektuje
bilo kakve neovlašćene izmene podataka i da ih
pritom odmah blokira.

autentifikabilnost

neporecivost

▶Obezbediti odgovornost — sve aktivnosti se
beleže i mogu se proveriti. Na primer, ukoliko se
korisnik žali da neko neovlašćeno koristi njegov
račun – banka mora biti u stanju da proveri ko
je koristio aplikacĳu i kada.

▶Osigurati autentifikabilnost — samo pravi kori-
snik može pristupiti svom računu. Banka mora
biti sigurna da se korisnik koji pokušava da se
prĳavi u aplikacĳu zaista identifikuje kao pravi
vlasnik računa. Ovo se može ostvariti korišće-
njem višefaktorske autentifikacĳe koja uključuje
na primer lozinku, biometrĳu i jednokratne ko-
dove. Dodatno, prĳava preko novog uređaja
treba da zahteva dodatnu verifikacĳu putem
elektronske pošte ili telefonskog poziva.

▶Omogućiti neporecivost — korisnik ne može

<!-- pdf_page=29 printed_page=1 -->

kasnĳe tvrditi da nĳe izvršio transakcĳu. To se
može ostvariti digitalnim potpisivanjem kripto-
grafskim ključevima. Pri tome, logovi moraju
biti nepromenljivi, tako da niko, pa ni admini-
stratori, ne mogu izbrisati ili izmeniti istorĳu
transakcĳa.

1.3.8 Održivost

Održivost (eng. maintainability) odgovara lakoći integri-
sanja promena. Promene uključuju dodavanje novih
funkcionalnosti, ispravljanje grešaka, poboljšanje per-
formansi, kao i prilagođavanje promenjenim zahtevima
korisnika ili izmenjenom okruženju. Izmene zahteva-
ju:

1. razumevanje softvera;

2. pronalaženje delova softvera koje treba izmeniti;
3. izvođenje željenih izmena;
4. proveru da izmenama nisu poremećene postojeće
funkcionalnosti.

Održivost se odnosi na lakoću svih ovih koraka. Smatra
se jednim od ključnih atributa kvaliteta.

Održivost je statička karakteristika softvera koja ne utiče
direktno na performanse i karakteristike softvera koje
su vidljive krajnjem korisniku. Iako ne utiče direktno
na ponašanje sistema u radu, ima značajan uticaj na
dugoročni kvalitet i održavanje softvera. Primeri metrika
softvera koje su važne u kontekstu održivosti su:

veličina (eng. size) — broj linĳa koda,
spregnutost (eng. coupling) — kvantitativna mera me-
đuzavisnosti između različitih modula,

kohezĳa (eng. cohesion) — kvantitativna mera poveza-
nosti funkcĳa ili objekata unutar istog modula,

ciklomatska složenost (eng. cyclomatic complexity) —
kvantitativna mera broja linearno nezavisnih pu-
tanja kontrole toka programa. Izračunava se po
formuli: 𝐶= 𝐸−𝑁+ 2𝑃, gde je:

<!-- pdf_page=30 printed_page=16 -->

▶𝐸broj grana (eng. edges) u grafu kontrole
toka programa,

▶𝑁broj čvorova (eng. nodes),
▶𝑃broj povezanih komponenti.

Mala veličina, niska spregnutost, visoka kohezĳa i ni-
ska ciklomatska složenost su karakteristike održivog
softvera. Kako se dizajn softvera i njegov ukupni kvali-
tet vremenom pogoršavaju, neophodno je primenjivati
različite tehnike za očuvanje održivosti. Refaktorisanje
softvera predstavlja proces poboljšanja dizajna posto-
jećeg koda i ključni je deo održavanja tokom evolucĳe
softvera. Održivost uključuje naredne podatribute: mo-
dularnost, iskoristivost, analizabilnost, izmenljivost i
testabilnost.

održivost

Modularnost se odnosi na stepen u kome je softver lo-
gički podeljen na nezavisne i međusobno zamenljive
module. Razbĳanje softvera na module (jedinice, kompo-
nente) omogućava skrivanje njegove ukupne složenosti
kroz apstrakcĳu i definisanje interfejsa. Modularnost
se obično postavlja kao jedan od ključnih ciljeva u fazi
dizajna softvera.

modularnost

iskoristivost

Idealan modul treba da bude:

analizabilnost

▶relativno male dimenzĳe,
▶niske ciklomatske složenosti,
▶visoke kohezĳe,
▶minimalno spregnut sa ostalim modulima.

izmenljivost

testabilnost

Ovakvi moduli se onda mogu nezavisno odvajati i fleksi-
bilno kombinovati na različite načine. Modularnost pod-
razumeva i standardizovane interfejse između modula,
što je posebno naglašeno u savremenim softverskim
arhitekturama poput mikroservisa.

Iskoristivost (ponovna upotrebljivost) predstavlja stepen
u kome se komponente jednog sistema mogu koristiti u
drugim sistemima. Postoje različiti nivoi iskoristivosti,
uključujući ponovnu upotrebu:

▶specifikacĳa,

<!-- pdf_page=31 printed_page=1 -->

▶dizajna,
▶koda,
▶podataka i
▶testova.

Umesto razvoja novih funkcionalnosti uvek treba razmo-
triti iskoristivost postojećih komponenti. Glavne pred-
nosti ponovne upotrebe uključuju:

▶povećanje produktivnosti,
▶smanjenje troškova,
▶poboljšanje kvaliteta,
▶ubrzanje razvoja i
▶smanjenje rizika u procesu razvoja.

Analizabilnost označava lakoću analize i razumevanja
softvera, te direktno utiče na prva dva koraka unoše-
nja izmena: (1) razumevanje softvera i (2) pronalaženje
delova softvera koje je potrebno izmeniti. Direktno je
povezana sa modularnošću (dobra modularnost sma-
njuje kompleksnost i time poboljšava analizabilnost) i
iskoristivošću (korišćenje postojećih komponenti olak-
šava analizu koda). Analizabilnost se poboljšava i kroz
postojanje dobre dokumentacĳe i kroz dosledno pošto-
vanje kodnih standarda. Za razumevanje neispravnog
ponašanja softvera, postojanje mehanizma za praćenje
rada sistema i aktivnosti korisnika može značajno da
poboljša analizabilnost.

Izmenljivost predstavlja lakoću implementacĳe izmena
bez uvođenja grešaka. Ključni pokazatelj izmenljivosti
je spregnutost, jer visoka spregnutost povlači potrebu
za izmenama u različitim delovima koda što dodatno
povećava i verovatnoću uvođenja grešaka. Dobra modu-
larnost utiče pozitivno na izmenljivost jer podrazumeva
smanjenje kompleksnosti i ograničava uticaj izmena na
lokalne delove koda.

Testabilnost označava lakoću provere da li su izmene
narušile postojeće funkcionalnosti. Prednosti visoke

<!-- pdf_page=32 printed_page=18 -->

testabilnosti uključuju bržu isporuku korisnicima i če-
šću povratnu informacĳu o ispravnosti softvera pro-
gramerima. Praktični izazovi uključuju balans između
potpunosti testova i vremena njihovog izvršavanja. Za
testabilnost je ključna automatizacĳa procesa testiranja,
mogućnost automatskog generisanja testova kao i do-
stupnost test slučajeva sa unapred poznatim rezultatom
izvršavanja.

Primer 1.3.8 (Razmena poruka - nastavak primera
1.3.3) Aplikacĳa za razmenu poruka mora da bude
laka za održavanje jer je karakteriše često dodava-
nje novih funkcionalnosti u skladu sa potrebama i
zahtevima korisnika.

Aplikacĳa za razmenu poruka treba da ima različite
funkcionalnosti, kao što su sistem za slanje poru-
ka, sistem za obaveštenja, korisničke postavke, lič-
no/grupno slanje poruka i sistem za autentifikacĳu.
Implementacĳa koju karakteriše lako održavanje je
modularna, odnosno podeljena u različite module
koje odgovaraju prethodno navedenim funkcionalno-
stima. Svaki od ovih modula mora da bude nezavisan,
ali poveziv sa ostatkom sistema putem jasno defini-
sanih interfejsa za komunikacĳu. Na primer, sistem
za autentifikacĳu mora biti odvojen od sistema za po-
ruke i pozive, kako bi se omogućilo lakše upravljanje
bez uticaja na ostatak aplikacĳe.

Poželjno je da se aplikacĳa može koristiti na različi-
tim platformama, na primer, na mobilnim telefonima
(Android, iOS) i desktop računarima (Linux, Windows).
Da bi se to ostvarilo, ključna je iskoristivost odnosno
da postoji mogućnost ponovne upotrebe koda. Sve
komponente i funkcionalnosti, koje nisu specifične za
platformu, potrebno je dizajnirati tako da ih je moguće
koristiti na različitim platformama. Na primer, sistem
za prĳavu treba da bude identičan na svim platforma-
ma, omogućavajući korisnicima da se prĳave koristeći

<!-- pdf_page=33 printed_page=1 -->

isti način verifikacĳe na svakom uređaju.

Analizabilnost aplikacĳe omogućava brzo praćenje i
analiziranje problema (na primer, ukoliko korisnici
prĳave da se neke poruke nisu stigle ili da su stigle dva
puta). Da bi se to ostvarilo, aplikacĳa treba da omogući
praćenje aktivnosti korisnika i sistema (logovi grešaka,
statistika korišćenja, praćenje mrežnih veza).

Usled potrebe za čestim promenama u skladu sa že-
ljama korisnika, aplikacĳa treba da je lako izmenljiva
i testabilna. Posebno važna vrsta izmene je nadograd-
nja. Aplikacĳa treba da bude dizajnirana tako da
omogući da se lako i brzo mogu dodati nove funkci-
onalnosti, bez uticaja na postojeće. Na primer, doda-
vanje video poziva mora biti odvojeno od sistema za
razmenu poruka, ali se mora integrisati u postojeći
korisnički interfejs. Testabilnost u kontekstu čestih
promena i nadogradnja ključna je za osiguravanje
da promene i novouvedene funkcionalnosti ne na-
rušavaju postojeće funkcionalnosti. Za testabilnost je
posebno značajna automatizacĳa procesa testiranja, na
primer kroz pisanje jediničnih testova i upotrebu alata
za pokretanje i automatsku proveru rezultata rada
testova. Testiranjem je potrebno pokriti različite scena-
rĳe (na primer, sve vrste poruka: tekstualne, glasovne
i multimedĳalne) uključujući i scenarĳe koji obuhva-
taju pogrešno korišćenje aplikacĳe ili nestandardne
slučajeve upotrebe (na primer, korišćenje aplikacĳe u
slučaju problema sa mrežom).

Atributi kvaliteta softvera nisu nezavisni, već su me-
đusobno povezani i isprepleteni. Na primer (slika 1.3),
modularnost, koja se obično postavlja kao jedan od
glavnih ciljeva faze projektovanja softvera, direktno uti-
če na sva ostala četiri atributa održivosti, jer je dobra
modularnost preduslov za iskoristivost, analizabilnost,
izmenljivost i testabilnost. Slično tome, analizabilnost
utiče na iskoristivost i modifikacĳu, dok testabilnost
indirektno utiče na iskoristivost i izmenljivost.

<!-- pdf_page=34 printed_page=20 -->

modularnost

testabilnost

iskoristivost

izmenljivost

Slika 1.3: Veze između atri-
buta koji utiču na održavanje
softvera: strelice sa punim li-
nĳama predstavljaju jak uticaj
jednog atributa na drugi, dok
isprekidane strelice odgovara-
ju indirektnom uticaju.

analizabilnost

1.3.9 Prenosivost

prenosivost

Prenosivost (eng. portability) odgovara stepenu u ko-
me se softver može koristiti u različitim okruženjima.
Prenosivost obuhvata naredne podatribute:

prilagodljivost — mogućnost korišćenja sa različitim
hardverom, softverom ili okruženjem,

instalabilnost — mogućnost instaliranja/deinstaliranja
softvera u različitim okruženjima i

prilagodljivost

zamenljivost — mogućnost zamene drugim softver-
skim proizvodom za iste svrhe.

instalabilnost

zamenljivost

Primer 1.3.9 (Kupovina karata — nastavak primera
1.3.2) Aplikacĳa za kupovinu avio karata treba da
bude prilagodljiva različitim uređajima (mobilnim
uređajima, tabletima, desktop računarima) i tržištima.
Na primer, aplikacĳa treba da može da se prilago-
di različitim veličinama ekrana, od malih ekrana na
mobilnim telefonima do velikih ekrana na desktop
računarima, pri čemu je potrebno da se automatski
prilagođava vizuelni prikaz u skladu sa veličinom
ekrana. Takođe, aplikacĳa treba da ponudi lokalizo-
vane opcĳe za različite jezike i valute.

<!-- pdf_page=35 printed_page=1 -->

Aplikacĳa treba da bude jednostavna za instalacĳu na
različitim uređajima. Na mobilnim uređajima, korisni-
ci treba da mogu da preuzmu aplikacĳu sa App Store-a
ili Google Play-a uz nekoliko klikova ili komandi. Za
desktop verzĳu, aplikacĳa treba da bude dostupna za
platforme Windows, Linux i macOS u vidu jednostav-
nih instalacĳa koje se pokreću sa par klikova. Za veb
verzĳe, aplikacĳa mora da omogući jednostavno kori-
šćenje u pretraživaču bez potrebe za preuzimanjem
ili instalacĳom.

Prilikom ažuriranja aplikacĳe, potrebno je omogući-
ti laku zamenljivost starĳe verzĳe novom verzĳom.
Zamenljivost znači da aplikacĳa omogućava da no-
va verzĳa može zameniti staru verzĳu bez gubitka
podataka, kao što su starĳa putovanja, preferencĳe
korisnika ili istorĳa pretrage. Takođe, zamenljivost
podrazumeva lako uklanjanje prethodne verzĳe apli-
kacĳe prilikom instalacĳe nove. U slučaju da korisnik
želi da pređe na konkurentsku aplikacĳu, zamenlji-
vost podrazumeva da će podaci kao što su rezervacĳe
ili istorĳa pretrage biti prenosivi ili lako eksportovani
u druge formate.

Rezime

▶Cilj upravljanja kvalitetom je da se ispune zahtevi
korisnika, optimizuju poslovni procesi i smanji
broj grešaka ili defekata.

▶Osnovni procesi koji su vezani za kvalitet softvera
uključuju planiranje, obezbeđivanje, kontrolu i
poboljšanje kvaliteta softvera.

▶Serĳa standarda ISO/IEC 25000 sadrži okvir za
procenu kvaliteta softvera.

▶U zavisnosti od svrhe i ciljeva softvera, svaki atri-
but kvaliteta softvera može imati različit nivo
važnosti.

▶Osnovni atributi kvaliteta softvera su funkcional-
na podobnost, performantnost, kompatibilnost,

<!-- pdf_page=36 printed_page=22 -->

pouzdanost, upotrebljivost, bezbednost, sigurnost,
održivost i prenosivost.

Literatura

[1]
ISO/IEC. Systems and Software Engineering: Sys-
tems and Software Quality Requirements and Eva-
luation (SQuaRE) – System and Software Quality
Models. ISO/IEC 25010. International Organizati-
on for Standardization, 2023.

[2]
Stephen H. Kan. Metrics and Models in Software
Quality Engineering. 2. izdanje. Addison-Wesley,
2002. isbn: 9780201729153.

[3]
Barbara Kitchenham i Shari Lawrence Pfleeger.
Software Quality: The Elusive Target. U: IEEE Sof-
tware (1996.). doi: 10.1109/52.476281.

[4]
Roger S. Pressman i Bruce R. Maxim. Software
Engineering: A Practitioner’s Approach. 8. izdanje.
McGraw-Hill, 2014. isbn: 9780078022128.

[5]
Ian Sommerville. Software Engineering. 10. izdanje.
Pearson, 2015. isbn: 9780133943030.

Ispitna pitanja

1. Značaj kvaliteta softvera. Procesi i standardi.

2. Značaj kvaliteta softvera. Atributi kvaliteta sof-
tvera: funkcionalna podobnost, performantnost,
kompatibilnost, pouzdanost. Primeri.

3. Značaj kvaliteta softvera. Atributi kvaliteta softve-
ra: održivost. Primeri.

4. Značaj kvaliteta softvera. Atributi kvaliteta softve-
ra: upotrebljivost, sigurnost, bezbednost, prenosi-
vost. Primeri.

<!-- pdf_page=37 printed_page=37 -->

2.1
Primeri poznatih
grešaka . . . . . . 24

Pregled

▶Na koji sve način neispravan softver utiče na svet
oko nas?

2.2
Troškovi usled
grešaka u softve-
ru . . . . . . . . . . 32

▶Koliko koštaju softverske greške?

Greške u softveru mogu na različite načine uticati na
korisničko iskustvo. Najblaži oblik posledica jeste ma-
nja neprĳatnost, kao što je iznenadno gašenje internet
pregledača (slika 2.1), muzičkog plejera ili mobilne igre,
ili greška u sistemu za izgradnju softvera (slika 2.2).
Ipak, te neprĳatnosti mogu biti i ozbiljnĳe — na primer,
ako navigacioni softver pogrešno usmeri korisnika ka
nebezbednoj lokacĳi ili ako, u hitnoj situacĳi, softverski
problem onemogući uspostavljanje poziva.

Drugi nivo uticaja softverskih grešaka ogleda se u
materĳalnim gubicima, koji mogu imati ozbiljne posle-
dice po pojedince ili finansĳsko poslovanje organizacĳa.
Ove greške se najčešće javljaju u poslovnom softveru i
bankarskim informacionim sistema, gde mogu izazvati
direktne novčane gubitke, kao i gubitak ili kompro-
mitovanje važnih podataka. U određenim slučajevima,
posledice se mogu reflektovati i na reputacĳu kompanĳe,
izazivajući dugoročne finansĳske probleme.

Slika 2.1: Greška u radu Inter-
net pregledača

Na kraju, greške u softveru mogu imati ifatalneposledice.
One se javljaju u kritičnim sistemima, kao što su sof-
tver za upravljanje avionima, automobilima i vozovima,
gde čak i najmanji propust može dovesti do teških sao-
braćajnih nesreća. Sličan rizik postoji i u medicinskim
uređajima koji se koriste za dĳagnostiku, praćenje vital-
nih funkcĳa i pružanje terapĳe, gde softverska greška
može direktno ugroziti život pacĳenta. Greške u sof-
tveru svemirskih letelica mogu dovesti do neuspeha

Slika 2.2: Greška u sistemu za
izgradnju softvera

<!-- pdf_page=38 printed_page=24 -->

misĳa vrednih više stotina miliona dolara, dok softver-
ski problemi u nuklearnim elektranama nose potencĳal
za katastrofe nesagledivih razmera. Zbog svega ovoga,
razvoj softvera u ovim oblastima zahteva najviši stepen
pažnje, rigorozno testiranje i stalnu proveru kvaliteta.

### 2.1 Primeri poznatih grešaka

Greška
proizvodi
−→

Greške koje naprave programeri, ukoliko se ne otkrĳu u
procesu ispitivanja ispravnosti softvera, čine da softver
nĳe u potpunosti ispravan, odnosno da sadrži defekte. Ti
defekti u određenim situacĳama uzrokuju pad sistema,
odnosno softver se ponaša drugačĳe od očekivanog.
Pad pravi incident koji može da ima posledice.

Defekt
uzrokuje
−→

Pad
pravi
−→

Incident
ima
−→𝑝𝑜𝑠𝑙𝑒𝑑𝑖𝑐𝑒

2.1.1 Neprĳatnosti i materĳalni gubici

Neke od najpoznatĳih softverskih grešaka, osim što
su izazvale ozbiljne neprĳatnosti korisnicima, ostavile
su i duboke finansĳske posledice po kompanĳe koje
su ih razvile. Njihov uticaj nĳe bio ograničen samo na
korisničko iskustvo, već je često vodio ka gubicima po-
verenja, padu akcĳa i tržišne vrednosti, kao i značajnim
materĳalnim štetama.

Aplikacĳa Apple Maps, 2012

Kompanĳa Apple je 2012. godine odlučila da ukloni
aplikacĳu za mape Google Maps na svom operativnom si-
stemu iOS i zameni je svojom aplikacĳom — Apple Maps.
Nova aplikacĳa je predstavljena uz operativni sistem
iOS 6, a trebalo je da bude modernĳa, sa 3D prikazima,
navigacĳom koja prati tekuće stanje u saobraćaju i gla-
sovnim navođenjem. Međutim, aplikacĳa Apple Maps
je odmah po lansiranju doživela veliku kritiku zbog
brojnih grešaka, uključujući:

<!-- pdf_page=39 printed_page=2 -->

Pogrešne lokacĳe — Gradovi, znamenitosti i firme su
bili loše označeni ili potpuno pogrešno locirani.

Na primer, policĳa u Austra-
lĳi je upozorila građane da
ne koriste Apple Maps jer je
vodič za grad Mildura ljude
odvodio usred opasne pusti-
nje.

Netačne rute — Navigacĳa je korisnike vodila pogre-
šnim ili nepostojećim putevima.

Izobličene mape — 3D prikazi zgrada i terena su iz-
gledali iskrivljeno ili neprirodno. Primer lošeg
prikaza dat je na slici 2.3.

Nedostajuće informacĳe — Mnoge lokacĳe i ulice nisu
bile uopšte ucrtane.

Izvršni direktor kompanĳe Apple, Tim Kuk (eng. Tim
Cook), uputio je javno izvinjenje i korisnicima čak pre-
poručio da privremeno koriste konkurentske aplikacĳe.
Zbog skandala, Apple je otpustio nekoliko ključnih ljudi
koji su bili na visokim pozicĳama. Negativna percepcĳa
kompanĳe dovela je do pada vrednosti akcĳa Apple-a za
približno 4,5%, što je bilo smanjenje tržišne vrednosti
za oko 30 milĳardi dolara. Kako bi ispravio početne de-
fekte i poboljšao kvalitet svoje aplikacĳe, Apple je tokom
narednih godina uložio više milĳardi dolara u razvoj
Apple Maps. Ova ulaganja obuhvatala su akvizicĳe kom-
panĳa specĳalizovanih za pravljenje mapa, prikupljanje
sopstvenih podataka, kao i razvoj novih funkcionalnosti.
Iako je teško precizno kvantifikovati ukupne finansĳske
gubitke, kombinacĳa pada tržišne vrednosti i višego-
dišnjih ulaganja u unapređenje Apple Maps sugeriše
da je ova greška imala značajan ekonomski uticaj na
kompanĳu.

Slika 2.3: Primer prikaza apli-
kacĳe Apple Maps

Knight Capital Group, 1. avgust 2012. godine

U avgustu 2012. godine, kompanĳa Knight Capital Gro-
up suočila se sa jednim od najozbiljnĳih tehnoloških
incidenata u istorĳi savremenog finansĳskog tržišta.
Softverska greška u sistemu za trgovanje rezultirala je
gubitkom od 440 miliona dolara za svega 45 minuta
— što predstavlja iznos gotovo četiri puta veći od neto
profita kompanĳe ostvarenog tokom prethodne godine.

<!-- pdf_page=40 printed_page=26 -->

Dodatno, vrednost akcĳa kompanĳe je u roku od dva
dana opala za čak 75%.

Knight Capital Group

Do incidenta je došlo prilikom implementacĳe novog
softverskog modula, kada je nenamerno reaktiviran
stari, nefunkcionalni deo koda. Aktivirani kôd je auto-
matski generisao veliki broj netačnih naloga, izazivajući
kupovinu i prodaju akcĳa po izrazito nepovoljnim ce-
nama. Ovaj događaj ne samo da je značajno ugrozio
reputacĳu kompanĳe, već je ubrzo doveo i do njenog
potpunog finansĳskog kolapsa.

▶Greška:
(1) Programer nĳe
ažurirao sve servere
sa najnovĳom
verzĳom softvera
(2) Nepostojanje
provere verzĳe koda
prilikom obrade upita

▶Defekt: Moguće je
pokrenuti kôd koji se
koristio za testiranje

▶Pad: Pokrenute su
pogrešne transakcĳe

Facebook Outage, 13. mart 2019. godine

▶Incident: Veliki
finansĳski gubitak

U martu 2019. godine, kompanĳa Facebook doživela je
jedan od najznačajnĳih prekida u svojoj istorĳi koji je
uticao na milĳarde korisnika širom sveta. Ovaj događaj,
poznat kao Facebook Outage 2019, izazvao je ozbiljne
poremećaje u funkcionisanju ne samo servisa Facebook,
već i njegovih povezanih servisa kao što su Instagram,
WhatsApp i Messenger.

Prema zvaničnom saopštenju kompanĳe, uzrok prekida
bila je „promena konfiguracĳe servera” koja je pokre-
nula lanac problema u sistemu. Nakon što su servisi
ponovo postali dostupni, Facebook se izvinio korisnici-
ma i naveo da su sistemi u fazi oporavka. Međutim,
kompanĳa nĳe pružila detaljnĳe informacĳe o tačnom
uzroku problema, što je izazvalo kritike stručne javnosti
i korisnika zbog nedostatka transparentnosti. Iako su
detalji ostali oskudni, izveštaji sugerišu da je došlo do
greške u internim sistemima za rutiranje podataka, što je
dovelo do prekida komunikacĳe između Facebook-ovih
centara podataka. Zbog toga su korisnici širom sveta
imali ograničen ili nikakav pristup platformama.

Zvanično saopštenje kompa-
nĳe Facebook:
”Juče smo izvršili promenu
konfiguracĳe servera koja
je pokrenula niz problema.
Kao rezultat toga, mnogi ko-
risnici su imali poteškoća u
pristupu našim aplikacĳama
i uslugama.”

Ovaj prekid je bio jedan od najopsežnĳih u istorĳi dru-
štvenih mreža. Pored korisničkih neugodnosti (slika
2.4), prekid je imao i finansĳske posledice. Analitičari

Slika 2.4: Poruka o nedostup-
nosti servisa

<!-- pdf_page=41 printed_page=2 -->

su procenili da je Facebook, sa prosečnim dnevnim pri-
hodima od oko 189 miliona dolara, pretrpeo značajan
gubitak prihoda tokom ovog perioda. Neki izvori na-
vode da je prekid trajao 14 sati, dok drugi navode da je
prekid trajao oko 24 sata. U skladu sa time se i razlikuju
procene finansĳskog gubitka. Takođe, ovaj incident je
uticao i na pad akcĳa kompanĳe Facebook za oko 2%.

Google Cloud Outage, 14. decembar 2020. godine

Kompanĳa Google je imala neželjeni prekid usluga 14.
decembra 2020. godine u trajanju od 47 minuta. Tokom
ovog perioda, korisnici širom sveta nisu mogli da pri-
stupe uslugama koje zahtevaju Google nalog, uključujući
Gmail, YouTube, Google Drive, Google Docs i druge. Ovaj
događaj je imao globalni uticaj na korisnike i kompanĳe
koje se oslanjaju na Google-ovu infrastrukturu.

Prema zvaničnom izveštaju kompanĳe Google (slika 2.5),
uzrok prekida bio je problem u sistemu za upravljanje
kvotama skladišnog prostora, koji je nenamerno smanjio
kapacitet centralnog sistema za upravljanje identitetima
korisnika. Ova greška je dovela do toga da se zahtevi
za autentifikacĳu nisu mogli obraditi, što je rezultiralo
greškama prilikom pokušaja pristupa uslugama koje
zahtevaju prĳavu.

Iako je prekid trajao manje od sat vremena, njegov
uticaj je bio značajan zbog široke upotrebe Google-ovih
servisa u svakodnevnom poslovanju i komunikacĳi.
Google se izvinio korisnicima i naveo da su preduzete
mere kako bi se sprečilo ponavljanje sličnih incidenata
u budućnosti.

Teško je precizno kvantifikovati direktan finansĳski
gubitak izazvan ovim konkretnim prekidom. Poznato
je da je Google Cloud u 2020. godini zabeležio operativni
gubitak od 5,61 milĳardu dolara. Ovaj gubitak pripisuje
se raznim poslovnim odlukama i nĳe vezan samo za
pomenuti incident.

Slika 2.5: Deo zvaničnog izve-
štaja kompanĳe Google https:
//status.cloud.google.
com/incident/zall/20013

<!-- pdf_page=42 printed_page=28 -->

2.1.2 Fatalne posledice

Većina softverskih grešaka ne rezultira fatalnim posle-
dicama. Ipak, kada se propusti jave u okviru kritičnih
sistema, njihovi efekti mogu biti izuzetno ozbiljni —
uključujući gubitke ljudskih života, teške povrede, zna-
čajne finansĳske štete i razorne sistemske havarĳe. Iako
su ovakvi incidenti retki u apsolutnim brojkama, njihov
uticaj na bezbednost, ekonomĳu i poverenje u tehnolo-
gĳu je nesrazmerno velik.

Uprkos kontinuiranom unapređenju programerskih
praksi, uključujući primenu formalnih metoda, auto-
matizovanog testiranja i usklađivanje sa bezbednosnim
standardima, učestalost najtežih grešaka nĳe opala u
meri u kojoj bi se očekivalo. Promenila se, međutim,
njihova priroda: umesto pojedinačnih grešaka u ko-
du, sve češće se javljaju kompleksni, sistemski defekti
koji proizilaze iz loše integracĳe, nejasnih zahteva ili
neočekivane interakcĳe među podsistemima.

Therac 25, 1985–1987

Aparat za radioterapĳu Therac-25 je bio proizvod kanad-
ske kompanĳe AECL (Atomic Energy of Canada Limited).
Ovaj aparat je bio napredni naslednik serĳe uređaja
Therac-6 i Therac-20, koji su takođe koristili sličnu tehno-
logĳu za primenu radioterapĳe. Therac-25 je kombinovao
softversku kontrolu i hardverske komponente u cilju
povećanja preciznosti zračenja.

Između 1985. i 1987. godine, aparat je uzrokovao najma-
nje šest slučajeva predoziranja pacĳenata radĳacĳom,
od kojih su troje umrli. Ovi nesrećni slučajevi bili su
rezultat softverske greške. Therac-25 je imao dva režima
zračenja:

▶Elektronski snop niskog intenziteta,
▶Fotonski snop visoke energĳe, koji mora da se
dodatno filtrira.

<!-- pdf_page=43 printed_page=2 -->

Ako bi tehničar najpre uneo prvi režim, a zatim ga
promenio u drugi, softver nĳe uvek uspevao da ispravno
ažurira stanje uređaja. Rezultat toga je bio da uređaj
misli da koristi snop niskog intenziteta i doze koje su za
to predviđene, ali bi zapravo poslao visokoenergetski
snop bez zaštitnog filtera. Greška je nastajala usled loše
sinhronizacĳe:

Therac 25
Greška:
(1) Programer je napravio
grešku u promeni podataka
bez adekvatne sinhronizaci-
je,
(2) Tehničar je promenio
režim rada u pogrešnom tre-
nutku
Defekt: Mogućnost slanja
visokoenergetskog snopa
bez zaštitnog filtera
Pad: Prekoračena je bezbed-
na doza zračenja
Incident: Pacĳent je umro

▶Jedan proces je ažurirao režim tretmana.
▶Drugi proces je proveravao spremnost uređaja za
zračenje.

Ako bi se ti procesi „preklopili“ u pogrešnom trenutku,
uređaj bi pogrešno zaključio da je sve spremno i poslao
snop visoke energĳe bez zaštitnog filtera sa dozom
zračenja koja je predviđena za snop niskog intenziteta.

Pored ove softverske greške, nesrećama su doprineli i
naredni propusti:

▶nedostatak hardverskih sigurnosnih sistema —
Therac-25 je uklonio fizičke sigurnosne blokade
koje su postojale u prethodnim uređajima, osla-
njajući se isključivo na softver,

▶loša dĳagnostika — interfejs aparata nĳe jasno
ukazivao na probleme, tehničari su dobĳali neja-
sne poruke o grešci i

▶zanemarivanje prethodnih incidenata — kompa-
nĳa AECL nĳe preduzela adekvatne mere nakon
inicĳalnih pritužbi i događaja.

Kao rezultat ovih nesrećnih događaja, razvĳeni su novi
standardi za sigurnost medicinskih uređaja, uključujući
rigoroznĳe zahteve za testiranje i formalnu verifikacĳu
softvera u medicinskim sistemima.

Dahran raketa, 25. februar 1991. godine

Tokom Zalivskog rata, 25. februara 1991. godine, iračka
balistička raketa pogodila je američku vojnu bazu u Da-
hranu (Saudĳska Arabĳa), usmrtivši 28 vojnika i ranivši

<!-- pdf_page=44 printed_page=30 -->

više od 100 vojnika. Nakon detaljne istrage, utvrđeno je
da je uzrok neuspeha protivraketnog sistema Patriot bila
greška u softveru koji je upravljao internim sistemskim
vremenom. Naime, zbog akumulacĳe zaokruživanja
decimalnih vrednosti u brojevima s pokretnim zarezom,
došlo je do odstupanja od približno jedne trećine se-
kunde nakon 100 sati neprekidnog rada sistema. Iako
se ovo odstupanje može činiti beznačajnim, u kontek-
stu ogromnih brzina kojima se balističke rakete kreću,
ono je rezultovalo prostornim promašajem od oko 600
metara. Radar je usled toga tražio raketu na pogrešnoj
lokacĳi, nĳe uspeo da je prati, i samim tim nĳe aktivirao
mehanizam za presretanje.

Dahran raketa
Greška: Neprecizno zaokru-
živanje vrednosti brojeva
Defekt: Pogrešno računanje
vremena
Pad: Neaktiviran mehani-
zam za presretanje rakete
Incident: Smrt 28 vojnika i
povrede više od 100 vojnika

Ovaj događaj predstavlja jedan od najupečatljivĳih pri-
mera fatalnih posledica softverske greške u savremenoj
vojnoj istorĳi. Osim ljudskih žrtava, incident je izazvao
ozbiljnu zabrinutost u vezi sa pouzdanošću softverski
vođenih odbrambenih sistema. Pentagon i američka voj-
ska bili su izloženi javnoj i političkoj kritici, a celokupan
događaj podstakao je temeljnu revizĳu načina na koji se
razvĳa, testira i primenjuje softver u vojnim i drugim
bezbednosno osetljivim sistemima.

Slika 2.6: Maketa rakete Aria-
ne 5, Muzej vazduhoplovstva
u Parizu, Francuska

Ariane 5, 4. jun 1996. godine

Raketa Ariane 5 Evropske svemirske agencĳe (ESA)
uništila se svega 37 sekundi nakon poletanja, 4. juna 1996.
godine. Pri tome su izgubljena četiri satelita namenjena
proučavanju Zemljine magnetosfere. Procenjena šteta
iznosila je preko 370 miliona dolara, čime je ovaj incident
postao jedan od najskupljih softverskih grešaka u istorĳi
svemirskih misĳa.

Ariane 5
Greška:
(1) Konverzĳa iz 64-bitne u
16-bitnu vrednost
(2) Nepostojanje adekvatne
obrade izuzetka Defekt: Si-
stem neadekvatno reaguje
na greške u ulaznim podaci-
ma
Pad: Skretanje sa putanje i
aktivacĳa sistema za samou-
ništenje
Incident: Veliki finansĳski
gubitak i propuštena prilika
za novim naučnim saznanji-
ma

Uzrok nesreće bio je softverski propust. Sistem je poku-
šao da konvertuje 64-bitnu vrednost brzine u 16-bitnu
vrednost, što je izazvalo numeričko prekoračenje i iz-
uzetak koji nĳe bio adekvatno obrađen. To je dovelo
do pogrešnih komandi, skretanja sa putanje i aktivacĳe
sistema za samouništenje.

<!-- pdf_page=45 printed_page=2 -->

Ova katastrofa je istakla kritičnu važnost verifikacĳe
softverskih komponenti u kompleksnim i bezbednosno
osetljivim sistemima, te je podstakla reforme u ESA-inim
procedurama testiranja i verifikacĳe softvera.

The Mars Climate Orbiter 23. septembar 1999. godine

Letelica Mars Climate Orbiter (NASA) nestala je prilikom
ulaska u orbitu Marsa 23. septembra 1999. godine, nakon
što je ušla u orbitu značajno niže od planirane putanje i
najverovatnĳe izgorela u atmosferi. Istragom je utvrđeno
da je uzrok nesreće bio propust u konverzĳi jedinica: deo
softvera je koristio imperĳalne jedinice dok je drugi deo
softvera očekivao metričke jedinice. Ova neusaglašenost
dovela je do pogrešnog proračuna putanje.

Sama letelica je koštala 125 miliona dolara, dok je ukup-
ni trošak misĳe procenjen na oko 327 miliona dolara.
Incident je izazvao ozbiljnu kritiku NASA-inih progra-
merskih i upravljačkih procedura. Kao rezultat, uvedene
su strože kontrole, standardizacĳa jedinica i unapređeni
protokoli testiranja softverskih komponenti.

Slika 2.7: Fotografija leteli-
ce Mars Climate Orbiter prili-
kom sklapanja, NASA, januar
1998. godine

Mars Climate Orbiter
Greška: Deo softvera je kori-
stio imperĳalne jedinice, dok
je drugi deo softvera očeki-
vao metričke jedinice
Defekt: Pogrešno računanje
putanje
Pad: Ulazak u orbitu Marsa
na pogrešnom rastojanju
Incident: Letelica je izgorela
u atmosferi Marsa

Greške u automobilskoj industrĳi

Softverske greške u automobilskoj industrĳi su ozbiljan
problem koji može imati direktne posledice po bezbed-
nost putnika. Na primer, kompanĳa General Motors je
softversku grešku otkrila tek nakon saobraćajnih ne-
sreća u kojima je bio jedan smrtni ishod i tri povrede.
Ova greška je sprečavala aktivacĳu prednjih vazdušnih
jastuka i zatezača sigurnosnih pojaseva tokom sudara,
povećavajući rizik od povreda putnika. Kompanĳa je
u septembru 2016. godine, najavila opoziv 4,3 miliona
vozila.

General Motors je naveo da ovaj opoziv neće imati znača-
jan uticaj na finansĳske rezultate kompanĳe i precizna

<!-- pdf_page=46 printed_page=32 -->

procena troškova nĳe javno objavljena. Međutim, u slu-
čaju koji je uključivao opoziv sličnog broja vozila (opoziv
zbog problema sa Takata vazdušnim jastucima) troškovi
su bili procenjeni na 550 miliona dolara. S obzirom na
to, može se pretpostaviti da su troškovi ovog opoziva
bili značajni, ali verovatno niži od pomenute sume, jer
je rešenje problema uključivalo ažuriranje softvera, što
je manje skupo od fizičke zamene delova.

Sličan problem je imala i kompanĳa Fiat Chrysler koja je
u maju 2017. odlučila da opozove više od 1,25 miliona
kamioneta širom sveta, s ciljem otklanjanja softverske
greške koja je potencĳalno povezana sa saobraćajnim
nesrećama sa jednim smrtnim ishodom i dve povrede.
Iako nisu postojali konačni dokazi da je softverski pro-
pust direktno uzrokovao ove nesreće, proizvođač vozila
je odlučio da opoziv sprovodi preventivno, kao meru
predostrožnosti.

Kako je navedeno u zvaničnom saopštenju, softver-
ska anomalĳa je privremeno onemogućavala aktivacĳu
bočnih vazdušnih jastuka, kao i mehanizama koji auto-
matski zatežu pojas. Do takvog neispravnog ponašanja
sistema je moglo da dođe u slučaju prevrtanja vozila
izazvanog snažnim udarcem u donji deo automobila,
na primer pri udaru u prepreke na putu ili prilikom
vožnje van uređenih saobraćajnica. Verovatnoća nastan-
ka takvog incidenta ocenjena je kao izuzetno mala, jer
je za njegovu pojavu potrebna vrlo specifična i retka
sekvenca događaja. U cilju otklanjanja uočene greške,
bilo je neophodno izvršiti reprogramiranje računarskih
modula u svim vozilima koja su obuhvaćena opozivom.
Tačni troškovi ovog opoziva nisu objavljeni.

### 2.2 Troškovi usled grešaka u softveru

Najveći troškovi usled grešaka u softveru nastaju kada
se greške otkrĳu nakon puštanja sistema u rad. To uklju-
čuje gubitke u prihodu, narušavanje reputacĳe, opozive

<!-- pdf_page=47 printed_page=2 -->

proizvoda, regulatorne kazne, kao i gubitke podataka
ili života.

Američki nacionalni institut za standarde i tehnologĳu
(eng. US National Institute of Standards and Technology,
skraćeno NIST) je 2002. godine napravio opsežnu studĳu
sa ciljem procene uticaja softverskih grešaka na ame-
ričku ekonomĳu. Po ovoj studĳi, neispravan softver je
koštao američku ekonomĳu 59.5 milĳardi dolara godi-
šnje. Dodatno, u studĳi je naglašeno da bi rano otkrivanje
grešaka moglo da uštedi 22 milĳarde dolara godišnje,
dakle nešto više od trećine ukupnih troškova.

Ova studĳa značajno je uticala na ulaganje u unapre-
đivanje procesa razvoja softvera sa ciljem poboljšanja
kvaliteta softvera i smanjenja količine grešaka u softveru.
Dodatno, posebna ulaganja su bila usmerena ka razvoju
alata koji daju podršku i omogućavaju automatizacĳu
procesa verifikacĳe softvera.

Dvadeset godina kasnĳe‗, Konzorcĳum za kvalitet in-
formacĳa i softvera (eng. Consortium for Information and
Software Quality), skraćeno CISQ) u izveštaju o ceni lo-
šeg kvaliteta softvera (eng. Cost of Poor Software Quality)
u Sjedinjenim Američkim Državama za 2022. godinu
navodi da su troškovi usled lošeg kvaliteta softvera
porasli na 2410 milĳardi američkih dolara. U izveštaju
za 2020. godinu, navedena je procena troškova 2080
milĳardi američkih dolara. Dakle, za kratko vreme uo-
čen je veliki porast troškova uzrokovanih softverskim
greškama.

CISQ u izveštaju za 2020. godinu navodi da su najbitnĳi
troškovi† proistekli iz softverskih grešaka:

Operativni softverski kvarovi: Procena je da su ope-
rativni softverski kvarovi (eng. operational software

‗ Iako najavljen, izveštaj za 2024. godinu još uvek nĳe dostupan.
Poslednji javno dostupan izveštaj je iz 2022. godine.

† Ovi troškovi nisu međusobno nezavisni, tj. ima preklapanja, pa
zbog toga njihov zbir nĳe 2080 već veći. Na primer, problemi
sa zastarelim sistemima i operativni softverski kvarovi su usko
povezani sa tehničkim dugom.

<!-- pdf_page=48 printed_page=34 -->

failures), uključujući greške u funkcionisanju si-
stema i nepredviđene zastoje, doveli do gubitaka
od oko 1560 milĳardi dolara. Ovaj broj predstavlja
povećanje od 22% u odnosu na 2018. godinu.

Neuspešni razvojni projekti: Neuspešni ili otkazani
softverski projekti, često zbog lošeg upravljanja
ili nedostatka kvaliteta, doveli su do gubitaka od
260 milĳardi dolara.

Problemi sa zastarelim sistemima: Održavanje i nado-
gradnja zastarelih sistema koštali su oko 520 mili-
jardi dolara.

Tehnički dug: Troškovi tehničkog duga‡ (eng. technical
debt), koji predstavlja nepopravljene greške i nee-
fikasnosti u kodu, procenjeni su na 1310 milĳardi
dolara.

Gubici zbog sajberkriminala: U izveštaju nĳe navede-
na tačna procena troškova usled sajberkriminala,
osim da su ovi troškovi značajni i u porastu.

CISQ u izveštaju za 2022. godinu navodi da su najviše
porasli gubici

▶prouzrokovani sajber kriminalom koji su rezultat
postojećih softverskih ranjivosti. Oni su između
2020. i 2021. godine porasli za 64%, a rastući
trend se nastavio i u 2022. godini. Prosečan trošak
jednog incidenta narušavanja podataka u SAD-u
dostigao je 9,44 miliona dolara.

▶nastali usled problema u komponentama softvera
otvorenog koda. Broj neuspeha zbog slabosti u
komponentama otvorenog koda povećao se za

‡ Tehnički dug se odnosi na posledice pravljenja brzih, kratkoročnih
rešenja u razvoju softvera, umesto boljih, dugoročno održivih
rešenja. To je cena koju tim mora da plati u budućnosti zbog
kompromisa u kvalitetu koda napravljenih da bi se nešto brže
isporučilo danas. Tehnički dug nastaje usled nejasnih i nepreciznih
zahteva, zaobilaženja dobrih programerskih praksi da bi se „stigao
rok“, odsustva testova i dokumentacĳe, održavanja starog koda bez
značajnih refaktorisanja i nedostatka automatizacĳe i sigurnosnih
provera. Posledice tehničkog duga su teži i sporĳi razvoj novih
funkcionalnosti, više grešaka i kvarova, kao i povećani troškovi
održavanja.

<!-- pdf_page=49 printed_page=2 -->

alarmantnih 650% između 2020. i 2021. godine.

▶koji su rezultat uticaja tehničkog duga. Ovaj trošak
je porastao na približno 1520 milĳardi dolara godi-
šnje, što ukazuje na ozbiljnost problema i potrebu
za njegovim rešavanjem.

Svi ovi izveštaji su vrlo konzervativni jer uzimaju u
obzir samo dostupne i javno prĳavljene podatke. U ve-
ćini slučajeva, oni se oslanjaju na analize izveštaja o
incidentima, javno objavljenim gubicima, regulatornim
dokumentima i istraživanjima sprovedenim među or-
ganizacĳama. Međutim, stvarna slika je često znatno
ozbiljnĳa.

Kompanĳe, iz različitih razloga, često smanjuju i ublaža-
vaju izveštaje o problemima koji su nastali usled grešaka
u softveru. To rade kako bi zaštitile svoj ugled, izbegle
pad poverenja korisnika i investitora, ili kako bi izbegle
regulatorne i pravne posledice. Greške u softveru koje
dovedu do curenja podataka, pada sistema, zastoja u
radu ili finansĳskih gubitaka neretko se interno rešavaju
i nikada ne dospeju u javnost.

Pored toga, mnoge organizacĳe nemaju razvĳen sistem
za praćenje i precizno merenje posledica softverskih
grešaka, pa čak i kada žele da prĳave problem – nemaju
celovite podatke. Zbog toga je procena ukupnih troško-
va lošeg kvaliteta softvera u izveštajima poput onih koje
objavljuje CISQ gotovo sigurno donji prag stvarne štete.
Pritom, stvarna cena lošeg softvera uključuje i skrivene
gubitke kao što su izgubljene prilike, pad produktiv-
nosti i frustracĳe korisnika. Sve to ostaje van zvanične
statistike, ali ima dugoročne posledice po poslovanje i
razvoj digitalnog tržišta.

Rezime

▶Uticaj neispravnog softvera: neprĳatnosti, materi-
jalni gubici i materĳalno nemerljive posledice.

<!-- pdf_page=50 printed_page=36 -->

▶Postoji veliki broj primera softverskih grešaka
koje su imale značajne materĳalne i nematerĳalne
posledice.

▶Materĳalni troškovi neispravnog softvera se mere
hiljadama milĳardi dolara na godišnjem nivou.

▶Troškovi neispravnog softvera u velikoj meri su
posledica tehničkog duga, odnosno pravljenja sof-
tvera bez adekvatnog kvaliteta.

Literatura

[1]
Victor R. Basili i Barry T. Perricone. Software Errors
and Complexity: An Empirical Investigation. U:
Communications of the ACM 27.1 (1984.), str. 42–
52. doi: 10.1145/69605.2085.

[2]
Albert Endres. An analysis of errors and their
causes in system programs. U: Proceedings of the
International Conference on Reliable Software. Los
Angeles, California: ACM, 1975., str. 327–336. doi:

10.1145/800027.808455.

[3]
Thomas J. Ostrand, Elaine J. Weyuker i Robert M.
Bell. Predicting the Location and Number of Faults
in Large Software Systems. U: IEEE Transactions
on Software Engineering 31.4 (2005.), str. 340–355.
doi: 10.1109/TSE.2005.49.

[4]
James Reason. Human Error. Cambridge Universi-
ty Press, 1990. isbn: 9780521314190.

Ispitna pitanja

5. Uticaj neispravnog softvera. Primeri neprĳatnosti
i materĳalnih gubitaka.

6. Uticaj neispravnog softvera. Primeri fatalnih po-
sledica.

7. Troškovi usled grešaka u softveru.

<!-- pdf_page=51 printed_page=51 -->

Pregled

3.1 Odnos verifikacĳe i
validacĳe softvera . 38

▶Koji je odnos verifikacĳe i validacĳe softvera?
▶Kako se definišu verifikacĳa i validacĳa softvera?
▶Koji pristupi i problemi koji se javljaju u okviru
verifikacĳe softvera?

3.2 Tehnike verifikacĳe
softvera . . . . . . . 40

▶Koje su specifičnosti automatske statičke verifika-
cĳe softvera?

Obezbeđivanje i kontrola kvaliteta softvera obuhvataju
procese validacĳe i verifikacĳe.

Verifikacĳa softvera obuhvata sve procese koji su po-
trebni da se osigura da razvĳeni softver zadovo-
ljava zadatu specifikacĳu, odnosno da ne sadrži
defekte i da bude ispravan. Verifikacĳom se odgo-
vara na pitanje „Da li je softver ispravno izgrađen?”
i fokusira se na proveru da li sistem u potpunosti
ispunjava specifikacĳu.

Validacĳa softvera obuhvata sve procese koji su po-
trebni da se osigura da razvĳeni softver zadovo-
ljava korisničke potrebe. Validacĳom se odgovara
na pitanje „Da li je izgrađen pravi softver?” i pro-
cenjuje da li softver ispunjava potrebe i očekivanja
krajnjih korisnika.

U oba slučaja, kontrola se najčešće sprovodi testiranjem,
ali postoje i druge napredne tehnike koje se mogu koristi-
ti. Kako bi softverski proizvod bio upotrebljiv i uspešan,
neophodno je da zadovolji i kriterĳume ispravnosti i
kriterĳume usklađenosti sa korisničkim zahtevima.

Funkcionalna podobnost, performantnost, kompatibil-
nost, pouzdanost, sigurnost, bezbednost i prenosivost
predstavljaju dinamička svojstva softvera i procenjuju
se primarno kroz procese verifikacĳe. Upotrebljivost

<!-- pdf_page=52 printed_page=38 -->

Verifikacĳa

Potrebe i
očekivanja korisnika
Specifikacĳa
Proces razvoja
Proizvod

Validacĳa

Slika 3.1: Verifikacĳa i validacĳa softvera

se uglavnom procenjuje kroz validacĳu, iako se poje-
dini aspekti, poput otpornosti na korisničke greške,
mogu ispitivati i verifikacĳom. Održivost je statička
karakteristika koja se ocenjuje kroz verifikacĳu, najčešće
pregledima koda i pomoću alata za statičku analizu.

Napomena: studentski i
industrĳski projekti. Pro-
ces verifikacĳe i validacĳe
studentskih projekata naj-
češće se sprovodi pri kraju
procesa razvoja softvera, ko-
risteći mali broj test primera.
Ovaj proces obično čini veo-
ma mali procenat ukupnog
napora koji studenti ulože
u razvoj softvera. S druge
strane, proces verifikacĳe i
validacĳe u industrĳi spro-
vodi se tokom celokupnog
razvoja softvera i najčešće
čini više od 30% ukupnog
napora, pri čemu taj proce-
nat može značajno da varira
u zavisnosti od vrste pro-
jekta i nivoa kvaliteta koji je
neophodno postići. Za be-
zbednosno kritične sisteme
ovaj procenat je značajno vi-
ši.
Osnovne razlike između
studentskih i industrĳskih
projekata su:

### 3.1 Odnos verifikacĳe i validacĳe softvera

U savremenom digitalnom okruženju, korisnici pokazu-
ju sve manju tolerancĳu prema softverskim greškama,
naročito kada je reč o mobilnim aplikacĳama. Ogromna
konkurencĳa i visoka očekivanja doveli su do toga da
i najmanji propust može biti presudan za uspeh pro-
izvoda. Korisnici danas imaju širok izbor – za svaku
potrebu postoji desetine alternativa, bilo da se radi o
aplikacĳama za zdravlje, zabavu, hobĳe ili društvene
mreže. Zbog toga, loše korisničko iskustvo se ne oprašta;
prelazak na konkurentski proizvod je lak i brz. Greške u
softveru nisu samo tehnički izazov — one predstavljaju
direktan poslovni rizik.

Upravo zato, procesi verifikacĳe i validacĳe softvera
postaju ključni u razvoju aplikacĳa. Verifikacĳa se od-
nosi na sve vrste provera ispravnosti rada aplikacĳe,
uključujući i testiranje aplikacĳe u realnim uslovima i
na različitim uređajima, kako bi se osiguralo da sistem
funkcioniše bez grešaka. Ako aplikacĳa ima bagove, ruši
se ili je spora, korisnici je percipiraju kao nepouzdanu i

▶dužina upotrebe
softvera,

▶način upotrebe
softvera,

▶broj korisnika,
▶očekivanja i
▶cena pada.

<!-- pdf_page=53 printed_page=3 -->

deinstaliraće je često i nakon samo prve greške. Dodatno,
negativne recenzĳe odvraćaju buduće korisnike.

S druge strane, validacĳa procenjuje da li aplikacĳa
zaista ispunjava očekivanja korisnika. Aplikacĳa može
biti tehnički ispravna, ali ako ne nudi jasnu vrednost ili
ako je interfejs zbunjujući, korisnik je verovatno više neće
koristiti. Upravo zbog toga, elementi kao što su dizajn
korisničkog iskustva i korisničkog interfejsa, uvodno
vođenje korisnika kroz aplikacĳu i prvi utisak igraju
presudnu ulogu u njenom prihvatanju.

Primer 3.1.1 (Verifikacĳa i validacĳa) U komunikacĳi
sa klĳentom, definisana je specifikacĳa sistema:

Aplikacĳa treba da prikazuje vreme.

U skladu sa zadatom specifikacĳom, moguće je na-
praviti dva rešenja.

Rešenje 1: Digitalni časovnik

Rešenje 2: Aplikacĳa za vremensku prognozu

Rešenja su fundamentalno različita jer je reč „vreme”
višeznačna.

Verifikacĳom se proverava da li je sistem koji je iz-
građen u skladu sa zadatom specifikacĳom, tj. da li
sistem tačno prikazuje vreme.

▶U slučaju digitalnog časovnika, verifikacĳa obu-
hvata proveru da li aplikacĳa ispravno prikazuje
trenutno lokalno vreme, u skladu sa sistemskim
vremenom uređaja ili referentnim vremenskim
serverom. To podrazumeva ispitivanje usklađe-
nosti prikazanog vremena sa vremenom opera-
tivnog sistema, kao i ispravnost prikaza prili-
kom promene vremenske zone. Takođe, prove-
rava se da li se vreme automatski osvežava bez
potrebe za dodatnom intervencĳom korisnika,

<!-- pdf_page=54 printed_page=40 -->

odnosno bez manuelnog osvežavanja stranice
ili aplikacĳe.

▶Kod aplikacĳa za prikaz vremenske progno-
ze, verifikacĳa se fokusira na tačnost i konzi-
stentnost prikaza prognoziranih meteoroloških
podataka koji se preuzimaju sa odgovarajućih
vremenskih servisa, kao što su AccuWeather ili
OpenWeatherMap. Neophodno je utvrditi da li se
podaci, poput temperature i opisa vremenskih
uslova, prikazuju u odgovarajućem i očekiva-
nom formatu. Pored toga, proverava se i da li
aplikacĳa ispravno prikazuje vremenske podat-
ke za različite lokacĳe, bilo da su one definisane
nazivima gradova ili geografskim koordinata-
ma.

Validacĳa predstavlja postupak kojim se utvrđuje da
li je razvĳeni sistem u skladu sa stvarnim potrebama i
očekivanjima korisnika. Na primer, ukoliko je korisnik
zahtevao digitalni časovnik, tada je rešenje koje imple-
mentira upravo tu funkcionalnost validno. Međutim,
ako je korisnik očekivao aplikacĳu za vremensku
prognozu, tada digitalni časovnik ne zadovoljava nje-
gove potrebe i smatra se potpuno neodgovarajućim
rešenjem.

Jasno je da i potpuno ispravan digitalni časovnik ne-
ma vrednost u kontekstu zahteva za aplikacĳom koja
prikazuje vremenske uslove. S druge strane, ukoli-
ko je korisnik zaista želeo digitalni časovnik, ali je
implementacĳa neispravna, sistem takođe postaje ne-
upotrebljiv.

### 3.2 Tehnike verifikacĳe softvera

Verifikacĳa softvera obuhvata skup sistematskih me-
toda i aktivnosti kojima se proverava da li softverski
proizvod ispravno implementira zadatu specifikacĳu.
Tehnike verifikacĳe softvera uključuju dinamičku i statič-

<!-- pdf_page=55 printed_page=3 -->

ku verifikacĳu softvera. Dinamička verifikacĳa softvera
podrazumeva ispitivanje ispravnosti softvera u toku
njegovog izvršavanja. Statička verifikacĳa softvera pod-
razumeva ispitivanje ispravnosti softvera bez njegovog
izvršavanja, odnosno analizu izvornog koda.

Dinamička verifikacĳa softvera.
Najčešći vid dina-
mičke verifikacĳe softvera je testiranje. Testiranje je iz-
vršavanje programa sa ciljem da se pronađe što više
mogućih defekata ili da se stekne dovoljno poverenja
u sistem koji se testira. Pravilnim i sistematičnim te-
stiranjem podižemo nivo pouzdanosti i smanjujemo
verovatnoću da greške promaknu. Obim testiranja i
aktivnosti koje su vezane za testiranje zavise od me-
todologĳe razvoja softvera i prilagođavaju se svakom
konkretnom projektu. Moderni pristupi razvoju softve-
ra podrazumevaju da je testiranje prisutno u svakoj
fazi razvoja softvera. U okviru dinamičke verifikacĳe
softvera, koriste se i alati za debagovanje kao i razne
vrste profajlera.

Napomena: Testiranje se če-
sto koristi i kao sinonim za
verifikacĳu i kao sinonim
za validacĳu softvera. Testi-
ranje se često koristi i kao
sinonim za brigu o kvalitetu
softvera. Međutim, testiranje
je ipak samo važan deo veri-
fikacĳe softvera, važan deo
validacĳe softvera, a verifika-
cĳa i validacĳa su važan deo
brige o kvalitetu softvera.

Statička verifikacĳa softvera.
Postoje različite vrste
statičke verifikacĳe:

Metode mašinskog učenja
mogu da se koriste za pred-
viđanje grešaka u softveru.
Jedan takav primer se može
videti u master radu Nikole
Vidiča:
Primena mašinskog učenja u
verifikacĳi softvera

▶Provere i pregledi koda koje rade ljudi
▶Formalne metode verifikacĳe softvera — uslo-
vi ispravnosti softvera iskazuju se u terminima
matematičkih tvrđenja na striktno definisanom
formalnom jeziku izabrane matematičke teorĳe.

Ručne provere i pregledi koda su veoma važni i svakod-
nevno se primenjuju u okviru procesa razvoja softvera.
Formalne metode se sve više koriste na najrazličitĳe
načine. Važno mesto u oblasti formalnih metoda zauzi-
ma formalna semantika programskih jezika. Formalna
semantika programskog jezika koristi matematičke mo-
dele i formalne tehnike za precizno definisanje značenja
programa. Cilj formalne semantike je da na rigorozan
način opiše kako se izvršavaju naredbe u programskom

<!-- pdf_page=56 printed_page=42 -->

jeziku, čime se eliminiše dvosmislenost i omogućava
proverljiva interpretacĳa. Formalna semantika pred-
stavlja temelj za razumevanje i analiziranje značenja
softverskog koda na precizan, matematički način.

Upravo kroz formalnu semantiku postaje moguće:

▶modelovati izvršavanje programa nezavisno od
konkretne mašine ili kompajlera,

▶dokazivati korektnost softverskih komponenti i
▶razvĳati alate za formalnu verifikacĳu.

Idealno rešenje za verifikacĳu softvera bi bio alat koji
automatski analizira kôd i daje precizne informacĳe o
njegovoj ispravnosti. Međutim, postoji fundamentalno
ograničenje zbog kojeg tako nešto nĳe moguće napraviti.
Naime, halting problem je neodlučiv.‗ Ne postoji opšti
automatizovan način za proveravanje da li je neka nared-
ba programa dostižna, pa sami tim ni da li je ispravna,
odnosno da li je sam program ispravan.

Slika
3.2:
Logo
alata
Rocq
(https:
//rocq-prover.org/)

Posledica teorĳskog ograničenja je da nĳe moguće na-
praviti program koji bi potpuno automatski u konačnom
vremenu, koristeći konačne resurse mogao da utvrdi
ispravnost proizvoljnog programa potpuno precizno.
Međutim, ukoliko se odreknemo potpune preciznosti,
možemo da napravimo program koji poptuno automat-
ski, u konačnom vremenu, koristeći konačne resurse
može da dâ veoma korisne informacĳe o ispravnosti
programa, iako ne u potpunosti precizne. Preciznost
može da bude narušena na dva načina. Alat može da
ima

Slika 3.3: Logo alata Isa-
belle (https://isabelle.in.
tum.de/)

Rocq je interaktivni dokazi-
vač teorema, odnosno po-
moćnik za dokazivanje. On
omogućava pisanje matema-
tičkih dokaza i formalnih
specifikacĳa, tj. pisanje pro-
grama i dokaza da programi
ispunjavaju svoje specifikaci-
je.
Rocq je ranĳe bio poznat kao
Coq Proof Assistant. Pod tim
imenom je 2013. godine do-
bio ACM Software System
Award kao i ACM SIGPLAN
Programming Languages Softwa-
re Award, dve najprestižnĳe
nagrade koje softver može
da dobĳe.

▶lažna upozorenja — da prĳavljuje problem koji u
realnom izvršavanju ne može da se desi,

▶propuštene greške — da ne prĳavljuje problem
koji u realnom izvršavanju može da se desi.

‗ Alan Turing, On Computable Numbers With an Application to the
Entscheidungsproblem, Proceedings of the London Mathematical
Society, 1936.

<!-- pdf_page=57 printed_page=3 -->

Automatski pristupi obično teže da imaju ili samo lažna
upozorenja, ili samo propuštene greške — kombinova-
nje lažnih upozorenja sa propuštenim greškama čini
alat praktično nepoželjnim.

Statička verifikacĳa softvera
je vremenski veoma zahtev-
na. Primer upotrebe parale-
lizacĳe sa ciljem poboljšanja
efikasnosti statičke verifika-
cĳe može se videti u master
radu Branislave Živković:
Paralelizacĳa statičke verifikacĳe
softvera

Takođe, prilikom izgradnje automatskog alata za ispi-
tivanje ispravnosti često se pravi kompromis između
preciznosti i efikasnosti. Efikasni alati najčešće nisu
precizni, dok precizni alati nisu efikasni.

U automatsku statičku analizu se ubrajaju:

▶simboličko izvršavanje,
▶proveravanje modela i
▶apstraktna interpretacĳa.

Pored alata za automatsko otkrivanje grešaka u progra-
mima, formalne metode verifikacĳe softvera obuhvataju
i tehnike razvoja ispravnog softvera. Generisanje koda
direktno iz specifikacĳe i formalno dokazivanje isprav-
nosti softvera koji se razvĳa predstavljaju najviši nivo
sigurnosti u ispravnost softvera. Ovo je ujedno i naj-
skuplji razvoj softvera i zahteva visoko stručne ljude
i upotrebu posebnih alata, kao što su npr Rocq (slika
3.2) i Isabelle (slika 3.3). Iako ovakav razvoj softvera
vodi najpouzdanĳem softveru, on je ujedno i najskuplji
i najsporĳi pa se u industrĳi najčešće koristi samo za
razvoj kritičnih delova koda.

Rezime

▶Obezbeđivanje i kontrola kvaliteta softvera obu-
hvataju validacĳu i verifikacĳu softvera.

▶Validacĳa softvera obuhvata sve procese koji su
potrebni da se osigura da definisana specifikacĳa
softvera zadovoljava korisničke potrebe.

▶Verifikacĳa softvera obuhvata sve procese koji
su potrebni da se osigura da razvĳeni softver
zadovoljava zadatu specifikacĳu.

▶I verifikacĳa i validacĳa su od suštinske važnosti
za kvalitet softvera.

<!-- pdf_page=58 printed_page=44 -->

▶Verifikacĳa softvera može da bude dinamička i
statička.

▶Dinamička verifikacĳa softvera se oslanja pre sve-
ga na testiranje, ali testiranje ne može da garantuje
ispravnost softvera.

▶Statička verifikacĳa softvera uključuje ljudske pre-
glede koda i formalne metode.

▶Automatska statička verifikacĳa: neophodni su
kompromisi između preciznosti i efikasnosti.

▶Razvoj direktno iz specifikacĳe i formalno doka-
zivanje ispravnosti softvera koristi se za razvoj
kritičnih delova aplikacĳa.

Literatura

[1]
Paul Ammann i Jeff Offutt. Introduction to Softwa-
re Testing. Cambridge University Press, 2017. doi:

10.1017/9781316771273.

[2]
Antonia Bertolino. Software Testing Research: Ac-
hievements, Challenges, Dreams. 2007., str. 85–103.
doi: 10.1109/FOSE.2007.25.

[3]
Edmund M. Clarke, Orna Grumberg i Doron A.
Peled. Model Checking. MIT Press, 1999. isbn:
9780262032704.

[4]
Glenford J. Myers, Corey Sandler i Tom Badgett.
The Art of Software Testing. 3. izdanje. Wiley, 2011.
isbn: 9781118031964.

[5]
Doron Peled. Software Reliability Methods. Sprin-
ger, 2001. doi: 10.1007/978-1-4757-3540-6.

Ispitna pitanja

8. Odnos verifikacĳe i validacĳe softvera. Primeri.
9. Tehnike verifikacĳe softvera. Osnovna podela. Mo-
gućnosti dinamičkog i statičkog pristupa verifika-
cĳi softvera.

<!-- pdf_page=59 printed_page=59 -->

Dinamička verifikacija softvera

<!-- pdf_page=61 printed_page=61 -->

Pregled

4.1
Testiranje i
razvoj softvera .
47

▶Koja je uloga testiranja u procesu razvoja softvera?
▶Koje vrste testiranja postoje — šta se proverava?
▶Koje tehnike testiranja postoje — kako napraviti
dobre test primere?

4.2
Vrste i nivoi
testiranja . . . .
62

4.3
Tehnike testira-
nja . . . . . . . .
86

▶Koji načini sprovođenja testiranja postoje — kada
koristiti manuelno, a kada automatsko testiranje?

4.4
Načini sprovođe-
nja testiranja . . 120

Dinamička verifikacĳa softvera predstavlja skup meto-
da i tehnika kojima se proverava ispravnost softverskog
sistema tokom njegovog izvršavanja. Među tim tehnika-
ma, najčešće primenjivana, i svakako najrasprostranjeni-
ja forma verifikacĳe uopšte, jeste testiranje. Testiranje se
ogleda u kontrolisanom pokretanju softvera uz korišće-
nje unapred definisanih skupova ulaznih podataka, pri
čemu se pažljivo prati njegovo ponašanje i upoređuje sa
očekivanim ishodima.

Kada se testiranje sprovodi na pravilan i sistematičan
način, ono može u velikoj meri doprineti unapređe-
nju kvaliteta softverskog proizvoda. Razumevanje toga
kako, kada i zašto testirati omogućava ne samo efikasni-
je otkrivanje grešaka, već i oblikovanje procesa razvoja
softvera tako da se od samog početka teži visokom kva-
litetu konačnog rešenja. Iz tih razloga, od suštinske je
važnosti da svi koji učestvuju u razvoju softvera pose-
duju znanje o metodologĳi testiranja, kao i o njegovim
procesima i osnovnim principima.

### 4.1 Testiranje i razvoj softvera

Softver nastaje kao odgovor na jasno definisane zahteve
korisnika, koji precizno određuju šta softver treba da

<!-- pdf_page=62 printed_page=48 -->

radi, na koji način treba da funkcioniše, u kojim uslo-
vima, koje potrebe korisnika treba da zadovolji i kako
treba da ostvaruje interakcĳu sa krajnjim korisnikom.
Svako odstupanje softvera od ovih zahteva smatra se
defektom. Defekti su neposredna posledica ljudskih gre-
šaka napravljenih u različitim fazama razvoja softvera
— od analize i dizajna, preko implementacĳe, pa sve do
testiranja i održavanja.

Testiranje softvera predstavlja sistematsku aktivnost u
okviru životnog ciklusa razvoja, koja ima za cilj da ot-
krĳe defekte pre nego što softver dospe u ruke krajnjih
korisnika. Osim što doprinosi identifikacĳi i ispravljanju
defekata, testiranje takođe pomaže u proceni pouzdano-
sti, performansi i ukupne stabilnosti softverskog proi-
zvoda. Na taj način, ono igra ključnu ulogu u postizanju
visokog kvaliteta i korisničkog zadovoljstva.

4.1.1 Cena greške u kontekstu vremena
otkrivanja

U savremenom razvoju softvera, osnovni cilj organiza-
cĳa i razvojnih timova jeste postizanje maksimalnog
profita kroz isporuku proizvoda visokog kvaliteta, ali
istovremeno uz poštovanje vremenskih rokova i bu-
džetskih ograničenja. Upravo iz tog razloga, metode i
pristupi koji omogućavaju bržu, efikasnĳu i pouzdanĳu
isporuku softverskih rešenja postaju sve važnĳi.

Slika
4.1:
Edger
Dĳkstra
(eng. Edsger Dĳkstra)a, do-
bitnik
Tjuringove
nagrade
1972. godine:

”Program testing
can show the pre-
sence of bugs, ne-
ver their absen-
ce”

Faze razvoja softvera su organizovane prema metodo-
logĳi koja se koristi za upravljanje razvojem softverskog
projekta, a osnovne faze se javljaju u svim modelima
razvoja. Osnovne faze razvoja softvera uključuju ana-
lizu zahteva, dizajn i implementacĳu softvera, razne
vrste testiranja i upotrebu softvera. Najzastupljenĳe i
trenutno najpopularnĳe su agilne metodologĳe razvoja
softvera (npr. Scrum, Kanban, Extreme Programming). One
se zasnivaju na iterativnom pristupu koji podrazumeva
paralelno razvĳanje i testiranje softverskih komponenti.
Umesto da se testiranje odlaže za kraj procesa (kao što je

Testiranje može da potvrdi pri-
sustvo grešaka u softveru —
testiranje ne može da dokaže
ispravnost softvera.

a Fotografiju je napravio Ha-
milton Richards. Fotografija
je dostupna pod licencom
Creative Commons Attribution-
Share Alike 3.0

<!-- pdf_page=63 printed_page=4 -->

to slučaj u tradicionalnim pristupima razvoju softvera),
ono se integriše u svaku fazu razvoja: svaka funkcio-
nalna celina se implementira i istovremeno proverava
testovima, čime se omogućava brza povratna informaci-
ja i pravovremeno otkrivanje defekata.

Savremeni pristupi razvoju
softvera obuhvataju i razvoj
vođen ponašanjem. Razvoj
vođen ponašanjem omoguća-
va jasnu definicĳu poslovnih
zahteva, poboljšava komu-
nikacĳu između razvojnih
i poslovnih timova i dopri-
nosi unapređenju kvaliteta
i pouzdanosti softverskih
sistema. Primer razvoja vo-
đenog ponašanjem može se
videti u master tezi Veroni-
ke Marinković:
Razvoj vođen ponašanjem kroz
primenu alata Cucumber

Kako složenost softverskih sistema raste, proporcional-
no raste i značaj testiranja. Greške koje promaknu u
ranim fazama razvoja mogu da izazovu lančane proble-
me, koji ne samo da komplikuju završne faze projekta,
već u krajnjem slučaju mogu dovesti i do potpunog
neuspeha proizvoda.

Zbog toga je od suštinskog značaja da se sve greške
otkrĳu što ranĳe u životnom ciklusu softvera. Ispravlja-
nje grešaka u početnim fazama razvoja je znatno brže,
jednostavnĳe i jeftinĳe u poređenju sa otklanjanjem gre-
šaka u kasnĳim fazama. To je povezano i sa brojem ljudi
koje je potrebno uključiti u proces ispravljanja greške,
a koji zavisi od faze razvoja softvera u kojoj se greška
pronađe:

Faza analize zahteva. Greška zahteva revizĳu defini-
sanih zahteva. Trošak uključuje dodatno vreme
analitičara.

Faza dizajna softvera. Ispravka greške podrazumeva
izmenu dizajna, što zahteva dodatni rad dizajnera
i ažuriranje opisa implementacĳe.

Faza implementacĳe softvera. Greške otkrivene tokom
kodiranja obično programer brzo ispravi. Cena
zavisi od složenosti, ali je niža ako programer sam
pronađe grešku. U okviru implementacĳa softve-
ra, posebno je bitna faza integracĳe komponenti,
koja obuhvata sklapanje različitih softverskih kom-
ponenti u veće celine. Greške su u ovoj fazi teže
za otkrivanje jer uključuju više različitih delova
softverskog sistema. Ispravka zahteva saradnju vi-
še članova tima i potencĳalno različitih razvojnih
timova pa samim tim i više vremena za analizu
uzroka, što utiče i na to da je ispravljanje greške
skuplje.

<!-- pdf_page=64 printed_page=50 -->

Faza sistemskog testiranja. Cena greške otkrivene u
ovoj fazi uključuje rad tima zaduženog za kvalitet
softvera, prĳavu greške, komunikacĳu sa progra-
merima, ponovna testiranja i praćenje kroz sistem
za praćenje defekata. Ukoliko u procesu razvo-
ja softvera postoji korak testiranja prihvatljivosti
softvera, cena greške dodatno obuhvata i rad kup-
ca odnosno korisnika koji vrši proveru da li je
softver prihvatljiv. Korisnički otkrivene greške
zahtevaju dodatnu koordinacĳu sa timom zadu-
ženim za kvalitet softvera i povratnu integracĳu
ispravki. Trošak uključuje vreme korisnika i pro-
dužava završne faze projekta.

Faza upotrebe. Greške u produkcĳi imaju najveću cenu.
Pored tehničke ispravke, dolazi do gubitka pove-
renja korisnika i potencĳalne reputacione štete.

4.1.2 Uloga testera u razvoju softvera

Projekti u oblasti razvoja softvera mogu se voditi na
najrazličitĳe načine. Briga o kvalitetu softvera podra-
zumeva primenu različitih pravila, procedura i praksi,
koje zavise kako od vrste projekta, tako i od zrelosti i
veličine same kompanĳe. U nekim slučajevima kvalitet
softvera je odgovornost razvojnog tima, dok u drugim
postoji posebno definisan tim zadužen za ovu oblast.

Tim za obezbeđenje kvaliteta softvera može postojati
kao zasebna organizaciona jedinica unutar kompanĳe
koja razvĳa softver (interni tim), ili može biti eksterno
angažovan od strane specĳalizovane firme koja pruža
usluge testiranja i kontrole kvaliteta. U nekim kompani-
jama, posebno u manjim i manje formalnim okruženji-
ma, ovakav tim uopšte ne postoji, a aktivnosti testiranja
programeri obavljaju ad-hoc.

Tester softvera (eng. software tester) ili jednostavno tester
je stručnjak koji se bavi planiranjem, izvođenjem i doku-
mentovanjem aktivnosti testiranja softverskog sistema,
sa ciljem da se obezbedi očekivani kvalitet proizvoda.

<!-- pdf_page=65 printed_page=4 -->

Njegov osnovni zadatak jeste sistematsko ispitivanje sof-
tvera kako bi se identifikovali defekti u funkcionisanju,
performansama ili upotrebljivosti.

Raspodela obaveza između programera i testera u timo-
vima može biti organizovana na različite načine:

▶programeri su istovremeno i testeri i sami prove-
ravaju svoj kôd,

▶programeri i testeri rade zajedno u istom timu,
blisko sarađujući,

▶programeri i testeri čine potpuno odvojene timove
sa jasnim razgraničenjem odgovornosti.

Iako je kvalitetan softver krajnji cilj i programera i testera,
često postoji veliki broj problema na relacĳi programer
— tester onda kada su programeri i testeri u razdvojenim
timovima. Problemi su u lošoj komunikacĳi, međusob-
nom nerazumevanju i opštoj netrpeljivosti. Ovi problemi
su najčešće posledica psihološke reakcĳe na pronalaže-
nje greške u softveru. Pronalaženje greške u softveru
testeru označava da je uspešno obavio svoj zadatak, dok
programeru to znači da nĳe uspešno obavio svoj posao
i da je potrebno ponovo da radi na nekom delu koda za
koji je verovao da je završen (slika 4.2).

Slika 4.2: Osnovni razlog ne-
slaganja testera i programera.

Da bi se osoba bavila testiranjem potrebno je da po-
seduje osnovno razumevanje programiranja i procesa
razvoja softvera. Posebno, mora da detaljno poznaje
procedure i proces testiranja kao i alate koji se koriste u
testiranju. Za efikasnu implementacĳu i automatizaci-
ju testiranja neophodno je i poznavanje skript jezika i
skript programiranja.

Dobri testeri su kreativni i imaju potrebu za stalnim
usavršavanjem, a vremenom upoznaju i česte greške
i propuste kao i nesvakidašnje slučajeve upotrebe, što
značajno olakšava i ubrzava proces testiranja. Za poslove
testiranja još uvek je dominantna neformalna edukaci-
ja kroz kurseve, konferencĳe i sastanke profesionalnih
udruženja. Za napredne poslove automatizacĳe u testi-
ranju neophodne su napredne programerske veštine.

<!-- pdf_page=66 printed_page=52 -->

4.1.3 Faze testiranja softvera

Za početak procesa testiranja, postojanje koda nĳe ne-
ophodno. Dovoljno je imati jasno definisane zahteve
korisnika jer priprema za testiranje počinje analizom
tih zahteva. Dakle, da bi se započeli procesi vezani za
testiranje, potrebno je da postoji specifikacĳa zahteva
sistema (eng. system requirements specification) kao i spe-
cifikacĳa zahteva softvera (eng. software requirements
specification).

Testiranje softvera se u opštem slučaju sastoji od na-
rednih faza, pri čemu svaka faza obuhvata veliki broj
aktivnosti.

1. Planiranje testiranja

2. Analiza, dizajn i implementacĳa testova
3. Izvršavanje testova
4. Evaluacĳa testova
5. Zatvaranje testiranja

Ove faze se usklađuju sa metodologĳom razvoja softvera
tako da se u okviru iterativnih modela razvoja izvršavaju
iterativno.

Planiranje testiranja

Planiranje definiše:

▶potrebne vrste
testova,

Planiranje testiranja (eng. test planning) predstavlja pri-
premu za proces testiranja. Plan testiranja se prilagođava
svakom konkretnom projektu.

▶tehnike testiranja koje
će se koristiti,

▶načine sprovođenja
testiranja,

Planiranje testiranja započinje analizom zahteva, pri
čemu se detaljno razmatraju svi funkcionalni i nefunk-
cionalni aspekti sistema. Na osnovu te analize definišu
se ciljevi testiranja, odnosno šta se želi postići samim
testiranjem. Sledeći korak obuhvata određivanje opsega
testiranja, uključujući odluku o tome koje će komponen-
te softvera biti testirane i koliko. Dodatno, određuju se i
načini testiranja: koji će delovi testiranja biti sprovedeni
ručno, a koji automatizovano, uključujući i alate koji će

▶opseg testiranja,
▶ulazne i izlazne
kriterĳume, posebno
kriterĳum završetka,

▶potrebne resurse,
▶procenu rizika,
▶metodologĳu
praćenja defekata i

▶uloge i način
komunikacĳe između
članova tima.

<!-- pdf_page=67 printed_page=4 -->

biti korišćeni tokom testiranja. Planiranje takođe uklju-
čuje precizno definisanje uloga i odgovornosti članova
tima.

Praćenje projekata i defekata
Jira https://www.

Važan deo planiranja je i procena rizika, koja uključu-
je identifikacĳu potencĳalnih problema i njihov uticaj
na kvalitet proizvoda. Vremenski okvir testiranja se
takođe detaljno planira, uz jasno definisane ulazne i
izlazne kriterĳume koji određuju kada testiranje može
da počne i pod kojim uslovima se smatra završenim.
Konačno, planiranje uključuje pripremu test okruženja,
odnosno obezbeđivanje potrebnog hardverskog i sof-
tverskog okruženja neophodnog za efikasno i pouzdano
izvođenje testova.

atlassian.com/software/

jira je komercĳalna platfor-
ma za upravljanje projekti-
ma, koja se često koristi u
okviru agilnog razvoja sof-
tvera.
Bugzilla https://www.

bugzilla.org/ je besplatan
alat otvorenog koda, specĳa-
lizovan za praćenje grešaka i
upravljanje defektima.

Neizostavan deo plana je i metodologĳa za praćenje
defekata, koja precizno definiše kako se greške prĳa-
vljuju, dokumentuju, prate tokom životnog ciklusa i na
kraju zatvaraju, čime se obezbeđuje kontrola kvaliteta i
transparentnost celokupnog procesa testiranja.

Analiza, dizajn i implementacĳa testova

Analiza, dizajn i implementacĳa testova (eng. test ana-
lysis, design and implementation) predstavljaju ključne
faze u okviru procesa testiranja softverskih sistema.
Ove aktivnosti podrazumevaju sistematski pristup u
osmišljavanju načina na koji će se sprovesti testiranje, u
skladu sa prethodno definisanim test planom.

Jedan od najbitnĳih rezultata ovih faza je koherentan i
sveobuhvatan skup test slučajeva i procedura koji služe
kao temelj za uspešno sprovođenje testiranja i verifika-
cĳu ispravnosti softverskog rešenja. Test slučaj (eng. test
case) predstavlja formalni dokument koji opisuje odre-
đenu situacĳu testiranja kroz definisani skup ulaznih
podataka i očekivane izlaze sistema. Svaki test slučaj
ima za cilj da proveri konkretnu funkcionalnost softvera,
njegovo ponašanje u graničnim uslovima ili otpornost
na nevalidne ili neočekivane ulaze. Procedura testiranja

<!-- pdf_page=68 printed_page=54 -->

(eng. test procedure) definiše tačan redosled i način pri-
mene test slučajeva u kontrolisanom okruženju. Testni
okvir, testno okruženje ili infrastruktura za testiranje
(eng. test harness) je skup skripti, alata i konfiguracĳa koji
omogućavaju automatsko pokretanje testova, simulacĳu
realnog upotrebnog okruženja i prikupljanje rezultata.
Poređenje ovih pojmova je dato u tabeli 4.1.

Tabela 4.1: Poređenje: test slučaj, procedura testiranja i testni okvir

Pojam
Opis

Test slučaj (test)
Konkretna situacĳa koja se testira, sa definisanim ulazima i
očekivanim izlazima.
Procedura testiranja
Skup jasno definisanih koraka koji opisuju kako se jedan ili
više test slučajeva izvršavaju u praktičnom okruženju.
Testni okvir
Skup alata i infrastrukture koji omogućavaju automatsko iz-
vršavanje testova, simulacĳu delova sistema i prikupljanje
rezultata testiranja.

faze testiranja

U fazi analize testova, vrši se detaljno ispitivanje mo-
gućnosti testiranja pojedinih delova softverskog sistema
i identifikacĳu zahteva koje sistem mora da ispuni. Ovaj
proces podrazumeva detaljno razlaganje korisničkih pri-
ča (eng. user story), upotrebnih scenarĳa (eng. use cases)
i tehničke dokumentacĳe, kako bi se identifikovali svi
elementi koji mogu i treba da budu predmet testiranja.
Kroz identifikacĳu zavisnosti, ograničenja i potencĳal-
nih rizika, analiza testova gradi detaljnu mapu puta koji
vodi ka dizajnu testova i njihovom kasnĳem izvršava-
nju. Time se obezbeđuje sveobuhvatna pokrivenost svih
relevantnih aspekata softverskog sistema.

planiranje
testiranja

analiza, dizajn
i implemen-
tacĳa testova

izvršavanje
testova

evaluacĳa testova

zatvaranje
testiranja

Primer 4.1.1 (Aplikacĳa za elektronsko bankarstvo)
Razmotrimo projekat razvoja aplikacĳe za elektron-
sko bankarstvo. Tokom faze analize testova, testeri
analiziraju funkcionalne zahteve sistema. Jedan od
njih je i

Korisnici treba da mogu da prenose novac
između računa.

<!-- pdf_page=69 printed_page=4 -->

Na osnovu ovog zahteva, identifikuju se različiti sce-
narĳi testiranja, kao što su:

▶Prenos novca između računa u istoj banci
▶Prenos ka računima u drugim bankama
▶Testiranje granica – npr. minimalni i maksimalni
iznos za prenos

Pored toga, identifikuju se i granični slučajevi (eng. ed-
ge cases), kao što su:

▶Pokušaj prenosa novca kada korisnik nema do-
voljno sredstava na računu

▶Pokušaj ponovljenog prenosa usled pada mreže
▶Neispravno unet broj računa primaoca

Svi ovi identifikovani scenarĳi biće u narednim faza-
ma formalizovani u test slučajeve, čime se obezbeđuje
da funkcionalnost prenosa novca bude testirana u ce-
losti — sa aspekta tačnosti, pouzdanosti i bezbednosti.
Na ovaj način, analiza testova ne samo da razbĳa kom-
pleksne zahteve na razumljive i proverljive jedinice,
već i postavlja temelj za kvalitetan dizajn i izvršavanje
testova, koji direktno doprinosi uspešnosti krajnjeg
softverskog proizvoda.

Analiza, dizajn i implementa-
cĳa testova:
Faza analize testova daje
odgovor na pitanje „šta testi-
rati?”.
Faza dizajna testova daje
odgovor na pitanje „kako
testirati?”.
Faza implementacĳe daje sve
što je potrebno da testiranje
može da počne.

Faza dizajna testova sledi nakon analize i predstavlja
temelj za dalji tok testiranja. U ovoj fazi definišu se
ciljevi testiranja, identifikuju funkcionalnosti koje tre-
ba proveriti i preciziraju uslovi pod kojima će testovi
biti sprovedeni. Identifikovani scenarĳi se razrađuju u
test slučajeve i prateću dokumentacĳu (eng. testware),
čime se obezbeđuje jasan i sistematičan pristup. Ključne
aktivnosti u okviru dizajna testova obuhvataju:

▶kreiranje i prioritizacĳu test slučajeva,
▶identifikacĳu potrebnih test podataka,
▶preciziranje testnog okruženja, uključujući potreb-
nu infrastrukturu i alate.

Cilj ove faze je da se obezbedi dosledna i kvalitetna
osnova za kasnĳu implementacĳu i izvršavanje testo-

<!-- pdf_page=70 printed_page=56 -->

va.

Primer 4.1.2 (Aplikacĳa za elektronsko bankarstvo
— nastavak primera 4.1.1) Razmotrimo identifikovan
scenario testiranja:

Pokušaj prenosa novca kada korisnik ne-
ma dovoljno sredstava na računu.

U fazi dizajna testova, za ovaj scenario, može se iden-
tifikovati naredni skup test slučajeva:

1. Apsolutno nedovoljno sredstava
Korisnik ima 0 RSD na računu, a pokušava da
prenese npr. 1000 RSD.
Očekivanje: Transakcĳa odbĳena; jasna poruka o
nedostatku sredstava.

2. Delimično pokrivanje iznosa
Korisnik ima 500 RSD na računu, a pokušava
da prenese 1000 RSD.
Očekivanje: Transakcĳa odbĳena; jasna poruka o
nedostatku sredstava, ali potrebno je testirati i
prikaz informacĳa o preostalom saldu i sugestĳu
da se izvrši prenos manjeg iznosa.

3. Nedovoljno sredstava zbog provizĳe
Korisnik ima dovoljno novca na računu, ali se
naplaćuje provizĳa za prenos.
Očekivanje: Transakcĳa odbĳena uz poruku o
dodatnoj provizĳi.

4. Nedovoljno sredstava zbog rezervacĳe sred-
stava
Na računu piše da ima dovoljno sredstava,
npr. 1000 RSD, ali je deo sredstava rezervisan,
npr. 800 RSD.
Očekivanje: Efektivno dostupno stanje je 200
RSD; prenos većeg iznosa treba da bude odbi-
jen.

5. Nedovoljno sredstava u drugoj valuti
Račun je u dinarima, a korisnik pokušava prenos

<!-- pdf_page=71 printed_page=4 -->

u evrima. Nakon konverzĳe, stanje nĳe dovolj-
no.
Očekivanje: Sistem treba da prikaže da konverto-
vani iznos nĳe dovoljan.

6. Ponovljeni pokušaji prenosa bez sredstava
Višestruki pokušaji prenosa istog iznosa bez
pokrića.
Očekivanje: Sistem blokira pokušaje, potencĳal-
no uvodi vremensko ograničenje ili detekcĳu
zloupotrebe.

Dodatno, potrebno je precizirati sve identifikovane
test slučajeve. Na primer, test slučaj za prenos novca u
slučaju delimičnog pokrivanja iznosa je dat u okviru
primera 4.2.3.

Ove test slučajeve može da izvršava tester, po zadatim
koracima, a može se i napisati skript koji automatizuje
njihovo izvršavanje i simulira sve korisničke korake.
Ukoliko je predviđeno da se testovi izvršavaju auto-
matizovano, u fazi implementacĳe obezbeđuje se kôd
koji je potreban za njihovo izvršavanje.

U višegodišnjim projekti-
ma koje razvĳa veliki broj
nezavisnih timova često se
javljaju redudantni testovi.
Oni otežavaju održavanje
testne infrastrukture i pro-
dužavaju vreme potrebno za
sprovođenje testiranja. Pri-
mer detekcĳe i uklanjanja
redundantnih testova može
se videti u master tezi Irene
Blagojević:
Automatsko uklanjanje redun-
dantnih testova

Faza implementacĳe testova predstavlja završni korak
u pripremi za izvršavanje testiranja. U ovoj fazi dolazi
do konkretizacĳe prethodno dizajniranih test slučajeva
kroz njihovo organizovanje u procedure testiranja, kao i
pripreme potrebne testne dokumentacĳe, alata i okru-
ženja. Cilj implementacĳe je da obezbedi doslednost,
ponovljivost i tehničku spremnost za efikasno izvršava-
nje testova.

Ključne aktivnosti koje se sprovode tokom implementa-
cĳe testova uključuju:

▶Razvoj procedura testiranja i razvoj test okvira
— omogućava strukturisano i, gde je primenljivo,
automatizovano izvršavanje test slučajeva.

▶Formiranje test kompleta (eng. test suites) gru-
pisanjem povezanih procedura i skripti — radi
lakše organizacĳe i povećanja efikasnosti tokom

<!-- pdf_page=72 printed_page=58 -->

izvršavanja.

▶Raspoređivanje test kompleta u plan izvršavanja
— u skladu sa raspoloživim resursima i prioriteti-
ma.

▶Pripremu test podataka i proveru njihove in-
tegracĳe u okruženje — kako bi se obezbedila
validnost ulaza i pouzdanost rezultata testiranja.

Na ovaj način, implementacĳa testova zatvara krug
pripremnih aktivnosti i postavlja temelj za sledeću fazu
— sâmo izvršavanje testiranja.

Primer 4.1.3 (Aplikacĳa za elektronsko bankarstvo —
nastavak primera 4.1.2) Naziv test procedure: Testira-
nje prenosa sredstava u uslovima nedovoljnog stanja
na računu

Opis: Ova test procedura pokriva slučajeve kada ko-
risnik pokušava da izvrši prenos novca, ali na računu
nema dovoljno sredstava za realizacĳu transakcĳe.
Cilj je da se verifikuje ispravno ponašanje sistema
u različitim varĳacĳama ovog problema, uključujući
osnovni nedostatak sredstava, rezervacĳe, provizĳe i
valute.

Preduslovi:

▶Korisnički nalog je kreiran i verifikovan.
▶Korisnik ima pristup elektronskom bankarstvu.
▶Test račun je aktivan i koristi dinarsku valutu
(RSD).

▶Testno okruženje koristi realne validacione me-
hanizme.

Koraci:

Test slučaj 1: Apsolutno nedovoljno sredstava
Test slučaj 2: Delimično pokrivanje iznosa
Test slučaj 3: Nedovoljno sredstava zbog provizĳe
Test slučaj 4: Nedovoljno sredstava zbog rezervisa-
nih sredstava

<!-- pdf_page=73 printed_page=4 -->

Test slučaj 5: Nedovoljno sredstava u drugoj valuti

Završni uslovi:

▶Sve test transakcĳe treba da budu evidentirane
u log fajlovima.

▶Nĳe dozvoljena promena stvarnog salda kori-
snika.

▶Sistem mora prikazati odgovarajuće poruke gre-
ške.

Primetimo da test slučaj vezan za ponovne uzastop-
ne pokušaje podizanja novca kada na računu nema
dovoljno sredstava može takođe da se uvrsti u ovu
proceduru testiranja ili da se grupiše u drugu proce-
duru testiranja, na primer, u neku koja se odnosi na
sigurnost sistema.

Izvršavanje testova

faze testiranja

Izvršavanje testova (eng. test execution) predstavlja fazu
u kojoj se praktično primenjuju test slučajevi i test proce-
dure razvĳene tokom prethodnih faza. Testovi se mogu
sprovoditi ručno – kada tester sam prati korake iz test
slučaja – ili automatski, korišćenjem specĳalizovanih
alata koji omogućavaju bržu proveru funkcionalnosti.

planiranje
testiranja

analiza, dizajn
i implemen-
tacĳa testova

Prilikom testiranja, neophodna je organizacĳa testiranja
kako bi se testovi izvršavali u skladu sa prioritetima
i efikasno, bez gubljenja resursa i vremena. To uklju-
čuje raspoređivanje testova, kontrolu test okruženja i
praćenje napretka test aktivnosti.

izvršavanje
testova

evaluacĳa testova

zatvaranje
testiranja

Izvršavanje testova predstavlja ključni korak u prove-
renju funkcionalnosti sistema i verifikacĳi da softver
ispunjava postavljene zahteve. Tokom ove faze, testovi
se sistematski sprovode kako bi se otkrile greške, ali i
kako bi se pratio trenutni status svih prethodno prĳa-
vljenih problema. Dakle, pored samog testiranja, važan
deo ove aktivnosti jeste praćenje i upravljanje greškama
– to podrazumeva ne samo prĳavu otkrivenih problema,

<!-- pdf_page=74 printed_page=60 -->

već i njihovo kontinuirano praćenje, proveru ispravki i
konačnu potvrdu da su greške uspešno otklonjene. Sva-
ka korekcĳa zahteva ponovno izvršavanje relevantnih
testova kako bi se osiguralo da popravka nĳe dovela do
novih problema ili narušila postojeću funkcionalnost.

Ova faza testiranja zahteva intenzivnu i jasnu komuni-
kacĳu između testera i programera. Bliska saradnja i
razmena informacĳa omogućavaju bržu identifikacĳu
uzroka grešaka, efikasnĳe rešavanje problema i osigura-
nje stabilnosti sistema u završnim fazama razvoja.

Evaluacĳa testova

faze testiranja

Evaluacĳa testova (eng. test evaluation) obuhvata proce-
nu kriterĳuma završetka testiranja i izveštavanje. Svaka
izmena u kodu, čak i koja podrazumeva popravljanje
grešaka, može da dovede do novih grešaka. Iz tog razlo-
ga se, za različite oblasti testiranja, definiše kriterĳum
završetka testiranja u odnosu na rezultate izvršavanja
testova, procenta nerešenih bagova ili preostalog vre-
mena za testiranje. Proces evaluacĳa uključuje i pregled
rezultata dobĳenih analizom izlaza test slučajeva.

planiranje
testiranja

analiza, dizajn
i implemen-
tacĳa testova

izvršavanje
testova

Izlazni kriterĳumi (eng. exit criteria) određuju da li je
testiranje kompletirano i da li je aplikacĳa spremna za
korišćenje u skladu sa korisničkim zahtevima. Da bi se
odredilo da li su izlazni kriterĳumi ispunjeni, potrebno
je uzeti u obzir rezultate testiranja date kroz sažeti
izveštaj testiranja (eng. test summary report), rezultate
izračunavanja raznih metrika i izveštaj o defektima
(eng. defect analysis report).

evaluacĳa testova

zatvaranje
testiranja

Primer 4.1.4 (Aplikacĳa za elektronsko bankarstvo —
nastavak primera 4.1.3) Primer izlaznih kriterĳuma
za elektronsko bankarstvo dat je u nastavku.

1. Pokrivenost testovima: 95% definisanih funkcio-
nalnih i nefunkcionalnih zahteva mora biti po-

<!-- pdf_page=75 printed_page=4 -->

kriveno odgovarajućim test slučajevima.

2. Prolaznost test slučajeva: 100% kritičnih test slu-
čajeva i najmanje 98% svih ostalih test slučajeva
mora biti uspešno izvršeno.

3. Odsustvo kritičnih i visoko-prioritetnih grešaka:

Nisu dozvoljene greške koje utiču na osnovnu
funkcionalnost sistema (npr. greške koje one-
mogućavaju prĳavu korisnika, pregled stanja
računa, ili izvršavanje transakcĳa).

4. Potvrđena sigurnost sistema: Sigurnosne provere
moraju potvrditi da sistem ne sadrži ranjivosti
koje bi mogle dovesti do neautorizovanog pri-
stupa, curenja podataka ili drugih sigurnosnih
incidenata.

5. Stabilnost u test okruženju: Aplikacĳa mora sta-
bilno funkcionisati tokom višednevnog testira-
nja bez rušenja, curenja memorĳe ili degradacĳe
performansi.

6. Obezbeđena testna dokumentacĳa: Sva testna do-
kumentacĳa (test planovi, zapisnici o testiranju,
rezultati testova, prĳave grešaka) mora biti ažur-
na i kompletna.

7. Odobrenje zainteresovanih strana: Tim za testira-
nje, razvoj, bezbednost i poslovni korisnici mo-
raju formalno potvrditi da su svi zahtevi zado-
voljeni i da je sistem spreman za dalji proces.

Zatvaranje testiranja

Zatvaranje testiranja označava završnu fazu test procesa,
koja nastupa kada su svi planirani testovi sprovedeni i
softver je isporučen krajnjem korisniku, bez daljih oba-
veza održavanja. Međutim, ovakva situacĳa je u praksi
veoma retka, jer se nakon isporuke softvera gotovo uvek
podrazumeva i njegovo održavanje, u okviru kog se
testiranje i dalje sprovodi — u vidu provera ispravki,
unapređenja funkcionalnosti ili novih verzĳa softvera.

Testiranje se može zatvoriti i u drugim okolnostima —

<!-- pdf_page=76 printed_page=62 -->

na primer, u slučaju da je projekat otkazan, ako su ciljevi
testiranja ostvareni ranĳe nego što je planirano, ili ako
nema više smisla nastavljati testiranje zbog promene
poslovnih prioriteta.

faze testiranja

Tokom faze zatvaranja testiranja, vrši se arhiviranje test
slučajeva, izveštaja i prateće dokumentacĳe, čime se
omogućava budući uvid u realizovane aktivnosti. Isto-
vremeno, sprovodi se analiza samog procesa testiranja,
uz identifikacĳu onih praksi koje su se pokazale uspe-
šnima i koje bi trebalo zadržati i primeniti u budućim
projektima.

planiranje
testiranja

analiza, dizajn
i implemen-
tacĳa testova

Podjednako je važno prepoznati i aspekte koji nisu
funkcionisali dobro, kako bi se greške iz prošlosti izbegle
i unapredila efikasnost testiranja u narednim iteracĳama.
Na taj način, zatvaranje testiranja ne označava samo kraj
jedne faze, već i priliku za učenje i stalno poboljšanje
procesa.

izvršavanje
testova

evaluacĳa testova

zatvaranje
testiranja

### 4.2 Vrste i nivoi testiranja

Testiranje softvera može se klasifikovati na više načina,
u zavisnosti od cilja, obima i nivoa na kojem se testira-
nje sprovodi. Osnovna podela testiranja odnosi se na
prirodu osobina koje se proveravaju, pa razlikujemo:

Testiranje funkcionalnih karakteristika usmereno je
na proveru da li aplikacĳa pravilno izvršava funk-
cĳe definisane specifikacĳom zahteva. Ova vrsta
testiranja ispituje ponašanje sistema u odnosu na
očekivane ulaze i izlaze.

Testiranje nefunkcionalnih karakteristika usmereno
je na tehničke i kvalitativne aspekte sistema, kao
što su performanse, sigurnost, upotrebljivost, kom-
patibilnost i pouzdanost.

Druga bitna podela je podela po nivoima testiranja (slika
4.3). Mogu se testirati

▶osnovne jedinice koda,

<!-- pdf_page=77 printed_page=4 -->

▶pojedinačni moduli,
▶grupe modula (vezanih namenom, upotrebom,
ponašanjem ili strukturom) ili

▶ceo sistem.

U skladu sa pomenutom podelom, prema nivou testi-
ranja, razlikujemo testove jedinice koda, komponentne,
integracione i sistemske testove. Na svakom nivou mogu
se testirati funkcionalne i nefunkcionalne karakteristike
softvera.

Testiranje

Komponentno

Integraciono

Sistemsko

testiranje

testiranje

testiranje

jedinica koda

Slika 4.3: Nivoi testiranja

Posebna vrsta testiranja koja se može javiti u okviru sva-
kog nivoa je regresiono testiranje. Regresiono testiranje
(eng. regression testing) predstavlja proces ponovnog iz-
vršavanja prethodno uspešno završenih test slučajeva s
ciljem da se proveri da li novouvedene izmene u softveru
nisu nenamerno dovele do regresĳe, tj. narušile postojeću
funkcionalnost sistema ili dovele do pada performansi.
Regresiono testiranje se sprovodi uvek nakon ispravki
grešaka, dodavanja novih funkcionalnosti i prilikom
refaktorisanja koda.

4.2.1 Testiranje jedinica koda

Primeri izazova testiranja u
funkcionalnim programskim
jezicima mogu se videti u
master tezi Ane Petrović:

Testiranje jedinica koda (eng. unit testing) predstavlja
proveru ispravnosti najmanjih delova softverskog si-
stema koji se mogu nezavisno testirati. U zavisnosti
od programske paradigme, jedinice koda mogu biti
različite: u objektno orĳentisanom programiranju to su
najčešće klase, u funkcionalnom programiranju funkcĳe,

Testiranje funkcionalnih progra-
ma na primeru aplikacĳe koja
koristi jezike Elm i Eliksir

<!-- pdf_page=78 printed_page=64 -->

dok se u imperativnom programiranju obično testiraju
procedure i pojedinačni moduli.

Ova vrsta testiranja omogućava detaljan uvid u po-
našanje svake pojedinačne jedinice, čime se osigurava
stabilna osnova za kasnĳu integracĳu u veće sisteme.
1008-1987 IEEE Standard for Software Unit Testing je stan-
dard koji definiše jedinično testiranje i koji postavlja
smernice i preporuke za njegovo sprovođenje.

Jedna od ključnih prednosti testiranja jedinica koda jeste
snažna podrška u alatima za automatsko izvršavanje i
proveru rezultata rada testova, koji su često integrisani
u savremena razvojna okruženja. Automatizacĳa ovih
testova omogućava brzu i čestu proveru funkcionalnosti
u toku razvoja.

Testiranje

jedinica koda

Cilj jediničnih testova je da se potvrdi da izolovani de-
lovi koda funkcionišu u skladu sa očekivanjima. Kada
jedinica koda komunicira sa spoljnim resursima, kao
što su standardni ulaz, mreža, baze podataka ili fajl
sistemi, ta komunikacĳa se u test okruženju zamenju-
je fiksiranim (eng. mock) vrednostima. Isto važi i za
komunikacĳu sa drugim klasama ili komponentama –
sve se apstrahuje, kako bi se test fokusirao isključivo
na ponašanje posmatrane jedinice. Dozvoljena je samo
interakcĳa sa memorĳom.

Ove testove najčešće pišu sami programeri tokom razvo-
ja, što omogućava brzo otkrivanje i otklanjanje grešaka.
Ukoliko postoji problem unutar same jedinice koda,
upravo ova faza testiranja treba da ga otkrĳe — pre nego
što dođe do složenĳih i skupljih grešaka u kasnĳim
fazama razvoja.

Primer 4.2.1 (Biblioteka unittest u jeziku Python)
Funkcĳa saberi(a, b) je jednostavna funkcĳa ko-
ja vraća zbir dva broja i definisana je u modulu

matematika.py.

1
def saberi(a, b):

<!-- pdf_page=79 printed_page=4 -->

2
return a + b

Naredni kôd (datoteka test_matematika.py koja je
u istom direktorĳumu sa datotekom matematika.py)
sadrži jednostavan jedinični test za ovu funkcĳu.

1 import unittest

2 from matematika import saberi

3

4 class TestSaberi(unittest.TestCase):

5
def test_saberi_pozitivne(self):

6
self.assertEqual(saberi(2, 3), 5)

7

8
def test_saberi_negativne(self):

9
self.assertEqual(saberi(-1, -1), -2)

10

11 if __name__ == ’__main__’:

12
unittest.main()

Klasa TestSaberi nasleđuje klasu unittest.TestCase
i sadrži dva testa:

▶Jedan testira sabiranje pozitivnih brojeva.
▶Drugi testira sabiranje negativnih brojeva.

Funkcĳa assertEqual proverava da li je rezultat funk-
cĳe jednak očekivanoj vrednosti. Funkcĳa

1 unittest.main()

pokreće ove testove.

Test se pokreće iz komandne linĳe narednom nared-
bom

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

rava ispravnost komponente. Komponenta je skup funk-
cionalno povezanih jedinica koda koje zajedno obavljaju
jednu logičku celinu i imaju jasno definisan interfejs.
Komponentno testiranje se obično sprovodi izolovano
od ostatka sistema i odmah nakon razvoja komponen-
te.

Iako se po načinu izvođenja komponentno testiranje če-
sto nadovezuje na jedinično testiranje, osnovna razlika je
u nivou koji obuhvataju — dok jedinično testiranje prove-
rava pojedinačne jedinice koda, komponentno testiranje
se fokusira na veće celine koje sadrže više jedinica koda
i njihovu međusobnu saradnju. Sama jedinica koda je
u prethodnoj fazi testiranja izolovana u potpunosti od
spoljašnjeg sistema, dok se sada isti princip izolacĳe pri-
menjuje ali na nivou komponente. To znači da jedinice
koda u okviru komponente komuniciraju međusobno,
ali da je sama komponenta izolovana u komunikacĳi sa
drugim komponentama i sa spoljašnjim sistemima.

Komponentno

testiranje

S obzirom da se u komponentnom testiranju integrišu
osnovne jedinice koda, ovo je vrsta integracionog testi-
ranja, tako da se često i ne izdvaja kao posebna vrsta
testiranja. Pošto se odnosi na direktno spajanje jedinica
koda, može se shvatiti i kao integraciono testiranje na
najnižem nivou. U praksi, komponentno testiranje mogu
obavljati i programeri i testeri, u zavisnosti od organiza-
cĳe projekta i kompleksnosti testiranih komponenti.

Integraciono testiranje (eng. integration testing) pred-
stavlja fazu u procesu testiranja u kojoj se proverava
saradnja između više softverskih komponenti koje za-
jedno čine funkcionalne celine sistema. Integraciono
testiranje ispituje ispravnost interfejsa i komunikacĳe
među komponentama. Cilj ovog testiranja je da se utvrdi
da li su veze između komponenti pravilno definisane i
implementirane, odnosno da li različiti delovi sistema
međusobno komuniciraju na način koji je predviđen
specifikacĳom projekta. Na taj način proverava se funk-
cionalna ispravnost u kontekstu saradnje, a ne samo u
izolacĳi.

Slika 4.4: Brava

Pretpostavimo da imamo
bravu kao na slici 4.4. Uko-
liko takva brava treba da se
integriše sa kliznim vratima
(vratima koja se pomeraju
levo-desno, a ne napred-
nazad), bez obzira što su i
brava i vrata ispravni, nji-
hova integracĳa neće davati
željene rezultate.

<!-- pdf_page=81 printed_page=4 -->

Integracioni testovi otkrivaju razne vrste problema,
uključujući:

▶nekompatibilnost podataka pri razmeni između
modula,

▶neusklađene formate, tipove ili protokole komu-
nikacĳe,

▶pogrešno tumačenje interfejsa ili očekivanih vred-
nosti,

▶greške u redosledu izvršavanja aktivnosti.

Ove testove obično sprovode testeri, iako je u praksi
česta saradnja sa programerima, naročito u složenim
sistemima. Dobra praksa je da se integraciono testiranje
sprovodi inkrementalno — kako se nove komponente ra-
zvĳaju i dodaju sistemu, tako se istovremeno proverava
njihova integracĳa.

Integraciono

testiranje

Primer 4.2.2 (Realni brojevi) Dve softverske kompo-
nente, Aproksimacĳa i Optimizacĳa, vrše računanja sa
realnim brojevima. Međutim, zbog nedovoljno pre-
cizne specifikacĳe, jedna komponenta koristi realne
brojeve jednostruke tačnosti (float), dok druga koristi
realne brojeve dvostruke tačnosti (double). Iako sva-
ka od komponenti zasebno funkcioniše ispravno u
okviru svojih testova, njihova integracĳa dovodi do
neočekivanih odstupanja u rezultatima. Na primer,
vrednost double d = 1234567.89; kada se prebaci u
float postaje 1234567.875 što doprinosi nepreciznosti
izračunavanja.

Upravo kroz integraciono testiranje, takva neusklađe-
nost u tipovima podataka treba da se otkrĳe. Testovi bi
trebalo da obuhvate međusobnu razmenu podataka
između komponenti i da provere konzistentnost vred-
nosti, preciznost proračuna i stabilnost u radu. Kada
se ovakva greška otkrĳe, neophodno je uskladiti po-
datkovne tipove kako bi se osigurala kompatibilnost
komponenti i sprečile greške u računanju.

<!-- pdf_page=82 printed_page=68 -->

4.2.3 Sistemsko testiranje

Sistemsko testiranje (eng. system testing) obuhvata prove-
ravanje sistema kao celine. Ispituje se da li je ponašanje
sistema u skladu sa specifikacĳom zadatom od strane kli-
jenta. Ovde se zahteva i potpun pristup svim delovima
sistema, uključujući bazu podataka, ukoliko se koristi,
pristup mreži i svim hardverskim delovima sistema.

Sistemsko

testiranje

Sistemsko testiranje uključuje i funkcionalne i nefunkcio-
nalne aspekte sistema. U sistemsko testiranje se ubrajaju
i istraživačko testiranje, testiranje prihvatljivosti i insta-
laciono testiranje.

sistemsko
testiranje

funkcionalno
testiranje

Funkcionalno sistemsko testiranje

nefunkcionalno
testiranje

Funkcionalno sistemsko testiranje predstavlja proveru
funkcionalnosti sistema u uslovima koji odgovaraju
stvarnom korišćenju. Cilj funkcionalnog sistemskog te-
stiranja je da se potvrdi da su sve očekivane funkcional-
nosti sistema implementirane (funkcionalna potpunost),
da svaka funkcionalnost pojedinačno radi u skladu sa
zahtevima korisnika (funkcionalna ispravnost) kao i
da su sve funkcionalnosti sistema prikladne (funkci-
onalna prikladnost). Ovo testiranje obuhvata provere
ulaza, obrada i izlaza za različite funkcionalne scenarĳe,
uključujući tipične, granične i nesvakidašnje slučajeve
upotrebe. Dodatno, potrebno je evaluirati i ponašanje
sistema u slučaju pogrešnih ili neočekivanih ulaza.

istraživačko
testiranje

testiranje
prihvaljtljivosti

instalaciono
testiranje

Primer 4.2.3 (Aplikacĳa za elektronsko bankarstvo —
nastavak primera 4.1.4) Primer test slučaja za funkci-
onalno testiranje.

Naziv test slučaja: TC-002 — Prenos novca sa nedo-
voljno sredstava na računu — Delimično pokrivanje
iznosa

Opis: Proverava da li aplikacĳa pravilno obrađuje

<!-- pdf_page=83 printed_page=4 -->

Testiranje
bezbed-
nosti

Testiranje
sigur-
nosti

Funkcionalno
testiranje

Testiranje
upotre-
bljivosti

Testiranje
preno-
sivosti

Nefunkcionalno
testiranje

Istraživačko
testiranje

Testiranje
pouzda-
nosti

Testiranje
kompati-
bilnosti

Sistemsko
testiranje

Testiranje
perfor-
mansi

Testiranje
kon-
figu-
racĳa

Testiranje
kapa-
citeta

Instalaciono
testiranje

Stres
testi-
ranje

Testiranje
prihva-
tljivosti

Paralelno
testiranje

Referentno
testiranje

Pilot
testiranje

Slika 4.5: Vrste sistemskog testiranja

pokušaj prenosa novca kada na korisničkom računu
nema dovoljno sredstava.

Preduslovi:

▶Korisnik je prĳavljen u aplikacĳu
▶Na računu korisnika nalazi se manje sredstava
od iznosa koji želi da prenese (npr. stanje: 500
RSD)

▶Primalac ima validan račun u sistemu

<!-- pdf_page=84 printed_page=70 -->

Test podaci:

▶Iznos za prenos: 1000 RSD
▶Broj računa primaoca: 170-1234567890123-45

Koraci:

1. Prĳaviti se u aplikacĳu sa validnim korisničkim
nalogom

2. Otvoriti sekcĳu „Prenos sredstava“
3. Uneti iznos prenosa: 1000 RSD
4. Uneti broj računa primaoca
5. Kliknuti na dugme „Potvrdi prenos“

sistemsko
testiranje

Očekivani rezultat:

▶Sistem prikazuje poruku o grešci: „Nedovoljno
sredstava na računu“

funkcionalno
testiranje

▶Sistem sugeriše prenos manje količine novca
▶Prenos se ne izvršava
▶Stanje na računu ostaje nepromenjeno

Stvarni rezultat: (popunjava se nakon izvršavanja testa)

Status: (PASS / FAIL – popunjava se nakon testiranja)

sistemsko
testiranje

Uspešno funkcionalno testiranje potvrđuje da sistem
zadovoljava svoje osnovne zahteve i da je spreman za
naredne faze verifikacĳe, uključujući nefunkcionalna
testiranja, istraživačko testiranje i konačno prihvatanje
od strane krajnjih korisnika.

nefunkcionalno
testiranje

performanse

Nefunkcionalno sistemsko testiranje

kompatibilnost

pouzdanost

Nefunkcionalno sistemsko testiranje obuhvata testira-
nje dinamičkih nefunkcionalnih aspekata sistema: per-
formanse, kompatibilnost, pouzdanost, upotrebljivost,
bezbednost, sigurnost i prenosivost. Testovi se spro-
vode za one aspekte kvaliteta softvera koji su za dati
sistem prepoznati kao važni i koji su stoga precizirani
specifikacĳom. Na primer,

upotrebljivost

bezbednost

sigurnost

prenosivost

<!-- pdf_page=85 printed_page=4 -->

Testovima performansi proverava se vremensko po-
našanje aplikacĳe i njena upotreba resursa. Ova
vrsta testiranja se fokusira na metrike kao što su
vreme odgovora na zahteve, broj obrađenih zahte-
va u jedinici vremena, vreme obrade podataka,
kao i iskorišćenost memorĳe i drugih sistemskih
resursa. Sastavni deo testiranja performansi su i
testovi kapaciteta, stresa i konfiguracĳe.

sistemsko
testiranje

Testovima kapaciteta proverava se ponašanje si-
stema pri obradi velikih količina podataka.
Posebna pažnja posvećuje se granicama si-
stema, tj. kako softver funkcioniše kada se
približi maksimalnim kapacitetima definisa-
nim u zahtevima.

nefunkcionalno
testiranje

performanse

Stres testovima se proverava kako se sistem po-
naša kada ga izložimo zahtevima izvan nje-
govog projektovanog kapaciteta, odnosno
šta se dogodi kada sistem preopteretimo i
kako se sistem oporavlja kada se opterećenje
smanji.

kapacitet

stres

Testovima konfiguracĳe proverava se rad siste-
ma u različitim hardverskim i softverskim
okruženjima. Time se obezbeđuje da apli-
kacĳa funkcioniše stabilno bez obzira na
konkretne kombinacĳe operativnih sistema,
drajvera, baza podataka ili uređaja.

konfiguracĳa

Primer 4.2.4 (Aplikacĳa za elektronsko bankar-
stvo — nastavak primera 4.2.3) Testovi kapa-
citeta su ključni za planiranje infrastrukture i
predviđanje kapaciteta u rastu korisničke ba-
ze. Rezultati mogu ukazati na potrebu za hori-
zontalnim skaliranjem ili optimizacĳom baze
podataka.
Naziv test slučaja: TC-C003 — Test kapaciteta

Cilj testa:
Proceniti ponašanje sistema pri obradi velikog

<!-- pdf_page=86 printed_page=72 -->

broja korisničkih zahteva i velikih količina po-
dataka u periodima maksimalnog opterećenja,
kako bi se utvrdili granični kapaciteti sistema.

Scenario:
Simulirati rad bankarskog sistema tokom vr-
šnog opterećenja (npr. kraj meseca, isplata plata)
kada veliki broj korisnika istovremeno koristi
aplikacĳu za pregled stanja, prenose sredstava
i uplate računa.

Uslovi testa:

▶10.000 simultanih korisničkih sesĳa.
▶Svaka sesĳa izvršava niz standardnih ope-
racĳa: prĳava, pregled stanja, prenos novca,
uvid u istorĳu transakcĳa.

▶Korišćenje stvarnog produkcionog okru-
ženja ili njegove precizne simulacĳe.

▶Baza podataka inicĳalizovana sa velikim
brojem (npr. 1.000.000) korisnika.

Metrike koje se prate:

▶Prosečno i maksimalno vreme odziva za
ključne operacĳe.

▶Percentili vremena odziva (npr. P50, P90,
P95, P99)a.

▶Iskorišćenost resursa (CPU, memorĳa, ba-
za podataka).

▶Broj uspešno izvršenih zahteva u sekundi.
▶Broj neuspešnih ili odbĳenih zahteva (gre-
ške, prekoračenja vremena ili kapaciteta).

Kriterĳum prolaznosti:
Sistem mora podržati najmanje 8.000 istovreme-
nih korisnika sa vremenom odziva manjim od
2 sekunde za sve ključne operacĳe. Maksimalni
gubitak zahteva ne sme preći 0.05%.

a : Vrednost Pk predstavlja vreme ispod koga se završava
𝑘% zahteva (npr. P95 znači da se 95% zahteva izvršava
brže od te vrednosti, dok preostalih 5% traje duže).

<!-- pdf_page=87 printed_page=4 -->

Testovima kompatibilnosti proverava se način na koji
sistem komunicira sa spoljnim komponentama
i sistemima. Ovaj vid testiranja uključuje ispiti-
vanje koegzistencĳe (mogućnosti rada zajedno
sa drugim softverima na istom sistemu) i inter-
operabilnosti (sposobnosti razmene podataka i
funkcionalne saradnje sa drugim sistemima). Ci-
lj je da se osigura da sistem može uspešno da
funkcioniše u širem okruženju bez konflikata ili
nekompatibilnosti.

sistemsko
testiranje

Primer 4.2.5 (Aplikacĳa za elektronsko bankar-
stvo — nastavak primera 4.2.4) Aplikacĳa mora
da se izvršava stabilno i kada se istovremeno
izvršavaju druge aplikacĳe.

nefunkcionalno
testiranje

Naziv test slučaja: TC-K009 — Koegzistencĳa
sa antivirusom, VPN klĳentom i upravljanjem
lozinkama.

kompatibilnost

Opis: Proveriti da li elektronska bankarska apli-
kacĳa može da funkcioniše ispravno kada se
izvršava paralelno sa drugim softverom instali-
ranim na korisnikovom uređaju, bez međusob-
nog negativnog uticaja.

Scenario: Korisnik koristi elektronsku bankar-
sku aplikacĳu dok su istovremeno aktivni drugi
programi koji zahtevaju mrežnu komunikaci-
ju i bezbednosne resurse, kao što su antivirus
softver, VPN klĳent i aplikacĳe za upravljanje
lozinkama.

Okruženje testa:

▶OS: Windows 11
▶Aktivni softveri:

• Antivirus: Kaspersky Internet Security
• VPN: Cisco VPN
• Password manager: Bitwarden

▶Aplikacĳa pokrenuta u pregledaču Chrome

<!-- pdf_page=88 printed_page=74 -->

Uslovi testa:

▶Pokrenuti sve navedene programe istovre-
meno sa aplikacĳom.

▶Izvršiti osnovne funkcĳe u aplikacĳi: pri-
java, pregled računa, slanje novca, pristup
izvodima.

▶Posmatrati eventualne konflikte: zamrza-
vanja, gubitak mrežne konekcĳe, bezbed-
nosna upozorenja, itd.

Metrike koje se prate:

▶Broj zabeleženih konflikata između apli-
kacĳe i drugih programa

▶Smanjenje performansi aplikacĳe u uslovi-
ma koegzistencĳe

▶Broj korisničkih funkcionalnosti koje su
otežano dostupne ili onemogućene

Kriterĳum prolaznosti:
Bankarska aplikacĳa mora biti funkcionalna i
stabilna tokom istovremenog rada sa drugim
programima. Ne sme doći do prekida funkci-
onalnosti, gubitka podataka, ili problema sa
bezbednosnim komponentama sistema. Maksi-
malno dozvoljen broj manjih vizuelnih ili funk-
cionalnih anomalĳa: 1.

Testovima pouzdanosti proverava se stabilnost softve-
ra i sposobnost da funkcioniše bez grešaka tokom
određenog vremenskog perioda, u realnim ili si-
muliranim uslovima rada. Na primer, proverava
se da li softver može da radi bez prekida i padova
tokom dužeg vremenskog korišćenja (stabilnost
u radu, zrelost i dostupnost), ispituje se sposob-
nost sistema da se oporavi nakon što dođe do
greške, bilo automatski ili uz minimalnu interven-
cĳu korisnika (oporavak od grešaka), softver se
izvršava neprekidno tokom više sati ili dana (du-
gotrajno testiranje) da bi se otkrile skrivene greške
(npr. curenje memorĳe, degradacĳa performansi)

sistemsko
testiranje

nefunkcionalno
testiranje

pouzdanost

<!-- pdf_page=89 printed_page=4 -->

i proverava se otpornost na promene okruženja,
tj. kako sistem reaguje na promene u okruženju
(npr. prekid mreže, promena konfiguracĳe).

Primer 4.2.6 (Aplikacĳa za elektronsko bankar-
stvo — nastavak primera 4.2.5) Testovi pouzda-
nosti su važni za kritične sisteme kao što su
bankarski, gde pouzdanost direktno utiče na
poverenje korisnika i bezbednost podataka.

Naziv test slučaja: TC-P006 — Pouzdanost to-
kom 72h
Opis:
Proceniti sposobnost sistema da radi stabilno
i bez prekida tokom produženog vremenskog
perioda, u realnim uslovima korišćenja.

Scenario:
Izvršavanje aplikacĳe u trajanju od 72 sata bez
prekida, tokom kojih se konstantno generišu ko-
risnički zahtevi (prĳave, pregledi računa, tran-
sferi sredstava, uplate računa), uz periodične
simulacĳe grešaka i poremećaja u mrežnom
okruženju.

Uslovi testa:

▶Aplikacĳa se pokreće u testnom okruženju
koje odgovara produkcionom.

▶Koristi se alat za automatizacĳu koji konti-
nuirano šalje realistične zahteve sa različi-
tih virtuelnih korisničkih naloga.

▶Na svakih 12 sati se simulira greška u ko-
munikacĳi sa bazom podataka, zatim opo-
ravak.

▶Prati se stabilnost sistema, ponašanje me-
morĳe i CPU-a, kao i sposobnost aplikacĳe
da se automatski oporavi.

Metrike koje se prate:

▶Broj sistemskih padova ili prekida rada.

<!-- pdf_page=90 printed_page=76 -->

▶Vremensko trajanje oporavka posle greške.
▶Prisustvo curenja memorĳe ili degradacĳe
performansi.

▶Očuvanost tačnosti i konzistentnosti poda-
taka.

Kriterĳum prolaznosti:
Tokom 72 sata kontinuiranog rada ne sme doći
do nĳednog sistemskog pada. Nakon svake si-
mulirane greške, sistem mora da se oporavi u
roku kraćem od 60 sekundi. Potrošnja memorĳe
ne sme rasti progresivno bez oslobađanja (in-
dikator curenja memorĳe). Podaci moraju biti
konzistentni i odgovarati obavljenim transakci-
jama.

Testovima upotrebljivosti proverava se koliko je sof-
tverski sistem lak za upotrebu krajnjim korisni-
cima. Ova vrsta testiranja je posebno važna za
aplikacĳe sa korisničkim interfejsom, kao što su
mobilne i veb aplikacĳe, jer ima direktan uticaj
na korisničko iskustvo i prihvatanje proizvoda. U
testovima upotrebljivosti proverava se koliko brzo
novi korisnik može da nauči da koristi sistem bez
pomoći ili obuke (naučljivost), da li korisnik može
da izvrši zadatke u prihvatljivom broju koraka
i u razumnom vremenskom okviru (efikasnost
korišćenja), da li sistem omogućava korisniku da
lako prepozna i ispravi greške (prevencĳa i opora-
vak od grešaka), pristupačnost da li su elementi
korisničkog interfejsa intuitivno raspoređeni i da
li korisnik lako razume njihovu svrhu (jasnoća
interfejsa), da li korisnici subjektivno ocenjuju
sistem kao prĳatan za korišćenje (zadovoljstvo
korisnika), da li je sistem upotrebljiv za osobe
sa različitim oblicima invaliditeta (pristupačnost),
da li je svrha aplikacĳe jasna i lako razumljiva
(prepoznatljivost).
Testiranje se često sprovodi kroz posmatranje kori-
snika dok izvršavaju tipične zadatke, uz praćenje

sistemsko
testiranje

nefunkcionalno
testiranje

upotrebljivost

<!-- pdf_page=91 printed_page=4 -->

vremena, broja grešaka i nivoa frustracĳe. Cilj je
da se identifikuju prepreke koje bi korisniku ote-
žale ili onemogućile korišćenje sistema. Takođe,
često se koriste upitnici i intervjui nakon testiranja
kako bi se saznao subjektivni utisak korisnika.

Primer 4.2.7 (Aplikacĳa za elektronsko bankar-
stvo — nastavak primera 4.2.6) Test naučljivosti
je važan u ranim fazama dizajna korisničkog
interfejsa i često se koristi za usmeravanje itera-
tivnih poboljšanja.

Naziv test slučaja: TC-N010 — Provera naučlji-
vosti prenosa novca sa jednog na drugi tekući
račun.

Opis: Proveriti koliko brzo novi korisnik, bez
prethodnog iskustva sa aplikacĳom, može sa-
mostalno da nauči kako da izvrši osnovnu funk-
cionalnost – prenos sredstava.

Scenario: Učesniku (koji ranĳe nĳe koristio apli-
kacĳu) se daje pametni telefon sa instaliranom
verzĳom aplikacĳe i osnovnim uputstvom za
početak (npr. kako da se prĳavi). Zadatak je
sledeći:

„Prenesite 1000 RSD sa tekućeg raču-
na na drugi račun koristeći opcĳu za
internu transakcĳu.“

Parametri koji se prate:

▶Vreme potrebno da korisnik pronađe opci-
ju za prenos sredstava.

▶Broj pokušaja i grešaka pre nego što se
uspešno izvrši transakcĳa.

▶Broj pitanja koje korisnik postavi (ako je
dozvoljena asistencĳa).

▶Subjektivna ocena korisnika (npr. ocena
složenosti na skali od 1 do 5).

Kriterĳum prolaznosti: Korisnik bi trebalo da

<!-- pdf_page=92 printed_page=78 -->

uspešno izvrši transakcĳu bez pomoći u roku
kraćem od 5 minuta, sa najviše jednom greškom
(npr. pogrešan izbor opcĳe ili unos iznosa u
pogrešno polje).

Napomena: Test se ponavlja sa 30 korisnika ka-
ko bi se dobila reprezentativna metrika. Ukoliko
većina ispitanika ima poteškoće sa istim delovi-
ma interfejsa, to je jasan indikator za poboljšanje
dizajna.

Testovima bezbednosti proverava se zaštita ljudi, opre-
me i okruženja od neželjenih efekata korišćenja
softvera, posebno u kritičnim sistemima kao što
su medicinski uređaji, automobilski sistemi, va-
zduhoplovstvo, industrĳska automatizacĳa i slični
domeni gde greška može imati ozbiljne posledice
po bezbednost.

sistemsko
testiranje

nefunkcionalno
testiranje

bezbednost

Primer 4.2.8 (Autonomna vožnja) Testovi be-
zbednosti su posebno važni u kontekstu auto-
nomne vožnje.

Naziv test slučaja: TC-S007 — Automatsko zau-
stavljanje prilikom iznenadne prepreke na putu.

Opis: Proveriti kako autonomni sistem reaguje
u slučaju iznenadne prepreke na putu, sa ciljem
zaštite putnika i drugih učesnika u saobraćaju.

Scenario: Tokom vožnje pri brzini od 50 km/h,
pešak iznenada ulazi na put na udaljenosti od
15 metara ispred vozila. Sistem za autonom-
nu vožnju mora da detektuje pešaka i aktivira
bezbednosne mehanizme: kočenje, izbegavanje
sudara i/ili upozorenje putnicima.

Uslovi testa:

▶Vozilo je u režimu potpunog autonomnog
upravljanja.

▶Test se izvodi u zatvorenom kontrolisa-
nom okruženju sa korišćenjem lutke kao

<!-- pdf_page=93 printed_page=4 -->

simulacĳe pešaka.

▶Sistem ima pristup svim funkcionalnim
senzorima.

Parametri koji se prate:

▶Vreme reakcĳe sistema nakon detekcĳe
prepreke.

▶Efikasnost kočenja (da li je došlo do zau-
stavljanja pre prepreke).

▶Aktivacĳa dodatnih sistema (upozorenja,
sigurnosni pojasevi, naglo kočenje).

▶Usklađenost sa bezbednosnim standardi-
ma.

Kriterĳum prolaznosti:
Vozilo mora zaustaviti pre nego što dođe do
kontakta sa preprekom u 99.9% slučajeva pri
definisanoj brzini i udaljenosti, uz tolerancĳu
za nepredviđene faktore kao što su vremenski
uslovi ili osvetljenje.

Testovima sigurnosti proverava se da li su određene
funkcionalnosti dostupne isključivo onim kori-
snicima kojima su namenjene. Proveravaju se do-
stupnost, integritet i poverljivost svih skupova
podataka.

sistemsko
testiranje

nefunkcionalno
testiranje

Primer 4.2.9 (Aplikacĳa za elektronsko bankar-
stvo — nastavak primera 4.2.7) Sigurnost ban-
karskih aplikacĳa i zaštita od neautorizovanih
pristupa je izuzetno važna i zato postoji posebna
kategorĳa testiranja koja se naziva penetraciono
testiranje (eng. penetration testing) koja pomaže
u identifikacĳi ranjivosti aplikacĳe na pokušaje
neautorizovanog pristupa.

sigurnost

Naziv test slučaja: TC-SC004 — Neautorizovani
pristupi grubom silom.

Opis: Proveriti da li je aplikacĳa otporna na po-
kušaj neautorizovanog pristupa putem napada

<!-- pdf_page=94 printed_page=80 -->

grubom silom (eng. brute force attack) na formu
za logovanje.

Scenario: Napadač pokušava da pristupi kori-
sničkom nalogu automatskim slanjem velikog
broja kombinacĳa korisničkog imena i lozinke
putem skripte.

Uslovi testa:

▶Test se izvodi u testnom okruženju uz nad-
zor administratora bez pristupa stvarnim
korisničkim podacima.

▶Koristi se alat za automatizovani napad
(npr. alat Hydra).

▶Postoji korisnički nalog sa poznatim kori-
sničkim imenom i slabom lozinkom radi
simulacĳe.

Parametri koji se prate:

▶Maksimalan broj dozvoljenih pokušaja uno-
sa lozinke pre zaključavanja naloga.

▶Vreme blokade naloga i mehanizam oba-
veštavanja korisnika.

▶Evidentiranje pokušaja napada u log fajlo-
vima i reakcĳa sistema.

▶Prisustvo mehanizama CAPTCHA nakon
prvog neuspešnog pokušaja.

Kriterĳum prolaznosti:
Aplikacĳa mora da blokira pristup korisničkom
nalogu nakon najviše 3 neuspešna pokušaja i
mora da onemogući dalju automatizovanu ve-
rifikacĳu lozinki. Napad mora biti zabeležen u
sistemskim logovima sa pripadajućim podaci-
ma (IP adresa, vreme napada, broj pokušaja).

sistemsko
testiranje

Testovima prenosivosti proverava se sposobnost sof-
tverskog sistema da funkcioniše u različitim okru-
ženjima. Glavni cilj ovih testova je da se potvrdi
da softver može lako da se instalira, koristi i radi
ispravno na više platformi, operativnih sistema,
hardverskih konfiguracĳa ili pregledača (u slučaju

nefunkcionalno
testiranje

prenosivost

<!-- pdf_page=95 printed_page=4 -->

veb-aplikacĳa), kao i da može da se u potpuno-
sti ukloni sa sistema bez ostavljanja tragova ili
neželjenih podataka.

Primer 4.2.10 (Aplikacĳa za elektronsko bankar-
stvo — nastavak primera 4.2.9) Test prenosivo-
sti je posebno značajan za bankarske aplikacĳe
jer se koristi na velikom broju različitih uređaja,
a doslednost i pouzdanost korisničkog iskustva
direktno utiču na poverenje korisnika.

Naziv test slučaja: TC-P003 — Prilagodljivost
različitim uređajima i operativnim sistemima.

Opis: Proveriti da li mobilna bankarska aplika-
cĳa funkcioniše dosledno na različitim operativ-
nim sistemima i verzĳama uređaja, bez potrebe
za izmenom izvornog koda.

Scenario: Mobilna aplikacĳa razvĳena je za plat-
forme Android i iOS. Testira se njeno ponašanje
na više verzĳa operativnih sistema i različitim
uređajima:

▶Android 10, 11 i 13 (Samsung Galaxy, Xiaomi,
Pixel)

▶iOS 15 i 17 (iPhone 11, iPhone 14)

Uslovi testa:

▶Instalacĳa najnovĳe verzĳe aplikacĳe sa
zvanične prodavnice (Google Play / App
Store).

▶Test uređaji resetovani na fabrička podeša-
vanja (čisto okruženje).

▶Stabilna internet konekcĳa (Wi-Fi).

Aktivnosti testa:

▶Instalacĳa i pokretanje aplikacĳe na sva-
kom test uređaju.

▶Prĳavljivanje korisnika sa validnim kre-
dencĳalima.

<!-- pdf_page=96 printed_page=82 -->

▶Provera prikaza početnog ekrana, menĳa
i funkcionalnosti (pregled stanja, prenos
sredstava).

▶Upoređivanje vizuelne konzistentnosti in-
terfejsa.

▶Provera lokalizacĳe (prikaz na srpskom i
engleskom jeziku).

Kriterĳum prolaznosti: Aplikacĳa mora da mo-
gući korisnicima da nesmetano obave sve osnov-
ne operacĳe na svim platformama. Ne sme do-
ći do pada sistema, vizuelnih nepravilnosti ili
funkcionalnih razlika među verzĳama.

Istraživačko testiranje

Jedna posebna forma sistemskog testiranja jeste istraži-
vačko testiranje (eng. exploratory testing). Ova metoda
testiranja oslanja se na znanje, intuicĳu i kreativnost
testera, pri čemu se testiranje ne zasniva isključivo na
prethodno definisanim test slučajevima, već se test slu-
čajevi osmišljavaju i izvršavaju u hodu.

sistemsko
testiranje

Istraživačko testiranje podrazumeva otkrivanje neoče-
kivanih pravaca korišćenja softverskog sistema, kao
i prepoznavanje potencĳalnih problema koji nisu bili
identifikovani tokom analize i dizajna testova. Tokom
ove aktivnosti tester intuitivno istražuje aplikacĳu, po-
smatra njeno ponašanje u različitim situacĳama i na
osnovu uočenih obrazaca formuliše nove test slučajeve
u realnom vremenu.

istraživačko
testiranje

Ova vrsta testiranja ima najveći značaj kada je softver
već funkcionalno zaokružen, odnosno kada je aplikacĳa
dostupna u svom gotovo finalnom obliku. Tada tester
ima mogućnost da uoči alternativne tokove korišće-
nja sistema koji nisu prethodno uzeti u obzir, čime se
značajno povećava pokrivenost testiranjem.

Ukoliko se istraživačko testiranje zanemari, postoji ri-
zik da određene funkcionalnosti ostanu neproverene,

<!-- pdf_page=97 printed_page=4 -->

naročito one koje se ne nalaze u primarnim ili očekiva-
nim tokovima rada. Stoga se ova vrsta testiranja često
koristi kao dopuna formalnim tehnikama, sa ciljem da
se dodatno osigura kvalitet konačnog proizvoda. U
okviru istraživačkog testiranja mogu se proveravati i
funkcionalna i nefunkcionalna svojstva sistema.

Primer 4.2.11 (Aplikacĳa za deljenje fotografija) Tester
istražuje neočekivane tokove korišćenja u aplikacĳi
koja omogućava korisnicima da postavljaju, komen-
tarišu i dele fotografije. Testiranje se sprovodi bez
prethodno definisanih test slučajeva, oslanjajući se
na intuicĳu, iskustvo i zapažanja testera. Na primer,
tester istražuje naredne scenarĳe upotrebe

▶Pokušaj postavljanja slike u formatu koji aplika-
cĳa formalno ne podržava (npr. format .tiff)
–– proverava se reakcĳa sistema.

▶Brzo višestruko postavljanje iste fotografije —
provera se da li dolazi do duplikata, grešaka ili
zamrzavanja aplikacĳe.

▶Istovremeno korišćenje više funkcionalnosti
(npr. slanje komentara dok je slika u procesu
postavljanja) — provera se stabilnost aplikacĳe
i ispravnost rada.

▶Pokušaj učitavanja sadržaja bez dostupnog in-
terneta, ili sa slabo propusnim internetom —
provera se prisustvo adekvatne poruke o grešci.

▶Promena jezičkih podešavanja tokom aktivne
sesĳe — provera se uticaj na postojeći sadržaj
korisničkog interfejsa.

U svakom od prethodnih situacĳa aplikacĳa bi tre-
balo da se ponaša stabilno, obezbedi korisniku jasne
poruke o greškama i izbegne pad sistema ili gubitak
podataka. Cilj ovih provera je otkrivanje potencĳalnih
grešaka i nepredviđenih ponašanja sistema u realnim,
kompleksnim i neobičnim scenarĳima koje standardni
test slučajevi možda ne pokrivaju.

<!-- pdf_page=98 printed_page=84 -->

Testiranje prihvatljivosti

Testovi prihvatljivosti (eng. acceptance testing) treba da
omoguće klĳentima i korisnicima da se sami uvere da
je napravljeni softver u skladu sa njihovim potrebama i
očekivanjima. Ovu vrstu testiranja izvode i procenjuju
korisnici, a razvojni tim im pruža pomoć oko tehničkih
pitanja, ukoliko za tim ima potrebe. Testiranje prihvatlji-
vosti obično spada u tehnike validacĳe softvera.

Klĳent može da proceni sistem na tri načina: referent-
nim testiranjem, pilot testiranjem i paralelnim testira-
njem.

sistemsko
testiranje

Referentno testiranje izvode korisnici kako bi proce-
nili da li je softver implementiran u skladu sa
očekivanjima. Kod referentnog testiranja, klĳent
generiše test slučajeve koji predstavljaju uobičajne
uslove u kojima sistem treba da radi.

Testiranje
prihvatljivosti

Pilot testiranje podrazumeva instalacĳu sistema na pri-
vremenoj lokacĳi i njegovu upotrebu. U ovom slu-
čaju, testiranje se vrši simulacĳom svakodnevnog
rada na sistemu.

referentno

pilot

paralelno

Paralelno testiranje se koristi tokom razvoja, kada jed-
na verzĳa softvera zamenjuje drugu ili kada novi
sistem treba da zameni stari. Ideja je paralelno
funkcionisanje oba sistema (starog i novog) čime
se korisnici postepeno privikavaju i prelaze na
korišćenje novog sistema.

Primer 4.2.12 Testiranje prihvatljivosti modernih apli-
kacĳa često se vrši na uzorku odabranih korisnika
(npr. zaposlenih u kompanĳi koja proizvodi aplikacĳu
ili zaposlenih u kompanĳi čĳi će korisnici da koriste tu
aplikacĳu). Na primer, za bankarski softver, to mogu
da budu zaposleni u banci ili manja grupa klĳenata
banke.

Tokom ove faze testiranja prati se korišćenje osnovnih

<!-- pdf_page=99 printed_page=4 -->

ili novododatih funkcionalnosti. Beleže se uočeni pro-
blemi, vreme izvršavanja operacĳa i reakcĳe korisnika
na interfejs i način rada sistema.

Na osnovu prikupljenih podataka identifikuju se even-
tualne greške, nejasnoće u korišćenju i problemi u
performansama, nakon čega se sistem unapređuje pre
šireg uvođenja u produkciono okruženje.

Instalaciono testiranje

Instalaciono testiranje predstavlja specifičnu vrstu testi-
ranja u kojoj se softver instalira u klĳentskom okruženju,
kako bi se proverila njegova sposobnost da se pravilno
instalira i funkcioniše u realnim uslovima. Tokom ovog
procesa, sistem se podešava u skladu sa tehničkim ka-
rakteristikama ciljne mašine, kao i sa specifičnostima
okruženja (npr. operativni sistem, mrežne postavke, po-
vezani uređaji). Ukoliko softver zahteva komunikacĳu sa
spoljnim uređajima ili servisima, testira se i sposobnost
uspostavljanja te komunikacĳe.

sistemsko
testiranje

Primer 4.2.13 Kompanĳe koje obezbeđuju uslugu
testiranja drugim softverskim kompanĳa često raspo-
lažu laboratorĳama za testiranje tj. kolekcĳama uređaja
i računara sa različitim softverskim konfiguracĳama.
Na primer, mogu posedovati desetine modela telefona
sa različitim verzĳama operativnih sistema Android i
iOS. Takav pristup omogućava proveru da li se aplika-
cĳa ispravno instalira i pokreće na svim relevantnim
uređajima i verzĳama operativnog sistema. Istovre-
meno, identifikuju se potencĳalni problemi koji se
javljaju samo u specifičnim kombinacĳama hardvera
i softvera, kao što je pad aplikacĳe na određenom
modelu telefona ili verzĳi operativnog sistema. Ova-
kve laboratorĳe takođe štede vreme i resurse svojih
klĳenata, koji oni ne moraju da poseduju sve moguće
uređaje i konfiguracĳe za testiranje, dok istovremeno

instalaciono
testiranje

<!-- pdf_page=100 printed_page=86 -->

omogućavaju da se testovi ponavljaju automatski ili u
serĳama na više uređaja odjednom, čime se povećava
ponovljivost i pouzdanost testiranja.

Instalacioni testovi se nekada sprovode i u saradnji sa
krajnjim korisnicima, kako bi se osiguralo da instalacĳa
teče bez grešaka i da sistem nakon instalacĳe ispravno
funkcioniše. Poseban akcenat stavlja se na detekcĳu
eventualnih uticaja okruženja na funkcionalne i nefunk-
cionalne karakteristike sistema, kao što su performanse,
sigurnost ili kompatibilnost. Ovo testiranje ima za cilj da
potvrdi da je softver spreman za rad u stvarnom okruže-
nju korisnika, bez potrebe za dodatnim intervencĳama
nakon instalacĳe.

### 4.3 Tehnike testiranja

Tehnike testiranja imaju za cilj da pruže sistematski
odgovor na pitanje kako identifikovati reprezentativ-
ni skup test slučajeva (test primera, ili samo testova).
Reprezentativni skup testova treba da obuhvati slučaje-
ve koji najbolje odražavaju stvarne uslove rada softver-
skog sistema, ali i one koji imaju povećanu verovatnoću
da otkrĳu potencĳalne slabosti u implementacĳi. Do-
datno, treba da omogući efikasno balansiranje između
obima testiranja i potrošnje resursa. Reprezentativni
skup testova treba da ima naredne karakteristike:

▶Visok potencĳal otkrivanja grešaka.
▶Relativno mala veličina.
▶Relativno velika brzina izvršavanja.
▶Pruža visok stepen poverenja u pouzdanost sof-
tvera.

Dobro definisan i pažljivo odabran skup testova predsta-
vlja osnovu za kvalitetno, ciljno-orĳentisano testiranje
koje doprinosi visokom kvalitetu softverskog rešenja.

<!-- pdf_page=101 printed_page=4 -->

4.3.1 Pokrivenost testiranjem

Pokrivenost testiranjem (eng. test coverage) je metrika ko-
ja pomaže da se proceni koliko su testovi sveobuhvatni
i koliko dobro proveravaju funkcionalnost, strukturu i
ponašanje sistema. Koristi se za procenu kvaliteta sof-
tvera. Takođe, može se koristiti i da ukaže na delove
sistema koji nisu testirani. Pomaže u donošenju odluke
da li je softver spreman za isporuku.

Pokrivenost
=
Broj testiranih elem.

Pokrivenost se definiše kao procenat elemenata sistema
koji su obuhvaćeni testiranjem u odnosu na sve elemente
te vrste. Postoje razne vrste pokrivenosti, a osnovne vrste
pokrivenosti su date u nastavku.

Ukupan broj elem. × 100%

Pokrivenost zahteva (eng. requirements coverage) Mera
koja pokazuje koliki je procenat zahteva prove-
ren testiranjem u odnosu na ukupan broj zahteva
korisnika koji su definisani kroz specifikacĳu. Pot-
puna pokrivenost podrazumeva da je svaki zahtev
testiran.

Pokrivenost zahteva
=

Broj testiranih zahteva

Ukupan broj zahteva × 100%

Pokrivenost funkcionalnosti (eng. functional coverage)
Mera koja pokazuje koliki je procenat funkcional-
nosti proveren testiranjem u odnosu na ukupan
broj funkcionalnosti sistema. Potpuna pokrivenost
podrazumeva da je svaka funkcionalnost testira-
na.

Pokrivenost funkcionalnosti =

Broj testiranih funkc.

Ukupan broj funkc. × 100%

Pokrivenost koda (eng. code coverage) Ova mera sadrži
u sebi veći broj različitih pokrivenosti. Na primer,
pokrivenost naredbi se definiše kao broj izvršenih
naredbi u okviru testiranja podeljen sa ukupnim
brojem naredbi u projektu. Pokrivenost koda se
detaljno razmatra u delu 4.3.4.

Pokrivenost koda
=

Broj izvršenih elem.

Ukupan broj tih elem. × 100%

Primer 4.3.1 (Veb aplikacĳa za kupovinu) Visoka po-
krivenost zahteva ne znači nužno i visoku pokrivenost
funkcionalnosti — mogu postojati funkcionalnosti ko-
je nisu formalno dokumentovane zahtevima, a koje
ipak treba testirati. Zato se u praksi često prate obe

<!-- pdf_page=102 printed_page=88 -->

pokrivenosti.

Na primer, za veb aplikacĳu za kupovinu, u okviru
specifikacĳe mogu biti zadati naredni zahtevi:

▶Korisnik može dodati proizvod u korpu.
▶Korisnik može obrisati proizvod iz korpe.
▶Korisnik može završiti kupovinu klikom na
dugme Kupi.

U okviru implementacĳe, uz te zadatke, programer
implementira i sledeće

▶Kada je korpa prazna, dugme Kupi se automat-
ski onemogućava.

▶Ako korisnik pokuša da doda negativan broj
proizvoda, sistem prikazuje poruku o grešci.

Pokrivenost zahteva u ovom slučaju ne obuhvata
pokrivenost funkcionalnosti jer nedostaju testovi im-
plementiranih funkcionalnosti za onemogućavanje
dugmeta Kupi kada je korpa prazna i za prikaziva-
nje poruke o grešci prilikom unosa negativnog broja
proizvoda.

4.3.2 Podela tehnika testiranja

Većina softverskih sistema podrazumeva mogućnost
relativno jasnog utvrđivanja očekivanog izlaza za zadate
uslove. U takvim slučajevima, dobri test primeri se mogu
naći na osnovu specifikacĳe programa (testiranje crne
kutĳe), na osnovu koda programa (testiranje bele kutĳe)
ili na osnovu kombinacĳe specifikacĳe i koda programa
(testiranje sive kutĳe).

Odnos: Testiranje crne kutĳe
je testiranje iz ugla kori-
snika dok je testiranje bele
kutĳe testiranje iz ugla pro-
gramera.

Testiranje crne kutĳe (eng. black box testing) — generi-
sanje test primera bez razmatranja interne struk-
ture koda već isključivo na osnovu specifikacĳe.
Ovakav način testiranja se fokusira na ponašanje
sistema, posmatrano iz korisničkog ugla. Drugi
nazivi su i funkcionalno testiranje (eng. functio-
nal testing), testiranje ponašanja (eng. behavioural

<!-- pdf_page=103 printed_page=4 -->

testing), testiranje vođeno podacima (eng. data dri-
ven testing). Prednost ovog pristupa je mogućnost
potpunog razdvajanja programera i testera i zato
ovo testiranje obično obavljaju testeri. Zadatak te-
stera je da sistemu pruži ulaze, a zatim da proveri
izlaze u odnosu na datu specifikacĳu.

Crna kutĳa

Ulaz

Izlaz

Slika 4.6: Testiranje crne kutĳe: fokus na ulazu i izlazu

Testiranje bele kutĳe (eng. white box testing) — generi-
sanje test primera na osnovu interne strukture i
logike koda. Alternativni nazivi za ovaj pristup su
strukturno testiranje (eng. structural testing) i testi-
ranje vođeno logikom (eng. logic driven testing), što
dodatno naglašava oslonac na logičku strukturu
koda i neophodnost poznavanja implementacĳe
radi pisanja testova za ovu vrstu testiranja. Zbog
toga testiranje bele kutĳe obično obavljaju progra-
meri tokom faze razvoja softvera. Primer testiranja
bele kutĳe su testovi jedinica koda u kojima se pro-
verava ispravnost najmanjih funkcionalnih delova
softvera.

Bela kutĳa

Ulaz

Izlaz

Slika 4.7: Testiranje bele kutĳe: fokus na strukturi koda.

<!-- pdf_page=104 printed_page=90 -->

Testiranje sive kutĳe (eng. gray box testing) — pred-
stavlja prelaz između tehnika crne i bele kutĳe
(mešovita strategĳa). Kod ove tehnike postoji uvid
u unutrašnju strukturu sistema, ali ne u toj meri
kao kod tehnika bele kutĳe. Koristi se, na primer,
kod komponentnog i integracionog testiranja. Ovo
je tehnika koju koriste i programeri i testeri.

Siva kutĳa

Ulaz

Izlaz

?

Slika 4.8: Testiranje sive kutĳe: mešovita strategĳa.

Problem proročišta

Prethodne tehnike testiranja podrazumevaju da je za
ulazne vrednosti moguće jednostavno odrediti odgova-
rajuće izlazne vrednosti. Međutim, to ne mora da bude
slučaj za sve softverske sisteme. Preciznĳe, proročište
(eng. test oracle) je mehanizam (ili znanje) koje omogu-
ćava testeru da odredi: „Očekivani rezultat za ulaz U
je izlaz I“ i da uporedi stvarni izlaz sa tim očekivanim.
Kada takav mehanizam ne postoji ili ga je teško defini-
sati, dolazi do problema proročišta. Problem proročišta
(eng. oracle problem) u testiranju softvera odnosi se na iza-
zov određivanja da li je rezultat testa ispravan — tj. kako
sa sigurnošću znati da je izlaz sistema za određeni ulaz
tačan. Problem proročišta je izražen u oblastima kao
što su računarska grafika, konstrukcĳa kompilatora i
mašinsko učenje.

<!-- pdf_page=105 printed_page=4 -->

Primer 4.3.2 (C kompajler) U razvoju kompajlera za
programski jezik C potrebno je da proverimo da li
kompajler ispravno prevodi programe. Test bi trebalo
da proveri da li je kompajler:

▶ispravno generisao mašinski kôd koji odgovara
očekivanom izvršavanju programa (zadržao je
semantiku izvornog programa),

▶ispravno optimizovao kôd (npr. eliminisao su-
višne promenljive).

Međutim

▶Najčešće ne postoji formalna specifikacĳa očeki-
vanog izlaza za proizvoljan ulazni program.

▶Ručna provera mašinskog koda ili ponašanja
može biti izuzetno teška i podložna greškama.

▶Automatizovana provera semantičke ekvivalen-
cĳe dva programa (izvorni i prevedeni) je u
opštem slučaju nerešiv problem.

Problem proročišta se rešava na različite načine.

▶Korišćenje alternativnih implementacĳa kao upo-
rednog standarda ili upotreba ranĳih verzĳa sof-
tvera kao referentnog ponašanja (onda kada su
ranĳe verzĳe softvera dostupne). Ukoliko su re-
zultati različiti, onda bar jedna od implementacĳa
ima grešku.

▶Metamorfno testiranje — ne proverava se konkre-
tan izlaz, već odnos između više izlaza koji se
računa na osnovu odnosa između ulaza i osobina
algoritma koji se testira.

Primer 4.3.3 (C kompajler — nastavak primera 4.3.2)
Jedan praktičan pristup prevazilaženju problema pro-
ročišta kod kompajlera je tzv. diferencĳalno testiranje:

▶Kôd se prevede pomoću više različitih kompaj-
lera (ili različitih verzĳa istog kompajlera),

<!-- pdf_page=106 printed_page=92 -->

Dĳagrami
stanja

Osnovne
putanje

Siva kutĳa

Tabele
odluči-
vanja

Tok
podataka

Crna kutĳa

Bela kutĳa

Tehnika
graničnih
vrednosti

Prolasci
kroz petlje

Tehnika
klasa ekvi-
valencĳe

Tehnike testiranja

Slika 4.9: Tehnike testiranja softvera

▶Izvrše se sve dobĳene verzĳe izvršivog koda u
kontrolisanom okruženju,

▶Ako svi rezultati izvršavanja daju isti izlaz, pret-
postavlja se da su tačni.

Jasno je da se čak i tada ne može sa sigurnošću tvrditi
da je rezultat ispravan, iz više razloga. Najpre, provera
je urađena samo na nekim konkretnim ulazima i za te
ulaze je utvrđeno da se različiti kompajleri isto pona-
šaju. Za neke druge ulaze možda bismo dobili razliku
u ponašanju. Dodatno, moguće je i da svi kompajleri
koji učestvuju u poređenju daju istu grešku.

Korišćenje različitih implementacĳa se ne može uvek
primeniti pošto često ne postoji više implementacĳa
istog algoritma (jer su te implementacĳe previše skupe
i zahtevaju puno vremena). Takođe, ako se različite
implementacĳe kreiraju od strane istih ljudi, moguće je
da oni prave iste greške.

4.3.3 Testiranje crne kutĳe

Testiranje crne kutĳe teorĳski se može uraditi isprobava-
njem svih mogućih ulaza (eng. exhaustive input testing).

<!-- pdf_page=107 printed_page=4 -->

Međutim, već za trivĳalne programe nĳe moguće kori-
stiti ovu tehniku.

Primer 4.3.4 (Kvadratna jednačina) Data kvadratna
jednačina
𝑎· 𝑥2 + 𝑏· 𝑥+ 𝑐= 0

ima rešenje

𝑥1,2 = −𝑏±
√

𝑏2 −4 · 𝑎· 𝑐
2 · 𝑎

Ako su koeficĳenti jednačine celobrojni i tipa int32
onda je broj različitih test primera za potpuno testira-
nje
232 · 232 · 232 = 296

Dodatno, pored isprobavanja svih mogućih ispravnih
vrednosti ulaza, potrebno je razmotriti i moguće nei-
spravne ulaze kojih takođe može biti mnogo.

Primer 4.3.5 Neispravan ulaz za očekivanu starost
osobe može da bude negativan broj ili unos neke
proizvoljne reči umesto broja. Očekivano ponašanje
softvera u takvim situacĳama može da bude signali-
ziranje greške korisniku sa mogućnošću unosa nove
vrednosti ili prekid rada softvera uz odgovarajuću
poruku.

Cilj tehnika testiranja crne kutĳe je da pronađu prihva-
tljiv broj test slučajeva (tj. kombinacĳa ulaza) koji od-
govara reprezentativnom skupu testova. Test slučajevi
mogu se podeliti u dve osnovne kategorĳe: test slučajevi
koji odgovaraju validnim ulazima i test slučajevi koji
odgovaraju nevalidnim ulazima.

Primer 4.3.6 (Kvadratna jednačina — nastavak prime-
ra 4.3.4.) Test slučaj koji odgovara ispravnom ulazu
za kvadratnu jednačinu može da sadrži ulazne vred-

<!-- pdf_page=108 printed_page=94 -->

nosti {1, -3, 2} i izlazne vrednosti {1, 2}. Test slučaj koji
odgovara neispravnom ulazu može da sadrži ulazne
vrednosti {"I", -3, 2} i izlaznu vrednost {"Neispravan
unos prvog koeficĳenta"}

Pronalaženje reprezentativnog skupa testova metoda-
ma crne kutĳe se ostvaruje postavljanjem odgovarajućih
pretpostavki o softveru koji treba da se testira. Najpo-
znatĳi tehnike obuhvataju tehniku klasa ekvivalencĳe,
tehniku graničnih vrednosti, tabele odlučivanja i dĳa-
grame stanja.

tehnike testiranja

testiranje
crne kutĳe

klase ekvi-
valencĳe

Klase ekvivalencĳe

granične
vrednosti

Testiranje pomoću klasa ekvivalencĳe (eng. equivalence
class testing) je tehnika koja se koristi da smanji broj test
slučajeva na prihvatljiv nivo, a da se pri tome zadrži
zadovoljavajuća pokrivenost ulaznog prostora podata-
ka. Klase ekvivalencĳe predstavljaju skupove ulaznih
podataka koji se obrađuju na isti način od strane sistema.
One se mogu podeliti na validne (ispravne) i nevalidne
(neispravne) klase, u zavisnosti od toga da li bi sistem
trebalo da prihvati te vrednosti za dalju obradu ili ih
odbaci.

tabele odlu-
čivanja

dĳagrami stanja

tabele stanja

Primer 4.3.7 (Validne i nevalidne klase) Ukoliko se
očekuje da korisnik unese broj godina između 18 i 65,
validne klase bi pokrivale sve vrednosti unutar tog
opsega, dok bi nevalidne klase uključivale vrednosti
ispod 18 i iznad 65.

tehnike testiranja

Ova tehnika se zasniva na pretpostavci da se sve vred-
nosti unutar jedne klase ponašaju identično u kontekstu
testiranja, te je dovoljno izabrati po jednog predstav-
nika iz svake klase. Preciznĳe, pretpostavke za klase
ekvivalencĳe su:

testiranje
crne kutĳe

klase ekvi-
valencĳe

▶Ukoliko jedan test slučaj iz određene klase ekvi-
valencĳe otkrĳe grešku, velika je verovatnoća da

<!-- pdf_page=109 printed_page=4 -->

bi i svi ostali test slučajevi iz iste klase otkrili istu
tu grešku.

▶Ukoliko jedan test slučaj iz određene klase ekvi-
valencĳe ne otkrĳe grešku, pretpostavlja se da ni
ostali test slučajevi iz te klase ne bi otkrili grešku.

Na osnovu ovih pretpostavki, testiranje se može raci-
onalizovati izborom po jednog predstavnika iz svake
klase. Ključni koraci primene ove tehnike su:

1. Identifikovati sve validne klase ekvivalencĳe za
ulazne vrednosti koje bi sistem trebalo da prihvati
za dalju obradu.

2. Izabrati po jedan test slučaj za svaku validnu
klasu.

3. Identifikovati nevalidne klase ekvivalencĳe za
ulazne vrednosti koje bi sistem trebalo da odbaci.

4. Izabrati po jedan test slučaj za svaku nevalidnu
klasu.

Na taj način se smanjuje broj potrebnih testova, a da
se pritom zadrži visok nivo pokrivenosti funkcionalnih
pravila sistema i otkrivanja potencĳalnih grešaka.

Primer 4.3.8 (Zapošljavanje na osnovu starosti) Pret-
postavimo da sistem za zapošljavanje sprovodi pravila
na osnovu starosti kandidata. Pravila su definisana
narednom tabelom:

Godine
Pravilo

0–16
Ne zaposliti
16–18
Može se zaposliti samo sa pola
radnog vremena
18–55
Može se zaposliti sa punim rad-
nim vremenom
55–99
Ne zaposliti

Validne klase ekvivalencĳe:

▶V1 — Godine u opsegu 0–16 (npr. 10)

<!-- pdf_page=110 printed_page=96 -->

▶V2 — Godine u opsegu 16–18 (npr. 17)
▶V3 — Godine u opsegu 18–55 (npr. 30)
▶V4 — Godine u opsegu 55–99 (npr. 70)

Nevalidne klase ekvivalencĳe:

▶I1 – Vrednost ispod minimalne vrednosti
(npr. −5)

▶I2 – Vrednost iznad maksimalne vrednosti
(npr. 105)

Test slučajevi:

ID
Klasa
Ulaz
Očekivani rezultat

TC1
V1
10
Ne zaposliti
TC2
V2
17
Zapošljavanje sa pola
radnog vremena
TC3
V3
30
Zapošljavanje sa punim
radnim vremenom
TC4
V4
70
Ne zaposliti
TC5
I1
−5
Odbiti unos
TC6
I2
105
Odbiti unos

Korišćenjem tehnike klasa ekvivalencĳe, broj test slu-
čajeva za ispravne unose se smanjuje sa 100 (po jedan
za svaku validnu godinu) na svega nekoliko repre-
zentativnih testova, uz zadržavanje pokrivenosti svih
funkcionalnih pravila sistema.

Napomena: Često je lakše identifikovati validne klase
ekvivalencĳe od nevalidnih. Na primer, pored neva-
lidnih unosa -5 i 105, potrebno je testirati i nevalidne
unose kao što je unos izraza koji vodi neispravnom
broju (npr. 66+35), unos slova i nenumeričkih karak-
tera i slično.

Granične vrednosti

Testiranje pomoću klasa ekvivalencĳe predstavlja osnov-
nu tehniku za oblikovanje test slučajeva. Međutim, u
praksi se pokazalo da se veliki broj grešaka javlja upravo

<!-- pdf_page=111 printed_page=4 -->

na granicama definisanih klasa. Odatle potiče ideja o
dodatnoj tehnici: testiranju graničnih vrednosti (eng. bo-
undary value testing).

tehnike testiranja

Ova tehnika fokusira se na vrednosti koje se nalaze na sa-
mim granicama, neposredno ispod i neposredno iznad
granica klasa ekvivalencĳe, jer upravo na tim mestima
programeri najčešće prave greške. Tipična greška je po-
grešno upisivanje operatora nejednakosti, na primer
korišćenje znaka > umesto znaka ≥(ili obratno).

testiranje
crne kutĳe

granične
vrednosti

Primetimo da su termini ispod i iznad relativni pojmo-
vi koji zavise od tipa i preciznosti vrednosti koje se
testiraju. Na primer, kod celobrojnih vrednosti, to su
uzastopni brojevi (𝑛−1 i 𝑛+1, ukoliko je 𝑛granica), dok
kod realnih brojeva razlika može biti definisana brojem
značajnih decimala. Dodatna složenost se javlja kada
postoje višedimenzionalni ulazi (npr. dve povezane nu-
meričke vrednosti) ili kada se radi sa realnim brojevima
visoke preciznosti. U takvim slučajevima, identifikacĳa
relevantnih granica i test tačaka zahteva dodatnu pažnju
i detaljnĳu analizu.

Osnovni koraci za primenu testiranja graničnih vredno-
sti su sledeći:

1. Identifikovati klase ekvivalencĳe na osnovu ula-
znih podataka.

2. Odrediti tačne granice svake identifikovane klase.
3. Za svaku granicu, definisati sledeće test tačke:

▶tačku na samoj granici,
▶tačku neposredno ispod granice,
▶tačku neposredno iznad granice.

Važno je imati u vidu da tačke koje se nalaze ispod i
iznad granice mogu da pripadaju klasama ekvivalencĳe
koje su već obuhvaćene testovima. Zbog toga treba paziti
da se testovi ne dupliraju kada se kombinuje testiranje
graničnih vrednosti sa testiranjem klasa ekvivalencĳe.

<!-- pdf_page=112 printed_page=98 -->

Primer 4.3.9 (Zapošljavanje na osnovu starosti — na-
stavak primera 4.3.8) Prilikom analize graničnih vred-
nosti, uočava se problem u specifikacĳi sistema na
granicama klasa ekvivalencĳe. Naime, vrednosti 16,
18 i 55 pojavljuju se u više klasa, što dovodi do pre-
klapanja. Na primer, jedno pravilo navodi da osobe
stare 16 godina ne treba zaposliti, dok drugo pravilo
ističe da se takve osobe mogu zaposliti sa pola radnog
vremena. Ovakvo preklapanje ukazuje na grešku u
specifikacĳi koju je neophodno ispraviti.

Ispravna verzĳa tabele, koja eliminiše ova preklapanja,
prikazana je u nastavku:

Godine
Pravilo

0–15
Ne zaposliti
16–17
Može se zaposliti samo sa pola
radnog vremena
18–54
Može se zaposliti sa punim rad-
nim vremenom
55–99
Ne zaposliti

Na osnovu nje možemo da definišemo slične validne
klase ekvivalencĳe i njihove predstavnike.

Validne klase ekvivalencĳe:

▶V1 — Godine u opsegu 0–15 (npr. 10)
▶V2 — Godine u opsegu 16–17 (npr. 17)
▶V3 — Godine u opsegu 18–54 (npr. 30)
▶V4 — Godine u opsegu 55–99 (npr. 70)

Dalje, na osnovu definisanih klasa ekvivalencĳe, mo-
žemo definisati odgovarajuće vrednosti na granicama:

▶Granica 0: {0, 1}
▶Granica 15: {14, 15, 16}
▶Granica 16: {15, 16, 17}
▶Granica 17: {16, 17, 18}
▶Granica 18: {17, 18, 19}

<!-- pdf_page=113 printed_page=4 -->

▶Granica 54: {53, 54, 55}
▶Granica 55: {54, 55, 56}
▶Granica 99: {98, 99, 100}

Unĳa svih ovih skupova daje sledeće test vrednosti:

{0, 1, 14, 15, 16, 17, 18, 19, 53, 54, 55, 56, 98, 99, 100}

Zajedno sa vrednostima identifikovanim za same
klase ekvivalencĳe, to čini skup

{0, 1, 10, 14, 15, 16, 17, 18, 19, 30, 53, 54, 55, 56, 70, 98,
99, 100}

Međutim, sada imamo preklapanja unutar istih klasa
ekvivalencĳe, i neke vrednosti mogu biti redundantne.
Na primer, vrednosti 0, 1, 10, 14 i 15 pripadaju istoj
klasi 0–15, dok su 18, 19, 30, 53 i 54 sve iz klase 18–
54. Testove koji pripadaju istoj klasi ekvivalencĳe, a
nisu granične vrednosti moguće je po potrebi ukloniti
u cilju smanjivanja troškova testiranja, bez gubitka
pokrivenosti.

Tabele odlučivanja

Tabela odlučivanja (eng. decision table) pruža pregled
složenih poslovnih pravila u strukturisanom i lako či-
tljivom obliku. One predstavljaju snažno sredstvo za
analizu i dizajn test scenarĳa u složenim informacio-
nim sistemima. Često se koriste u testiranju softvera za
sistematsko generisanje test slučajeva, naročito u situaci-
jama kada postoji veći broj kombinacĳa ulaznih uslova i
očekivanih akcĳa.

tehnike testiranja

Tabela odlučivanja je organizovana u redove i kolone.
Redovi se dele u dve grupe: prvu grupu čine uslovi
nad ulazima, dok drugu grupu čine moguće akcĳe
koje sistem treba da izvrši. Kolone predstavljaju pravi-
la — svaka kolona odgovara jedinstvenoj kombinacĳi
vrednosti uslova i opisuje koje se akcĳe u tom slučaju
preduzimaju.

testiranje
crne kutĳe

tabele odlu-
čivanja

<!-- pdf_page=114 printed_page=100 -->

Uslovi mogu biti binarni (na primer, da/ne, istina/laž)
ili viševrednosni (na primer, malo/srednje/veliko). Kada
su uslovi binarni, iz svakog pravila se obično izvodi
jedan test slučaj. Kod viševrednosnih uslova može se
izvesti više test slučajeva, u zavisnosti od željenog nivoa
pokrivenosti.

U slučajevima kada više pravila dovode do iste akcĳe,
bez obzira na vrednost nekog uslova, moguće je izvršiti
objedinjavanje pravila (eng. table collapsing). U takvim
slučajevima, uslov koji ne utiče na ishod označava se
simbolom „—” (crtica) i naziva se nebitnim (eng. don’t
care).

Test slučajevi izvedeni iz tabele odlučivanja mogu se
dodatno kombinovati sa drugim tehnikama testiranja,
kao što su testiranje pomoću klasa ekvivalencĳe ili te-
stiranje graničnih vrednosti. Ova kombinacĳa povećava
preciznost i efektivnost testiranja.

Primer 4.3.10 (Bankomat) Klĳent zahteva isplatu go-
tovine na bankomatu. Sistem treba da odluči da li će
da odobri isplatu. Odlučivanje vrši pomoću podata-
ka o sredstvima na računu i o dozvoljenom minusu.
Način odlučivanja je prikazan narednom tabelom.

Pravilo 1
Pravilo 2
Pravilo 3

Uslovi
Dovoljno sredstava na računu
Da
Ne
Ne
Dozvoljen minus
—
Da
Ne
Akcĳe
Isplata odobrena
Da
Da
Ne

Prvo pravilo je dobĳeno spajanjem dva pravila: kada
ima dovoljno sredstava na računu, nezavisno od toga
da li je minus dozvoljen ili ne, isplata se odobrava. Iz
drugog pravila može se izvesti test slučaj tako što se
za ulaz uzme da korisnik nema dovoljno sredstava na
računu i da mu je dozvoljen minus. Zatim se izlaz iz
programa poredi sa očekivanom akcĳom, a to je da
je isplata odobrena. Iz trećeg pravila može se izvesti
test slučaj za koji isplata nĳe odobrena.

<!-- pdf_page=115 printed_page=4 -->

Dĳagrami stanja

Sistemi koji reaguju na spoljašnje događaje i čĳe ponaša-
nje zavisi od prethodno izvršenih akcĳa mogu se efika-
sno modelovati pomoću konačnih automata (eng. finite
state machines). U svakom trenutku, takav sistem se
nalazi u jednom od konačno mnogo mogućih stanja i
pasivno čeka na neki ulazni događaj. Kada se dogodi
odgovarajući događaj, sistem, u zavisnosti od trenutnog
stanja, prelazi u novo stanje. Tokom ovog prelaza često
se izvršava i određena akcĳa, kao što je generisanje
izlaza, slanje poruke ili promena internog podatka.

Jedan od najvažnĳih načina prikaza konačnog automa-
ta u inženjerskoj praksi je dĳagram stanja (eng. state-
transition diagram). Ovaj dĳagram kompaktno i pregled-
no opisuje složene zahteve sistema i njegov način in-
terakcĳe sa spoljašnjim svetom. Posebno se koristi za
modelovanje sistema čĳe ponašanje zavisi od sekvence
prethodnih događaja.

tehnike testiranja

Osnovni elementi dĳagrama stanja prikazani su na
slici 4.10 i uključuju:

testiranje
crne kutĳe

Stanje — Predstavlja određeno ponašanje ili konfigura-
cĳu sistema; čuva informacĳu o prošlim događaji-
ma i određuje reakcĳu na buduće.

dĳagrami stanja

Prelaz — Predstavlja promenu iz jednog stanja u drugo,
iniciranu događajem.

Događaj — Spoljašnji ili unutrašnji signal koji izaziva
prelaz između stanja.

Akcĳa — Operacĳa koju sistem izvršava kao odgovor
na prelaz, kao što su promene izlaza, logovanje ili
pozivi metoda.

Dĳagram stanja omogućava vizuelizacĳu svih mogućih
stanja sistema, događaja koji uzrokuju promene stanja,
kao i pratećih akcĳa. Ova tehnika je široko rasprostra-
njena u razvoju softverskih komponenti koje zahtevaju
precizno definisano ponašanje u skladu sa spoljašnjim

<!-- pdf_page=116 printed_page=102 -->

Događaj/Akcĳa

Stanje 1
Stanje 2

Slika 4.10: Prikaz prelaza u
okviru dĳagrama stanja

stimulusima, kao što su korisnički interfejsi, komunika-
cioni protokoli i kontrolni sistemi.

Pored modelovanja ponašanja, dĳagram stanja može
se koristiti i za generisanje test slučajeva. Budući da
je dĳagram stanja oblik usmerenog grafa, testiranje se
može zasnivati na njegovom obilasku. Na primer, može-
mo zahtevati da svaki prelaz u dĳagramu bude ispitan
bar jednom — što predstavlja dobar kompromis izme-
đu pokrivenosti i obima testova. Alternativno, može
se zahtevati pokrivenost svih stanja ili čak svih mo-
gućih putanja kroz dĳagram, u zavisnosti od ciljeva i
kritičnosti sistema.

Primer 4.3.11 (Ugrađena kasa) Posmatramo softverski
sistem za maloprodaju koji ima ugrađenu opcĳu za
otvaranje i zatvaranje (fioke) kase prikazan na slici
4.11. Primeri test slučajeva

1. Otvori, zatvori, ugasi program

2. Otvori, otvori, zatvori, zatvori, ugasi program.

Drugi test slučaj aktivira svaki prelaz datog dĳagra-
ma bar jednom. Pri izvršavanju navedenih naredbi
proverava se da li sistem reaguje u skladu sa zadatim
zahtevima.

tehnike testiranja

testiranje
crne kutĳe

Tabele stanja

Konačni automat koji modeluje sistem se može prikazati
i tabelama stanja (eng. state transition tables). Osnovna

tabele stanja

<!-- pdf_page=117 printed_page=4 -->

Zatvori

Otvori

Otvori/Obavesti

Zatvorena
Otvorena

Zatvori/Obavesti

Ugasi
program

Slika 4.11: Dĳagram stanja za
ugrađenu kasu

prednost tabela stanja jeste njihov sistematični pristup
jer prikazuju sve moguće kombinacĳe stanja i događaja.
Takvim pristupom mogu da se uoče situacĳe u kojima
ponašanje sistema nĳe definisano, što može da spreči
pojavu grešaka. Kod tabela stanja, iz svakog reda se
može direktno izvesti jedan test slučaj. Tabele stanja
postaju nepraktične ukoliko postoji veliki broj mogućih
stanja i događaja.

Primer 4.3.12 (Ugrađena kasa — nastavak primera
4.3.11) Tabela stanja za ugrađenu kasu prikazana je u
narednoj tabeli.

Trenutno stanje
Događaj
Akcĳa
Naredno stanje

Zatvorena
otvori
obavesti
Otvorena
Zatvorena
zatvori
-
Zatvorena
Zatvorena
ugasi program
-
Zatvorena
Otvorena
otvori
-
Otvorena
Otvorena
zatvori
obavesti
Zatvorena
Otvorena
ugasi program
-
Nedefinisano

Na osnovu tabele možemo lako da uočimo da postoji
test slučaj za koje stanje nĳe definisano. To je test slučaj
koji odgovara situacĳi u kojoj korisnik sistema želi
da ugasi program, a kasa nĳe zatvorena (poslednji
red tabele). Mogućnost ostavljanja otvorene kase nĳe
očigledna na dĳagramu stanja 4.11, ali jeste u tabeli

<!-- pdf_page=118 printed_page=104 -->

stanja. Moguća rešenja su da sistem upozori korisnika
i spreči zatvaranje programa ili da automatski zatvori
kasu.

4.3.4 Testiranje bele kutĳe

tehnike testiranja

Testiranje bele kutĳe podrazumeva detaljno poznavanje
unutrašnje strukture softverskog sistema. Test slučajevi
se kreiraju na osnovu analize izvornog koda, pri čemu se
posebno proučava tok izvršavanja programa. Najčešće
ih izrađuju sami programeri tokom razvoja, ali ih mogu
pisati i iskusni test inženjeri koji imaju pristup kodu i
razumevanje implementacĳe.

testiranje
bele kutĳe

Zbog potrebe za dubinskim uvidom u rad sistema,
testiranje bele kutĳe je zahtevnĳe i skuplje u poređenju
sa tehnikama crne kutĳe. Zato se najčešće primenjuje u
sistemima za koje je potrebna visoka pouzdanost i gde
su softverske greške posebno skupe.

Cilj ovog testiranja je ispitivanje različitih putanja kroz
kôd programa. Putanja (eng. execution path) predstavlja
konkretan niz naredbi koje se izvršavaju tokom jednog
prolaska kroz program, u zavisnosti od ulaznih podata-
ka i kontrole toka programa. Ključni elementi koji utiču
na formiranje putanja su:

▶uslovna grananja (na primer, naredbe if i switch),
▶petlje (na primer, naredbe while, for i do-while),
▶skokovi (na primer, break, continue, return i

goto),

▶pozivi funkcĳa,
▶izuzeci i obrada izuzetaka (na primer, naredbe

try, catch i finally).

Primer 4.3.13 (Funkcĳa pozitivni) Posmatrajmo kôd
funkcĳe koja proverava da li je broj pozitivan.

1 int pozitivni(int a) {

2
if (a > 0)

3
return 1;

<!-- pdf_page=119 printed_page=4 -->

4
return 0;

5 }

Ova funkcĳa ima dve putanje. Prva putanja nakon pro-
vere uslova a > 0 (linĳa 2) izvršava naredbu return

1 (linĳa 3). Druga putanja nakon provere uslova a >

0 (linĳa 2) izvršava naredbu return 0 (linĳa 3).

Analogno ispitivanju svih kombinacĳa ulaza kod tehni-
ka zasnovanih na modelu crne kutĳe, može se zahtevati
ispitivanje svih putanja kroz program. Međutim, zbog
eksponencĳalnog rasta broja mogućih putanja sa po-
rastom složenosti programa, potpuno testiranje svih
putanja je u praksi najčešće neizvodljivo.

Primer 4.3.14 (Funkcĳa pozitivni — nastavak prime-
ra 4.3.13) Posmatrajmo kôd funkcĳe koja za tri broja
računa koliko njih je pozitivno.

1 int pozitivni(int a1, int a2, int a3) {

2
int brojPozitivnih = 0;

3
if (a1 > 0)

4
brojPozitivnih++;

5
if (a2 > 0)

6
pozitivan++;

7
if (a3 > 0)

8
brojPozitivnih++;

9
return brojPozitivnih;

10 }

Broj putanja kroz ovaj program je 23, jer za svaku
od tri naredbe grananja imamo opcĳu izvršavanja
ukoliko je uslov ispunjen i ukoliko nĳe. Konkretno, to
su putanje koje prolaze kroz naredne linĳe koda:

1. 1, 2, 3, 4, 5, 6, 7, 8, 9

2. 1, 2, 3, 4, 5, 6, 7,
9

3. 1, 2, 3, 4, 5,
7, 8, 9

4. 1, 2, 3, 4, 5,
7,
9

5. 1, 2, 3,
5, 6, 7, 8, 9

6. 1, 2, 3,
5, 6, 7,
9

7. 1, 2, 3,
5,
7, 8, 9

8. 1, 2, 3,
5,
7,
9

<!-- pdf_page=120 printed_page=106 -->

Primer 4.3.15 (Funkcĳa pozitivni — nastavak pri-
mera 4.3.14) Posmatrajmo kôd funkcĳe koja za niz od
100 brojeva računa koliko njih je pozitivno.

1 int pozitivni(int a[], int n) {

2
int i = 0, brojPozitivnih = 0;

3
while (i < n) {

4
if (a[i] > 0)

5
brojPozitivnih++;

6
}

7
return brojPozitivnih;

8 }

Broj putanja kroz ovaj program je 2100, jer za svaku
naredbu grananja imamo opcĳu izvršavanja ukoliko
je uslov ispunjen i ukoliko nĳe. Bez pretpostavke
da niz ima tačno 100 elemenata, broj putanja kroz
ovu funkcĳu zavisi od veličine niza 𝑛i iznosi 2𝑛za
fiksiranu vrednost 𝑛.

Primer 4.3.16 (Funkcĳa pozitivni — nastavak prime-
ra 4.3.15) Posmatrajmo kôd funkcĳe koja za vrednosti
koje se unose sa standardnog ulaza (sve do unosa
broja nula) računa koliko njih je pozitivno.

1 int pozitivni() {

2
int broj, brojPozitivnih = 0;

3
do {

4
scanf("%d", &broj);

5
if (broj > 0)

6
brojPozitivnih++;

7
} while (broj!=0);

8
return brojPozitivnih;

9 }

Broj putanja kroz ovaj program zavisi od broja unetih
elemenata sa standardnog ulaza i nĳe ograničen.

Zbog velikog broja mogućih putanja i kroz jednostavne
programe, umesto testiranja svih mogućih putanja, ko-
riste se metrike pokrivenosti koda kako bi se obezbedio
balans između kvaliteta i troškova testiranja. Pre počet-
ka testiranja, treba odrediti odgovarajući nivo i vrstu

<!-- pdf_page=121 printed_page=4 -->

pokrivenosti. Osnovni koraci u testiranju bele kutĳe
su:

1. Analiza i razumevanje strukture i logike izvornog
koda;

2. Kreiranje test primera na osnovu

a) identifikovanih relevantnih putanja i

b) odabranih metrika pokrivenosti;

3. Izvršavanje test primera.

Metrike pokrivenosti koda

Metrike pokrivenosti koda predstavljaju važno sredstvo
za procenu kvaliteta testiranja softvera. One pomažu
u identifikacĳi delova sistema koji su testirani i onih
koji su ostali neprovereni, čime omogućavaju donošenje
informisanih odluka o daljem razvoju i unapređenju
testne infrastrukture. Metrike pokrivenosti koda koje se
najčešće koriste su pokrivenost putanja, naredbi, odluka,
uslova, višestrukih uslova i funkcĳa.

Pokrivenost putanja
=

Izvršenih putanja

Pokrivenost putanja (eng. path coverage) Mera koja po-
kazuje koliki je procenat putanja u programu koje
su izvršene tokom testiranja. Potpuna pokrivenost
znači da je svaka moguća putanja kroz program
izvršena bar jednom.

Ukupno putanja × 100%

Pokrivenost naredbi
=

Izvršenih naredbi

Pokrivenost naredbi (eng. statement coverage) Mera ko-
ja pokazuje koliki je procenat naredbi u programu
koje su izvršene tokom testiranja. Potpuna pokrive-
nost se postiže kada je svaka naredba u programu
izvršena bar jednom.

Ukupno naredbi × 100%

Pokrivenost odluka
=

Ispitanih odluka

Pokrivenost grana/odluka (eng. branch/decision covera-
ge) Mera koja pokazuje koliki je procenat ishoda
odluka testirano u odnosu na ukupan broj odlu-
ka u programu. Za potpunu pokrivenost, svaka
odluka u kodu mora biti evaluirana bar jednom
kao tačna i bar jednom kao netačna.

Ukupno odluka × 100%

<!-- pdf_page=122 printed_page=108 -->

Pokrivenost uslova (eng. condition coverage)‗ Mera koja
pokazuje koliki je procenat pojedinačnih logičkih
uslova unutar složenĳih izraza (npr. A && B) do-
bio i tačnu i netačnu vrednost tokom testiranja. Za
potpunu pokrivenost, svaki uslov u svakoj odluci
u kodu mora biti evaluiran bar jednom kao tačan
i bar jednom kao netačan.

Pokrivenost uslova
=

Ispitanih uslova

Ukupno uslova × 100%

Pokrivenost višestrukih uslova (eng. multiple conditi-
on coverage) Mera koja pokazuje koliki je proce-
nat mogućih kombinacĳa vrednosti pojedinačnih
uslova u okviru svake odluke izvršen tokom te-
stiranja. Za potpunu pokrivenost, svaka moguća
kombinacĳa vrednosti pojedinačnih uslova za sva-
ku odluku mora biti izvršena bar jednom.

Pokrivenost višestrukih uslova =

Izvršenih kombinacĳa viš. uslova

Ukupno kombinacĳa viš. uslova

×100%

Pokrivenost funkcĳa (eng. function coverage) Mera ko-
ja pokazuje koliki je procenat funkcĳa izvršen
tokom testiranja. Za potpunu pokrivenost, potreb-
no je obezbediti da je svaka funkcĳa bar jednom
pozvana.

Pokrivenost funkcĳa
=

Izvršenih funkcĳa

Ukupno funkcĳa × 100%

Pokrivenost funkcĳa je korisna za osnovnu proveru
testne infrastrukture. Ukoliko neka funkcĳa nĳe nikada
pozvana tokom testiranja, to znači da taj deo softvera
nĳe uopšte pokriven testovima, što može ukazivati na
potencĳalne rizike ili nepotrebni (mrtvi) kod.

Najčešće korišćena metrika u praksi je pokrivenost na-
redbi. Ova metrika je jednostavna za implementacĳu i
brzo se izračunava prilikom pokretanja testova pa je nje-
no izračunavanje podržano u okviru većine modernih
razvojnih okruženja. Međutim, pokrivenost naredbi ne
odražava složenost logike programa i ne garantuje da
su sve bitne situacĳe obuhvaćene testovima.

Za detaljnĳu analizu ponašanja softvera, neophodno je
koristiti naprednĳe metrike, kao što je metrika pokrive-
nosti grana/odluka. Pokrivenost grana pruža uvid u to
da li su testovi prošli kroz sve moguće logičke tokove.

‗ Za lakše razumevanje razlika između pokrivenosti odluka, uslova
i višestrukih uslova, pogledati primer 4.3.18.

<!-- pdf_page=123 printed_page=4 -->

Primer 4.3.17 (Maksimalna vrednost) Razmotrimo
naredni kôd

1 max = b;

2 if (a > max) {

3
max = a;

4 }

Test {a=6, b=3} pokriva sve naredbe (izvršavanje pro-
lazi kroz naredbe 1, 2, 3 i 4), ali ne i sve putanje
(nedostaje putanja 1, 2, 4) kao ni sve odluke (odluka
u linĳi 2 se razmatra samo kao tačna, ne i kao netačna).

Testovi {a=6, b=3} i {a=3, b=6} pokrivaju i sve naredbe,
sve putanje i sve odluke. Dodati drugi test pokriva
putanju kroz linĳe 1, 2, 4. Odluka u linĳi 2 u ovom
testu ima vrednost netačno.

Međutim, za visokokvalitetno testiranje kao i za kritične
delove sistema, gde su greške neprihvatljive ili izuzetno
skupe, prati se pokrivenost putanja, uslova i višestrukih
uslova. Odabir odgovarajuće metrike treba da zavisi
od konteksta upotrebe softvera, njegove složenosti i
posledica potencĳalnih grešaka.

Primer 4.3.18 (Inkrementiranje pozitivnih brojeva)
Razmotrimo naredni kôd i njegovu pokrivenost testo-
vima.

1
if(a > 0 && b > 0) {

2
a++;

3
b++;

4
}

Test
{a=1, b=2}
pokriva sve naredbe ali

▶ne pokriva sve odluke — nedostaje odluka da
uslov 𝑎> 0 && 𝑏> 0 nĳe ispunjen,

▶ne pokriva sve uslove — nedostaje da su vred-
nosti oba podizraza netačne,

<!-- pdf_page=124 printed_page=110 -->

▶ne pokriva sve višestruke uslove — nedostaju još
tri kombinacĳe vrednosti podrizraza, tj. testovi
za koje su vrednosti podrizraza tačno-netačno,
netačno-tačno i netačno-netačno,

▶ne pokriva sve putanje — nedostaje putanje koja
prolazi samo kroz linĳu 1.

Testovi
{a=1, b=2} i
{a=-1, b=2}
pokrivaju sve naredbe, sve odluke i sve putanje, ali

▶ne pokrivaju sve uslove — nedostaje da je vred-
nost podizraza 𝑏> 0 netačna,

▶ne pokrivaju sve višestruke uslove — nedosta-
ju još dve kombinacĳe vrednosti podrizraza,
tj. testovi za koje su vrednosti podrizraza tačno-
netačno i netačno-netačno.

Testovi
{a=1, b=2},
{a=-1, b=2} i
{a=-1, b=-2}
pokrivaju sve naredbe, sve odluke, sve putanje i sve
uslove, ali ne pokrivaju sve višestruke uslove, nedo-
staje kombinacĳa vrednosti podizraza koja odgovara
vrednostima tačno-netačno. Testovi
{a=1, b=2},
{a=-1, b=2},
{a=-1, b=-2} i
{a=1, b=-2}
pokrivaju sve naredbe, sve odluke, sve putanje, sve
uslove i sve višestruke uslove.

Pokrivenost putanja

Pokrivenost odluka

Odnosi između različitih metrika

Pokrivenost naredbi

Potpuna pokrivenost naredbi podrazumeva potpunu
pokrivenost funkcĳa. Potpuna pokrivenost odluka pod-
razumeva potpunu pokrivenost naredbi, dok potpuna
pokrivenost putanja podrazumeva potpunu pokrivenost
odluka (slika 4.12).

Pokrivenost funkcĳa

Slika 4.12: Odnosi različitih
pokrivenosti počevši od pokri-
venosti putanja

<!-- pdf_page=125 printed_page=4 -->

Primer 4.3.19 (Apsolutne vrednosti) Potpuna pokri-
venost odluka ne podrazumeva potpunu pokrivenost
putanja. Na primer, razmotrimo naredni kôd.

1
if (a < 0) {

2
a = -a;

3
}

4
if (b < 0) {

5
b = -b;

6
}

Test {a=-6, b=-3} pokriva sve naredbe, ali ne pokriva
sve odluke niti sve putanje.

Testovi {a=-6, b=-3} i {a=6, b=3} pokrivaju sve naredbe
i sve odluke. Međutim, ne pokrivaju sve putanje.

Testovi {a=-6, b=-3}, {a=6, b=3}, {a=-6, b=3} i {a=6,
b=-3} pokrivaju sve naredbe, sve odluke i sve putanje.

Takođe, potpuna pokrivenost višestrukih uslova podra-
zumeva potpunu pokrivenost uslova i potpunu pokrive-
nost odluka (slika 4.13). Međutim, potpuna pokrivenost
uslova i višestrukih uslova nisu u nužnoj vezi sa potpu-
nom pokrivenošću putanja.

Pokrivenost višestrukih uslova

Primer 4.3.20 (Inkrementiranje pozitivnih brojeva —
nastavak primera 4.3.18) Razmotrimo naredni kôd i
njegovu pokrivenost testovima.

Pokrivenost uslova

1
if(a > 0 && b > 0) {

2
a++;

Pokrivenost odluka

3
b++;

4
}

Slika 4.13: Odnosi različitih
pokrivenosti vezanih za uslove
u grananjima

5
if(c > 0 && d > 0) {

6
c++;

7
d++;

8
}

Testovi
{a=1, b=2, c=3, d=4} i
{a=-1, b=2, c=-3, d=4}
pokrivaju sve naredbe i sve odluke (ali ne i sve uslove,

<!-- pdf_page=126 printed_page=112 -->

sve višestruke uslove ni sve putanje).

Testovi
{a=1, b=2, c=3, d=4} i
{a=-1, b=-2, c=-3, d=-4}
pokrivaju sve naredbe, sve odluke i sve uslove (ali ne
i sve višestruke uslove ni sve putanje).

Testovi
{a=1, b=2, c=3, d=4},
{a=1, b=-2, c=3, d=-4},
{a=-1, b=2, c=-3, d=4} i
{a=-1, b=-2, c=-3, d=-4}
pokrivaju sve naredbe, sve odluke, sve uslove i sve
višestruke uslove, ali ne i sve putanje.

Testovi
{a=1, b=2, c=3, d=4},
{a=1, b=2, c=-3, d=4},
{a=-1, b=2, c=3, d=4} i
{a=1, b=-2, c=3, d=-4}
pokrivaju sve naredbe, sve odluke, sve uslove i sve
putanje, ali ne i sve višestruke uslove.

Preporučeni nivo pokrivenosti

U praksi, pitanje „Koliki nivo pokrivenosti je dovoljno
dobar?“ nema univerzalni odgovor i zavisi od priro-
de softverskog sistema, njegovog konteksta upotrebe,
kritičnosti i ciljeva testiranja. Ipak, industrĳska praksa
pokazuje određene smernice koje se često koriste kao
polazna tačka.

Na primer, za pokrivenost naredbi, iako se potpuna
pokrivenost često postavlja kao cilj, kao preporučeni
prag navodi se nivo od 80% do 90%. Ova vrednost
predstavlja kompromis između efikasnosti testiranja
i troškova njegove realizacĳe. Važno je napomenuti
da čak i potpuna pokrivenost ne garantuje odsustvo
grešaka. Ona samo znači da je sav kôd bio izvršen tokom
testiranja, ali ne i da su obuhvaćeni svi logički putevi,

<!-- pdf_page=127 printed_page=4 -->

uslovi ili granični slučajevi, odnosno logički propusti i
dalje mogu ostati neprimećeni. Sa druge strane, nizak
nivo pokrivenosti jasno ukazuje na povišen rizik da
greške mogu ostati neotkrivene i sugeriše da značajni
delovi koda nisu uopšte testirani.

Pokrivenost koda testovima se menja tokom razvoja
softvera i dodavanja novih funkcionalnosti. Zbog toga je
potrebno redovno merenje i praćenje pokrivenosti koda
testovima.

Alati za merenje pokrivenosti koda

Alati za merenje pokrivenosti koda koriste se za ana-
lizu koji delovi izvornog koda su bili izvršeni tokom
testiranja. Oni predstavljaju ključnu podršku u proce-
su testiranja softvera, jer omogućavaju jasan uvid u to
koliko je testiranje temeljno.

Razlike u pokrivenosti koda
su značajne za razumevanje
kako dodavanje testova utiče
na pokrivenost. Master rad
Nikole Perića:
Alat za generisanje i prikaz
razlika u pokrivenosti koda
testovima

Većina alata funkcioniše na osnovu instrumentacĳe —
procesa u kojem se u kôd automatski umeću dodatne in-
strukcĳe koje beleže rezultate izvršavanja. Instrumenta-
cĳa može da se vrši pre ili za vreme procesa kompilacĳe,
kao i nakon kompilacĳe, na nivou bajtkoda (npr. za Java
programe) ili izvršivog formata (npr. za kompajlirane
C/C++ binarne fajlove).

Izvršavanjem instrumentovanog koda nad ulazima ko-
je određuju testovi, prikupljaju se podaci o tome koje
su linĳe, grane, uslovi ili funkcĳe izvršeni. Na osnovu
tih informacĳa generiše se izveštaj o pokrivenosti, koji
pomaže programerima da identifikuju nedovoljno testi-
rane delove sistema. Ovi izveštaji se često vizualizuju
kroz procente pokrivenosti i označene delove koda (npr.
bojama), kako bi se lakše uočili segmenti koji zahtevaju
dodatne testove.

<!-- pdf_page=128 printed_page=114 -->

Izbor relevantnih testova i putanja kroz program

Jedan od ključnih izazova u testiranju metodama bele
kutĳe jeste izbor odgovarajućih test primera. Dobar izbor
testova treba da obezbedi visok nivo pokrivenosti uz
minimalan broj test primera, čime se postiže efikasnost
i izbegava redundantnost.

U praksi, preporučuje se korišćenje više jednostavnih i
kratkih putanja koje se međusobno razlikuju u malim
detaljima, umesto jedne veoma složene putanje. Takav
pristup olakšava dĳagnostikovanje grešaka i održavanje
testova.

Primer 4.3.21 (Petlje) Petlje u kodu mogu potencĳal-
no generisati beskonačan broj putanja, pa je važno
odabrati reprezentativne slučajeve, kao što su:

▶Petlja se preskače (nula iteracĳa).
▶Petlja se izvršava jednom.
▶Petlja se izvršava dva puta.
▶Ako postoji poznat gornji limit 𝑛, izvršavanje
𝑛−1 i 𝑛puta.

Testiranje osnovnih putanja
(eng. basis path testing)
predstavlja tehniku kojom se osigurava da su sve logičke
grane u programu ispitane bar jednom. Ova tehnika se
zasniva na analizi grafa toka kontrole (eng. control flow
graph) i uključuje sledeće korake:

1. Izgradnja grafa kontrole toka programa iz posma-
tranog softverskog modula;

2. Izračunavanje ciklomatične kompleksnosti grafa†,
označene sa 𝐶;

† Ciklomatična kompleksnost je broj linearno nezavisnih putanja
kroz graf. Dve putanje su linearno nezavisne ako postoji bar jedna
grana koja se pojavljuje u jednoj putanji, a ne pojavljuje se u
drugoj. Ciklomatična kompleksnost se računa kao vrednost izraza
𝐸−𝑁+ 2𝑃gde je 𝐸broj grana u grafu, 𝑁broj čvorova grafa, a 𝑃
broj komponenti povezanosti grafa.

<!-- pdf_page=129 printed_page=4 -->

3. Odabir skupa od 𝐶linearno nezavisnih osnovnih
putanja;

4. Kreiranje test primera za svaku osnovnu putanju;
5. Izvršavanje testova i analiza rezultata.

Primena testiranja osnovnih putanja garantuje pokri-
venost svih naredbi i svih grana u kodu, jer je skup
osnovnih putanja konstruisan tako da pokriva svaki
čvor i svaku logičku odluku u grafu toka upravljanja.

Primer 4.3.22 (Osnovne putanje) Naredni graf odgo-
vara grafu kontrole toka programa P.

A

1
2

B

D

5
6

3
4

E

7

8

C

F

9
10

G

Ciklomatična kompleksnost za dati graf je 5, jer je

𝐶= 10 −7 + 2 = 5

Primenimo naredni algoritam odabira 5 linearno ne-
zavisnih osnovnih putanja. U svakom čvoru odluke
potrebno je promeniti odluku, počevši od poslednje
donete odluke. U skladu sa time, imamo naredne
putanje:

1. A, B, C, G

2. A, B, C, B, C, G
3. A, B, E, F, G
4. A, D, E, F, G
5. A, D, F, G

<!-- pdf_page=130 printed_page=116 -->

Glavni izazov ove tehnike leži u pretpostavci da su
sve osnovne putanje dostižne i izvodljive. U složenim
programima, određene putanje mogu biti logički ili
praktično nedostižne zbog međuzavisnosti uslova. Zbog
toga je neophodna pažljiva analiza grafa kontrole toka i
dodatna provera da izabrane putanje zaista odgovaraju
realnim scenarĳima izvršavanja.

Testiranje na osnovu grafa toka podataka
(eng. data
flow testing) ispituje ispravnost životnog ciklusa pro-
menljivih i upotrebe promenljivih u različitim delovima
programa. Tipične anomalĳe u upotrebi podataka uklju-
čuju:

▶Upotreba neinicĳalizovane promenljive – pro-
menljiva se koristi pre nego što joj je dodeljena
vrednost.

▶Neiskorišćena definicĳa – promenljiva je defini-
sana i inicĳalizovana, ali se nikada ne koristi.

▶Ponovno definisanje – promenljivoj se dodeljuje
nova vrednost pre nego što je prethodna upotre-
bljena.

▶Upotreba nakon oslobađanja resursa – promen-
ljiva (ili referenca) se koristi nakon dealokacĳe
memorĳe.

▶Neusaglašenost dodeljivanja i korišćenja u ra-
zličitim granama izvršavanja.

Cilj testiranja je osigurati da se sve promenljive koriste
na ispravan način — da su inicĳalizovane pre upotrebe,
iskorišćene nakon dodeljivanja i oslobođene samo kada
više nisu potrebne. Za to je potrebno u kodu identifiko-
vati mesta gde se promenljive definišu i gde se koriste,
i kreirati test primere koji pokrivaju tok izvršavanja
programa koji prolazi kroz date definicĳe i korišćenja.
Ova vrsta testiranja je naročito korisna za otkrivanje
suptilnih grešaka koje nisu nužno vidljive kroz stan-
dardne tehnike testiranja kontrole toka i često se koristi
u bezbednosno kritičnim i složenim sistemima.

<!-- pdf_page=131 printed_page=4 -->

4.3.5 Metamorfno testiranje

Metamorfno testiranje predstavlja tehniku testiranja sof-
tverskih sistema koja omogućava proveru ispravnosti
bez potrebe za proročištem — komponentom koja odre-
đuje da li je rezultat testa ispravan. Umesto toga, koristi
se poznavanje osobina sistema koji se testira, odnosno
metamorfna svojstava (relacĳe).

Metamorfna relacĳa izražava kako bi se izlaz programa
trebalo da promeni kada je ulaz izmenjen na određeni
način. Osnovna ideja je da se na osnovu dva ulaza koja
su u nekom specifičnom odnosu odredi odnos između
odgovarajućih izlaza.

tehnike testiranja

metamorfno
testiranje

Primer 4.3.23 (Standardna devĳacĳa) Ukoliko ne mo-
žemo da proverimo ispravnost rezultata za računanje
standardne devĳacĳe za veoma dugačak niz brojeva,
možemo da iskoristimo sledeće odnose (metamorfna
svojstva):

▶Permutacĳa elemenata ne utiče na standardnu
devĳacĳu.

▶Množenje svake vrednosti sa -1, ne utiče na
standardnu devĳacĳu.

▶Ako se svaki broj pomnoži sa nekom konstan-
tom, standardna devĳacĳa novog niza brojeva
bi trebalo da je srazmerna standardnoj devĳacĳi
originalnog niza.

Testiranjem se proverava da li se za zadate ulaze na
očekivani način menjaju izlazi. Testiranjem se detektuje
greška u sistemu ukoliko se javi odstupanje u očekiva-
nim odnosima između odgovarajućih izlaza.

Primer 4.3.24 (Standardna devĳacĳa — nastavak pri-
mera 4.3.23) Na osnovu identifikovanih metamorfnih
relacĳa za algoritam standardne devĳacĳe, možemo
da napravimo test primere koji su permutacĳa istog ni-

<!-- pdf_page=132 printed_page=118 -->

za brojeva i da proverimo da li svaki put dobĳemo isti
rezultat. Takođe, možemo da napravimo test primere
sa skaliranim vrednostima niza i da proverimo da li
za dobĳenu devĳacĳu važi da je skalirana u odnosu
na devĳacĳu originalnog niza. Na primer, možemo
da napravimo naredne testove:

▶Test 1: Proveriti za četiri permutacĳe istog niza
da li daju isti rezultat.

▶Test 2: Proveriti da li se dobĳa isti rezultat za
početni niz i za niz u kojem su sve vrednosti
pomnožene sa -1.

▶Test 3: Proveriti da li su srazmerne devĳacĳe
za početni niz, niz u kojem su svi elementi
pomnoženi sa 2, i niz u kojem su svi elementi
pomnoženi sa -5.

Metamorfno testiranje značajno doprinosi povećanju
stepena automatizacĳe u testiranju i omogućava detek-
cĳu grešaka u situacĳama kada tradicionalne metode
nisu primenljive. Za uspešnu primenu metamorfnog
testiranja neophodno je:

▶dobro razumevanje domena problema,
▶identifikacĳa relevantnih i pouzdanih metamorf-
nih svojstava,

▶automatizacĳa generisanja izvedenih testova i nji-
hove verifikacĳe.

Ključni korak u primeni metamorfnog testiranja jeste
identifikacĳa odgovarajućih metamorfnih relacĳa. Kva-
litet i snaga ovih relacĳa direktno utiču na efikasnost
testiranja.

Jedan od najkorisnĳih tipova metamorfnih relacĳa je re-
lacĳa ekvivalencĳe. Ova relacĳa podrazumeva da trans-
formisani ulaz mora proizvesti potpuno isti izlaz kao i
original, što omogućava jednostavnu i preciznu detekci-
ju nepravilnosti u ponašanju sistema. Zbog svoje stroge
prirode, relacĳa ekvivalentnosti omogućava detektova-
nje širokog spektra grešaka.

<!-- pdf_page=133 printed_page=4 -->

Primer 4.3.25 (Konstrukcĳa kompilatora) Veoma je
teško utvrditi ekvivalencĳu između izvornog koda i
izvršivog koda. Jedna alternativa je da se u dati izvor-
ni kôd dodaju određene naredbe ili delovi naredbi
koje mu ne menjaju semantiku. Na primer, to može
biti dodavanje nule izrazu (time se ne menja vred-
nost izraza) ili dodavanje uslova koji je uvek ispunjen
(uslov if (true) ... takođe ne menja semantiku
programa). Za tako izmenjene izvorne programe, tre-
balo bi da bude generisan izvršivi kôd koji se ponaša
na isti način kao i početni kôd.

Primer 4.3.26 (Mašinsko učenje — klasifikacĳa slika)
Razmotrimo klasifikator slika obučen da prepoznaje
kategorĳe objekata na slikama. Jedan primer meta-
morfnog odnosa je:

Ako se ulazna slika rotira za mali ugao
(npr. do 10◦), očekuje se da klasifikacĳa
ostane nepromenjena.

Na osnovu ove osobine, moguće je konstruisati sledeći
postupak testiranja:

1. Izabrati originalni test primer 𝑥(sliku) za koji
klasifikator daje rezultat 𝑓(𝑥).

2. Generisati transformisani primer 𝑥′ (npr. rotaci-
ja slike za 5◦).

3. Uporediti rezultate 𝑓(𝑥) i 𝑓(𝑥′); ukoliko se razli-
kuju, to može ukazivati na potencĳalnu grešku
u modelu, ili na potrebu za dodatnim podacima
u obuci.

Međutim, u praksi, relacĳa ekvivalencĳe nĳe uvek do-
stupna metamorfna relacĳa. U tim slučajevima koriste
se slabĳe forme, kao što su relacĳe očuvanja određe-
nih karakteristika rezultata ili relacĳe koje predviđaju
smer promene izlaza. Pravilna selekcĳa metamorfnih
relacĳa zahteva duboko razumevanje testiranog sistema

<!-- pdf_page=134 printed_page=120 -->

i domena primene.

Primer 4.3.27 (Predviđanje cene nekretnine) Sistem
predviđa cenu nekretnine na osnovu kvadrature, lo-
kacĳe i broja soba. U slučaju povećanja kvadrature, za
isti ili veći broja soba i za nekretninu na istoj lokacĳi,
očekuje se povećanje predviđene cene.

Na primer, ako imamo kao ulaz nekretninu koja ima
60m² i tri sobe, za koju sistem predviđa cenu 90.000
evra, onda možemo da kreiramo novi ulaz tako što
samo povećamo kvadraturu na 80m². Za ovaj novi
ulaz očekujemo da cena treba da bude veća od 90.000
evra. Izlaz se menja, ali postoji logički odnos između
prvog i drugog izlaza (monotonost u predikcĳi), što
se koristi za proveru ponašanja modela.

### 4.4 Načini sprovođenja testiranja

U procesu testiranja mogu se izdvojiti dve osnovne
aktivnosti:

(i) definisanje test primera

(ii) sprovođenje postupka izvršavanja i evaluacĳe tih
test primera.

Obe ove aktivnosti, prema načinu na koji se sprovo-
de, mogu biti obavljane manuelno ili automatski. Iako
postoje četiri moguće kombinacĳe:

(1) manuelno generisanje testova i manuelno sprovo-
đenje testiranja,

(2) manuelno generisanje testova i automatsko spro-
vođenje testiranja,

(3) automatsko generisanje testova i manuelno spro-
vođenje testiranja i

(4) automatsko generisanje testova i automatsko spro-
vođenje testiranja,

u praksi se (3) obično ne koristi.

<!-- pdf_page=135 printed_page=4 -->

Automatsko
generisa-
nje testova

Automatsko
izvršava-
nje testova

Manuelno
generisa-
nje testova

Manuelno
izvršava-
nje testova

(2) Polu-
automatsko
testiranje

(3) Polu-
automatsko
testiranje

Automatsko
generisa-
nje testova

Manuelno
izvršava-
nje testova

Manuelno
generisa-
nje testova

Automatsko
izvršava-
nje testova

(4) Auto-
matsko
testiranje

(1) Manuelno
testiranje

Načini sprovo-
đenja testiranja

Slika 4.14: Načini izvođenja testiranja softvera

4.4.1 Manuelno testiranje

Termin manuelno testiranje podrazumeva da se obe
aktivnosti sprovode manuelno, odnosno da testeri smi-
šljaju test slučajeve i samostalno sprovode testiranje i
ocenjuju rezultate testiranja. Manuelno testiranje je ne-
zamenjivo u delovima verifikacĳe koji zahtevaju ljudsku
percepcĳu, razumevanje konteksta i subjektivnu proce-
nu kvaliteta. Dodatno, manuelno testiranje je ključno u
domenu validacĳe softvera, gde je cilj da se utvrdi da li
softver zaista zadovoljava potrebe i očekivanja krajnjih
korisnika, a ne samo da li funkcioniše prema tehničkim
specifikacĳama.

U kontekstu verifikacĳe softvera, primer upotrebe ma-
nuelnih tehnika testiranja je istraživačko testiranje, koje
se oslanja na iskustvo i intuicĳu testera. Umesto striktno
definisanih koraka, tester istražuje softver u realnom
vremenu, tražeći neočekivane greške i ponašanja. Au-
tomatizacĳa ne može da zameni ovu vrstu kreativnog
pristupa.

Manuelnim testiranjem često se proveravaju svojstva ko-

<!-- pdf_page=136 printed_page=122 -->

ja se nalaze na preseku validacĳe i verifikacĳe softvera.
Na primer, testiranjem prihvatljivosti, koje obično spro-
vodi sam korisnik ili predstavnik korisnika, procenjuje
se da li je softver upotrebljiv i spreman za puštanje u
produkcĳu. Osim što uključuje funkcionalne provere,
često podrazumeva i subjektivne ocene o korisničkom
iskustvu i interfejsu.

Slično tome, aplikacĳe u realnom vremenu i interaktiv-
ne aplikacĳe, poput video igara, sistema za virtuelnu
realnost ili specĳalizovanih simulacĳa, zahtevaju manu-
elnu evaluacĳu ponašanja sistema tokom neposredne
upotrebe. U takvim slučajevima, subjektivno korisnič-
ko iskustvo ima ključnu ulogu u oceni ispravnosti i
kvaliteta softvera.

U kontekstu validacĳe softvera, provera korisničkog in-
terfejsa često zahteva manuelni pristup. Vizuelni aspek-
ti kao što su poravnanje elemenata, čitljivost i jasnoća
poruka najbolje se procenjuju ljudskim okom. Automa-
tizovani alati mogu potvrditi prisustvo odgovarajućih
elemenata, ali ne i njihovu funkcionalnu ili estetsku
vrednost. Slično, testiranja vezana za ocenu naučivosti i
intuitivnosti korišćenja fokusiraju se na iskustvo krajnjeg
korisnika. Ona ocenjuju koliko je softver jednostavan
za učenje i upotrebu, što zahteva direktno posmatranje
korisnika, analizu ponašanja i prikupljanje povratnih
informacĳa.

4.4.2 Automatsko izvršavanje test primera

Primeri kako automatsko
izvršavanje testova ubrzava
razvojni ciklus, poboljšava
kvalitet koda i osigurava
stabilnost aplikacĳa mogu
se videti u master radovima
Milice Galjak:
Automatsko testiranje mobilnih
aplikacĳa
i Nikole Dimića:
Automatsko testiranje mikroser-
visnih aplikacĳa

Iako manuelno testiranje omogućava uvid u korisničko
iskustvo i subjektivne aspekte sistema, ono je često
podložno greškama, sporo i teško skalabilno. Zbog toga
je automatizacĳa testiranja od ključnog značaja, naročito
kod složenih sistema i testova koji se često ponavljaju.
Automatizovani testovi smanjuju potrebu za ručnim
intervencĳama, ubrzavaju razvoj i unapređuju kvalitet
softverskog proizvoda.

<!-- pdf_page=137 printed_page=4 -->

Najčešći oblik automatizovanog testiranja je izvršavanje
testova jedinica koda. Ovakvi testovi se često automat-
ski pokreću prilikom svake izmene u kodu, a njihova
integracĳa sa alatima za merenje pokrivenosti koda
omogućava praćenje kvaliteta testiranja. Postoji veliki
broj okruženja za automatsko izvršavanje testova, po-
znatih po obrascu xxxUnit, gde xxx označava konkretni
programski jezik. Na primer, za C++ postoji CppUnit,
za Javu JUnit, a za Python PyUnit.

Testiranje veb aplikacĳa
Selenium je softver otvorenog
koda koji se dominantno
koristi za automatizovano
testiranje veb aplikacĳa. Se-
lenium podržava testiranje
veb aplikacĳa u gotovo svim
dostupnim pretraživačima.
Test skriptovi mogu biti pi-
sani u različitim program-
skim jezicima, kao što su C#,
Java, Ruby, Python i Perl i
pokretani na operativnim
sistemima Windows, macOS
ili Linux.

Pored alata za izvršavanje testova, postoje i alati koji
automatizuju čitav proces testiranja — uključujući upra-
vljanje test slučajevima, integracĳu sa repozitorĳumima
koda, praćenje defekata i generisanje izveštaja. Ovi alati
su često deo većih razvojnih okruženja ili sistema za
kontinuiranu integracĳu.

Kontinuirana integracĳa softvera

Automatizacĳa omogućava brzo, ponovljivo i pouzdano
izvršavanje test primera, što je posebno važno u okru-
ženjima kontinuirane integracĳe i isporuke softvera.
Kontinuirana integracĳa (eng. continuous integration, CI)
predstavlja ključni proces u razvoju softvera, posebno
u timovima gde više članova svakodnevno unosi izme-
ne u zajednički kodni repozitorĳum. Cilj kontinuirane
integracĳe je da se svaka izmena odmah objedini sa
trenutnim stanjem projekta, automatski izgradi i testira,
kako bi se potencĳalne greške otkrile što ranĳe.

Popularni alati za kontinui-
ranu integracĳu su:

Prilikom svakog objedinjavanja koda, sistem prolazi
kroz sledeće faze:

▶Jenkins
▶Buildbot
▶Travis CI
▶GitLab CI
▶CircleCI
▶TeamCity (JetBrains)
▶Bamboo (Atlassian)

Integracĳa — sve trenutne izmene se spajaju u jedin-
stvenu verzĳu projekta,

Izgradnja — kôd se kompajlira i pakuje u izvršni fajl ili
instalacioni paket,

Testiranje — automatski test primeri se izvršavaju kako
bi se proverila ispravnost sistema,

<!-- pdf_page=138 printed_page=124 -->

Arhiviranje — rezultujući artefakti se verzionišu i ču-
vaju za buduću upotrebu,

Primena — sistem se učitava u okruženje za testiranje
ili integracĳu, gde može biti pokrenut i dostupan
za evaluacĳu.

Testiranje u okviru kontinu-
irane integracĳe softvera je
često vremenski i memorĳ-
ski veoma zahtevno. Jedna
opcĳa smanjenja troškova
testiranja je selektivno te-
stiranje. Primer selektivnog
testiranja može se videti u
master tezi Jovane Bošković:
Optimizacĳa procesa kontinui-
rane integracĳe i isporuke kroz
selektivno testiranje zasnovano
na analizi pokrivenosti koda

Ovakav pristup značajno doprinosi:

▶ranom otkrivanju grešaka,
▶smanjenju troškova projekta,
▶kraćem vremenu razvoja,
▶i nižem riziku prilikom isporuke novih verzĳa
softvera.

4.4.3 Automatsko generisanje test primera

Generisanje test primera moguće je automatizovati samo
za određene vrste testiranja, u kojima se mogu formalno
definisati kriterĳumi pokrivenosti i ponašanja sistema.
Tipični primeri uključuju testiranje robusnosti i testove
usmerene na otkrivanje grešaka u kodu kao što su delje-
nje nulom, korišćenje neinicĳalizovanih promenljivih ili
pristupi nedozvoljenim memorĳskim lokacĳama (vidi
poglavlje 9).

Primer automatskog gene-
risanja test primera može
se videti u master tezi Ane
Ðorđević:
Automatsko generisanje test
primera uz pomoć statičke
analize i rešavača Z3

U ovim scenarĳima, automatizacĳa ima značajnu pred-
nost jer omogućava sistematsko generisanje velikog
broja ulaznih podataka uz minimalni ljudski napor. Po-
sebno je korisna za otkrivanje ekstremnih i graničnih
slučajeva koji bi lako mogli ostati neotkriveni manuel-
nim testiranjem. Na primer, alati za rasplinuto testiranje
(eng. fuzzing) mogu nasumično, ali ciljno, generisati
razne kombinacĳe ulaza, uključujući i one koji izlaze
iz uobičajenih opsega, kako bi izazvali neželjeno ili
nepredviđeno ponašanje softverskog sistema.

Primer implementacĳe ra-
splinutog testiranja može
se videti u master tezi Ane
Mitrović:
Primena jezika Skala u paraleli-
zacĳi rasplinutog testiranja

Slično tome, statička analiza softvera omogućava identi-
fikacĳu potencĳalno problematičnih mesta u kodu, kao
što su upotreba promenljivih pre dodeljivanja vredno-
sti ili dereferenciranje null pokazivača. Na osnovu tih
nalaza, mogu se automatski generisati test primeri koji

<!-- pdf_page=139 printed_page=4 -->

ciljano testiraju te kritične tačke i tako povećavaju vero-
vatnoću otkrivanja grešaka u ranim fazama razvoja.

Međutim, kada se radi o testiranju složenih funkcio-
nalnosti koje zavise od višeslojnih uslova, konteksta
upotrebe ili korisničkih odluka, automatizovano generi-
sanje test primera postaje izuzetno izazovno, a često i
neizvodljivo. U takvim situacĳama, uspešno testiranje
zahteva duboko razumevanje poslovne logike, očeki-
vanog ponašanja sistema u realnim scenarĳima, kao
i interakcĳa među različitim komponentama softve-
ra. Ove aspekte je teško formalizovati na način koji bi
omogućio automatsko pouzdano i smisleno generisanje
kvalitetnih test primera. Zbog toga se u praksi auto-
matizovano generisanje testova najefikasnĳe koristi kao
dopuna manuelnom procesu.

Rezime

▶Testiranje softvera ima za cilj da otkrĳe defekte u
softveru.

▶Poželjno je ispravljanje grešaka u početnim fazama
razvoja softvera.

▶Testiranje mogu da obavljaju i programeri i testeri.
▶Proces testiranja obuhvata planiranje, analizu, di-
zajn, implementacĳu, evaluacĳu, izvršavanje i za-
tvaranje procesa testiranja

▶Osnovna podela testiranja je na testiranje funkcio-
nalnih i nefunkcionalnih karakteristika softvera.

▶Prema nivou testiranja, razlikujemo testove jedini-
ce koda, komponentne, integracione i sistemske
testove.

▶Nefunkcionalno sistemsko testiranje uključuje te-
stiranje performansi, kompatibilnosti, pouzdano-
sti, upotrebljivosti, bezbednosti, sigurnosti i pre-
nosivosti.

▶U sistemsko testiranje se ubrajaju i istraživačko
testiranje, testiranje prihvatljivosti i instalaciono
testiranje.

<!-- pdf_page=140 printed_page=126 -->

▶Regresiono testiranje predstavlja proces ponovnog
izvršavanja prethodno uspešno završenih testova.

▶Pokrivenost testiranjem je metrika koja pomaže
da se proceni koliko su testovi sveobuhvatni.

▶Tehnike testiranja se dele na testiranje crne kutĳe,
testiranje bele kutĳe i testiranje sive kutĳe.

▶Metamorfno testiranje je pristup testiranju pri
postojanju problema proročišta.

▶Testiranje može da bude manuelno i automatizo-
vano.

Literatura

[1]
Paul Ammann i Jeff Offutt. Introduction to Softwa-
re Testing. Cambridge University Press, 2017. doi:

10.1017/9781316771273.

[2]
Boris Beizer. Software Testing Techniques. 2. izda-
nje. Van Nostrand Reinhold, 1990.

[3]
Robert Binder. Testing Object-Oriented Systems.
Addison-Wesley, 1999.

[4]
Koen Claessen i John Hughes. QuickCheck: A
Lightweight Tool for Random Testing of Haskell
Programs. U: ACM SIGPLAN Notices 35.9 (2000.),
str. 268–279. doi: 10.1145/357766.351266.

[5]
Gordon Fraser i Andrea Arcuri. A Large-Scale
Evaluation of Automated Unit Test Generation
Using EvoSuite. U: ACM Transactions on Software
Engineering and Methodology 24.2 (2014.). doi:

10.1145/2685612.

[6]
Barton P. Miller, Lars Fredriksen i Bryan So. An
Empirical Study of the Reliability of UNIX Utiliti-
es. U: Communications of the ACM 33.12 (1990.),
str. 32–44. doi: 10.1145/96267.96279.

[7]
Glenford J. Myers, Corey Sandler i Tom Badgett.
The Art of Software Testing. 3. izdanje. Wiley, 2011.
isbn: 9781118031964.

<!-- pdf_page=141 printed_page=127 -->

Ispitna pitanja

10. Testiranje u razvoju softvera. Cena greške u kon-
tekstu vremena otkrivanja.

11. Testiranje u razvoju softvera. Uloga testera u ra-
zvoju softvera.

12. Testiranje u razvoju softvera. Faze testiranja sof-
tvera: planiranje, analiza, dizajn i implementacĳa
testova.

13. Testiranje u razvoju softvera. Faze testiranja sof-
tvera: izvršavanje i evaluacĳa testova. Zatvaranje
testiranja.

14. Vrste testiranja. Testiranje jedinica koda. Primeri.
15. Vrste testiranja. Komponentno i integraciono te-
stiranje. Primeri.

16. Vrste testiranja. Sistemsko testiranje. Funkcional-
no sistemsko testiranje. Regresiono testiranje. Pri-
meri.

17. Vrste testiranja. Sistemsko testiranje. Istraživač-
ko testiranje. Testovi prihvatljivosti. Instalaciono
testiranje. Primeri.

18. Vrste testiranja. Nefunkcionalno testiranje. Testo-
vi performansi. Testovi kompatibilnosti. Testovi
pouzdanosti. Primeri.

19. Vrste testiranja. Nefunkcionalno testiranje. Testovi
upotrebljivosti. Testovi bezbednosti. Testovi sigur-
nosti. Testovi prenosivosti. Primeri.

20. Tehnike testiranja. Karakteristike dobrog skupa
testova. Pokrivenost testiranjem. Podela na tehnike
testiranja.

21. Tehnike testiranja. Testiranje metodama crne kuti-
je. Isprobavanja svih mogućih ulaza. Metod klasa
ekvivalencĳe. Primeri.

22. Tehnike testiranja. Testiranje metodama crne ku-
tĳe. Metod klasa ekvivalencĳe. Metod graničnih
vrednosti. Primeri.

23. Tehnike testiranja. Karakteristike dobrog skupa
testova. Tabele odlučivanja. Primeri.

24. Tehnike testiranja. Karakteristike dobrog skupa
testova. Dĳagrami stanja. Tabele stanja. Primeri.

<!-- pdf_page=142 printed_page=128 -->

25. Tehnike testiranja. Testiranje metodama bele kutĳe.
Putanja i broj putanja u programu. Pojam i vrste
pokrivenosti. Njihovi odnosi. Primeri.

26. Tehnike testiranja. Testiranje metodama bele ku-
tĳe. Pojam i vrste pokrivenosti. Preporučen nivo
pokrivenosti. Alati za merenje pokrivenosti. Pri-
meri.

27. Tehnike testiranja. Testiranje metodama bele kuti-
je. Izbor relevantnih testova i putanja. Testiranje
osnovnih putanja. Testiranje na osnovu grafa toka
podataka. Primeri.

28. Tehnike testiranja. Problem proročišta. Metamorf-
no testiranje. Primeri.

29. Načini testiranja. Manuelno testiranje.
30. Načini testiranja. Automatsko izvršavanje i evalu-
acĳa testova. Kontinuirana integracĳa.

31. Načini testiranja. Automatsko generisanje test pri-
mera.

<!-- pdf_page=143 printed_page=143 -->

— If Broken it is, Fix it You Should —
(Yoda, Star Wars)

5.1
Veza izvršivog
koda i debagera 130

5.2
Vrste debagova-
nja . . . . . . . . 136

Pregled

5.3
Primeri debage-
ra . . . . . . . . . 147

▶Kada se u okviru testiranja otkrĳe da postoji de-
fekt u radu softvera, kako pronaći grešku koja je
uzrokovala taj defekt?

5.4
Otvoreni proble-
mi
. . . . . . . . 152

5.5
Štampanje
umesto debagera153

▶Koja je uloga debagovanja u procesu razvoja sof-
tvera?

▶Zašto je debager sistemski alat?
▶Koje vrste debagovanja postoje?
▶Koje alternative debagovanju postoje?

Debagovanje je proces u razvoju softvera koji ima za
cilj pronalaženje greške odnosno uzroka defekta u pro-
gramu. Debager (eng. debugger) je alat koji se koristi za
praćenje izvršavanja programa radi boljeg razumeva-
nja ponašanja programa i lakšeg pronalaženja greške u
programu.

Kako bi informacĳe koje debager pruža programeru bile
precizne i razumljive, neophodna je podrška kompajlera
i linkera, koji obezbeđuju povezivanje izvršivog koda
sa izvornim kodom, kao i razne druge korisne podatke.
Funkcionalnost debagera takođe zavisi od podrške ope-
rativnog sistema, a u određenim slučajevima i samog
hardvera.

Poznati debager GDB, koji
se razvĳa u okviru projekta
GNU, se može koristiti kroz
veliki broj razvojnih okru-
ženja, uključujući QtCreator,
Visual Studio Code, Eclipse,
NetBeans, CLion i IntelliJ.

Debageri se često integrišu u razvojna okruženja koja
im obezbeđuju grafički korisnički interfejs. Iako grafički
interfejs može znatno olakšati upotrebu i unaprediti ko-
risničko iskustvo, važno je imati na umu da je ono samo
sredstvo interakcĳe sa debagerom, a ne njegov suštinski
deo. Sama funkcionalnost debagera ostaje nezavisna od
načina na koji se korisniku prikazuje.

<!-- pdf_page=144 printed_page=130 -->

### 5.1 Veza izvršivog koda i debagera

Tokom kompilacĳe softverskog projekta dostupne su
brojne opcĳe i podešavanja koja omogućavaju precizno
upravljanje načinom prevođenja izvornog koda u iz-
vršivi program. Ova podešavanja se često koriste za
optimizacĳu performansi, lakše pronalaženje grešaka,
ili prilagođavanje ciljnim platformama.

Režim kompilacĳe je skup opcĳa kompilacĳe koje se
često zajedno koriste sa određenim ciljem. Postoje:

režim prevođenja za upotrebu (eng. release mode), skra-
ćeno režim riliz — to je svaki režim koji ima za cilj
dobĳanje optimizovane izvršive verzĳe namenje-
ne krajnjem korisniku,

režim prevođenja za pronalaženje grešaka (eng. debug
mode), skraćeno režim debag — to je režim prevo-
đenja koji ima za cilj dobĳanje izvršive verzĳe
programa namenjene programeru radi lakšeg ot-
krivanja grešaka u kodu i

kombinovani režim koji odgovara kombinacĳi odabra-
nih opcĳa režima za prevođenje za upotrebu i
režima za pronalaženje grešaka — ovaj režim se
koristi u situacĳama kada je potrebno naći grešku
u programu, a režim prevođenja za pronalaženje
grešaka ne daje željene rezultate.

Na program koji se dobĳa prevođenjem za upotrebu če-
sto se referiše sa riliz verzĳa programa, dok se na program
koji se dobĳa prevođenjem za pronalaženje grešaka
referiše sa debag verzĳa programa.

Nakon generisanja izvršive verzĳe programa, moguće
je primeniti specĳalizovane alate koji modifikuju izvr-
šivi kôd sa ciljem otežavanja i ometanja debagovanja‗.
Ovakve tehnike se nazivaju anti-debagovanje (eng. anti-
debugging) i koriste se radi zaštite intelektualne svojine,

‗ Iako anti-debagovanje može da se koristi na svakoj izvršivoj verzĳi
programa, ima ga smisla koristiti samo nad programima koji su
prevedeni u riliz režimu.

<!-- pdf_page=145 printed_page=5 -->

kako bi se sprečilo analiziranje logike programa i kra-
đa koda, ili pak u zlonamernom softveru, kako bi se
onemogućilo prepoznavanje i analiziranje malicioznog
ponašanja.

Debager se može koristiti za svaku izvršivu verzĳu
programa. Mogućnosti i informacĳe koje se dobĳaju
za debag verzĳu su povezane sa izvornim kodom i
olakšavaju programeru da poveže stanje izvršavanja
sa izvornim kodom. S druge strane, informacĳe koje
debager može da pruži za riliz verzĳu su često samo
uvid u asemblerski kôd, na isti način kao što ih vidi i pro-
cesor. U slučaju primene anti-debagovanja, mogućnosti
debagera su dodatno ograničene.

5.1.1 Režim prevođenja za upotrebu

Primarni cilj prevođenja u režimu za upotrebu jeste
postizanje visoke efikasnosti izvršavanja kroz različi-
te strategĳe optimizacĳa koje sprovodi kompajler. Ove
optimizacĳe mogu uključivati uklanjanje nepotrebnog
koda, preuređivanje instrukcĳa radi boljeg iskorišće-
nja procesora, zamenu složenĳih konstrukcĳa bržim
ekvivalentima, kao i umetanje funkcĳa. Kao rezultat,
generisani izvršivi kôd je kompaktnĳi i brži u odnosu
na verzĳu prevedenu u režimu za uklanjanje grešaka.

Režim prevođenja za upotrebu podrazumeva optimi-
zacĳe koje kao primarni cilj imaju optimizacĳu brzine
izvršavanja programa. Međutim, za neke aplikacĳe, na
primer za one koje se izvršavaju na uređajima sa malom
količinom memorĳe, neophodne su optimizacĳe koje se
odnose na smanjivanje veličine izvršive datoteke kao i
upotrebe memorĳe u fazi izvršavanja. Režim prevođenja
za upotrebu u ovom slučaju se naziva režim prevođenja
za upotrebu sa minimalnom veličinom (eng. minimum
size release mode).

Sprovedene optimizacĳe smanjuju mogućnost poveziva-
nja izvršivog koda sa izvornim datotekama. Neki delovi

<!-- pdf_page=146 printed_page=132 -->

koda se mogu potpuno izostaviti, promeniti redosled
ili transformisati do neprepoznatljivosti, što značajno
otežava proces razumevanja izvršavanja koda i traženja
greške u kodu. Zbog toga se ova verzĳa prevođenja goto-
vo nikada ne koristi za analizu i dĳagnostiku grešaka.

Primer 5.1.1 (Prevođenje za upotrebu) Prilikom pre-
vođenja programa pomoću kompajlera gcc, ne postoji
jedinstvena opcĳa za režim prevođenja za upotre-
bu, već se to postiže kombinovanjem odgovarajućih
kompajlerskih opcĳa. Ove opcĳe uključuju korišće-
nje visokog nivoa optimizacĳe, na primer -O2 ili -O3,
dok se za režim za upotrebu sa minimalnom veliči-
nom koristi opcĳa optimizacĳe -Os. Dodatno, druga
bitna opcĳa je -DNDEBUG. Ova opcĳa definiše makro

NDEBUG, koji onemogućava izvršavanje poziva funk-
cĳe assert(), čĳa je upotreba karakteristična u fazi
otklanjanja grešaka.

S druge strane, u mnogim sistemima za izgradnju
koda, izbor režima može da se uključi jedinstvenom
opcĳom. Na primer, u sistemu CMake, koristi se opcĳa

-DCMAKE_BUILD_TYPE koja se za režim prevođenja za
upotrebu postavlja na vrednost Release, a za režim
prevođenja za upotrebu sa minimalnom veličinom
postavlja na vrednost MinSizeRel.

5.1.2 Režim prevođenja za pronalaženje grešaka

Primarni cilj prevođenja u režimu za pronalaženje gre-
šaka je pravljenje izvršive verzĳe koda koja za svaku
instrukcĳu u fazi izvršavanja omogućava preciznu pove-
zanost sa odgovarajućim linĳama izvornog koda. Kom-
pajler u ovom režimu generiše dodatne informacĳe koje
omogućavaju debageru da poveže izvršavane instrukcĳe
sa odgovarajućim linĳama izvornog koda.

Za razliku od režima riliz, gde su uključene optimizacĳe
radi postizanja što efikasnĳeg izvršavanja, u režimu

<!-- pdf_page=147 printed_page=5 -->

debag su te optimizacĳe isključene ili svedene na mi-
nimum kako bi se očuvala što preciznĳa veza između
izvornog i izvršivog koda. Zbog odsustva optimizacĳa,
izvršiva datoteka generisana u režimu debag najčešće je
znatno veća od datoteke prevedene u režimu riliz†. Ta-
kođe, izvršavanje programa prevedenog u ovom režimu
može biti primetno sporĳe i manje efikasno u pogledu
iskorišćenja memorĳe. Međutim, ta neefikasnost je pri-
hvatljiva u fazi razvoja, jer omogućava precizno praćenje
toka izvršavanja i stanja promenljivih.

Primer 5.1.2 (Prevođenje za pronalaženje grešaka)
Prilikom prevođenja programa pomoću kompajlera

gcc, ne postoji jedinstvena opcĳa za režim prevođenja
za pronalaženje grešaka, ali se to postiže kombinova-
njem opcĳe koja uključuje korišćenje najnižeg nivoa
optimizacĳe -O0 i opcĳe -g koja uključuje upisivanje
informacĳa za debagovanje u izvršivu datoteku.

Kao što je pomenuto, u mnogim sistemima za iz-
gradnju koda, izbor režima može da se uključi jedin-
stvenom opcĳom. U sistemu CMake, opcĳa -DCMAKE_-

BUILD_TYPE se za režim prevođenja za pronalaženje
grešaka postavlja na vrednost Debug.

Formati za predstavljanje pomoćnih informacĳa

Formati za predstavljanje pomoćnih informacĳa potreb-
nih za debagovanje preciziraju način na koji kompajler
može da zapiše podatke kao što su nazivi funkcĳa, na-
zivi promenljivih, tipovi podataka, odgovarajuće linĳe
iz izvorne datoteke i slično. Najpoznatĳi formati za
predstavljanje pomoćnih informacĳa potrebnih za deba-
govanje su format DWARF i format Microsoft CodeView.
Ovi formati nisu kompatibilni.

† Izvršiva datoteka može biti značajno veća i iz drugih razloga.
Na primer, informacĳe u formatu DWARF se upisuju direktno u
izvršivu datoteku.

<!-- pdf_page=148 printed_page=134 -->

Iako je format DWARF nezavisan od formata izvrši-
ve datoteke, najčešće se koristi uz format za izvršive
i povezane datoteke ELF (eng. Executable and Linkable
Format) u okviru UNIX-olikih operativnih sistema, kao
što su Linux i macOS. Format DWARF se može koristiti
prilikom prevođenja programa koji su napisani u razli-
čitim programskim jezicima — npr. C, C++ i Fortran,
a karakteristike formata omogućavaju i proširenja za
dodatne jezike i njihove specifične konstrukte, ukoliko
je to potrebno. Za format DWARF je karakteristično
da se metapodaci koje on definiše umeću direktno u
izvršivi kôd, što čini debag verzĳu programa dodatno
većom u odnosu na riliz verzĳu koja te podatke ne sadrži.

DWARF je dizajniran kao
nezavisan format, ali u slič-
no vreme sa formatom za
izvršive i povezane datoteke
ELF. ELF na engleskom zna-
či vilenjak, dok DWARF zna-
či patuljak. Nazivi DWARF i
ELF su uklopljeni kao sklad-
ni delovi epske fantastike.
Ipak, kasnĳe je predložen
odgovarajući akronim i za
format DWARF — Debug-
ging With Arbitrary Record
Formats (debagovanje sa pro-
izvoljnim formatima zapisa).

Primer 5.1.3 (Format DWARF) Kompajleri kao što su
GCC i Clang generišu informacĳe u formatu DWARF i
njih mogu da koriste debageri GDB i LLDB.

Operativni sistem Windows koristi sopstveni format za
pomoćne informacĳe Microsoft CodeView, koji je integri-
san u Majkrosoftove razvojne alate. Ovaj format koristi
se prilikom prevođenja programa koji su napisani u pro-
gramskim jezicima C, C++ i jezicima .NET platforme.
Metapodaci u formatu CodeView se distribuiraju odvoje-
no od izvršivog koda (u okviru datoteka sa ekstenzĳom
pdb). Oni se koriste po potrebi, ne opterećuju izvršivi
kôd, ali se učitavaju u debager prilikom debagovanja.

Primer 5.1.4 (Format Microsoft CodeView) Kompajler
MSVC (kompajler Microsoft Visual Studio C++) generi-
še podatke u formatu Microsoft CodeView i njih mogu
da koriste debageri WinDbg i Visual Studio Debugger.

5.1.3 Kombinovani režimi prevođenja

Moguće je da ponašanje programa dobĳenih u režimima
debag i riliz bude različito, što može značajno otežati

<!-- pdf_page=149 printed_page=5 -->

proces otklanjanja grešaka. Na primer, može se desiti
da se određene greške ispoljavaju isključivo u riliz ver-
zĳi, dok se u debag verzĳi program izvršava ispravno.
Ovakva situacĳa može imati više uzroka.

Poboljšavanju korisničkog
iskustva prilikom korišćenja
debagera nad optimizova-
nom verzĳom programa
aktivno doprinose Ðorđe
Todorović & Nikola Prica,
diplomirani master studenti
Matematičkog fakulteta:

Jedan od mogućih razloga je to što debag verzĳa sadrži
dodatne informacĳe, kao i inicĳalizacĳu memorĳe koju
riliz verzĳa ne poseduje. Time se greška može privre-
meno „zamaskirati“, iako je prisutna u izvornom kodu.
S druge strane, uzrok može biti i greška u kompajleru,
koja se manifestuje tokom optimizacĳe prilikom generi-
sanja riliz verzĳe. Iako su ovakve greške izuzetno retke,
one i dalje predstavljaju ozbiljan problem jer zahteva-
ju pronalaženje zaobilaznog rešenja kako bi se dobila
ispravna optimizovana verzĳa programa.

▶Debug info in optimized
code - how far can we go?
Improving LLVM debug
info with function entry
values

https://www.

youtube.com/watch?

v=1cWAmLMF1eI

▶Improving Debug
Information in LLVM to
Recover Optimized-out
Function Parameters

U oba opisana slučaja, debagovanje debag verzĳe progra-
ma ne može otkriti uzrok problema, dok je debagovanje
riliz verzĳe otežano zbog nepostojanja veze između
izvornog i izvršivog koda. Zbog toga se u savremenom
razvoju softvera sve više ulaže u unapređenje moguć-
nosti za debagovanje optimizovanog koda, a problemu
se pristupa upotrebom hibridnog režima kompilacĳe,
u kojem se optimizacĳe kombinuju sa zadržavanjem
debag informacĳa (onoliko koliko to optimizacĳe do-
zvoljavaju).

https://www.

youtube.com/watch?

v=ih5v65K10M8

Doprinos unapređenju ko-
risničkog iskustva pri deba-
govanju dao je i Vladimir
Vuksanović, diplomirani
master student Matematič-
kog fakulteta. Njegov master
rad:
Unapređenje infrastrukture
LLVM čuvanjem originalne loka-
cĳe pri debagovanju izdvojenog
koda

Primer 5.1.5 (Kombinovani režim prevođenja) Kom-
binovani režim prevođenja, za kompajler gcc, podra-
zumeva viši stepen optimizacĳe, na primer -O2 kao
i opcĳu koja uključuje informacĳe za debagovanje

-g. Dodatno, uključuje se i opcĳa -DNDEBUG kako bi
izvršavanje bilo više nalik izvršavanju koje se dobĳa
sa režimom prevođenja za upotrebu.

Ovakav režim prevođenja u sistemu CMake može se
postići postavljanjem opcĳe -DCMAKE_BUILD_TYPE na
vrednost RelWithDebInfo.

<!-- pdf_page=150 printed_page=136 -->

5.1.4 Anti-debagovanje

Mogućnost debagovanja izvršive verzĳe programa ni-
je uvek poželjna osobina, naročito u kontekstu zaštite
intelektualne svojine, bilo radi zaštite od neovlašćenog
kopiranja (eng. software copy protection) ili radi spreča-
vanja obrnutog inženjeringa (eng. reverse engineering).
U takvim slučajevima, primenjuju se različite tehnike
poznate pod nazivom anti-debagovanje. Tehnike anti-
debagovanja se koriste i u malicioznim programima,
gde služe kao sredstvo za izbegavanje analize i pre-
poznavanje od strane antivirusnih alata i sistema za
detekcĳu pretnji.

Anti-debagovanje obuhvata implementacĳu jedne ili
više metoda čĳi je cilj da ometaju ili potpuno onemogu-
će pokušaje debagovanja ciljanog procesa. Ove tehnike
mogu uključivati detekcĳu prisustva debagera, izmenu
toka izvršavanja u slučaju da je debager prisutan, kori-
šćenje specifičnih instrukcĳa koje se ponašaju drugačĳe
u prisustvu nadgledanja, kao i tehnike obfuskacĳe‡.

Iako tehnički sofisticirano, anti-debagovanje uvek pred-
stavlja balans između zaštite i funkcionalnosti. Pre-
komerna zaštita može negativno uticati na stabilnost,
efikasnost i održivost softverskog proizvoda.

### 5.2 Vrste debagovanja

Debagovanje možemo podeliti na interaktivno deba-
govanje, udaljeno debagovanje i debagovanje nakon
prekida izvršavanja programa (post-mortem debagova-
nje). Debager može da započne proces i da prati njegovo
izvršavanje, može da prati izvršavanje procesa koji je

‡ Obfuskacĳa ne menja funkcionalnost programa, već samo način
na koji je on predstavljen i uključuje preimenovanje simbola, doda-
vanje beskorisnog (mrtvog) koda, dinamičko generisanje koda i
šifrovanje delova koda ili podataka (kôd se generiše ili dešifruje
tokom izvršavanja, umesto da bude prisutan u izvršivoj datoteci,
kako bi se sprečila statička analiza koda).

<!-- pdf_page=151 printed_page=5 -->

već započeo sa radom kao i da analizira stanje programa
nakon što je program završio sa radom.

5.2.1 Interaktivno debagovanje

Interaktivnodebagovanje podrazumeva dinamičku ana-
lizu programa u realnom vremenu uz aktivno učešće
programera, koji koristi debager da bi pratio i kontroli-
sao tok izvršavanja aplikacĳe. Ovaj način debagovanja
omogućava dvosmernu komunikacĳu sa debagerom,
putem komandne linĳe ili grafičkog korisničkog inter-
fejsa.

Osnovni mehanizam interaktivnog debagovanja zasniva
se na tačkama prekida (eng. breakpoints), koje omogu-
ćavaju da se izvršavanje programa automatski pauzira
na odabranoj linĳi koda. Kada izvršavanje programa
dođe do linĳe koda na kojoj je postavljena tačka prekida,
debager omogućava inspekcĳu promenljivih, sadržaja
steka, registara i drugih komponenti stanja programa.
Nakon analize, izvršavanje može biti nastavljeno, korak
po korak (naredbe koje se nazivaju na engleskom step i
next) ili do sledeće tačke prekida.

Primer 5.2.1 (Funkcĳa ptrace) Debageri su sistemski
zavisni alati. Za razumevanje funkcionisanja debagera
potrebno je razumeti procese i sistem prekida na
odgovarajućem operativnom sistemu.

Pod operativnim sistemom Linux, za rad debagera
od suštinske važnosti je sistemska funkcĳa ptracea.
Korišćenjem sistemskog poziva ptrace, jedan proces,
upravljački proces, najčešće debager, može da kontroliše
drugi, ciljni proces, i da upravlja njegovim unutrašnjim
stanjem. Debageri koriste funkcĳu ptrace kako bi mogli
da zaustavljaju program, da posmatraju memorĳu
zaustavljenog programa i da je menjaju.

a ptrace je skraćeno od „pratilac procesa” (eng. process trace).

<!-- pdf_page=152 printed_page=138 -->

Pored običnih tačaka prekida, moguće je postavljati i
uslovne tačke prekida koje se aktiviraju samo kada je
ispunjen određeni logički uslov. Na taj način se izvrša-
vanje ne zaustavlja pri svakom prolazu, već samo kada
je stanje sistema relevantno za otkrivanje greške.

Primer 5.2.2 (Implementacĳa tačaka prekida) Kada
se postavi prekidna tačka u programu sa željom da se
na tom mestu zaustavi program, debager zameni od-
govarajuću instrukcĳu instrukcĳom prekida, pri čemu
sačuva i originalnu instrukcĳu. Kada se prilikom izvr-
šavanja programa naiđe na instrukcĳu prekida, desi
se hardverski izuzetak, operativni sistem zaustavlja
rad procesa i obaveštava o tome debager.

Debager najpre proverava da li je prekid u listi oče-
kivanih prekida koje je postavio debager (tj. da li je
u pitanju namerno zaustavljanje ili greška u original-
nom kodu). Ukoliko je greška u originalnom kodu,
onda se dopusti da se ta greška i izvrši.

Ukoliko je u pitanju tačka prekida koju je postavio
debager, onda debager na tom mestu omogući uvid u
sve vrednosti fizičkih registara procesa kao i u stanje
memorĳe. Debager prikazuje pročitane informacĳe
o procesu povezane sa informacĳama o izvornom
kodu koje su generisali kompajler i/ili linker prilikom
prevođenja programa.

Kada korisnik želi da nastavi sa izvršavanjem,

1. debager zameni instrukcĳu prekida original-
nom instrukcĳom,

2. izvrši je,
3. zameni ponovo originalnu instrukcĳu instruk-
cĳom prekida,

4. prepusti dalje kontrolu programu.

Ukoliko je u pitanju uslovna prekidna tačka, debager
proverava uslov i u slučaju da uslov nĳe ispunjen,
preskače se zaustavljanje i prikaz stanja memorĳe

<!-- pdf_page=153 printed_page=5 -->

već se samo nastavlja dalje sa izvršavanjem procesa.
Ukoliko uslov jeste ispunjen, debager zaustavlja rad
procesa i prikazuje relevantne informacĳe, kao i za
obične tačke prekida.

Savremeni debageri omogućavaju i postavljanje tačaka
posmatranja (eng. watchpoint) nad određenim lokacĳa-
ma u memorĳi. Kada se sadržaj označene memorĳske
lokacĳe promeni, debager automatski pauzira izvršava-
nje programa, čime se olakšava praćenje neželjenih ili
neočekivanih promena podataka u toku rada aplikacĳe.
Ova tehnika se naročito koristi kod analize grešaka iza-
zvanih nepredviđenim upisima u memorĳu, kao što su
prekoračenje bafera (eng. buffer overflow) ili konkurentni
pristupi deljenim resursima.

Primer 5.2.3 (Hardver — specĳalni registri za deba-
govanje) Za efikasno funkcionisanje, debager može
da koristi i direktno neke funkcionalnosti hardvera,
ukoliko su dostupne. Na primer, tačke posmatranja
omogućavaju praćenje vrednosti neke promenljive u
memorĳi, tj. da li se neka vrednost u memorĳi me-
nja ili se sa nje nešto čita. Ukoliko postoji podrška
hardvera (specĳalni registri koji pamte i proveravaju
odgovarajuće adrese), biće podignut izuzetak koji će
debager da obradi. Ukoliko to nĳe dostupno ili se
zahteva praćenje većeg broja vrednosti nego što je to
dostupno podrškom hardvera, onda debager mora
da izvršava instrukcĳu po instrukcĳu i da za svaku
proverava šta se dešava na traženim memorĳskim
lokacĳama, što značajno usporava izvršavanje.

Interaktivno debagovanje omogućava precizno i flek-
sibilno praćenje toka izvršavanja, što je od izuzetne
važnosti u složenim programima gde je ponašanje teško
predvideti. Kroz kombinacĳu pauziranja, ispitivanja i
nastavljanja rada, programer stiče detaljan uvid u pona-
šanje softverskog sistema i može efikasno identifikovati
greške.

<!-- pdf_page=154 printed_page=140 -->

Primer 5.2.4 (Interaktivno debagovanje: gdb iz ko-
mandne linĳe) Analizirajmo program maksimum_ni-
za.c interaktivnim debagerom gdb.

1 #include <stdio.h>

2

3 int maksimum_niza(int* niz, size_t velicina_niza

) {

4
int max = niz[0];

5
for (size_t i = 1; i < velicina_niza; i++) {

6
int tekuci = niz[i];

7
if (tekuci > max) {

8
max = tekuci;

9
}

10
}

11
return max;

12 }

13

14 int main() {

15
int niz[] = {8,1,16,0,256,5};

16
int max = maksimum_niza(niz, sizeof(niz)/

sizeof(int));

17

18
printf("maksimum = %i\n", max);

19
return 0;

20 }

Najpre je potrebno prevesti program (nivo optimiza-
cĳe -O0 je podrazumevan pa se može i izostaviti) i
pokrenuti debager.

1 gcc -g -O0
maksimum_niza.c
-o maksimum_niza

2 gdb maksimum_niza

Nakon toga, pokreće se debager gdb koji štampa svoju
pozdravnu poruku. Nakon toga je dostupan prompt
za komunikacĳu.

1 ...

2 Reading symbols from maksimum_niza...

3 (gdb)

Osnovna komanda je komanda run koja će pokrenuti
i izvršiti program

1 (gdb) run

<!-- pdf_page=155 printed_page=5 -->

2 Starting program: /home/matf/Desktop/

maksimum_niza

3 maksimum = 256

4 [Inferior 1 (process 42904) exited normally]

5 (gdb)

Komandom

1 break

možemo postaviti tačku prekida na željeni broj linĳe
koda ili na željenu funkcĳu. Na primer,

1 break maksimum_niza

će postaviti tačku prekida na početak izvršavanja
funkcĳe maksimum_niza. Naredba

1 run

će pokrenuti izvršavanje programa i zaustaviti se na
linĳi 3 (jer je tu postavljena tačka prekida, tj. tu je
početak funkcĳe maksimum_niza). Komandom

1 next

prelazimo na narednu naredbu programa, linĳu 4.
Komandom

1 info locals

možemo videti vrednost svih lokalnih promenljivih.
Komandom

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

7 3
int maksimum_niza(int* niz, size_t

velicina_niza) {

8 (gdb) next

9 4
int max = niz[0];

<!-- pdf_page=156 printed_page=142 -->

10 (gdb) next

11 5
for (size_t i = 1; i < velicina_niza; i

++) {

12 (gdb) info locals

13 i = 140737488346839

14 max = 8

15 (gdb) next

16 6
int tekuci = niz[i];

17 (gdb) info locals

18 tekuci = 0

19 i = 1

20 max = 8

21 (gdb) info args

22 niz = 0x7fffffffded0

23 velicina_niza = 6

Uslovne tačke prekida postavljaju se dodavanjem
uslova prekida. Na primer, komandom

1 break 6 if i==3

prekidamo izvršavanje na linĳi 6 ukoliko je vrednost
promenljive i jednaka 3. Slično, komandom

1 watch max

možemo da prekinemo izvršavanje svaki put kada se
promeni vrednost promenljive max. Komandom

1 info break

možemo da vidimo koje su sve prekidne tačke trenut-
no postavljene u programu.

1 (gdb) break 6 if i==3

2 Breakpoint 2 at 0x55555555518c: file

maksimum_niza.c, line 6.

3 (gdb) watch max

4 Hardware watchpoint 3: max

5 (gdb) info break

6 Num
Type
Disp Enb Address

What

7 1
breakpoint
keep y
0

x0000555555555169 in maksimum_niza at

maksimum_niza.c:3

8
breakpoint already hit 1 time

<!-- pdf_page=157 printed_page=5 -->

9 2
breakpoint
keep y
0

x000055555555518c in maksimum_niza at

maksimum_niza.c:6

10
stop only if i==3

11 3
hw watchpoint
keep y

max

Komandom

1 continue

nastavljamo izvršavanje programa do prve naredne
prekidne tačke.

1 (gdb) continue

2 Continuing.

3

4 Hardware watchpoint 3: max

5

6 Old value = 8

7 New value = 16

8 maksimum_niza (niz=0x7fffffffded0, velicina_niza

=6) at maksimum_niza.c:5

9 5
for (size_t i = 1; i < velicina_niza; i

++) {

10 (gdb) continue

11 Continuing.

12

13 Breakpoint 2, maksimum_niza (niz=0x7fffffffded0,

velicina_niza=6) at maksimum_niza.c:6

14 6
int tekuci = niz[i];

15 (gdb) info locals

16 tekuci = 16

17 i = 3

18 max = 16

Dodatno, savremeni debageri pružaju i niz naprednih
mogućnosti koje prevazilaze klasično postavljanje tača-
ka prekida i izvršavanje koda korak po korak. Jedna
od značajnih funkcionalnosti jeste mogućnost izmene
koda u toku izvršavanja (eng. hot code replacement), što
omogućava programeru da prilagodi ili ispravi deo
programa bez potpunog zaustavljanja i ponovnog po-
kretanja izvršavanja. Ova osobina značajno ubrzava
razvoj i testiranje, naročito u kompleksnim sistemima
sa dugim vremenom pokretanja. Još jedna napredna

<!-- pdf_page=158 printed_page=144 -->

tehnika jeste debagovanje unazad (eng. reverse debug-
ging), koje omogućava programeru da prati izvršavanje
koda unazad, analizirajući operacĳe koje su dovele do
određenog stanja.

5.2.2 Udaljeno debagovanje

Pored interaktivnog debagovanja koje se sprovodi na
lokalnoj mašini, često se koristi i udaljeno debagovanje
(eng. remote debugging). Ova tehnika podrazumeva in-
teraktivno debagovanje pri čemu se aplikacĳa izvršava
na jednom sistemu — ciljnom sistemu, dok se proces
debagovanja obavlja sa drugog sistema — udaljenog
sistema. Povezivanje se ostvaruje preko mreže koristeći
odgovarajuće protokole i servise.

Udaljeno debagovanje omogućava da debager sa uda-
ljenog računara upravlja izvršavanjem programa na cilj-
nom sistemu, postavlja tačke prekida, ispituje vrednosti
promenljivih i dobĳa informacĳe o stanju memorĳe i re-
gistara ciljne aplikacĳe. Ova tehnika je naročito korisna
u scenarĳima kada ciljni sistem ima ograničene resurse
i ne može lokalno izvršavati debager, što je čest slučaj
kod uređaja sa ugrađenim računarom (eng. embedded
systems), kao i prilikom razvoja sistema za koje nĳe lako
obezbediti direktni fizički pristup, kao što su IoT (eng. in-
ternet of things) platforme ili sistemi u produkcionom
okruženju.

Primer 5.2.5 (Udaljeno debagovanje korišćenjem de-
bagera gdb) Korišćenjem alata gdb na udaljenom si-
stemu i servisa gdbserver na ciljnom sistemu, moguće
je uspostaviti vezu između razvojne stanice i ciljnog
sistema, čime se omogućava upravljanje izvršavanjem
programa sa udaljene lokacĳe. Da bi udaljeno deba-
govanje bilo moguće, potrebno je da ciljna i udaljena
arhitektura budu iste, ili da debager na udaljenom
sistemu ima podršku za arhitekturu ciljnog sistema

<!-- pdf_page=159 printed_page=5 -->

(npr. multiarch podrška za debager gdb). Dodatno,
mrežna povezanost između dva sistema treba da bu-
de stabilna i odgovarajuće konfigurisana (na primer,
često se koristi protokol TCP/IP).

5.2.3 Debagovanje nakon prekida izvršavanja
programa

Doprinos unapređenju de-
bagovanja nakon prekida iz-
vršavanja programa alatom
gdb dao je Ðorđe Todorović,
diplomirani master student
Matematičkog fakultata. Nje-
gov master rad:
Podrška za naprednu analizu
promenljivih lokalnih za niti
pomoću alata GNU GDB

Debagovanje nakon prekida izvršavanja programa ili
post-mortem debagovanje je tehnika analize ponašanja
programa nakon što je njegovo izvršavanje već prekinu-
to, najčešće usled greške kao što su pristup nevažećoj
memorĳi ili neobrađen izuzetak. Za razliku od interak-
tivnog debagovanja, koje se sprovodi tokom izvršavanja
programa, post-mortem debagovanje se oslanja na in-
formacĳe koje su zabeležene u trenutku prekida, bez
mogućnosti ponovnog pokretanja aplikacĳe u istom
stanju. Post-mortem debagovanje je posebno važno u
produkcionim okruženjima, gde se greške moraju anali-
zirati bez direktnog ponovnog izvršavanja programa u
identičnim uslovima.

Za post-mortem debagovanje ključnu ulogu imaju tzv. co-
re dump datoteke, koje sadrže snimak memorĳe procesa
u trenutku njegovog pada, uključujući relevantne in-
formacĳe kao što su sadržaj steka, registra, segmenta
podataka i koda. Da bi se generisala core dump datoteka
prilikom prekida rada programa usled kritične greške,
potrebna su dodatna podešavanja u okviru operativnog
sistema pošto je najčešće opcĳa generisanja ove datoteke
podrazumevano isključena.

Tehnike post-mortem analize uključuju:

▶pregled sadržaja memorĳe i registara,
▶rekonstrukcĳu steka poziva funkcĳa (eng. backtra-
ce),

▶utvrđivanje poslednjih instrukcĳa koje su se izvr-
šile,

▶uvid u vrednosti promenljivih u trenutku prekida,

<!-- pdf_page=160 printed_page=146 -->

▶analizu sistemskih logova i izlaznih datoteka.

Debageri kao što su GDB,
LLDB i WinDbg podržavaju
post-mortem debagovanje.

Primer 5.2.6 (Datoteka core dump) Naredni jednosta-
van program izaziva grešku Segmentation fault zbog
derefernciranja NULL pokazivača u linĳi 6.

1 // crash.c

2 #include <stdio.h>

3

4 int main() {

5
int *p = NULL;

6
*p = 42;

7
return 0;

8 }

Ukoliko se program prevede sa

1
gcc -g crash.c -o crash

i pokrena sa

1 ./crash

dobĳa se poruka

1 Segmentation fault (core dumped)

Standardna podešavanja većine Linux distribucĳa pod-
razumevaju da se core dump datoteka ne generiše, ali
se to može promeniti podešavanjima sistema koja
zavise od distribucĳe i verzĳe same distribucĳe. Pored
ostalog, potrebno je podesiti da veličina core dump da-
toteke ne bude ograničena. Na primer, u okviru Linux
distribucĳe Ubuntu, to se radi komandom ulimit -c

unlimited. Takođe, potrebno je pokrenuti odgvaraju-
ći sistemski servis za generisanje core dump datoteka
kao i pronaći lokacĳu gde se core dump datoteka sme-
šta (ili namestiti da se on smesti u isti direktorĳum
kao i izvršiva datoteka).

Ime core dump datoteke može da bude u različitim
formatima. Na primer, ako se generisana datoteka
zove

core.24122.crash.1750685973
i ako se nalazi u istom direktorĳumu, onda se deba-

<!-- pdf_page=161 printed_page=5 -->

gerom gdb post-mortem debagovanje može pokrenuti
na sledeći način

1 gdb ./crash core.24122.crash.1750685973

Debager gdb će, nakon standardne uvodne poruke,
odštampati sledeće

1 Reading symbols from ./crash...

2 [New LWP 24122]

3 Core was generated by ‘./crash’.

4 Program terminated with signal SIGSEGV,

Segmentation fault.

5 #0
0x0000562e1631313d in main () at crash.c:6

6 6
*p = 42;

7 (gdb)

Ova poruka govori da je do greške došlo u linĳi broj
6 programa crash i prikazuje nam sadržaj te linĳe
(*p = 42;). Takođe, saznajemo i da je program za-
vršen sa signalom SIGSEGV koji odgovara grešci tipa
Segmentation fault. Dalje u okviru prompta debagera
možemo da koristimo standardne komande, na pri-
mer štampanje vrednosti promenljivih (print p) ili
tekućih registara (info registers) u trenutku kada
je došlo do greške.

1 (gdb) print p

2 $1 = (int *) 0x0

3 (gdb) info registers

4 rax
0x0
0

5 rbx
0x562e16313150

94755940806992

6 ...

### 5.3 Primeri debagera

Debagovanje se najčešće dovodi u vezu sa tradicional-
nim sistemskim i imperativnim programskim jezicima
kao što su C i C++. Međutim, odgovarajući alati postoje
i za druge programske jezike i paradigme.

Upotreba debagera u različitim jezicima ima mnogo
zajedničkih osobina: uobičajene funkcionalnosti uklju-
čuju postavljanje i uklanjanje tačaka prekida, koračanje

<!-- pdf_page=162 printed_page=148 -->

naredbu po naredbu, ispitivanje vrednosti promenljivih
i stanja memorĳe, kao i praćenje kontrole toka izvr-
šavanja. Iako se sintaksa i interfejs mogu razlikovati,
osnovni principi debagovanja ostaju isti i čine sastavni
deo efikasnog procesa razvoja softvera.

Primer 5.3.1 (Debager gdb) Debager gdb je jedan od
najpoznatĳih i najmoćnĳih alata za debagovanje. On
omogućava interaktivno debagovanje, udaljeno de-
bagovanje i debagovanje nakon prekida rada progra-
ma. Dodatno, multiarch gdb omogućava pokretanje i
analizu izvršivih datoteka namenjenih procesorskim
arhitekturama koje su različite od one na kojoj se
debagovanje izvršava.

Gdb je napisan u programskom jeziku C i kontinu-
irano se razvĳa kao deo GNU projekta. Podržava
debagovanje programa napisanih u više programskih
jezika, uključujući Ada, C, C++, Objective-C, Pascal,
Fortran, Go, Rust i Java. GDB se može integrisati u
veliki broj različitih razvojnih okruženja, kao što su
Eclipse, Visual Studio, Qt Creator i CLion. Takođe, gdb
je dostupan na velikom broju operativnih sistema,
uključujući razne Unix i GNU/Linux distribucĳe, kao i
Microsoft Windows platforme.

Primer 5.3.2 (Debager LLDB) Debager LLDB je savre-
meni debager koji se razvĳa kao deo projekta LLVM,
sa ciljem da ponudi efikasnu, modularnu i proširivu
alternativu tradicionalnim alatima za debagovanje.
LLDB omogućava interaktivno debagovanje. U dizaj-
niranju ovog debagera, fokus je bio na ostvarivanje
brzine, lake nadogradivosti i mogućnosti integracĳe
sa modernim alatima.

LLDB je implementiran u programskom jeziku C++ i
kontinuirano se razvĳa u okviru razvoja kompajler-
ske infrastrukture LLVM, odakle i koristi veliki broj

<!-- pdf_page=163 printed_page=5 -->

komponenti. Podržani programski jezici uključuju C,
C++, Objective-C i Swift. LLDB se može integrisati u
različita razvojna okruženja, kao što su Xcode, CLion,
Qt creator i Visual Studio Code.

Debager je prvenstveno razvĳan za Unix-olike ope-
rativne sisteme, uključujući macOS i Linux, ali je u
poslednjim verzĳama proširena i podrška za Microsoft
Windows, iako još uvek u nešto manjoj meri nego kod
debagera GDB. LLDB ima poseban značaj u ekosiste-
mu Apple platformi, gde predstavlja podrazumevani
debager u razvoju aplikacĳa za macOS, iOS i srodne
sisteme.

Primer 5.3.3 (Debageri Visual Studio Debugger i WinDbg)
Debagere Visual Studio Debugger i WinDbg razvĳa kom-
panĳa Microsoft. Oba su namenjena za rad u okviru
Windows operativnih sistema i pored podrške za jezike
C i C++, imaju podršku i za programske jezike zasno-
vane na .NET platformi (uključujući, na primer, C#,
Visual Basic i F#). Oba alata podržavaju interaktivno
debagovanje i post-mortem analizu.

Visual Studio Debugger je duboko integrisan u grafičko
razvojno okruženje Visual Studio i prvenstveno je na-
menjen razvoju korisničkih aplikacĳa, pri čemu nudi
intuitivni korisnički interfejs, automatsku inspekci-
ju vrednosti, vizuelno upravljanje tačkama prekida i
druge udobnosti grafičkog korisničkog interfejsa koje
ga čine pogodnim za svakodnevni razvoj aplikacĳa.

Debager WinDbg je manje poznat u širem krugu pro-
gramera u poređenju sa debagerom Visual Studio
Debugger, ali predstavlja naprednĳi alat sa širim spek-
trom mogućnosti, posebno u kontekstu sistemskog
debagovanja. WinDbg nudi preciznĳu kontrolu i de-
taljnĳi uvid u sistemski kontekst, što ga čini pogodnim
za analizu modula kernela, drajvera, sistemskih kom-
ponenti i složenih grešaka koje se ne mogu lako otkriti

<!-- pdf_page=164 printed_page=150 -->

putem standardnog razvojnog okruženja. Koristi se
kao samostalna aplikacĳa, često iz komandne linĳe, i
zahteva viši nivo tehničkog znanja.

Primer 5.3.4 (Debageri za programski jezik Java) Za
programski jezik Java dostupan je debager jdb koji
je deo standardne Java distribucĳe. Debager jdb se
može koristiti iz komandne linĳe na sličan način
kao i gdb, omogućavajući interaktivno debagovanje
(postavljanje tačaka prekida, koračanje kroz kôd i
ispitivanje vrednosti promenljivih). Takođe, može
se integrisati u razvojna okruženja poput Eclipse i
IntelliJ IDEA, što omogućava grafički interfejs i lakšu
upotrebu. Iako je jdb namenski alat za Javu, moguće
je koristiti za Javu i druge debagere u kombinacĳi
sa specifičnim podešavanjima i prevodiocima koji
generišu izvršivi kôd. Na primer, debager gdb može
da se koristi u kombinacĳi sa kompajlerom Native
Image koji je sastavni deo kompajlerske infrastrukture
GraalVM.

Primer 5.3.5 (Debageri za programski jezik Python)
Za skript jezike takođe postoje odgovarajući debageri.
Na primer, programski jezik Python ima standardni
modul pdb, koji omogućava interaktivno debagova-
nje direktno iz terminala ili integracĳu u razvojne
alate. Modul pdb podržava osnovne debagerske funk-
cĳe: postavljanje tačaka prekida, koračanje kroz kôd i
inspekcĳu stanja programa.

Primer 5.3.6 (Debageri za programski jezik Go) Stan-
dardno okruženje za razvoj u jeziku Go ne dolazi sa
ugrađenim interaktivnim debagerom. Programi napi-
sani u programskom jeziku Go mogu se debagovati
debagerom gdb, ali uz ograničene mogućnosti zbog
modela konkurentnosti koji jezik Go koristi. Najzna-

<!-- pdf_page=165 printed_page=5 -->

čajnĳi i najrasprostranjenĳi alat za debagovanje Go
programa je Delve koji omogućava standardne funk-
cionalnosti interaktivnih debagera. Delve se može
integrisati sa mnogim popularnim razvojnim okru-
ženjima i editorima, uključujući Visual Studio Code
(preko ekstenzĳe za Go) i GoLand, koji razvĳa kompa-
nĳa JetBrains.

Primer 5.3.7 (Debageri za programski jezik JavaScript)
Debagovanje JavaScript koda podržano je kroz širok
spektar alata, kako integrisanih u same veb pregleda-
če, tako i kroz zasebna razvojna okruženja i pomoćne
biblioteke. Najrasprostranjenĳi i najčešće korišćeni
debagerski alati za JavaScript su ugrađeni direktno
u moderne veb pregledače kao što su Google Chrome,
FireFox, Safari i Microsoft Edge.

Primer 5.3.8 (Debageri za programski jezik Haskell)
Debagovanje Haskell programa razlikuje se od deba-
govanja u imperativnim jezicima zbog njegove funk-
cionalne prirode i podrške lenjom izračunavanju. U
ovom jeziku prioritet ima razumevanje evaluacĳe
izraza i praćenje toka podataka kroz čiste funkcĳe,
pa su alati za debagovanje posebno prilagođeni tim
konceptima.

Najpoznatĳi i najčešće korišćeni alat za debagovanje
Haskell programa jeste GHCi Debugger, koji dolazi kao
deo standardnog kompajlera GHCi i koji omogućava
standardno interaktivno debagovanje: postavljanje
tačaka prekida u funkcĳama i praćenje evaluacĳe
izraza korak po korak.

Pored GHCi debagera, programeri se često oslanjaju i
na alate Haskell Tracer Hat i Hoed koji se najviše koriste
za post-mortem analizu izvršavanja Haskell programa.

<!-- pdf_page=166 printed_page=152 -->

### 5.4 Otvoreni problemi

Protivnici debagera
Iako velika većina programe-
ra koristi debagere, postoji
izvesan broj značajnih pro-
gramera koji ne vole deba-
gere i glasno se izjašnjavaju
protiv njihove upotrebe:

Iako je debagovanje ključna tehnika za analizu izvrša-
vanja programa, primenljivost debagera je ograničena.
Jedan od najizraženĳih problema upotrebe debagera
javlja se kod debagovanja višenitnih aplikacĳa. Zbog
konkurentnog izvršavanja više niti, greške mogu zavi-
siti od redosleda izvršavanja koji se teško reprodukuje.
Debageri često ne uspevaju da precizno upravljaju svim
nitima istovremeno, a samo pokretanje aplikacĳe u de-
bageru može promeniti ponašanje programa i redosled
izvršavanja niti, prikrivajući probleme poput trke za
resursima i međusobnog blokiranja. Iako savremeni
debageri podržavaju praćenje pojedinačnih niti, njihova
primena u kompleksnim višenitnim sistemima ostaje
nepraktična, neprecizna i često nedovoljna. Zbog toga se
pronalaženje grešaka u ovakvim aplikacĳama uglavnom
oslanja na kombinovanje više tehnika. Tehnike uključuju
dinamičke pristupe: logovanje, profajliranje, upotrebu
specĳalizovanih sanitajzera za otkrivanje konkurent-
nih grešaka ali i statičku analizu (na primer, tehniku
proveravanje modela).

Rob Pike, jedan od autora
programskog jezika
Go, kaže sledeće
If you dive into the bug,
you tend to fix the local
issue in the code, but if
you think about the bug
first, how the bug came
to be, you often find and
correct a higher-level
problem in the code that
will improve the design
and prevent further
bugs.

Linus Torvalds, kreator
operativnog sistema
Linux, ne koristi
debager.

Robert C. Martin, jedan od
autora agilnog
programiranja, kaže
sledeće
Debuggers are a wasteful
timesink.

Distribuirane aplikacĳe predstavljaju dodatni izazov, jer
njihovo izvršavanje uključuje više nezavisnih kompo-
nenti koje rade na različitim fizičkim mašinama. Tradi-
cionalni debageri nisu dizajnirani za takav kontekst i ne
omogućavaju jedinstveno praćenje toka izvršavanja u
svim delovima sistema.

Debagovanje je takođe problematično u sistemima sa
ugrađenim računarom i aplikacĳama koje rade u re-
alnom vremenu, gde ograničenja resursa i strogi vre-
menski zahtevi ne dozvoljavaju pauziranje programa
ili umetanje dodatnog koda za analizu. U takvim okru-
ženjima debager može biti nepristupačan, a njegovo
korišćenje može dovesti do narušavanja funkcionalnosti
sistema.

Važno ograničenje odnosi se i na debagovanje aplikacĳa
koje su prevedene u režimu za upotrebu. Optimizacĳe

<!-- pdf_page=167 printed_page=5 -->

koje vrši kompajler menjaju strukturu izvršivog koda:
uklanjaju se delovi koda, funkcĳe se spajaju ili reorgani-
zuju, čime se narušava mogućnost jasnog povezivanja
sa izvornim kodom što čini debagovanje značajno ote-
žanim.

Na kraju, kod veoma velikih i kompleksnih sistema,
količina podataka i broj međusobno povezanih kom-
ponenti često prevazilaze mogućnosti praćenja putem
debagera. U takvim slučajevima, debagovanje postaje
sporo, nepregledno i nedovoljno skalabilno.

Zbog svega navedenog, debagovanje se u praksi često
kombinuje sa drugim tehnikama: logovanjem, automat-
skim testiranjem, statičkom analizom i specĳalizovanim
alatima za otkrivanje specifičnih vrsta grešaka. Razu-
mevanje ograničenja debagovanja je ključno kako bi se
odabrala odgovarajuća strategĳa za ispitivanje i ispra-
vljanje softverskih problema.

### 5.5 Štampanje umesto debagera

Štampanje vrednosti promenljivih pomoću funkcĳe

Print umesto debagera

print (odnosno funkcĳe koja vrši štampanje) predstavlja
jednu od prvih tehnika debagovanja koju većina progra-
mera usvaja. Razlog za to je jednostavnost — tehnika
je intuitivna, lako primenljiva i ne zahteva poznavanje
dodatnih alata.

Brian W. Kernighan,

koautor knjige
Programski jezik C i
pionir u razvoju
operativnog sistema
Unix, čĳi su radovi
oblikovali savremeno
sistemsko
programiranje, tvrdi:
The most effective
debugging tool is still
careful thought, coupled
with judiciously placed
print statements.

Ova metoda podrazumeva umetanje naredbe za štam-
panje u ključne delove programa, kako bi se:

▶prikazale trenutne vrednosti promenljivih,
▶pratila kontrola toka (npr. ulazak u funkcĳu, izvr-
šavanje određenih grana uslova, izlazak iz petlji),

▶uočili neočekivani rezultati tokom izvršavanja.

Guido van Rossum, autor
programskog jezika
Python, koristi poziv
funkcĳe print za
90% svog
debagovanja.

Na primer, ako program proizvodi netačan rezultat, pro-
gramer može umetnuti štampanje unutar petlje ili grane
uslova kako bi ispratio kako se vrednosti promenljivih
menjaju. Ovo omogućava osnovni uvid u ponašanje

<!-- pdf_page=168 printed_page=154 -->

programa bez potrebe za korišćenjem spoljašnjih alata
za debagovanje.

Primer 5.5.1 (Print za debagovanje) Funkcĳa suma_-

niza dopunjena je sa pozivom funkcĳe printf unutar
petlje koji služi za praćenje trenutnog indeksa, vred-
nosti elementa niza i trenutne sume. Ovo pomaže da
se uoče greške, npr. ako petlja ide van granica ili ako
se neka vrednost ne sabira kako treba.

1 int suma_niza(int niz[], int duzina) {

2
int suma = 0;

3
for (int i = 0; i < duzina; i++) {

4
printf("niz[%d]=%d, suma=%d\n", i, niz[i],

suma);

5
suma += niz[i];

6
}

7
return suma;

8 }

Uprkos dostupnosti savremenih i veoma moćnih alata
za debagovanje, upotreba štampanja za praćenje toka
izvršavanja programa i dalje je široko rasprostranjena.
Jedan od osnovnih razloga za to jeste jednostavnost ume-
tanja funkcĳe print nasuprot nepoznavanja upotrebe
alata za debagovanje.

Oslanjanje na štampanje kao zamenu za debager danas
se smatra prevaziđenim pristupom iz više razloga:

▶Svaka izmena u vidu umetanja poziva funkcĳe za
štampanje zahteva ponovno prevođenje progra-
ma, što je kod većih projekata vremenski zahtevno.

▶Umetanje poziva funkcĳe za štampanje može pro-
meniti raspored memorĳe programa i time prikriti
ili izmeniti ponašanje greške.

▶Štampanjem se ne mogu lako ispratiti svi relevant-
ni aspekti stanja programa, kao što su sadržaji
registara, vrednosti pokazivača ili stanja steka.

▶Štampanje ne omogućava zaustavljanje programa,
niti interaktivno ispitivanje stanja promenljivih.

<!-- pdf_page=169 printed_page=5 -->

Uprkos tim nedostacima, štampanje ostaje važna do-
punska tehnika jer mogu postojati i opravdani razlozi
za upotrebu štampanja umesto debagera. To su, na
primer:

▶nepostojanje debagera za određenu platformu ili
arhitekturu, i

▶slučajevi kada i sam debager svojim prisustvom
menja ponašanje programa i time otežava detek-
cĳu greške.

U takvim situacĳama, štampanje može predstavljati
poslednje dostupno sredstvo za ispitivanje izvršavanja
programa.

Primer 5.5.2 (Štampanje u programskom jeziku Ha-
skell) Iako postoje specĳalizovani alati za debagova-
nje Haskell programa, programeri često pribegavaju
i osnovnim tehnikama poput umetanja funkcĳa za
ispis (trace) iz paketa Debug.Trace kako bi pratili
tok evaluacĳe izraza prilikom izvršavanja programa.

Uporedna analiza korišćenja debagera i štampanja data
je u tabeli 5.1. Iako korisna, tehnika štampanja ne može
zameniti funkcionalnosti modernih debagera i trebalo
bi je koristiti kao dopunu, tj. kao pragmatičnu i ponekad
neizbežnu pomoćnu tehniku, ali nikako kao osnovnu
metodu za analizu ponašanja programa.

<!-- pdf_page=170 printed_page=156 -->

Tabela 5.1: Poređenje pristupa: print i debager

Print
Debager

Zahteva izmene u izvornom kodu i
ponovno prevođenje

Omogućava analizu bez izmena izvor-
nog koda

Statičan — unapred definisano šta se
prikazuje

Dinamičan — moguće je menjati prika-
zane informacĳe u realnom vremenu

Može prikriti greške ili uticati na iz-
vršavanje programa

Može prikriti greške ili uticati na izvr-
šavanje programa, ali ređe i manje

Uvek moguće koristiti
Nekada debager nĳe dostupan

Pruža delimičan uvid u stanje progra-
ma

Pruža kompletan uvid u stanje progra-
ma

Jednostavno za upotrebu
Kompleksno za upotrebu za početnike

Pogodno za jednostavne analize izvr-
šavanja programa

Pogodno za kompleksne analize izvr-
šavanja programa

Rezime

▶Debager je sistemski alat koji se koristi za pra-
ćenje izvršavanja programa u kojem je potrebno
identifikovati greške.

▶Rad debagera se oslanja na operativni sistem,
hardver i kompajler.

▶Tri osnovna režima prevođenja su režim prevođe-
nja za upotrebu, režim prevođenja za pronalaženje
grešaka i kombinovani režim.

▶Tehnike anti-debagovanja se koriste radi ometanja
ili otežavanja procesa debagovanja.

▶Interaktivno debagovanje je osnovni pristup deba-
govanju koji obuhvata postavljanje tačaka prekida
i tačaka posmatranja, i izvršavanje programa ko-
rak po korak.

▶Udaljeno debagovanje podrazumeva interaktivno
debagovanje pri čemu se aplikacĳa koja se deba-
guje izvršava na jednom, a debager na drugom

<!-- pdf_page=171 printed_page=157 -->

sistemu.

▶Debagovanje nakon prekida izvršavanja progra-
ma omogućava uvid u stanje memorĳe nakon
prekida izvršavanja programa u situacĳama kada
se greške moraju analizirati bez direktnog ponov-
nog izvršavanja programa u identičnim uslovima.

▶Najpoznatĳi debageri su gdb, lldb, Visual Studio
Debugger i WinDbg.

▶Debagovanje ima niz ograničenja i ne može se
uvek primeniti.

▶Štampanje umesto debagovanja je tehnika koja se
smatra prevaziđenom i koju treba koristiti samo
kada ne postoji alternativa.

Literatura

[1]
David J. Agans. Debugging. Amacom, 2002. isbn:
9780814471685.

[2]
Holger Cleve i Andreas Zeller. Locating causes
of program failures. U: Proceedings of the 27th
International Conference on Software Engineering.
ICSE ’05. St. Louis, MO, USA: ACM, 2005., str. 342–
351. doi: 10.1145/1062455.1062522.

[3]
James A. Jones i Mary Jean Harrold. Empirical eva-
luation of the tarantula automatic fault-localization
technique. U: Proceedings of the 20th IEEE/ACM
International Conference on Automated Softwa-
re Engineering. ASE ’05. Long Beach, CA, USA:
ACM, 2005., str. 273–282. doi: 10.1145/1101908.

1101949.

[4]
Andreas Zeller. Why Programs Fail. Morgan Kauf-
mann, 2009. isbn: 978-0-12-374515-6. doi: 10.1016/

B978-0-12-374515-6.X0000-7.

[5]
Andreas Zeller i Ralf Hildebrandt. Simplifying and
Isolating Failure-Inducing Input. U: IEEE Transac-
tions on Software Engineering 28.2 (2002.), str. 183–
200. doi: 10.1109/32.988498.

<!-- pdf_page=172 printed_page=158 -->

Ispitna pitanja

32. Debagovanje. Veza izvršivog koda i debagera. Re-
žim prevođenja za upotrebu. Primeri.

33. Debagovanje. Veza izvršivog koda i debagera. Re-
žim prevođenja za pronalaženje grešaka. Formati
za predstavljanje pomoćnih informacĳa. Primeri.

34. Debagovanje. Veza izvršivog koda i debagera.
Kombinovani režimi prevođenja. Primeri.

35. Debagovanje. Veza izvršivog koda i debagera.
Anti-debagovanje.

36. Debagovanje. Vrste debagovanja. Interaktivno de-
bagovanje. Implementacĳa interaktivnog debago-
vanja, tačaka prekida i tačaka posmatranja. Prime-
ri.

37. Debagovanje. Vrste debagovanja. Udaljeno deba-
govanje. Debagovanje nakon prekida izvršavanja
programa. Primeri.

38. Debagovanje. Primeri debagera.
39. Debagovanje. Otvoreni problemi.
40. Debagovanje. Štampanje umesto debagera. Prime-
ri.

<!-- pdf_page=173 printed_page=173 -->

Pregled

6.1
Instrumentacĳa 160

6.2
Profajleri . . . . 166

▶Šta je instrumentacĳa i kako se ona koristi?
▶Koja je uloga profajliranja, a koja sanitiziranja u
procesu razvoja softvera?

6.3
Alati za dina-
mičku detekcĳu
grešaka . . . . . 183

▶Koje vrste profajlera postoje?
▶Koji su najpoznatĳi sanitajzeri i šta oni omoguća-
vaju?

U procesu razvoja softvera, naročito složenih i zahtevnih
sistema, neophodno je osigurati efikasnost i pouzdanost
krajnjeg proizvoda. Za postizanje ovih ciljeva koriste se
različiti alati za dinamičku analizu programa i detekcĳu
grešaka, od kojih se izdvajaju profajleri i sanitajzeri. Ovi
alati omogućavaju detaljno praćenje ponašanja softvera
tokom njegovog izvršavanja, ali na drugačĳi način u
odnosu na debagere.

Profajleri prikupljaju informacĳe o performansama pro-
grama — na primer, koliko često se izvršavaju određene
funkcĳe, koliko vremena se troši u različitim delovima
koda i koliko se memorĳe i ostalih resursa koristi. Profaj-
leri se koriste kada postoje problemi sa performansama
i kada je potrebno optimizovati kôd, najčešće u kasni-
jim fazama razvoja, kada su osnovne funkcionalnosti
sistema implementirane.

Sanitajzeri, s druge strane, fokusirani su na automatsku
detekcĳu grešaka koje mogu dovesti do nestabilnosti,
kvarova ili sigurnosnih propusta. Oni identifikuju pro-
bleme kao što su pristupi neinicĳalizovanoj ili nealoci-
ranoj memorĳi, curenje memorĳe ili greške u pristupu
podacima kod višenitnih aplikacĳa. Sanitajzeri se mogu
koristiti da olakšaju pronalaženje uzroka uočenog de-
fekta u kodu, ali i za proveru da li kôd sadrži greške čak
i onda kada nema uočenih defekata. Sanitajzeri mogu

<!-- pdf_page=174 printed_page=160 -->

da se koriste i u ranĳim fazama razvoja, odnosno nĳe
neophodno čekati na potpunu implementacĳu funkcio-
nalnosti sistema. Naziv sanitajzer vezuje se za porodicu
alata koji rade u fazi kompilacĳe. Pored sanitajzera, po-
stoji i veliki broj drugih alata koji imaju za cilj otkrivanje
sličnih vrsta grešaka. Većina tih alata je komercĳalne
prirode.

U tabeli 6.1 data je uporedna analiza profajlera i alata
za dinamičku detekcĳu grešaka. Razumevanje rada i
primene profajlera i alata za dinamičku detekcĳu greša-
ka predstavlja osnovu za efikasno testiranje, analizu i
unapređenje softverskih sistema.

Tabela 6.1: Poređenje profajlera i detektora grešaka

Karakteristika
Profajleri
Dinamička detekcĳa grešaka

Cilj upotrebe
Za odabir delova koda
koji treba optimizovati

Za otkrivanje grešaka u kodu

Šta meri ili prati
Vreme izvršavanja, broj
poziva funkcĳa, memorĳ-
ska potrošnja, promašaji
u keš memorĳi...

Neispravni pristupi memorĳi,
curenja memorĳe, nesinhroni-
zovan pristup podacima u vi-
šenitnim aplikacĳama, neinici-
jalizovane promenljive...

Vrsta analize
Kvantitativna: koliko se
šta koristi?

Kvalitativna: da li postoje gre-
ške, koje i gde?

Faza razvoja
U kasnim fazama, kada
je funkcionalnost imple-
mentirana

U ranim fazama

Primeri alata
gprof, perf, VTune, Call-
grind, Cachegrind, Java
Flight Recorder, Visual Stu-
dio Profiler, Instruments,
dotTrace, cProfile, JProfiler,
YourKit

Sanitajzeri: ASan, MSan, TSan,
UBSan. Alati: Memcheck, Massif,
Helgrind, DRD, BoundsChecker,
Purifier, Insure++, Intel Inspec-
tor, Go race detector

### 6.1 Instrumentacĳa

Instrumentacĳa (eng. instrumentation) je proces dodava-

<!-- pdf_page=175 printed_page=6 -->

nja instrukcĳa u program kako bi se tokom njegovog
izvršavanja, pratile određene pojave i prikupljali poda-
ci o njegovom ponašanju. Instrumentacĳa se koristi u
jednoj vrsti profajlera kao i u sanitajzerima i drugim
alatima za dinamičko otkrivanje grešaka.

Najvažnĳe osobine koje dobra instrumentacĳa treba da
zadovolji su:

1. Ne utiče na funkcionalnost programa.

2. Prikuplja sve neophodne podatke i samo njih.
3. Ne usporava previše rad programa.
4. Ne povećava previše upotrebu memorĳe.

Prvi uslov ističe da ukoliko dodata instrumentacĳa utiče
na funkcionalnost programa onda prikupljeni podaci
neće oslikavati pravi način njegovog rada. Drugi uslov
je važan jer prikupljanje nepotrebnih podataka dodatno
usporava program i samu njihovu obradu, dok premalo
informacĳa može biti beznačajno.

Preterano usporavanje rada programa može da vodi do
praktične neupotrebljivosti programa zbog instrumenta-
cĳe. Na primer, ako izvršavanje programa traje jedan sat,
a usporenje koje instrumentacĳa nameće izvršavanju je
sto puta, onda izvršavanje instrumentovanog programa
traje 100 sati što je prilično nepraktično. Slično, ako pro-
gram već zahteva upotrebu velike količine memorĳe,
onda povećanje potrošnje memorĳe može da utiče na
to da instrumentovan program ne može da stane na
uređaj na kojem treba da se izvršava. Usporavanje i po-
većavanje upotrebe memorĳe zavise od tipa aplikacĳe i
mogu se kontrolisati izborom delova programa koji se
instrumentuju.

Primer 6.1.1 (Uređaji koji rade u realnom vremenu)
Usporavanje rada programa koje je posledica instru-
mentacĳe je posebno važno u kontekstu sistema koji
treba da rade u realnom vremenu. Ovi sistemi često
imaju vrlo stroga vremenska ograničenja koja se in-

<!-- pdf_page=176 printed_page=162 -->

strumentacĳom mogu poremetiti (prekršiti) i time
onemogućiti relevantnu smislenu analizu rada ure-
đaja. Dodatno, problem mogu da budu i memorĳska
ograničenja uređaja jer dodatni kôd za instrumentaci-
ju i njeno rukovanje može uvećati program tako da
on ne može da stane na uređaj.

Instrumentacĳa se može klasifikovati prema načinu na
koji se nove instrukcĳe dodaju u program: može je vršiti
programer ili se može vršiti automatski. Programer mo-
že izvršiti instrumentacĳu dodavanjem i inkrementira-
njem brojača na željenim mestima u kodu. Automatsku
instrumentacĳu može da sprovodi:

▶kompajler i/ili linker tokom prevođenja i linkova-
nja programa,

▶specĳalizovani alat na već prevedenom (izvrši-
vom) programu i

▶specĳalizovani alat tokom samog izvršavanja pro-
grama.

Instrumentacĳa se može vršiti prilikom proizvoljne vrste
prevođenja kao i nad proizvoljnom izvršivom verzĳom
programa. Za dinamičku analizu koja ima za cilj ot-
krivanje grešaka, obično je poželjno debag prevođenje
(ili verzĳa) programa, dok je za praćenje performansi
najčešće neophodno koristiti riliz prevođenje (verzĳu)
programa, odnosno onu verzĳu programa koja će biti
isporučena korisniku (jer je za tu verzĳu ključno izmeriti
performanse).

Primer 6.1.2 (Manuelna instrumentacĳa) Dodava-
njem globalne promenljive brojac_saberi i njenim
inkrementiranjem unutar funkcĳe saberi moguće je
izbrojati pozive ove funkcĳe tokom izvršavanja progra-
ma. Na kraju rada programa potrebno je odštampati
vrednost ove promenljive kako bi se prikazao rezultat
brojanja, ili sačuvati tu vrednost u nekoj datoteci.

1 int brojac_saberi = 0;

2 int saberi(int a, int b) {

<!-- pdf_page=177 printed_page=6 -->

3
brojac_saberi++;

Ime alata Valgrind (izgovara
se Velgrind, između a i e) po-
tiče iz nordĳske mitologĳe,
gde Valgrind označava glav-
nu kapĳu koja vodi u Val-
halu (eng. Valhalla) — Odi-
novu dvoranu u koju ulaze
duše palih ratnika. Odin je
vrhovni bog u nordĳskoj
mitologĳi, bog mudrosti, po-
ezĳe, rata i smrti. Valgrind je
simbolično opisan kao širo-
ka, čvrsta kapĳa kroz koju
prolaze samo oni koji su do-
stojni Odinove časti i poziva.

4
return a + b;

5 }

Manuelna instrumentacĳa se u praksi gotovo nikada
ne primenjuje. Ovde se koristi kao ilustracĳa, jer se
sličan kôd automatski ubacuje, bilo putem kompajlera,
bilo putem specĳalizovanih alata.

Instrumentacĳa u fazi izvršavanja

Valgrind je platforma koja omogućava izvršavanje pro-
grama, njegovu instrumentacĳu u fazi izvršavanja i sni-
manje izveštaja koji nastaju prilikom analize izvršavanja
programa. Valgrind se koristi kao osnova za pravljenje
alata za dinamičku analizu programa: profajlera i alata
za dinamičku detekcĳu grešaka u programima.

Autori alata su ovo ime oda-
brali kako bi dočarali ideju
ulaska u „unutrašnjost“ pro-
grama: kao što Valgrind u
mitologĳi otvara put u svet
hrabrih ratnika, tako i sof-
tverski Valgrind omogućava
programerima da zavire u
unutrašnje stanje svojih apli-
kacĳa, otkrivajući greške i
nedostatke koje inače ne bi
mogli da vide. Ovo ime isti-
če ulogu alata kao „čuvara
kapĳe“ između uobičaje-
nog izvršavanja programa i
njegove detaljne analize na
nivou memorĳe i performan-
si.

Svi Valgrind alati rade na istoj osnovi koja obuhvata
podršku za izvršavanje i snimanje rezultata analize, kao
i interfejs ka definisanju instrumentacĳe. Informacĳe
koje se emituju variraju u zavisnosti od zadate instru-
mentacĳe koja je specifična za svaki pojedinačni alat:

Valgrind + Instrumentacĳa = Alat za dinamičku analizu

Izazovi uspešnog rada alata zasnovanog na platformi
Valgrind sastoje se, pre svega, u sklapanju dva procesa
u jedan: program koji se analizira i program alata se
sklapaju u jedan proces. Mnogi resursi se dele između
ova dva programa, kao što su registri ili memorĳa, i
potrebno ih je pravilno uskladiti.

Dostupnost Valgrinda
Valgrind je sistemski i arhi-
tekturalno zavisni alat koji
radi na sledećim platforma-
ma:

Prilikom analize izvršavanja programa nĳedan deo pro-
grama koji se analizira se ne izvršava u svom izvornom
obliku. Valgrind deli originalni kôd u sekvence koje
se nazivaju osnovni blokovi. Osnovni blok je linearna
sekvenca mašinskog koda, na čĳi se početak dolazi ne-
kom naredbom skoka, koja u sebi ne sadrži grananja,
pozive funkcĳa ili skokove, i koja se završava sa sko-
kom, pozivom funkcĳe ili naredbom povratka u funkcĳu

Linux - x86, AMD64, ARM,
ARM64, PPC32,
PPC64, S390X,
MIPS32, MIPS64

Solaris - x86, AMD64
Android - ARM, ARM64,
x86, MIPS32

Darwin - x86, AMD64 (Mac
OS X 10.12)

<!-- pdf_page=178 printed_page=164 -->

pozivaoca. Veličina osnovnog bloka je ograničena na
maksimalno šezdeset mašinskih instrukcĳa. Valgrind
dopunjava mašinski kôd programa kodom koji vrši
instrumentacĳu. Dopunjavanje se vrši pojedinačno po
osnovnim blokovima, neposredno pre prvog izvršava-
nja samog bloka.

Proces transformisanja koda se sastoji iz podizanja ori-
ginalnog mašinskog koda u odgovarajuću međurepre-
zentacĳu (eng. intermediate representation) koja se zatim
instrumentuje i ponovo prevodi u novi mašinski kôd.

disasembliranje

Izgradnja optimizovane međureprezentacĳe sastoji se
od disasembliranja (Valgrind vrši podizanje ma-
šinskog koda programa u internu međureprezen-
tacĳu) i standardnih optimizacĳa programskih
prevodilaca (kao što su uklanjanje redundantnog
koda i eliminacĳa zajedničkih podizraza). Disa-
sembliranje je arhitekturalno zavisno.

optimizacĳa 1

instrumentacĳa

Instrumentacĳa se vrši nad generisanom međurepre-
zentacĳom. Blok koda u međureprezentacĳi se
prosleđuje alatu, koji može proizvoljno da ga trans-
formiše. Alat u zadati blok dodaje novi međukod,
kojim proverava ispravnost ili prati i skuplja infor-
macĳe o radu programa.

optimizacĳa 2

izgradnja grafa

Prevođenje u izvršivi kôd obuhvata optimizacĳe, iz-
gradnju grafa, odabir instrukcĳa, alokacĳu regi-
stara i asembliranje. Druga faza optimizacĳe je
jednostavnĳa od prve i uključuje samo izračuna-
vanje vrednosti izraza koji se mogu izračunati pre
faze izvršavanja i uklanjanje mrtvog koda. Zatim
se od međureprezentacĳe kreira stablo radi lakšeg
odabira instrukcĳa. Prilikom odabira instrukcĳa,
koriste se virtuelni registri koji se određuju u fazi
alokacĳe registara. Na kraju, u fazi asembliranja,
kôd se prevodi u mašinski i smešta se u odgovara-
jući blok memorĳe. Odabir instrukcĳa, alokacĳa
registara i asembliranje su arhitekturalno zavisni.

odabir instrukcĳa

alokacĳa
registara

asembliranje

Razvoju platforme Valgrind
doprinela je Aleksandra Ka-
radžić, diplomirani master
student Matematičkog fakul-
tata. Njena master teza:
Alat Valgrind — Implementacĳa
konvencĳe FPXX za arhitekturu
MIPS

Sve faze procesa transformacĳe koda obavlja Valgrind,
osim instrumentacĳe koju obavlja odgovarajući alat. Re-

<!-- pdf_page=179 printed_page=6 -->

Mašinski kôd

0110001010
1010110101
0110101011

Disasembliranje

Međukod

Originalni međukôd

Optimizacĳa 1

Redundantan originalni
međukôd, podizrazi...

Dodatni međukôd
Mrtav međukôd,
izrazi koji se
mogu izračunati
pre izvršavanja

Instrumentacĳa

Optimizacĳa 2

Izgradnja grafa

Instrukcĳe,
virtuelni registri

Instrukcĳe,
izabrani registri

Odabir instrukcĳa

Virtuelni
registri

Alokacĳa registara

Registri

Asembliranje

0111000101
0010101010
1101010101
0101110010
1110100010

Slika 6.1: Faze transformacĳe koda koje su neophodne radi instrumentacĳe koda u fazi izvršavanja
(platforma Valgrind)

<!-- pdf_page=180 printed_page=166 -->

zultat procesa transformacĳe koda se čuva u memorĳi i
izvršava se po potrebi. Valgrind troši najviše vremena
na sam proces transformacĳe koda, kao i na pronalaže-
nje i izvršavanje transformisanog koda. Usporenje koje
Valgrind nameće izvršavanju programa je od 5 do 100
puta, u zavisnosti od konkretnog alata.

Najpoznatĳi Valgrind alati su:

Kako Valgrind i njegovi alati
ne analiziraju izvorni kôd
već mašinski kôd programa,
to znači da ih je moguće
koristiti za analizu progra-
ma napisanih u bilo kom
programskom jeziku. Ipak,
najčešće se koriste za ana-
lizu programa napisanih
u jezicima C i C++ jer su i
greške koje se analiziraju i
prate karakteristične za te
jezike.

▶Memcheck — detektor memorĳskih grešaka,
▶Massif — detektor memorĳskih grešaka praće-
njem upotrebe dinamičke memorĳe,

▶Cachegrind — profajler keš memorĳe,
▶Callgrind — profajler funkcĳa,
▶Helgrind i DRD — detektori grešaka višenitnog
izvršavanja.

### 6.2 Profajleri

Važan deo testiranja performansi odnosi se na merenje
vremenske i memorĳske efikasnosti programa. Ukoliko
program ne zadovoljava postavljene kriterĳume perfor-
mansi, neophodno je identifikovati uzroke i sprovesti
odgovarajuće optimizacĳe. Proces optimizacĳe pred-
stavlja sastavni i neizostavan deo razvoja softverskih
sistema, jer obezbeđuje da implementacĳa ispunjava
zahteve u pogledu brzine izvršavanja i potrošnje resur-
sa.

Kako bi se precizno identifikovali delovi koda koji za-
htevaju poboljšanje, u praksi se koriste specĳalizovani
pomoćni alati — profajleri — koji generišu detaljne in-
formacĳe o ponašanju programa tokom izvršavanja. Na
osnovu ovih informacĳa donose se odluke o prioritetima
i načinima optimizacĳe.

Profajliranje je vid dinamičke analize programa. Profajli-
ranjem se tokom izvršavanja programa nad unapred de-
finisanim skupom ulaznih podataka prikupljaju detaljni

<!-- pdf_page=181 printed_page=6 -->

podaci o ponašanju programa u realnim uslovima. Re-
zultat ovog procesa je skup podataka poznat kao profil
programa. Profil može da obuhvata različite informaci-
je, uključujući frekvencĳe poziva funkcĳa i izvršavanja
osnovnih blokova koda, procenat ukupnog vremena
utrošenog u pojedinačnim delovima koda, informacĳe
o korišćenju memorĳe — uključujući alokacĳe i dealo-
kacĳe — zatim učestalost promašaja u kešu procesora,
kao i redosled zaključavanja i otključavanja katanaca
prilikom višenitnog izvršavanja.

Profajliranje može biti implementirano softverski, oslo-
njeno na podršku hardvera ili kao kombinacĳa oba
pristupa. Kada se koristi hardverska podrška, profajli-
ranje postaje efikasnĳe i omogućava prikupljanje šireg
spektra podataka. Za određene vrste merenja, poput
broja promašaja u keš memorĳi ili vremena utrošenog
zbog čekanja u protočnoj obradi instrukcĳa (eng. pipeline
stall), hardverska podrška je neophodna.

Profajliranje se može zasnivati na instrumentacĳi, tj. uba-
civanju dodatnih instrukcĳa u kôd radi preciznog pra-
ćenja ponašanja programa tokom izvršavanja, ili na
uzorkovanju (eng. sampling), gde se povremeno beleže
karakteristični podaci o stanju sistema. Obe tehnike
imaju svoje prednosti i ograničenja, a izbor tehnike,
tj. odgovarajućeg alata, treba načiniti u skladu sa za-
htevima za preciznošću i dozvoljenim opterećenjem
sistema.

6.2.1 Upotreba profila

Profil programa se može upotrebljavati na različite na-
čine, u zavisnosti od informacĳa koje on sadrži. Najče-
šća upotreba je identifikacĳa tzv. vrućih delova koda
(eng. hot spots). To su delovi koda koji se najčešće iz-
vršavaju ili koji najviše doprinose ukupnom vremenu
izvršavanja, što je od suštinskog značaja za optimizacĳu
performansi. Takođe, profil može da posluži za procenu
pokrivenosti koda datim skupom testova, čime se dobĳa

<!-- pdf_page=182 printed_page=168 -->

uvid na koji način dalje proširiti skup testova sa ciljem
da se dobĳe veća pokrivenost koda. Pored toga, profil
se može koristiti i za detektovanje curenja memorĳe i
raznih grešaka u kodu.

Optimizacĳu na osnovu profila može da izvrši pro-
gramer, a može je automatski sprovesti i programski
prevodilac. Samo programer može da suštinski izmeni
algoritam koji se koristi u implementacĳi ali i automat-
ska optimizacĳa može da napravi važna poboljšanja u
efikasnosti koda.

Primer 6.2.1 Razmotrimo aplikacĳu koja obrađuje
tekst i broji koliko puta se svaka reč pojavljuje u
datoteci.

Profajliranjem je utvrđeno da se najviše vremena
troši na ponovljeno pretraživanje liste reči kako bi
se proverilo da li se neka reč već pojavila. Kako lista
raste, ova operacĳa postaje sve sporĳa.

Na osnovu toga, programer može optimizovati kod
zamenom liste odgovarajućom heš mapom, gde se
provera postojanja i ažuriranje broja pojavljivanja oba-
vlja u konstantnom vremenu. Ova izmena značajno
poboljšava performanse, posebno za velike ulazne
tekstove.

Automatska optimizacĳa može da se sprovodi u fazi
kompilacĳe pre izvršavanja programa ili u fazi kom-
pilacĳe tokom izvršavanja programa. U oba slučaja,
optimizacĳe koje se sprovode na osnovu profila progra-
ma nazivaju se optimizacĳe vođene profilom (eng. profile
guided optimizations). Ove optimizacĳe značajno pobolj-
šavaju performanse i prevazilaze domete standardnih
kompajlerskih optimizacĳa.

Optimizacĳa u fazi kompilacĳe pre izvršavanja pro-
grama, da bi mogla da se sprovede, zahteva da je
profil programa dostupan, što znači da toj kom-
pilacĳi prethodi jedna kompilacĳa i izvršavanje

<!-- pdf_page=183 printed_page=6 -->

programa sa ciljem prikupljanja profila. Priku-
pljanje profila koji je potreban za optimizacĳu je
često veoma zahtevan posao koji značajno tro-
ši memorĳske i vremenske resurse. Zbog toga se
umesto prikupljanja profila, nekada koriste statički
profajleri, odnosno predviđanje profila metodama
mašinskog učenja na osnovu karakteristika koda.
Na primer, obrada grešaka i izuzetaka odgovara-
ju putanjama programa koje se ređe izvršavaju
u odnosu na glavne funkcionalnosti programa.
Modeli mašinskog učenja mogu da nauče takve i
kompleksnĳe zakonitosti i da na osnovu statičkih
osobina koda predvide koji će se delovi programa
najčešće izvršavati.

Razvoju statičkih profajlera
modelima mašinskog učenja
aktivno doprinosi i dr Milan
Čugurović, sa Matematičkog
fakulteta:
GraalSP: Polyglot, efficient, and
robust machine learning-based
static profiler
Njegova doktorska teza:
Predviđanje profila izvršavanja
programa tehnikama mašinskog
učenja

Optimizacĳa u fazi kompilacĳe tokom izvršavanja pro-

grama je karakteristična za kompilacĳu u toku
izvršavanja‗ (eng. Just-In-Time compilation, JIT).
Kompilacĳa u toku izvršavanja koristi profil koji
se dobĳa tokom izvršavanja da bi se donele odluke
o tome da se neki delovi koda kompiliraju, umesto
interpretiraju, i da se dodatno optimizuju.

6.2.2 Kvalitet profila

Na izvršavanje programa utiču konkretni ulazi i razli-
čiti ulazi daju različite rezultate profajliranja. Da bi se
donosile odluke o optimizacĳi na osnovu profajliranja,
važno je da izvršavanje u okviru kojeg se vrši profaj-
liranje reflektuje realnu upotrebu programa, odnosno
da su skupljeni podaci na osnovu relevantnih ulaznih
podataka ili da su skupljeni podaci na osnovu više razli-
čitih skupova ulaznih podataka. U suprotnom, mogu se
propustiti prilike za optimizacĳu programa ili se mogu
doneti pogrešne odluke.

‗ Kompilacĳa u toku izvršavanja je karakteristična za sve jezike koji
se izvršavaju na Javinoj virtuelnoj mašini, na primer Java, Scala i
Kotlin.

<!-- pdf_page=184 printed_page=170 -->

Primer 6.2.2 (Propuštena prilika) Razmotrimo funkci-
ju koja vrši obradu elemenata niza algoritmom kubne
složenosti i pretpostavimo da se ta funkcĳa u praksi
koristi nad velikim nizovima. Ukoliko se program pro-
fajlira sa ulazom koji funkcĳi prosleđuje niz sa malim
brojem elemenata, onda se profajliranjem ne može
uočiti problem koji će nastati u praksi, jer kubna slože-
nost za mali niz može i dalje da daje zadovoljavajuće
performanse.

Primer 6.2.3 (Pogrešne odluke) Razmotrimo funkcĳu
𝑓koja ima naredbu grananja u okviru koje se u then
grani poziva funkcĳa 𝑓𝑡ℎ𝑒𝑛, a u else grani funkcĳa
𝑓𝑒𝑙𝑠𝑒. Pretpostavimo da se u praksi then grana izvr-
šava 20 puta češće nego else grana ali da su ulazni
podaci za profajliranje izabrani tako da nas vode u

else granu. Na osnovu takvog profajliranja, može
da se donese pogrešan zaključak, tj. da je potrebno
optimizovati funkcĳu 𝑓𝑒𝑙𝑠𝑒. Optimizacĳa te funkcĳe u
praksi neće davati vidljive rezultate, s obzirom na to
da se ona retko izvršava.

Prilikom optimizacĳe na osnovu dobĳenih profila va-
žno je pronaći ravnotežu između vremena utrošenog
na prikupljanje podataka i koristi od dobĳenih informa-
cĳa. U početnim fazama optimizacĳe mogu se koristiti
jednostavnĳe i manje precizne metode kako bi se identi-
fikovali najveći problemi. Kako optimizacĳa napreduje,
preostale prilike za unapređenje postaju suptilnĳe, što
zahteva preciznĳe tehnike profajliranja.

6.2.3 Profajliranje uzimanjem uzoraka

Profajler zasnovan na uzorkovanju (eng. sample based pro-
filer) periodično prekida izvršavanje programa, najčešće
u fiksnim vremenskim intervalima, koristeći prekide
operativnog sistema. Prilikom svakog prekida, profajler

<!-- pdf_page=185 printed_page=6 -->

snima stek poziva (eng. call stack) svake niti, beležeći niz
aktivnih funkcĳskih poziva u tom trenutku. Prikupljeni
podaci se zatim agregiraju tako da budu pogodni za
analizu.

Na osnovu dovoljno velikog broja uzoraka i za dobro iza-
brane intervale merenja, moguće je napraviti preciznu
statističku procenu koji delovi koda se najčešće izvrša-
vaju ili gde se troši najviše vremena. Uzorkovanje pruža
statističku aproksimacĳu, a ne precizno merenje broja
poziva ili vremena izvršavanja. Ako se funkcĳa izvršava
vrlo brzo i retko, moguće je da neće biti obuhvaćena
uzorkovanjem.

Ovaj pristup omogućava programu da se izvršava go-
tovo punom brzinom, što ga čini pogodnim za velike
i složene aplikacĳe, dugotrajne aplikacĳe i sisteme u
realnom vremenu. Dodatno, nĳe potrebno ponovno pre-
vođenje izvornog koda već se profajliranje uzimanjem
uzoraka može vršiti nad proizvoljnim izvršivim dato-
tekama (ali prisustvo debag simbola može da poboljša
analizu i interpretacĳu rezultata).

Najpoznatĳi alati koji vrše profajliranje uzorkovanjem
su perf, oprofile, gprof (kombinacĳa uzorkovanja i in-
strumentacĳe), Visual Studio Profiler (ima podršku i za
instrumentaciono profajliranje), Intel VTune Profiler, Go-
ogle CPU Profiler i Instruments (Xcode).

Primer 6.2.4 (perf) Alat perf uveden je kao deo Li-
nux kernela verzĳe 2.6.31, objavljene u septembru
2009. godine. Cilj alata bio je da zameni starĳe i manje
fleksibilne alate za profajliranje uzorkovanjem, poput
alata oprofile, kao i da pruži moderan interfejs za kori-
šćenje savremenih ugrađenih hardverskih brojača za
performanse (eng. performance monitoring units). Od
tada se perf aktivno razvĳa zajedno sa Linux kerne-
lom i održava ga Linux kernel zajednica, uz značajan
doprinos programera iz kompanĳa kao što su Red Hat,
Intel, Google u IBM.

<!-- pdf_page=186 printed_page=172 -->

Perf pruža statistički pregled vremena izvršavanja i
resursa koje program koristi. Zahvaljujući malim tro-
škovima upotrebe i visokoj preciznosti, perf je postao
standardni alat za profajliranje na Linux platformama.
Njegova fleksibilnost omogućava primenu kako na
nivou pojedinačnih procesa, tako i na nivou celog
sistema, a rezultati mogu biti prikazani tekstualno ili
vizuelno.

Primer 6.2.5 (Plameni graf u Javi) Plameni graf (eng. fla-
me graph) je vizuelizacĳa koji se koristi za analizu per-
formansi softvera, posebno za identifikovanje uskih
grla i razumevanje upotrebe resursa. Plameni graf se
generiše na osnovu rezultata rada profajlera.

Primer dela plamenog grafa za program Game of Life
u Javi čĳi je deo koda prikazan u listingu 6.1 dat je na
slici 6.2. Primer pokazuje da se u programu najviše
vremena troši redom u metodama koje pozivaju me-
tod main, koja zatim poziva metod run u okviru koje
se najviše vremena troši u metodama nextGeneration i
printGrid. Histogram u dnu slike pokazuje sortirano
koliko najviše vremena se troši u pojedinačnim meto-
dama isključujući vreme koje troše funkcĳe koje su iz
njih pozvane. Dakle, najviše vremena se troši u funkci-
ji koja preuzima karaktere getChars, a zatim i u funkcĳi
koja računa narednu generacĳu nextGeneration.

Listing 6.1: Deo koda aplikaci-
je Game of Life
1 import java.io.FileWriter;

2

3 // A simple Java program to implement Game of

Life

4 // Modified from https://www.geeksforgeeks.org/

program-for-conways-game-of-life/

5 public class GameOfLife {

6
...

7
public static void main(String[] args) {

8
new GameOfLife().run();

9
}

10
private void run() {

<!-- pdf_page=187 printed_page=6 -->

11
// Initializing the grid.

12
int[][] grid = newGrid();

13
printGrid(grid);

14
for (int i = 0; i < GENERATIONS; i++) {

15
grid = nextGeneration(grid);

16
printGrid(grid);

17
}

18
}

19
...

20
static int[][] nextGeneration(int[][] grid) {

21
int[][] future = new int[M][N];

22
// Loop through every cell

23
for (int l = 0; l < M; l++) {

24
for (int m = 0; m < N; m++) {

25
...

26
}

27
}

28
return future;

29
}

30

31
private static void printGrid(int[][] grid) {

32
try (FileWriter myWriter = new FileWriter("f

")) {

33
for (int i = 0; i < M; i++) {

34
for (int j = 0; j < N; j++) {

35
if (grid[i][j] == 0)

36
myWriter.write(".");

37
else

38
myWriter.write("*");

39
}

40
myWriter.write(System.lineSeparator

());

41
}

42
} catch (Exception e) {

43
throw new IllegalStateException();

44
}

45
}

46
...

Plameni graf je obično interaktivan prikaz poziva
metoda tokom izvršavanja programa. Svaka traka
(pravougaonik) odgovara pozivu jedne metode, a
svaki „plamen“ odgovara jednom nizu poziva metoda.

<!-- pdf_page=188 printed_page=174 -->

Slika 6.2: Deo plamenog grafa za izvršavanje programa Game of Life u Javi

Širina svake trake proporcionalna je vremenu koje je
program proveo u tom metodu i metodama koje su iz
njega pozvane.

Plameni graf na pregledan način prikazuje veliki broj
uzoraka i pomaže u donošenju odluka o prioritetima
u optimizacĳi performansi. Vizuelni prikaz putanja
poziva olakšava i otkrivanje neočekivanih redosleda
izvršavanja ili neefikasnih rekurzivnih poziva.

6.2.4 Instrumentaciono profajliranje

Informacĳe o pokriveno-
sti koda se generišu nakon
završetka rada programa.
Međutim, specifičnosti ne-
kih programa, poput serve-
ra, operativnih sistema ili
sistema za rad u realnom
vremenu, zahtevaju uvid u
pokrivenost i pre završetka
rada programa. Jedno reše-
nje za prikazivanje podataka
o pokrivenosti koda u fazi
izvršavanja može se videti u
master radu Marine Nikolić:
Prikupljanje i prikaz podataka o
izvršavanju programa

Instrumentacĳom se mogu pratiti najrazličitĳe karakte-
ristike izvršavanja programa. Profili koji se koriste za
određivanje delova koda koji se najčešće izvršavaju kao i
tačni udeli učestalosti izvršavanja različitih delova koda,
za kompajlerski zasnovane optimizacĳe i za utvrđiva-
nje pokrivenosti koda testovima, dobĳaju se na osnovu
sledećih vrsta profajliranja:

1. profajliranje putanja,

2. profajliranje grana i
3. profajliranje blokova.
