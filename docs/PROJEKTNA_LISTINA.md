# Projektna listina (Project Charter) in definicija MVP – DijakPomaga

Srednja elektro-računalniška šola Maribor · PTI – Tehnik računalništva · Modul: Računalniški produkti in storitve (RPS) · Šolsko leto 2026/2027

## Podatki o skupini

- **Ime projektne ekipe:** DijakPomaga
- **Izbran projekt:** Dijaško tutorstvo – spletna platforma za medsebojno pomoč dijakov
- **Člani ekipe:** Marko Laptuš, Timotej Pučko, Lan Lerher (2. D)
- **Mentor:** Sergej Lah
- **GitHub repozitoriji članov:**
  - Marko Laptuš: https://github.com/LovkarDijak/rps-skupinski-projekt (spletna stran: https://lovkardijak.github.io/rps-skupinski-projekt/)
  - Timotej Pučko: (dopolni)
  - Lan Lerher: (dopolni)

## 1.) Razdelitev vlog v ekipi

| Vloga v ekipi | Ime in priimek | GitHub | Glavne zadolžitve |
|---|---|---|---|
| Vodja ekipe & Backend razvijalec | Marko Laptuš | @LovkarDijak | Načrtovanje PHP logike, usklajevanje delovnega toka. |
| Frontend razvijalec | Timotej Pučko | @ (dopolni) | Izdelava semantičnega HTML5 vmesnika s Pico.css: obrazec za prošnjo, seznam in filter. |
| Skrbnik podatkovne baze & cPanel | Marko Laptuš | @LovkarDijak | Načrtovanje MariaDB tabel (prosnje, odzivi), namestitev na šolski strežnik. |
| Testiravec & Dokumentalist | Lan Lerher | @ (dopolni) | Vodenje GitHub Projects (Kanban), testiranje napak, README. |

## 2.) Opredelitev problema in cilja projekta

**1. Kateri konkreten problem rešujemo?**

Dijaki na SERŠ ob težavah pri učenju pomoč iščejo pri sošolcih na Discordu ali v zasebnih sporočilih. Vprašanja se med drugimi sporočili hitro izgubijo, dijak pa ne ve, kdo na šoli zna določeno snov. Dijaki, ki bi radi pomagali, nimajo mesta, kjer bi pomoč ponudili. Zato dijak na odgovor pogosto čaka več dni ali pa ga sploh ne dobi.

**2. Cilj MVP projekta:**

Spletna aplikacija DijakPomaga, v kateri dijak prek obrazca objavi prošnjo za pomoč pri predmetu, drugi dijaki pa na seznamu vidijo odprte prošnje in se nanje s klikom »Pomagam« odzovejo.

## 3.) Definicija ciljne persone in zemljevid empatije

### A. Profil persone

- **Ime persone in starost:** Marko Novak, 18 let, 3. letnik
- **Vloga na šoli:** dijak programa tehnik računalništva, ki pomoč išče pri matematiki in fiziki, sam pa dobro obvlada programiranje
- **Raven računalniške pismenosti:** Visoka
- **Glavni cilj persone:** hitro najti sošolca, ki mu razloži snov, in svoje znanje ponuditi drugim
- **Glavni strah / frustracija:** vprašanja na Discordu se izgubijo, ko profesorja ni, pa ne ve, koga vprašati

### B. Zemljevid empatije

| Kvadrant | Vprašanje za vživljanje | Zapis naše ekipe |
|---|---|---|
| **REČE** | Kaj uporabnik dobesedno izjavi, ko govori o tej težavi? | »A kdo zna rešiti to nalogo iz fizike? Jaz lahko komu pomagam pri programiranju.« |
| **DELA** | Kako uporabnik danes fizično rešuje ta problem? | Piše v razredno skupino na Discordu, med odmori sprašuje sošolce in išče razlage na YouTubu. |
| **MISLI** | Kaj si uporabnik v resnici misli, a morda ne upa povedati na glas? | »Nočem, da bi sošolci mislili, da ne znam osnov. Kaj če bo moje vprašanje izpadlo neumno?« |
| **ČUTI** | Kakšna čustva doživlja ob neuspehu oz. ob rešitvi? | Stres in nemoč pred testom, ko nima koga vprašati, ter olajšanje, ko mu sošolec snov hitro razloži. |

## 4.) Meje obsega (Scope Boundaries) za naš MVP

### A. V obsegu (IN SCOPE – 2 jedrni funkciji, povezani z bazo MariaDB)

**Prva jedrna funkcija (Vnos podatkov): Objava prošnje za pomoč**

- Kratek opis: HTML obrazec → PHP validacija → SQL INSERT INTO prosnje.
- Kaj točno vnaša uporabnik: ime, razred, predmet (izbira s seznama), kratek opis težave in kontaktni e-naslov.

**Druga jedrna funkcija (Izpis in proces): Pregled prošenj in odziv**

- Kratek opis: Dinamičen izpis iz baze SQL SELECT → Pico.css kartice; odziv shrani SQL UPDATE prosnje (status).
- Kaj točno vidi in lahko naredi uporabnik: Seznam odprtih prošenj s predmetom, opisom in datumom, ki ga lahko filtrira po predmetu. Pri prošnji klikne »Pomagam« in vpiše svoje ime, prošnja pa dobi status »v teku«, da drugi vidijo, da nekdo že pomaga.

### B. Izven obsega (OUT OF SCOPE – faza 2.0)

- ❌ prijava s šolskim računom (Microsoft/Google SSO) in uporabniški profili,
- ❌ klepet v živo med dijakoma (WebSockets),
- ❌ ocenjevanje tutorjev z zvezdicami in točkami za pomoč,
- ❌ potisna obvestila in e-pošta ob novi prošnji,
- ❌ mobilna aplikacija in koledar terminov za skupno učenje.

Po metodi SCAMPER smo uporabili korak E (Eliminate – odstrani): vse, kar ni nujno za objavo in pregled prošenj, smo prestavili v fazo 2.0. Pri prijavi smo uporabili korak S (Substitute – zamenjaj), saj namesto prijave v obrazec vpišemo samo ime in kontakt.

## 5.) Tehnološki sklad in stroškovna ocena

| Komponenta | Standardno orodje RPS | Potrditev ekipe |
|---|---|---|
| Kodno okolje | github.dev v spletnem brskalniku | DA |
| Zaledje & Baza | PHP 8.x + MariaDB na šolskem cPanelu | DA |
| Oblikovanje (UI) | Semantični Pico.css (vključitev prek CDN) | DA |
| Verzioniranje | Git + šolski GitHub repozitorij | DA |
| Projektno vodenje | GitHub Projects (Kanban deska) | DA |

**Skupni strošek orodij: 0 € (odprta koda in SERŠ infrastruktura).**
