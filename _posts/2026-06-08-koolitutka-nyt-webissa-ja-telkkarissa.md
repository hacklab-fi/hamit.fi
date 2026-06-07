---
layout: post
title: Koolitutka nyt netissä ja telkkarissa!
subtitle: Koolitutka ei ole enää vain chattibotti.
comments: false
tags: [koolitutka, tekstitv]
---

Koolitutka on ollut chattibotti, joka on palvellut aluksi OH6AD:n
irkkikanavalla vuodesta 2016 ja vuodesta 2020 myös meidän monialustaisessa
Hamit.fi-keskusteluhuonessa. Se on väsymättä kymmenen vuoden
ajan seurannut muutoksia Traficomin julkaisemassa voimassaolevien
radioamatöörikutsujen listassa.

Bottimme ei ole menossa mihinkään, mutta on saanut rinnalleen kaksi
jämäkkää mediaa niin menneisyydestä kuin tulevaisuudestakin. Nimittäin
[Teksti-TV:n](https://fi.wikipedia.org/wiki/Teksti-TV) ja Webin.

Kummankin eteen on tehty jämäkkää tuotekehitystä nykymaailman keinoin
tekoälyä kaihtamatta. Lopputuloksena on käyttöliittymä, joka
kunnioittaa yksityisyyttäsi, eli paluukanavaa ei ole. Teksti-TV
luonnollisesti on yksisuuntainen, mutta myös toteutettu webbipalvelu
on sellainen, että se lataa tietokannan käyttäjän selaimeen
kokonaisuudessaan ja käyttäjän tekemiä kyselyitä ei lähetetä lainkaan
verkkoon vaan data luetaan selaimen muistissa olevasta
[SQLite](https://fi.wikipedia.org/wiki/SQLite)-tietokannasta.

Syytä tälle ei oikeastaan ole muuta kuin sen näyttäminen, että
tällaistakin sekoilua voi yhä harrastaa. Ja hauskaa onkin ollut. Lähtien
siitä, että Teksti-TV-sivujen lähettämistä varten on täytynyt
[takaisinmallintaa](https://fi.wikipedia.org/wiki/Takaisinmallinnus)
Ylen Teksti-TV-Editorin protokolla ja rakentaa sen pohjalta moderni
komentorivityökalu
[ylettv-cli](https://github.com/zouppen/ylettv-cli).

Teksti-TV:stä Koolitutka löytyy sivun Suomen Radioamatööriliiton sivun
590 alasivulta 10, joka tämän jutun julkaisuhetkellä näytti tältä:

![Teksti-TV-sivu](/assets/img/ttv.png "Ylen Teksti-TV:n sivu 590-10")

Ja tuoreimman näkymän saa auki tietysti lähimmästä telkkarista tai
[Teksti-TV:n verkkoversiosta](https://yle.fi/aihe/tekstitv?P=590#10).

Webbisovellus on puolestaan saatavilla osoitteesta
[koolit.hamit.fi](https://koolit.hamit.fi/) ja se näytti julkaisuhetkellä tältä:

![Koolitutka-ruutukaappaus](/assets/img/koolitutka-ruutu.png "Koolitutkan käyttöliittymä")

Lähdekoodiin voi tutustua [GitHubissa](https://github.com/OH6AD/koolitutka).

Nauttikaa!

*Joel Lehtonen / OH64K / Zouppen*
