# Projektna listina – DijakPomaga

- **Tematska smer:** Dijaško tutorstvo
- **Predmet:** Razvoj produktov in storitev (RPS), 2. D, šolsko leto 2026/27
- **Mentor:** Sergej Lah
- **Skupina:** Timotej Pučko, Lan Lerher, Marko Laptuš
- **Datum:** 20. 10. 2026

## 1. Problem

Dijaki na SERŠ se pri učenju pogosto zataknejo pri nalogi ali snovi, profesor pa takrat ni na voljo. Pomoč iščejo pri sošolcih na Discordu ali v zasebnih sporočilih, kjer se vprašanja hitro izgubijo. Hkrati je na šoli veliko dijakov, ki določeno snov dobro znajo in bi radi pomagali, vendar ni enega mesta, kjer bi se dijaki, ki potrebujejo pomoč, in dijaki, ki jo lahko nudijo, našli.

**Komu olajšamo delo:** dijakom, ki potrebujejo razlago snovi ali pomoč pri nalogi, in dijakom, ki bi radi pomagali drugim. Posredno tudi profesorjem, ker dobijo manj enakih vprašanj.

## 2. Cilj projekta

Izdelati preprosto spletno aplikacijo, kjer dijak v nekaj sekundah objavi, pri čem potrebuje pomoč, in kjer drugi dijaki vidijo vse odprte prošnje ter se nanje odzovejo.

## 3. Meje obsega (Scope)

### V obsegu (IN SCOPE) – MVP

1. **Objava prošnje za pomoč:** dijak vpiše predmet, letnik, kratek opis težave in kontakt (npr. šolski e-naslov). Vse odprte prošnje so prikazane na seznamu, ki ga lahko filtriramo po predmetu.
2. **Odziv na prošnjo:** dijak, ki snov zna, pri prošnji klikne »Pomagam«. Prošnja dobi status »v teku« in kasneje »rešeno«, da je jasno, katere prošnje še čakajo na pomoč.

### Izven obsega (OUT OF SCOPE) – faza 2.0

- prijava s šolskim računom in uporabniški profili,
- klepet oziroma sporočila znotraj aplikacije,
- ocene, zahvale in točke za dijake, ki pomagajo,
- koledar terminov za skupno učenje,
- obvestila po e-pošti ali na telefon,
- mobilna aplikacija.

## 4. Vloge v ekipi

| Član ekipe | Vloga | Naloge |
|---|---|---|
| Marko Laptuš | skrbnik baze in zaledja | podatkovni model prošenj, shranjevanje podatkov, logika statusov |
| Timotej Pučko | vmesnikar | izgled strani, obrazec za objavo prošnje, seznam in filter |
| Lan Lerher | testiravec | testni primeri, iskanje napak, preverjanje z uporabniki, dokumentacija |

## 5. Persona

**Marko Novak, 18 let** – dijak 3. letnika programa tehnik računalništva na SERŠ Maribor.

- **Tehnična pismenost:** napredna (HTML, CSS, JavaScript, osnove PHP in MySQL, GitHub).
- **Glavni cilji:** hitro najti sošolca, ki mu razloži snov, in svoje znanje deliti z drugimi.
- **Skrite frustracije:** ne ve, na koga se lahko obrne; vprašanja na Discordu se izgubijo; ni enega mesta, kjer bi videl, kdo pomaga pri katerem predmetu.

> »Včasih potrebujem samo nekoga, ki mi zna snov razložiti na preprost način, hkrati pa bi tudi sam rad pomagal sošolcem pri stvareh, ki jih dobro razumem.«

### Zemljevid empatije

| Dimenzija | Kaj opazimo |
|---|---|
| **REČE** | »A kdo zna rešiti to nalogo?« · »Lahko pomagam pri programiranju, samo povej.« |
| **DELA** | sprašuje na Discordu, išče razlage na spletu, sošolcem pošilja zapiske in povezave |
| **MISLI** | »Koga lahko vprašam, ko profesorja ni? Kaj če bo moje vprašanje izpadlo neumno?« |
| **ČUTI** | olajšanje, ko hitro dobi razlago, in zadovoljstvo, ko sam pomaga drugemu |

## 6. Orodja in stroški

Spletno stran razvijamo s HTML, CSS in JavaScriptom, kodo hranimo na GitHubu, stran gostujemo na GitHub Pages, delo pa vodimo na Kanban deski v GitHub Projects. Vsa orodja so za dijake brezplačna, zato so stroški projekta praktično 0 €.
