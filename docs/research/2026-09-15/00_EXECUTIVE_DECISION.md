# Wine Serbia — Executive Decision

**Research cut-off:** 15. septembar 2026.  
**Status:** strateški due diligence; nije autorizacija za razvoj.  
**Konačna odluka:** **VALIDATE BEFORE BUILDING**

## 1. Odluka u jednoj rečenici

Ne graditi još jednu mapu ili katalog vinarija. Najperspektivnija hipoteza je **verified winery experience + digital Wine Passport + repeat-purchase bridge**, gde javni discovery/SEO sloj dovodi korisnika do vinarije, QR/Pasport pamti konkretno vino i berbu koje je probao, a platforma kasnije korisnika vraća ka istoj vinariji za ponovnu kupovinu ili sledeću posetu.

## 2. Preporučeni wedge

**Primarni wedge:**

> **Pronađi provereno iskustvo u srpskoj vinariji, sačuvaj vina koja si probao i lako ih pronađi ili kupi ponovo.**

Ovo nije konačno potvrđen proizvod. To je hipoteza koja trenutno najbolje prolazi kroz kombinaciju: korisnička vrednost, B2B vrednost, diferencijacija, tehnička izvodljivost i mogućnost da se dokaže ROI vinariji.

**Drugi najbolji wedge:** **corporate Serbian wine gifting**, testiran ručno kao zaseban revenue eksperiment. Ima potencijal za viši AOV i brži prvi prihod, ali je sezonski i operativno/logistički teži.

## 3. Zašto ne “Vinski putevi Srbije” kao osnovni proizvod

Mapa, direktorijum i rute već imaju ozbiljnu pokrivenost. VinarijeSrbije trenutno navodi 430 vinarija, 22 rejona i 3 regije, uz interaktivnu mapu, profile, degustacije i planer rute. SerbianWine ima 100+ vinarija, wine routes, events i filtere za degustacije, restorane i smeštaj. Vivino indeksira 433 srpska proizvođača. [S01][S02][S03]

Zbog toga **directory + map + route** nije tržišna rupa. Može biti acquisition sloj, ali ne sme biti poslovna teza.

## 4. Zašto ne full marketplace u MVP-u

Full marketplace prerano uvodi najskuplje probleme:

- merchant-of-record i payment-flow odluke;
- fiskalizaciju i računovodstveni model;
- starosnu verifikaciju pri prodaji/isporuci alkohola;
- refund/chargeback odgovornost;
- multi-winery cart;
- više pošiljki ili consolidation;
- lom stakla i reklamacije;
- stock freshness;
- korisničku podršku.

Stripe standardno ne navodi Srbiju kao podržanu zemlju za lokalno payment-processing poslovanje, dok NBS ima domaći IPS i registrovane banke/platne institucije. To znači da payment nije nemoguć, ali arhitektura mora biti dizajnirana za realnost Srbije, ne prema generičkom Stripe Connect tutorijalu. [S14][S15][S16]

Dodatno, u 2026. je sprovedena javna rasprava o novom Zakonu o vinu i drugim proizvodima od grožđa i vina. Na research cut-off datum taj tekst treba tretirati kao **predlog/nacrt regulatorne tranzicije, ne kao važeći zakon**, dok se postojeći Zakon o vinu i podzakonski akti i dalje proveravaju za konkretan flow. [S27]

## 5. Zašto ne booking marketplace odmah

Booking ima smisla, ali postojeći konkurenti već nude Srbija inventory. WineTourism.com ima konkretne srpske degustacije od približno €9 do €65+ i globalno naplaćuje oko 15% za instant booking i 20% za booking na potvrdu, uz minimum po osobi. [S05][S06]

Prva verzija zato treba da testira:

1. discovery -> qualified booking request;
2. response time vinarije;
3. conversion;
4. willingness-to-pay vinarije;

bez toga da platforma odmah drži novac korisnika.

## 6. Najvažniji tržišni signal

Globalna potrošnja vina nije rastuća plima. OIV procenjuje 208 miliona hl u 2025, -2,7% YoY i oko -14% od 2018. Promene životnih navika, generacijske promene i pritisak na kupovnu moć utiču na potražnju. [S08]

Zato poslovna teza ne treba da bude “više ljudi će piti više vina”, već potencijalno:

- premium iskustva;
- lokalni turizam;
- bolji discovery;
- direktan odnos proizvođača i gosta;
- repeat purchase;
- gifting;
- B2B ROI.

## 7. Zašto sada ipak postoji razlog za validaciju

Srbija ima stvarnu i rastuću proizvođačku bazu, ali različiti izvori mere različite skupove. Ministar poljoprivrede je 21. maja 2026. naveo **529 registrovanih vinarija**, dok VinarijeSrbije trenutno navodi 430 javno profilisanih vinarija, a SerbianWine 154. To nije kontradikcija sama po sebi: registry, komercijalno vidljiva i tourism-ready baza nisu isti skup. RZS je za 2025. evidentirao 17.437 ha pod grožđem i 140.718 t proizvodnje grožđa. [S01][S02][S10][S26]

