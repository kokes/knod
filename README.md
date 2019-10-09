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
- [MS2014+](https://ms14opendata.mssf.cz) a [Seznam operací/příjemců](https://dotaceeu.cz/cs/Statistiky-a-analyzy/Seznamy-prijemcu)
  - Dva datasety od MMR ohledně evropských dotací, tedy vyšších desítkách miliard ročně.
  - MS2014+ jsou otevřená data přímo z informačního systému pro správu dotací, obsahují strukturovaná data o dotacích pro období 2014-2020.
  - Druhý dataset, Seznam operací, obsahuje data pro období 2007-13 a 2014-20, jde ale o celkem zvláštně strukturované Excely, které se navíc v čase mění. Takže pro nahlížení dobré, ale pro analytiku je lepší export z MS2014+.
- [CzechInvest](https://www.czechinvest.org/cz/Sluzby-pro-investory/Investicni-pobidky)
  - udělené investiční pobídky
  - starší data neobsahují IČO informace, tak pozor na to
- [Státní zemědělský invervenční fond (SZIF)](https://www.szif.cz/irj/portal/szif/seznam-prijemcu-dotaci)
  - Fond operuje s 30-40 miliardami ročně, na webu jsou jednotliví žadatelé k dohledání.
  - Existují XML exporty pro poslední dva roky dat.

### Smlouvy
- [Registr smluv](https://smlouvy.gov.cz)
  - Jde o přelomový informační systém, kam mají tisíce veřejných subjektů povinnost publikovat skoro všechny smlouvy přesahující hodnotu 50 tisíc Kč (jsou výjimky mj. z důvodů bezpečnosti či obchodních tajemství).
  - [Poskytuje otevřená data](https://smlouvy.gov.cz/stranka/otevrena-data) na denní bázi ve formátu XML.
  - Systém lze používat napřímo, zprácováním dat nebo přes [Hlídače státu](https://www.hlidacstatu.cz), nejznámějšího zpracovatele těchto dat, kde jsou krom smluvních dat prolinkovány další datasety pro lepší kontext a analytiku.
- Ad hoc smluvní data
  - Před účinností Registru smluv publikovaly některé subjekty smluvní informace z vlastního popudu.
  - Výhodou těchto dat je, že smlouvy často predatují vznik Registru smluv - do registru totiž subjekty vkládají jen nové smlouvy (případně staré smlouvy, pokud je nové smlouvy rozšiřují, žádné dávkové vkládání starých smluv se ale nekoná).
  - Příklady exportů
    - [Ministerstvo kultury](https://data.mkcr.cz/homepage/dataset/b679e84b-7163-4f4c-b08d-3b2c851dec69) - data pro 1994-2019
    - [Ministerstvo pro místní rozvoj a jeho přidružené organizace](http://data.mmr.cz/dataset?q=smlouvy)
    - TODO: další instituce

### Zakázky
- vestnik (jak se liší?)
- profil zadavatele
- vsechny zakazky?

### Faktury

Neexistuje centralizace faktur, je na jednotlivých úřadech či jiných entitách, jestli své faktury zveřejní. Tato data jsou často cennější než smlouvy nebo zakázky, protože obsahují reálné útraty a jejich metadata jsou kvalitnější než např. u registru smluv.

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
  - ČSSZ nabízí převážně přehledové datasety - počty penzistů, OSVČ, průměrné mzdy, průměrné důchody, statistiky pracovní neschopnosti, typy důchodů atd.

### Rozpočty
- [Monitor](https://monitor.statnipokladna.cz/) Státní pokladny je _aplikace_ pro rozklikávání rozpočtů a dalších účetních informací o spoustě složek státu - měst, obcí, příspěvkových organizací, škol atd.
  - [Datový katalog](https://monitor.statnipokladna.cz/2019/zdrojova-data/) - všechna data z Monitoru jde exportovat jako CSV.
  - [Příklad detailu dat](https://monitor.statnipokladna.cz/2019/obce/detail/00291471#prehled) - ukázka dat z Uherského Hradiště - máme tu rozvahu, účetní závěrky, seznam příspěvkových organizací atd.
- [CityVizor](https://cityvizor.cz) - původně projekt z Ministerstva financí se přesunul pod spolek [Otevřená města](https://www.otevrenamesta.cz) a jde mu o vizualizaci rozpočtů samosprávních jednotek
  - Hlavní rozdíl proti Monitoru je ten, že Monitor má rozpočty na úrovni rozpočtových kapitol (např. odvoz odpadu), ale nemáte tam jednotlivé faktury, průběžné plnění, informace o dodavatelích atd. To je přesně mezera, kterou vyplňuje CityVizor.
  - [Praha má vlastní instanci CityVizoru.](https://cityvizor.praha.eu)

### Metainfo o státu

TODO: prolinkovat toto nějak s admin informacemi výše? Aby člověk nemusel scrollovat mezi nima, obojí patří pod stejnou podkategorii

- Orgány veřejné moci
  - Často je třeba identifikovat složky státu, ať už pro kategorizaci dat (jdou finance od soukromníka státu nebo mezi soukromníky atd.) nebo třeba pro adresnou komunikaci. Bohužel neexistuje jeden autoritativní zdroj.
  - Seznam orgánů veřejné moci (OVM) je možné získat z [exportu datových schránek](https://www.mojedatovaschranka.cz/sds/welcome.do?part=opendata)
  - [Otevřená data Czech POINTu](http://www.czechpoint.cz/public/vyvojari/otevrena-data/) mají též seznam orgánů veřejné moci
  - Registr práv a povinností má [webový náhled](https://rpp-ais.egon.gov.cz/AISP/verejne/katalog-ovm/8129) a [JSON export](https://data.gov.cz/datová-sada?iri=https%3A%2F%2Fdata.gov.cz%2Fzdroj%2Fdatové-sady%2FMV%2F706529437%2F44a9d6abacd4d0e83a0694e74d028f51) těchto dat
- [Data Poslanecké sněmovny a Senátu](https://www.psp.cz/sqw/hp.sqw?k=1300)
  - Jde o sadu datasetů, kterou na webu nikdy nenajdete, je ale velmi cenná.
  - Jde o denně aktualizované soubory, ve formátu podobné CSV, jejich zpracování je celkem snadné, jen pozor, jsou normalizovaná, takže budete občas joinovat přes několik tabulek.
  - Obsahuje mj.
    - Hlasování ve Sněmovně (od vzniku České republiky)
    - Stenozáznamy
    - Tisky ze Sněmovny i Senátu
    - Plány schůzí
    - Interpelace
- [Volby](https://volby.cz/opendata/opendata.htm)
  - Český statistický úřad nabízí data z voleb jako otevřená data, má to však několik zádrhelů.
  - Starší data jsou zpravidla v jiném formátu než ta současná (např. FoxPro vs. XML vs. CSV), takže pro delší časové řady musí člověk trochu pracovat.
  - Otevřená data neobsahují informace o historicky všech volbách v České republice, plné pokrytí je až cca od roku 2004. Pro starší informace musí jít člověk na web [volby.cz](https://volby.cz) a dohledat údaje tam.
  - Kandidáti ani zvolení zastupitelé nemají žádný unikátní identifikátor, celkem špatně se tedy mapují např. na angažované osoby z ARES nebo Justice, nemáme totiž ani datum narození, jen věk osoby, který není platný k nějakém určitému datu.
- [Centrální registr oznámení](https://cro.justice.cz) je informační systém založen pro účely zákona o střetu zájmů.
  - Obsahuje data o veřejných činitelích (soudci, zastupitelé, poslanci, ...), zejména pak jejich majetkové poměry, účastnictví ve firmách a funkce/členství.
  - _Systém nemá datový export nebo veřejné API_, k nahližení je ale i tak užitečný.
- registr prav a povinnosti
- wikidata?
- sčítání?

### Legislativa
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
- politicke finance
- rozhlas data
- úřední desky
- insolvence
- Něco z ČSÚ? ČNB (ARAD)?
- https://data.gov.cz/wishlist/