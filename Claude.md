Olet senior frontend-kehittäjä. Rakenna täydellinen suomenkielinen autoliikkeen verkkosivusto staattisena HTML/CSS/JS-projektina. Sivusto on tarkoitettu Verceliin deployattavaksi ja sen sisältö crawlataan RAG-chatbotin tietolähteeksi — siksi sivuilla pitää olla paljon informatiivista tekstisisältöä, ei pelkkiä kuvia ja nappeja.

Yrityksen tiedot
Nimi: AutoCenter Helsinki
Sijainti: Mäkelänkatu 42, 00550 Helsinki
Puhelin: 09 123 4567
Sähköposti: myynti@autocenterhki.fi
Aukioloajat: ma-pe 9-18, la 10-15, su suljettu
Y-tunnus: 1234567-8
Perustettu: 2008
Henkilöstö: 12 työntekijää, 4 myyjää, 3 mekaanikkoa
Toimitusjohtaja: Mikko Lahtinen
Sivurakenne (jokainen omana .html-tiedostona)
index.html — Etusivu

Hero-alue sloganilla ja CTA
Lyhyt esittely yrityksestä (historia, arvot, miksi valita meidät)
3 nostettua vaihtoautoa varastosta
Asiakasarviot (3-4 kpl, keksittyjä mutta realistisia)
Yhteystiedot footer
varasto.html — Vaihtoautovarasto (lista)

Vähintään 12 autoa kortteina (grid-layout)
Jokaisessa: merkki, malli, vuosimalli, kilometrit, polttoaine, vaihteisto, hinta
Hintaluokat 8 000 € – 45 000 €
Monipuolisesti eri merkkejä: Toyota, Volkswagen, Škoda, BMW, Mercedes, Volvo, Tesla, Hyundai jne.
Linkki yksittäisen auton sivulle
auto-[1-12].html — Yksittäisen auton sivu (12 kpl)

Auton täydelliset tekniset tiedot: moottori, teho (kW/hv), vääntö, CO2-päästöt, kulutus (l/100km), vetotapa, renkaat, väri, paino, tilavuus
Varusteet listamuodossa (vähintään 10 per auto): ilmastointi, navigaattori, peruutuskamera, lämmitettävät istuimet, LED-ajovalot jne.
Katsastustiedot, seuraava katsastus
Huoltohistoria lyhyesti (esim. "Merkkihuollettu, huoltokirja")
Hinta ja rahoitusesimerkki (kuukausierä)
CTA: "Kysy lisää" ja "Varaa koeajo"
Myyjän nimi ja puhelinnumero
rahoitus.html — Rahoitus ja vakuutukset

Rahoitusvaihtoehdot: osamaksu, leasing, ballon-rahoitus
Jokaisesta selitys miten toimii, kenelle sopii, tyypillinen korko ja laina-aika
Esimerkkilaskelma taulukkomuodossa (15 000 € auto, 3 vuotta, eri koroilla)
Rahoituskumppanit: Santander, Nordea Rahoitus
Vakuutusyhteistyö: If, LähiTapiola — liikennevakuutus, kasko, autoturva
FAQ: "Saanko rahoituksen?", "Mikä on käsiraha?", "Voiko laina-aikaa pidentää?" jne.
vaihtoauto-arvio.html — Vaihtoautoarvio ja myynti

Miten vaihtoautoarvio toimii (prosessi vaihe vaiheelta)
Mitä tarvitaan: rekisterinumero, kilometrit, kuntoluokka, huoltohistoria
Vaihdossa tuonti: "Tuo vanha autosi meille, hyvitämme sen uuden hinnasta"
Konsignaatiomyynti: "Myymme autosi puolestasi, provisio 5 %"
Lomake (HTML form, ei tarvitse toimia): nimi, puhelin, sähköposti, auton tiedot, vapaa viesti
huolto.html — Huolto ja korjaamopalvelut

Palvelulista: määräaikaishuollot, öljynvaihdot, jarruhuollot, jakohihnan vaihto, ilmastointihuolto, renkaanvaihto, nelipyöräsuuntaus, pakoputkiremontit, diagnostiikka (OBD), katsastuskunnostus
Jokaisen palvelun lyhyt kuvaus ja suuntaa-antava hinta
Huoltovaraus-lomake (staattinen)
Huollon aukioloajat (eri kuin myynti)
Takuuhuollot: "Teemme myös takuunalaiset huollot"
yritys.html — Tietoa meistä

Yrityksen historia 2008 → nyt (aikajana-tyylinen)
Arvot: rehellisyys, läpinäkyvyys, asiakaslähtöisyys
Henkilöstöesittely: toimitusjohtaja, myyntipäällikkö, 2 myyjää, huoltopäällikkö (nimi, rooli, lyhyt esittely jokaisesta)
Tunnusluvut: "Yli 3 000 autoa myyty", "4.7/5 Google-arvosana", "15 vuotta kokemusta"
Sertifikaatit ja jäsenyydet: Autoalan Keskusliitto AKL, Luotettava Kumppani
yhteystiedot.html — Yhteystiedot

Osoite, kartta (Google Maps embed placeholder), puhelinnumerot, sähköpostit
Ajo-ohjeet: "Kehä I:ltä, käänny Mäkelänkadulle..."
Yhteydenottolomake (staattinen)
Henkilöstön suorat yhteystiedot (myynti, huolto, hallinto)
Tekniset vaatimukset
Puhdas HTML5 + CSS (Tailwind CDN tai oma CSS, ei build-toolia)
Responsiivinen (mobile-first)
Yhteinen header (navigaatio) ja footer kaikilla sivuilla
Kuvat: käytä Unsplash-kuvia suoraan URL:lla (esim. https://images.unsplash.com/photo-XXXXX?w=600) — etsi oikeat kuva-ID:t autoista, autokaupasta, huollosta
Semantic HTML: käytä article, section, nav, main, aside oikein — tämä on tärkeää koska sivut crawlataan ja parsitaan koneellisesti
Värimaailma: tummansininen (#1e3a5f) + valkoinen + oranssi korostusväri (#f97316)
Fontti: Inter (Google Fonts)
Ei frameworkeja, ei npm:ää, ei buildeja — pelkkä staattinen sivusto joka toimii avaamalla index.html selaimessa
Tärkeää sisällön kannalta
Sivuston tarkoitus on toimia RAG-chatbotin tietolähteenä. Siksi:

Kirjoita paljon informatiivista tekstiä — ei pelkkiä luetteloita vaan myös selittäviä kappaleita
Käytä luonnollista kieltä jota asiakas kysyisi: "Minkälaisia rahoitusvaihtoehtoja on?", "Paljonko jakohihnan vaihto maksaa?", "Onko teillä sähköautoja?"
Jokaisella sivulla tulee olla vähintään 300 sanaa varsinaista sisältötekstiä
Autojen kuvauksissa käytä myyjämäistä mutta informatiivista kieltä: "Erittäin siisti ja hyvin huollettu perhesedaani..."
Hintatiedot oltava selkeästi esillä (crawleri poimii ne)
Tästä tulee n. 20+ HTML-tiedostoa ja 1 CSS. Luo kaikki tiedostot kerralla. Aloita.