U julu 2026. Srbija je imala 475.871 turistički dolazak i 1.380.922 noćenja; stranih turista bilo je 283.890, sa 671.153 noćenja. Beograd, Novi Sad i Subotica bili su vodeće gradske destinacije. To ne dokazuje wine-tourism demand, ali daje dovoljnu bazu da se testira strani i domaći weekend segment. [S11]

## 8. Preporučeni primarni korisnik

### Consumer pilot

1. domaći parovi/grupe koji planiraju vikend iz Beograda ili Novog Sada;
2. strani turisti sa bazom u Beogradu/Novi Sad koji žele pouzdano wine experience rešenje;
3. sekundarno: početnici koji žele da zapamte i ponovo pronađu vino koje su probali.

### Supply / payer pilot

Turistički spremna mala/srednja vinarija kojoj su važni:

- novi gosti;
- booking leadovi;
- repeat purchase nakon posete;
- bolja atribucija izvora gosta;
- English visibility.

## 9. Pilot geografija

### #1 Fruška gora / Srem

Najbolji prvi cluster zbog gustine ponude, blizine Novog Sada i relativne dostupnosti iz Beograda. SerbianWine trenutno vodi 32 vinarije u Sremu i region opisuje kao najgušći cluster za day/weekend trip. [S04]

### #2 Šumadija / Topola

Dobar premium i heritage cluster, praktičan iz Beograda, ali geografski nešto rasutiji. [S18]

Župa/Three Moravas, Negotin i drugi regioni su važni za brand Srbije, ali nisu prvi izbor za najjeftiniji pilot zbog distance i supply density faktora.

## 10. MVP ako validacija prođe

**IN:**

- SEO-first responsive web, sr-Latn + English;
- 20–30 ručno verifikovanih tourism-ready vinarija iz 2 clustera;
- 100–200 pravilno modelovanih wine/vintage zapisa;
- verified winery profile;
- experience price/range, lead time, jezik, restoran/smeštaj/amenities;
- search/filter/map;
- booking/request handoff bez platform paymenta;
- Wine Passport: save wine + vintage + private note/rating;
- QR na tasting lokaciji;
- direct reorder/buy link ili lead ka vinariji;
- winery claim i manual verification;
- osnovna atribucija i B2B analytics;
- occasion-based filters pre naprednog Taste Match-a.

**OUT:**

- full marketplace;
- multi-winery cart;
- warehouse/fulfillment;
- native mobile app;
- social feed;
- label scanner;
- user reviews;
- complex ML recommender;
- POS/CRM replacement;
- wine club;
- regional alcohol commerce;
- microservices/Kubernetes/Elasticsearch/vector DB.

## 11. North Star

Za pilot koristiti:

> **Confirmed Winery Actions per 100 qualified sessions**

Qualified action = booking/request potvrđen od vinarije, verifikovana poseta ili verifikovan repeat-purchase lead.

Dugoročno se može razviti u **Verified Winery Value Events**, ali kompozitna metrika se ne sme koristiti da sakrije lošu konverziju pojedinačnih funnel koraka.

## 12. Najvažniji moat kandidati

1. svež i verifikovan Serbia winery/wine/experience dataset sa provenance-om;
2. supply relationships i QR prisustvo u fizičkim vinarijama;
3. offline -> online attribution;
4. visit/tasting -> repeat-purchase graph;
5. kasnije preference/taste behavior data;
6. SEO/brand autoritet.

**Nisu moat:** mapa, AI chatbot, običan katalog, filteri, route planner ili generičke recenzije.

## 13. Poslovna ekonomika — zaključak

Subscription sam po sebi ima ograničen plafon u Srbiji. Ako je realan početni supply 100–150 tourism-ready vinarija i cena €20–50 mesečno, čisti SaaS prihod je relativno mali. Zato proizvod mora dokazati transakcionu ili lead vrednost.

Booking-only economics takođe zahtevaju volumen: iskustvo od €30 po osobi, 2,2 gosta i 12% take rate daje približno €7,9 platform revenue po booking-u pre payment/support troška. Zato booking treba da bude kombinovan sa subscription/lead/retention vrednošću, ne jedina ekonomika.

**€10k MRR u Srbiji:** moguće, ali zahteva kombinaciju većeg broja aktivnih vinarija, booking/lead revenue i dodatni B2B kanal.  
**€50k MRR samo Srbija:** niska verovatnoća bez ozbiljnog commerce/corporate-gift volumena ili potpuno drugačijeg B2B proizvoda. Regionalna ekspanzija ili veći transaction layer bi bili potrebni.

## 14. Najjači razlog da se projekat NE gradi

