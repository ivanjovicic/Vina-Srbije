# Legal, Payments & Logistics Risk Matrix

## 0. Regulatory status note

Ovaj dokument je research, ne pravni savet. Posebno je važno da se **Nacrt zakona o vinu iz maja/juna 2026. ne tretira kao važeći zakon**. Nacrt predviđa značajne promene registara, geografskih oznaka, sledljivosti i faznu primenu od 2027/2028, ali pre implementacije treba proveriti da li je i u kom tekstu usvojen. Do tada konkretni flow mora biti mapiran prema trenutno važećim propisima i podzakonskim aktima. [S27]

> Ovo nije pravni savet. Dokument identifikuje pitanja koja pre produkcione monetizacije moraju potvrditi advokat, računovođa i odgovarajući payment/provider partneri.

## 1. Risk summary

| Oblast | Status | Zašto |
|---|---|---|
| Informativni directory | GREEN-ish | nizak rizik uz tačne podatke/prava sadržaja |
| Direct lead/contact | GREEN / REVIEW | jasno objasniti ko pruža uslugu |
| Reservation request without payment | REVIEW | consumer terms/data/role platforme |
| Experience marketplace with payment | LEGAL REVIEW REQUIRED | merchant/payment/refund/tourism role |
| Tour + transport + accommodation bundle | HIGH RISK | može ući u turističko putovanje/posredovanje |
| Wine ecommerce | LEGAL REVIEW REQUIRED | maloletnici, consumer law, fiscalization |
| Multi-winery split payment | HIGH RISK | payment services + accounting + merchant roles |
| Cross-border alcohol commerce | HIGH RISK | customs/excise/tax/courier rules |
| Sponsored wine content | REVIEW | alcohol advertising restrictions/transparency |

## 2. Maloletnici i alkohol

Zakon o zaštiti potrošača 2026 sadrži zabranu prodaje, isporuke, usluživanja i poklanjanja alkoholnih pića licima mlađim od 18 godina; u slučaju sumnje trgovac može tražiti uvid u identifikacioni dokument. Tačan datum primene svih odredbi i praktičan delivery verification workflow treba potvrditi pravno zbog prelaznih odredbi. [S19]

### Product implication

Ako platforma kasnije prodaje vino:

- age gate u UX-u nije dovoljan sam po sebi;
- treba definisati seller/delivery odgovornost;
- courier/driver age-check proces mora biti potvrđen.

## 3. Oglašavanje vina

Zakon o oglašavanju postavlja generalnu zabranu alkoholnog oglašavanja sa izuzecima za pića ispod 20% alkohola, uključujući internet oglašavanje, uz dodatne zabrane načina promocije i zaštitu maloletnika. [S20]

### Product implication

Potrebna pravna provera za:

- sponsored wine cards;
- personalized recommendations;
- push/email marketing;
- influencer campaigns;
- age targeting;
- mandatory warnings/format ako su primenljivi.

Ne koristiti copy koji povezuje alkohol sa vožnjom, uspehom ili prekomernom konzumacijom.

## 4. Tourism law

APR vodi Registar turizma i posebne režime za organizatore i posrednike. Organizator turističkog putovanja može zahtevati licencu, garanciju i depozit; kategorije A/B imaju različite uslove. [S21][S22]

### Critical product boundary

Razlikovati:

1. informacije o vinariji;
2. direct lead ka jednoj vinariji;
3. reservation jedne tasting usluge;
4. marketplace jedne experience usluge;
5. kombinaciju više usluga;
6. organizovan day tour sa prevozom;
7. vino + prevoz + smeštaj/package.

Što se više približavamo 5–7, veća je verovatnoća da ulazimo u regulisani turizam. Ne kombinovati ih u MVP bez pravnog memoranduma.

## 5. Payment reality in Serbia

Stripe global availability trenutno ne navodi Srbiju kao standardno podržanu zemlju za lokalno prihvatanje plaćanja. [S14]

Ali Srbija ima domaće opcije:

- NBS IPS online QR/deep-link plaćanje i merchant-side internet acceptance workflow; [S15][S24]
- bank card acquiring;
- registrovane platne institucije; NBS registar uključuje PayX, Moneta Financial Services, Transfernova, VAKEL i druge. [S15][S16]

### Implication

Payment architecture mora biti provider/legal discovery task, ne engineering assumption.

