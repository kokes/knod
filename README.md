# Katalog nejen otevřených dat

Středobod českých otevřených dat je [NKOD](https://data.gov.cz), národní katalog otevřených dat. Je v něm spousta zajímavých informací, ale pro takový ten letmý přehled o tom, jaká data jsou k dispozici, je celkem obtížně použitelný.

Nechceme tedy NKOD replikovat, jde nám o trochu obecnější přehled, aby si každý mohl dohledat data pro jednotlivé oblasti zájmu.

### Katalogy

[Národní katalog otevřených dat (NKOD)](https://data.gov.cz) je katalog všech katalogů, jednotlivé úřady a instituce si ale občas založí vlastní katalog, lokální katalog otevřených dat (LKOD), zde je výpis některých z nich.

- Ministerstva
  - [Ministerstvo dopravy](https://www.mdcr.cz/Ministerstvo/Otevrena-data)
    - obsahuje i data pro Státní fond dopravní infrastruktury, Řízení letového provozu nebo Drážního úřadu
  - [Ministerstvo financí](http://data.mfcr.cz/)
    - má i data z Generálního finančního ředitelství, Generálního ředitelství cel a dalších
  - [Ministerstvo kultury](https://data.mkcr.cz)
  - [Ministerstvo obrany](https://data.army.cz)
  - Ministerstvo práce a sociálních věcí - asi nemá?
  - [Ministerstvo pro místní rozvoj](http://data.mmr.cz/)
    - krom MMR je tam i CzechTourism nebo Státní fond rozvoje bydlení
  - [Ministerstvo průmyslu a obchodu](https://www.mpo.cz/cz/rozcestnik/ministerstvo/otevrena-data/lokalni-katalog/)
  - [Ministerstvo spravedlnosti](https://data.justice.cz)
    - Technicky vzato jde o _Otevřená data české justice_
  - Ministerstvo vnitra - nemá? asi fakt ne, maj NKOD
  - Ministerstvo zahraničních věcí - nemá?
  - [Ministerstvo zdravotnictví](https://opendata.mzcr.cz)
    - včetně dat z krajských hygienických stanic, Národního ústavu duševního zdraví nebo Koordinačního střediska transplantací.
  - Ministerstvo zemědělství - nemá?
  - [Ministerstvo životního prostředí](https://opendata.mzp.cz)
    - Obsahuje i data z ČHMÚ, Správy jeskyní, Správy NP Šumava a dalších přidružených organizací
  - [Ministerstvo školství, mládeže a tělovýchovy](https://data.msmt.cz)
- Města
  - [Hlavní město Praha](http://opendata.praha.eu/)
    - nejen město, ale i Operátor ICT, jednotlivé městské části, Městská knihovna atd.
  - [Brno](https://data.brno.cz)
- Ostatní
  - [Český telekomunikační úřad (ČTÚ)](https://data.ctu.cz)

### Administrativni informace

K transakčním datům (dotace, smlouvy, zakázky, ...) je třeba doplnit data o smluvních stranách, protože tato data jsou v transakčních datasetech zpravidla nedostačující. Neexistuje jedno centrální úložiště, je několik zdrojů těchto informací, záleží na tom, co člověk požaduje.

- Některé informace o některých fyzických, právnických a veřejných entitách jde získat z [exportů datových schránek](https://www.mojedatovaschranka.cz/sds/welcome.do?part=opendata)
  - Orgány veřejné moci mají sice DS povinně, ale u privátních subjektů to tak není, takže v datech nejsou zdaleka všechny.
  - Dobré pro přehled o orgánech veřejné moci, případně jako zdroj pro mapování z adres datových schránek na IČO či naopak.
- [Administrativní registr ekonomických subjektů (ARES)](https://wwwinfo.mfcr.cz/ares/ares.html.cz)
  - Historicky nejpodstatnější dataset pro administrativní data, do dneška má svou relevanci.
  - V sekci _XML služby_ najdete popis řady endpointů, ideální pro získání informací o několika málo subjektech. Nejdůležitější je OR (obchodní rejstřík - údaje z Justice), RES (registr ekonomických subjektů - základní údaje od Českého statistického úřadu) a RŽP (živnostenský rejstřík).
  - API mají limity v řádek desítek tisíc dotazů denně, tak pozor na to, protože můžete být snadno zablokováni.
  - V sekci _otevřená data_ je relativně nově **bulkový export** obchodního rejstříku. Obsahuje skoro vše, co by člověk potřeboval o právnických osobách - chybí historie názvů subjektů a data narození fyzických osob (jednatelů, společníků atd.).
  - MFČR tento registr provozuje, ale data jen poskytuje dál, nejsou v jeho vlastnictví.
- [Otevřená data Veřejného rejstříku a Sbírky listin](https://dataor.justice.cz)
  - Ministerstvo Spravedlnosti poskytuje export dat z webu Justice.cz, zejm. z rejstříku právnických osob. Cokoliv vidíte na webové verzi rejstříku, to si můžete stáhnout v XML v bulkové formě.
  - Pro aktuální informace stačí stáhnout data pro současný rok a všechny rejstříkové soudy a právní formy. Bohužel nejde stáhnout vše najednou nějak jednodušeji.
  - Informace o zaniklých subjektech je trochu těžší získat, protože firma zaniklá v roce 2009 bude naposledy v datasetu pro rok 2009, takže člověk musí stáhnout data pro všechny roky, aby získal informace o všech zaniklých subjektech. Tato limitace se netýká exportů ARES výše, tam je snadné získat informace o zaniklých subjektech.
  - Oproti ARES člověk získá informace o akcionářích, insolvencích a dalších metadatech.
  - **Tento dataset bude v budoucnu jediný nutný pro identifikaci smluvních stran, v tuto chvíli má stále několik zádrhelů.**

### Dotace
- [DotInfo](https://www.dotinfo.cz)
  - Ze systému DotInfo existuje [jeden export](http://data.mfcr.cz/cs/dataset/dotace-dotinfo) z roku 2017
  - TODO: vysvětlit, proč bohužel tenhle dataset existuje
- [Centrální evidence dotací (CEDR III)](http://cedr.mfcr.cz/cedr3internetv419/OpenData/DocumentationPage.aspx)
  - obsahuje CSV exporty pro dotace, rozhodnutí nebo příjemce
  - je možné dohledat informace v číselnících
  - doporučuji [schéma na straně 12](http://cedropendata.mfcr.cz/c3lod/C3_OpenData%20-%20datov%C3%A1%20sada%20IS%20CEDR%20III.pdf), pro lepší pochopení relačního modelu
  - TODO: popsat rozsah
- , mmr?
- opendata MS2014+
- [CzechInvest](https://www.czechinvest.org/cz/Sluzby-pro-investory/Investicni-pobidky)
  - udělené investiční pobídky
  - starší data neobsahují IČO informace, tak pozor na to
- [Státní zemědělský invervenční fond (SZIF)](https://www.szif.cz/irj/portal/szif/seznam-prijemcu-dotaci)
  - Fond operuje s 30-40 miliardami ročně, na webu jsou jednotliví žadatelé k dohledání.
  - Existují XML exporty pro poslední dva roky dat.

### Smlouvy
- registrsmluv
- hlidac smluv

- adhoc smlouvy - často predatují datově (i existenčně) registr smluv
 - například MKČR https://data.mkcr.cz/homepage/dataset/b679e84b-7163-4f4c-b08d-3b2c851dec69

### Zakázky
- vestnik (jak se liší?)
- profil zadavatele
- vsechny zakazky?

### Faktury

- Neexistuje centralizace faktur, je na jednotlivých úřadech či jiných entitách, jestli své faktury zveřejní. Tato data jsou často cennější než smlouvy nebo zakázky, protože obsahují reálné útraty a jejich metadata jsou kvalitnější než např. u registru smluv.

- Ministerstva
  - [Ministerstvo dopravy](https://www.mdcr.cz/Ministerstvo/Otevrena-data/Faktury?returl=/Ministerstvo/Otevrena-data)
    - obsahuje i data pro Státní fond dopravní infrastruktury, Drážní inspekci, Ředitelství silnic a dálnic a další entity
  - [Ministerstvo financí](http://data.mfcr.cz/cs/dataset/prehled-faktur-ministerstva-financi-cr)
    - portál obsahuje i faktury [Úřadu pro zastupování státu ve věcech majetkových](http://data.mfcr.cz/cs/dataset/prehled-faktur-uzsvm)
  - [Ministerstvo kultury](https://data.mkcr.cz/homepage/dataset/f0c8f8e7-153e-4b9c-bca8-6473f40c4f16)
  - [Ministerstvo obrany](https://data.army.cz/cs/faktury-2015)
  - Ministerstvo práce a sociálních věcí - nemají?
  - [Ministerstvo pro místní rozvoj](http://data.mmr.cz/dataset?q=faktury&sort=score+desc%2C+metadata_modified+desc)
    - Krom MMR jsou tu faktury i agentury CzechTourism, Státního fondu rozvoje bydlení nebo Centra pro regionální rozvoj
  - [Ministerstvo průmyslu a obchodu](https://www.mpo.cz/cz/rozcestnik/ministerstvo/otevrena-data/lokalni-katalog/faktury-2013-2018--243884/)
    - Odkaz vede na jednorázový export z února 2019, pro aktuálnější data je třeba na rozcestník (vizte seznam LKOD výše).
  - [Ministerstvo spravedlnosti](https://data.justice.cz/SitePages/msp/Ministerstvo%20spravedlnosti%20ČR.aspx)
    - Na stejném webu jsou i faktury soudů, státních zastupitelství, vězeňských služeb, justiční akademie a dalších orgánů české justice
  - Ministerstvo vnitra - nemá?
  - Ministerstvo zahraničních věcí - nemá?
  - [Ministerstvo zdravotnictví](https://opendata.mzcr.cz/dataset?tags=Faktury) - na svém portálu MZČR nejsou jen faktury ministerstva, ale i z dalších entit - např. krajských hygienických stanic, Národního ústavu duševního zdraví nebo Koordinačního střediska transplantací.
  - Ministerstvo zemědělství - zdá se, že nemá
    - Dle zákona o svobodném přístupu k informacím (106/1999 Sb.) ministerstvo některá data [poskytlo](http://eagri.cz/public/web/mze/ministerstvo-zemedelstvi/povinne-zverejnovane-informace/informace-podle-zakona-c-106-1999-sb/poskytnute-informace/poskytnute-informace-na-zadosti-o-84.html), ale systematicky nic nevydává
  - [Ministerstvo životního prostředí](https://opendata.mzp.cz/organization/749d5ed0-107c-4c04-a17a-1acc3a12329e?groups=faktury)
    - Obsahuje i faktury [pro další přidružené organizace](https://opendata.mzp.cz/dataset?groups=faktury), např. pro Českou geologickou službu nebo Agenturu ochrany přírody a krajiny.
  - Ministerstvo školství, mládeže a tělovýchovy - nemá?
- Samosprávy
  - [Hlavní město Praha](http://opendata.praha.eu/dataset?q=faktury)
    - obsahuje nejen data pro magistrát, ale i pro některé městské části a městské podniky
- Ostatní
  - [Český telekomunikační úřad (ČTÚ)](http://data.ctu.cz/dataset/faktury)
  - [IPR](http://opendata.praha.eu/dataset/ipr-faktury) - Institut plánování a rozvoje

### Ostatní výdaje
- [Česká správa sociálního zabezpečení (ČSSZ)](https://data.cssz.cz)
- random smlouvy, faktury
- czechinvest

### Rozpočty
- [Monitor](https://monitor.statnipokladna.cz/) Státní pokladny je _aplikace_ pro rozklikávání rozpočtů a dalších účetních informací o spoustě složek státu - měst, obcí, příspěvkových organizací, škol atd.
  - [Datový katalog](https://monitor.statnipokladna.cz/2019/zdrojova-data/) - všechna data z Monitoru jde exportovat jako CSV.
  - [Příklad detailu dat](https://monitor.statnipokladna.cz/2019/obce/detail/00291471#prehled) - ukázka dat z Uherského Hradiště - máme tu rozvahu, účetní závěrky, seznam příspěvkových organizací atd.
- [CityVizor](https://cityvizor.cz) - původně projekt z Ministerstva financí se přesunul pod spolek [Otevřená města](https://www.otevrenamesta.cz) a jde mu o vizualizaci rozpočtů samosprávních jednotek
  - Hlavní rozdíl proti Monitoru je ten, že Monitor má rozpočty na úrovni rozpočtových kapitol (např. odvoz odpadu), ale nemáte tam jednotlivé faktury, průběžné plnění, informace o dodavatelích atd. To je přesně mezera, kterou vyplňuje CityVizor.
  - [Praha má vlastní instanci CityVizoru.](https://cityvizor.praha.eu)

### Metainfo o státu
- Seznam orgánů veřejné moci (OVM) je možné získat z [exportu datových schránek](https://www.mojedatovaschranka.cz/sds/welcome.do?part=opendata)
- psp
- volby
- centralni registr oznameni
- registr prav a povinnosti
- wikidata?

### legislativa
- psp.cz o tvorbě
- eklep, veklep
- bude elegislativa, esbírka
- zákony pro lidi + ASPI?

### Regionální data
- golemio
- data.brno.cz

### Geodata

- ČUZK
- městská
- katastr
- IPR prazsky model

### Ostatní
- [Úřad průmyslového vlastnictví (ÚPV)](https://isdv.upv.cz/webapp/webapp.opendata.tm) - denní exporty v XML
- wikidata
- portal.gov.cz
- rozhlas data
- úřední desky
- Něco z ČSÚ? ČNB (ARAD)?
- https://data.gov.cz/wishlist/