Korisnik već može da kombinuje Google Maps + Instagram + Vivino + direktan kontakt vinarije, dok vinarija već može imati sopstveni web-shop i rezervacije. Ako intervjui pokažu da taj workflow nije dovoljno bolan i da vinarije ne vide vrednost u atribuciji/repeat purchase-u, projekat nema dovoljno jak wedge.

## 15. Najvažniji blocking unknowns

1. Da li tourism-ready vinarije smatraju acquisition/repeat purchase/booking top-3 problemom?
2. Da li će vinarija aktivno postaviti QR i održavati kritične podatke?
3. Da li korisnik posle degustacije zaista želi digitalno da sačuva vino?
4. Da li to vodi do measurable repeat action-a u 30–60 dana?
5. Koliko vinarija bi platilo nakon dokazanog ROI-a?
6. Koji legal/payment model je dozvoljen i praktičan ako platforma kasnije uvede naplatu?

## 16. Minimalni validation gates

**Winery gate:** najmanje 20 intervjua; najmanje 5 vinarija prihvata pilot; najmanje 30–40% navodi acquisition/booking/repeat purchase kao jedan od glavnih problema.  
**Supply gate:** najmanje 10 vinarija daje kompletne podatke i prihvata obavezu osvežavanja kritičnih informacija.  
**Concierge gate:** najmanje 20 realnih korisnika; >=40% kvalifikovanih korisnika završi konkretan winery action.  
**Passport gate:** >=30% stvarnih tasting gostiju skenira/snimi vino kada je QR vidljivo ponuđen; >=15% ima relevantan povratak/reorder signal u 60 dana.  
**Monetization gate:** najmanje 5 vinarija spremno je da plati ili deli revenue nakon dokazanog rezultata.  
**Commerce gate:** blokiran dok nisu potvrđeni pravni/payment model, shipping economics i najmanje 50 mesečnih realnih purchase/reorder intent događaja.

Svi pragovi su **HYPOTHESIS**, ne industrijski standard. Njih treba korigovati posle prvih realnih kohorti.

## 17. Najbolja neposredna prilika za research

Wine Vision by Open Balkan je zakazan za **10–12. oktobar 2026. u Beogradu**. Organizator navodi 535 izlagača, 34 zemlje, 302 profesionalna kupca i 1.500+ poslovnih sastanaka za prethodni/aktuelni scale događaja, uz 2026 fokus na strukturiran B2B matchmaking. To je izuzetno efikasan teren za proveru supply-side pretpostavki, ali i konkurentski signal: generički B2B katalog/matching nije whitespace. [S07]

## 18. Investiciona odluka

**Ne bih danas uložio 12 meseci razvoja u full Wine Serbia platformu.**

Uložio bih 30–45 dana u veoma disciplinovanu validaciju wedge-a **visit -> save -> repeat purchase**, paralelno sa booking/lead i corporate-gifting eksperimentom. Ako QR/repeat loop i winery willingness-to-pay ne daju signal, ne bih dalje ulagao u veliku consumer platformu.

## 19. IF THIS WERE MY MONEY

**Da li bih danas uložio narednih 12 meseci?**  
**ONLY AFTER SPECIFIC VALIDATION.**

**Jedan problem koji bih napao:** gubitak odnosa sa gostom nakon fizičke degustacije — gost zaboravi šta je probao, a vinarija nema jednostavan način da dokaže i podstakne ponovnu kupovinu.

**Prvi kupac/payer:** tourism-ready mala ili srednja vinarija sa realnim prometom degustacija i direktnom prodajom.

**Prva funkcija:** QR save konkretnog vina/vintage-a + consented follow-up + merljiva atribucija ka reorder/booking akciji.

**Funkcija koju ne bih gradio sada:** multi-winery marketplace/cart.

**Najbrži put do prvog prihoda:** nakon besplatnog pilota naplatiti potvrđenu lead/repeat-purchase vrednost ili mali B2B plan onim vinarijama kod kojih je ROI stvarno izmeren.

**Najveći rizik:** workflow Google/Instagram/direct contact je već dovoljno dobar, a post-tasting repeat-purchase problem nije dovoljno čest niti vredan da stvori naviku ili B2B budžet.

**Najopasnija pretpostavka:** da će vinarija aktivno promovisati QR i deliti outcome podatke, a gost imati dovoljno razloga da ga koristi i vrati se.

**Eksperiment sledeće nedelje:** 8–10 winery interviews + 5 konkretnih pilot asks + prototype QR Passport na jednom realnom tasting flow-u.

**Metrika za nastavak:** najmanje 5 kvalitetnih vinarija pristaje na merljiv pilot i realni gosti pokazuju >=30% save rate uz jasno izložen QR/staff prompt.

**Metrika za stop/pivot:** manje od 5 pilot commitments iz 20–30 relevantnih razgovora ili <15% save rate i praktično nula repeat intent-a nakon korektno izvedenog pilot-a.

# FINAL VERDICT

**VALIDATE BEFORE BUILDING**