### Provider checklist before any checkout

Za najmanje dve konkretne banke/PSP-a proveriti u pisanom obliku:

- internet card acquiring za domaće i strane kartice;
- IPS internet payment;
- recurring payment/tokenization ako ikada bude potreban wine club;
- Apple Pay / Google Pay support kroz njihov acquiring stack;
- refunds/partial refunds;
- chargeback workflow;
- multi-merchant/split payout — ako postoji;
- ko je merchant of record;
- da li provider može da podrži platform fee bez platforme koja drži tuđ novac.

PayPal/Stripe ili drugi strani provider ne smeju se podrazumevati samo zato što postoje globalno.

## 6. Money-flow question

Ako platforma primi 10.000 RSD od kupca i 9.000 prosledi vinariji, nije dovoljno tehnički “napraviti payout”. Treba odgovoriti:

- ko je trgovac prema kupcu?
- čiji je prihod 10.000?
- ko izdaje račun/fiskalni račun?
- ko obrađuje reklamaciju?
- ko vraća novac?
- ko snosi chargeback?
- da li platforma pruža platnu uslugu ili PSP/banka rešava strukturu?

**Commerce gate se ne otvara bez pisanog odgovora pravnika/računovođe/PSP-a.**

## 7. Fiscalization

Srbija je 2026. menjala propise u oblasti fiskalizacije. Exact implementation za marketplace/service fee/refund nije analiziran dovoljno za produkcioni dizajn. Ovo je BLOCKING LEGAL/ACCOUNTING REVIEW pre checkout-a.

## 8. Consumer protection

Za distance sales/booking treba analizirati:

- obavezne informacije pre ugovora;
- identitet trgovca;
- cenu/naknade;
- cancellation/refund pravila;
- reklamacije;
- digital confirmations;
- ko je odgovoran kada winery otkaže.

## 9. Privacy

Data set može sadržati:

- account identity;
- email/phone;
- location;
- visit history;
- wine preferences;
- purchase/reorder behavior;
- marketing consent.

Principi:

- minimum collection;
- separate marketing consent;
- export/delete workflow;
- retention policy;
- role-based winery access;
- no cross-winery sharing of identifiable consumer data without lawful basis/clear user expectation.

Za EU turiste proveriti GDPR territorial scope pre targeted EU marketing/profiling.

## 10. Content/data rights

Publicly visible does not mean reusable. Need explicit source/right policy for:

- winery photos;
- labels;
- descriptions;
- tasting notes;
- awards;
- user reviews;
- map/place data.

Preferred:

- winery-provided assets;
- licensed/open data;
- original editorial;
- official public data under confirmed reuse terms.

## 11. Wine registry data

Ministarstvo vodi Vinski/Vinogradarski registar i zvanični wine geography sistem. To je potencijalno najbolji canonical identity baseline, ali javni API/download i reuse terms nisu dovoljno potvrđeni u ovom research-u. Potrebno je tražiti legal/technical access pre automatizovanog ingest-a. [S09]

## 12. Logistics

Before wine delivery:

- confirm which couriers accept alcohol/glass;
- packaging standard;
- insurance/breakage;
- COD;
- failed delivery;
- age verification;
- return/replacement.

Do not design “free shipping” economics without actual courier quotes.

## 13. Cross-border

Regional content/tourism expansion is much simpler than regional alcohol commerce. Serbia -> Croatia/Slovenia/BiH/Montenegro etc. can trigger customs/excise/VAT/import/courier issues. Treat cross-border commerce as separate product/legal program.

## 14. Responsible drinking requirement

Route UX must not incentivize drinking and driving. Mandatory design requirements:

- transport disclaimer;
- designated driver option/filter when known;
- taxi/transfer partner links only after verification;
- accommodation suggestion;
- reasonable number of tastings;
- no “drink more / visit max wineries” gamification.

## 15. Recommended legal sequence

### Before public directory pilot

- Terms/Privacy;
- content rights policy;
- winery consent/claim rules.

### Before booking requests

- confirm platform role;
- cancellation wording;
- privacy/data sharing.

### Before deposit/payment

- tourism legal memo;
- payment provider confirmation;
- consumer-law flow;
- fiscal/accounting memo.

### Before alcohol checkout

- seller-of-record;
- age/delivery workflow;
- fiscalization;
- courier contract;
- returns/reklamacije.
