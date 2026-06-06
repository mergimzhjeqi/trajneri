# Raport ne shqip per inspektimin Mango MIT

**VIN:** WDDZF0EB2KA502673  
**Linku i dhene:** https://mangoworldcar.com/en/mit-inspection/WDDZF0EB2KA502673?readonly=true  
**Data e pergatitjes:** 2026-06-06

## Statusi i marrjes se raportit

Raporti i plote Mango MIT dhe fotot e inspektimit **nuk u arriten te shkarkohen nga kjo makine**, sepse faqja/API e MangoCar ktheu bllokim `403 Forbidden` nga Bunny Shield/CDN.

U provuan keto rruge:

- Faqja publike:
  - `https://mangoworldcar.com/en/mit-inspection/WDDZF0EB2KA502673?readonly=true`
  - rezultati i lexueshem publik: vetem titulli `Korean Used Car Export Platform - Mango Car`
- Aplikacioni MIT:
  - `https://mit.mangoworldcar.com`
  - u gjet qe perdor GraphQL ne `https://chatapi.mangoworldcar.com/graphql/`
- Query i raportit:
  - `GetMangoInspection`
  - filter: `identifyNumber = WDDZF0EB2KA502673`
  - fusha qe do te ktheheshin: `inspectionPayload`, `score`, `ownerKey`, `createDate`, `updateDate`, `mangoInspectionAttachments`
- Endpoint-i real i te dhenave ktheu `403 Forbidden`, prandaj nuk pati akses te vlerat konkrete te inspektimit ose te linkat e fotove.

## Te dhenat e verifikuara per VIN-in

Burim i verifikuar: NHTSA VIN Decoder API.

| Fushe | Vlere |
| --- | --- |
| VIN | WDDZF0EB2KA502673 |
| Marka | Mercedes-Benz |
| Prodhuesi | Mercedes-Benz Cars |
| Tipi i automjetit | Passenger Car |
| Viti i modelit | 2019 |
| Vendi i prodhimit | Germany |
| Qyteti/fabrika | Sindelfingen |
| Check digit | korrekt |
| Airbag frontal | rreshti i pare, shofer dhe pasagjer |
| Airbag anesor | rreshti i pare dhe i dyte |
| Rripat e sigurimit | manuale |
| Pretensioner | po |

Shenim: NHTSA e dekodoi VIN-in si te vlefshem, por nuk dha model/trim te plote per disa pozicione te VIN-it.

## Cfare perfshin normalisht Mango MIT

Nga informacioni publik i MangoCar per MIT (Mango Inspection Technology), sherbimi eshte nje kontroll i gjendjes aktuale te makines dhe zakonisht perfshin rreth **115 pika inspektimi**, nder te tjera:

1. Gjendja e jashtme e automjetit
   - bojatisje/paneleri
   - parakolpe
   - defekte vizuale te karrocerise
2. Motorr, transmision dhe pjese kryesore
   - kontroll i komponenteve kryesore
   - rrjedhje vaji/uje kur jane te dukshme
3. Pjesa e poshtme e automjetit
   - kontroll vizual nga poshte
   - gjendje e shasise dhe elementeve te ekspozuar
4. Interieri dhe opsionet
   - pajisje/opsione te brendshme
   - funksione qe mund te kontrollohen ne vend
5. Vleresim aksidenti/permbytjeje
   - kontroll i shenjave te demtimeve strukturore ose aksidentit
   - kontroll i shenjave te mundshme te permbytjes

## Kufizimet normale te MIT

Sipas informacionit publik te MangoCar, MIT:

- nuk garanton gjendjen e ardhshme te automjetit;
- nuk zevendeson garanci teknike;
- kryhet ne gjendje te ndaluar, prandaj nuk verifikon te gjitha funksionet qe shfaqen vetem gjate ecjes;
- nuk garanton zbulimin e manipulimit te kilometrazhit;
- sherben per t'i dhene bleresit nje pamje me te qarte te gjendjes aktuale.

## Fotot e inspektimit

**Linkat konkrete te fotove nuk u arriten te merren**, sepse ato ruhen ne te dhenat `mangoInspectionAttachments` te raportit GraphQL dhe endpoint-i ktheu `403 Forbidden`.

Fushat ku priteshin fotot:

| Fushe ne API | Kuptimi |
| --- | --- |
| `fileName` | emri teknik i files |
| `fileRealName` | emri origjinal i files |
| `fileContentType` | tipi, p.sh. image/video |
| `attachmentId` | ID e attachment-it |
| `filePath` | path/linku baze i fotos |
| `sortOrder` | renditja e fotos ne raport |

## Per ta kompletuar 100%

Per te nxjerre raportin komplet me detajet reale dhe linkat e fotove, duhet akses i suksesshem ne raport nga nje shfletues/IP qe nuk bllokohet nga MangoCar/Bunny Shield, ose nje nga keto:

1. HTML/JSON i faqes se raportit pas hapjes ne browser;
2. eksport/print i raportit nga MangoCar;
3. screenshot-et/fotot e raportit;
4. rezultat direkt i query `GetMangoInspection` per VIN `WDDZF0EB2KA502673`.

Pa keto te dhena, nuk eshte e sigurt te shpiken detaje inspektimi ose linka fotosh.
