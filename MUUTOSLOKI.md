# Muutosloki – Tampereen seurakuntavaalit 2026

### 17.11.2026 – Vaalikohtaiset henkilöäänet tarkistettu

- Käyttäjän toimittamista neljästä seurakuntakohtaisesta tulospalvelun CSV-tiedostosta luettiin erikseen ylempi **yhteisen kirkkovaltuuston vaali** ja alempi **seurakuntaneuvoston vaali**. Molemmista käsiteltiin vain merkinnällä `Valittu` olevat henkilöt.
- Verrattiin 113 henkilö-/toimielin-/seurakuntatietuetta täsmällisellä nimiosumalla dashboardiin: **49 kirkkovaltuuston ääntä täsmäsivät jo ennestään**, **64 seurakuntaneuvoston äänimäärää lisättiin**. Ei puuttuvia tai ristiriitaisia osumia.
- Sekä yhteiseen kirkkovaltuustoon että seurakuntaneuvostoon valituille käytetään **kummankin vaalin omia ääniä**.
- Valitut henkilöt -näkymän lajittelut täsmennettiin kahdeksi vaihtoehdoksi: **Sukunimen mukaan (A–Ö)** ja **Äänimäärän mukaan (suurin ensin)**. Äänimäärä ei ole valintajärjestys (valinnan ratkaisee vertausluku).
- `neuvosto_aanet.csv` täydennettiin 64 lukuarvolla, ja numerot lisättiin myös itse dashboardin dataan, jotta ne toimivat ilman erillistä tiedostolatausta.
- Lähdetiedostot ladattu vaalien tulospalvelusta 17.11.2026. Tulokset saattavat vielä muuttua ennen vahvistamista.


Dashboard: https://samikallioinen-ops.github.io/tampere-vaalit-2026/

## 17.11.2026 – Luettavuus, lajittelu ja tietojen täydentäminen

- **Valitut henkilöt:** oletuslajittelu sukunimen mukaan (A–Ö) molemmissa toimielimissä. Myös sukunimeltään kaksiosaiset *Haurinen Karhola* ja *von Knorring* huomioitu. Äänimäärän mukainen lajittelu säilyy silloin, kun äänimäärät ovat käytettävissä.
- **Toimielimen nimi:** ”Yhteinen kirkkovaltuusto” käytössä kaikkialla käyttöliittymässä ja CSV-viennissä.
- **Luettavuus:** pienikokoisia tekstejä suurennettu, vaaleita harmaita tekstejä tummennettu ja henkilökorttien tietoihin lisätty kontrastia.
- **Seurakuntaneuvostojen äänet:** valmisteltu `neuvosto_aanet.csv` (64 valitun riviä neljässä suomenkielisessä seurakunnassa). Henkilökohtaiset äänimäärät puuttuvat toistaiseksi; dashboard osaa lukea ne tiedostosta, kun luvut täydennetään. Ruotsalaisen seurakunnan sopuvaalista ei ole henkilökohtaisia ääniä.
- Aloitettu tämä muutosloki, johon kirjataan vastaiset päivitykset.

## 17.11.2026 – Ikärakenteen toteutus ja rajaus

- Uusi **Ikärakenne**-välilehti seurakunta- ja toimielinvalitsimineen.
- Ikäryhmät 18–30, 31–50, 51–65 ja 66+ vuotta, ikäryhmien osuudet sekä keski-iät.
- Paikkajakonäkymän tavoin tummapohjaiset lukumäärät värillisissä palkeissa.
- Yksittäisten henkilöiden ikäluettelo ja henkilökorttien ikätiedot poistettu julkisesta versiosta. Koontitilastot säilytetty. **Huom:** henkilötason ikätietoja on yhä aiemmassa GitHub-commit-historiassa.
- Ruotsalaisen seurakunnan ikätiedot eivät sisälly näkymään sopuvaalin vuoksi.

## Aiempi prototyyppi

- Äänestysaktiivisuuden, paikkajaon, edustavuuden ja valittujen henkilöiden vertailunäkymät sekä CSV-vienti. Tarkemmat alkuperäiset muutokset löytyvät GitHubin commit-historiasta.

## Tiedossa olevat täydennykset

- **Seurakuntaneuvostojen henkilökohtaiset äänimäärät**: 64 valitun luvut lisätään tiedostoon `neuvosto_aanet.csv`, kun ne on tarkistettu tulospalvelusta.
- **Vaalituloksen vahvistus ja lähteiden ristiriidat**: ks. dashboardin Tietolähteet-välilehti.
