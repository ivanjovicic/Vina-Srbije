# Assumption & Evidence Ledger

## 1. Pet pretpostavki koje mogu ubiti projekat

| ID | Pretpostavka | Zašto je kritična | Trenutni dokaz | Confidence | Ako je netačna | Najjeftiniji test |
|---|---|---|---|---|---|---|
| A1 | Vinarije imaju merljiv problem sa acquisition/booking/repeat purchase | Bez supply pain-a nema payer-a | Postoje direktni booking/e-commerce modeli; više vinarija već ulaže u tourism/DTC, ali nema dokaz da žele novu platformu | LOW | B2B prihod pada | 20 strukturiranih winery intervjua |
| A2 | Posetilac želi da sačuva vino posle tasting-a | Osnova Passport/retention loop-a | Analogija sa Vivino/notes; nema lokalnog behavioral dokaza | LOW | Passport postaje gimmick | QR pilot na 3–5 vinarija |
| A3 | Save -> repeat purchase postoji u 30–60 dana | Ključna monetizaciona/diferencijaciona teza | Logičan DTC problem, ali nema lokalne kohorte | LOW | Repeat bridge nije wedge | Follow-up kampanja za realne tasting goste |
| A4 | Vinarija će održavati kritične podatke | Freshness je core trust problem | SerbianWine savetuje reconfirm; mnoge posete su by appointment | MEDIUM-LOW | Data postaje stale/manual hell | Claim pilot + 30-dnevni update test |
| A5 | Postoji dovoljan consumer pain iznad Google/Vivino/direct | Bez njega nema acquisition/retention | Lokalni proizvodi već dobro pokrivaju directory/map; booking je fragmentisan | LOW | Discovery platform je suvišna | 25 consumer/tourist interviews + concierge test |

## 2. Evidencija koja trenutno podržava projekat

| ID | Evidence | Šta podržava | Snaga |
|---|---|---|---|
| E1 | VinarijeSrbije navodi 430 vinarija i 22 rejona | Supply je dovoljno širok za vertikalni proizvod | MEDIUM |
| E2 | SerbianWine označava 112 vinarija sa degustacijama, 33 sa restoranom i 21 sa smeštajem | Postoji tourism-ready podskup i enrichment data | MEDIUM |
| E3 | WineTourism prodaje konkretne Srbija experiences €9–€65+ | Ljudi mogu rezervisati/platiti wine experiences u Srbiji | MEDIUM |
| E4 | Direktni sajtovi vodećih vinarija imaju tasting i web-shop ponudu | Vinarije monetizuju tourism/DTC i imaju reason-to-care | MEDIUM |
| E5 | Jul 2026: 475.871 turistički dolazak, 283.890 stranih | Postoji inbound tourism base | HIGH za turizam, LOW za wine-specific demand |
| E6 | Wine Vision okuplja stotine izlagača i profesionalnih kupaca | Supply-side/B2B ekosistem je aktivan | HIGH |
| E7 | Globalni winery DTC sistemi naplaćuju SaaS + transaction fees | Winery software/DTC ima dokazanu međunarodnu ekonomiku | HIGH globalno, LOW za Srbiju |

## 3. Evidencija protiv ili koja smanjuje atraktivnost

| ID | Evidence | Rizik | Snaga |
|---|---|---|---|
| C1 | OIV: svetska potrošnja vina 2025 -2,7% YoY, -14% od 2018 | Ne oslanjati se na rast volumena konzumacije | HIGH |
| C2 | Map/directory/route već imaju lokalni konkurenti | Slaba diferencijacija discovery-only proizvoda | HIGH |
| C3 | Vivino ima 433 srpske vinarije | Taste/ratings/label data je incumbent teritorija | HIGH |
| C4 | WineTourism/Viator već prodaju wine experiences | Booking nije whitespace | HIGH |
| C5 | Wine Vision ima ozbiljan B2B matching i product graph | Export/B2B catalog nije čist greenfield | HIGH |
| C6 | Leading wineries već imaju direktan web-shop i booking/contact | Platforma mora doneti novi demand/ROI, ne samo tooling | MEDIUM |
| C7 | Stripe nije standardno dostupan srpskim firmama | Generic marketplace stack nije plug-and-play | HIGH |
| C8 | Turistički paket/posredovanje može povući licenciranje/garancije | Route+transport+stay kombinacije mogu postati pravno skupe | HIGH kao risk, exact scope UNKNOWN |

## 4. Blocking unknowns

- stvarni winery CAC i onboarding cost;
- winery willingness-to-pay;
- wine-tourism demand kao poseban procenat ukupnog turizma;
- repeat purchase stopa nakon fizičke degustacije;
- acceptable booking take rate u Srbiji;
- pravni status platformskog payment/split-payout modela;
- javni pristup i reuse uslovi Vinskog registra;
- courier age-verification i alcohol-shipping prakse po konkretnim providerima;
- realan consumer acquisition cost kroz SEO/social/partners.

## 5. Unknown but not blocking za prvi pilot

- konačan brand;
- native mobile app;
- regionalni commerce;
- ML recommender;
- multi-winery basket;
- warehouse;
- HORECA/export modules.

## 6. Pravilo odluke

Nijedna LOW-confidence pretpostavka sa HIGH business impact ne sme ući u implementation roadmap bez eksplicitnog validation experimenta.
