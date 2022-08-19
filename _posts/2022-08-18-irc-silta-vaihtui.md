---
layout: post
title: IRC-silta vaihtui
subtitle: Taustaa muutoksen takaa ja pari ohjetta IRC-käyttäjille
comments: false
tags: [irc]
---

Elokuun puolessavälissä jouduimme vaihtamaan IRC-sillan aiemmasta
Twenten yliopiston ylläpitämästä sillasta Suomen Hacklabien liiton
[Hacklab ry](https://hacklab.fi/):n ylläpitämään siltaan. Tässä hiukan
taustaa muutoksen takaa ja vinkkejä IRC-käyttäjille muutoksen jälkeen.

## IRC:stä

[IRC](https://en.wikipedia.org/wiki/Internet_Relay_Chat) on yksi
Hamit.fi-keskusteluryhmän viestimistä [Matrixin](https://matrix.org/),
Telegramin ja WhatsAppin ohella. Kun erityisesti WhatsApp-käyttäjäksi
ajaudutaan ympäristön painostuksesta, niin IRC:llä on oma vannoutunut
käyttäjäkuntansa. On toki myös mukava tukea alustaa, jolla on jopa
1980-luvulta ulottuva historia, yksi Internetin pitkäikäisimmistä yhä
käytössä olevista protokollista.

Tätä kirjoittaessa IRC-käyttäjiä ryhmässä on 20 yhteensä 130:n käyttäjän
joukosta.

## Miksi muutos tehtiin?

Tähän saakka käyttämämme [Twenten
yliopiston](https://www.snt.utwente.nl/en/service/matrix) silta on
ns. puppetoiva, eli jokaista käyttäjää vastaa oma IRC-nimimerkkinsä
kanavalla. Tämä helpottaa kommunikaatiota ja tämän lisäksi käytössä on
ollut [IRC-nimimerkkejä vaihtava
sovellus](https://github.com/HacklabJKL/matrix-irc-nick/), joka on
laittanut nimimerkin perään kirjaimen, josta pystyi päättelemään, onko
käyttäjä esimerkiksi Telegramista tai WhatsAppista. Näille ihmisille
ei pystynyt myöskään lähettämään yksityisviestejä.

Siltaa ylläpitävän Twenten palvelimet ovat eri teknisistä syistä
olleet kovan kuormituksen alla. IRC-käyttäjämäärän laskiessa ja
Matrixin käyttäjämäärän kasvaessa kymmeniin miljooniin on merkittävä
osuus IRC-liikenteestä kulkenut tämän yhden pisteen kautta. Lisäksi
kyseinen JavaScriptillä toteutettu silta,
[matrix-appservice-irc](https://github.com/matrix-org/matrix-appservice-irc),
on todettu hankalasti ylläpidettäväksi ja vikaherkäksi ja siinä on
ollut pahimmillaan useamman päivän mittaisia huoltokatkoja.

Viime keväänä Hacklab-yhteisö tarjosi
[Assembly-tietokonetapahtumalle](https://assembly.org/) käyttöön uuden
IRC-siltausratkaisun,
[Heisenbridgen](https://github.com/hifi/heisenbridge), joka käyttää
perinteisempää relaybot-tyyppistä siltausta, jossa IRC:n suuntaan on
yksi nimimerkki mutta aiemmista relaybot-silloista poiketen Matrixin
suuntaan puppetoiva ratkaisu, eli Matrixin suunnalla jokainen
IRC-käyttäjä näkyy omana nimimerkkinään.

Assembly-yhteisössä parannus oli huomatava aiempiin erillisiin
siltausjärjestelmiin verrattuna ja kokemuksesta rohkaistuneena
päätimme, että otamme sillan käyttöön laajemminkin jossakin vaiheessa
tänä vuonna.

Aikataulu kuitenkin nopeutui, kun kamelin selän katkaisi
se, että IRC-silta alkoi siivota yli 90 päivää idlanneita käyttäjiä
pois ja Telegram-sillan kautta potkut propagoituivat Telegrammiin
asti, poistaen parisenkymmentä Telegram-käyttäjää
Hamit.fi-ryhmästä. Se oli vielä pientä verrattuna
[Instanssi](https://instanssi.org/)-tapahtuman yhteisöön. Monet
käyttäjistä siellä olivat seuranneet tiedotusta, mutta eivät
kommentoineet mitään, joten huonostihan siinä kävi. Silta kävi
heittämässä yhteensä 70 käyttäjää pellolle.

## Käyttöönotto

Eli jotakin hyvää, jotakin huonoa. Luotettavuus on tuntuvasti parempi
ja järjestelmä yksinkertaisempi, mutta IRC-käyttäjät kokevat tämän
tietysti hiukan sotkuisempana kuin edellisen ratkaisun. Matrixia ja
muita viestimiä käyttäville kokemus ei muutu.

Käyttöönotto toteutettiin viikolla 33/2022 ja aiheetta poistetut
Telegram-käyttäjät saatiin myös pyydettyä liittymään takaisin ryhmään,
joten pysyvämpää vahinkoa ei sattunut.

## Pari hyödyllistä skriptiä irkkaajille

Nykyinen Heisenbridge tuottaa jonkun verran enemmän roskaa
irkkikanavalle, kun viestit tulevat yhdeltä käyttäjältä. Tähän on
olemassa kuitenkin keinoja, joilla viestit saa näyttämään selkeämmiltä:

* Irssi: [Detelexify-skripti](https://github.com/zouppen/irssi-detelexify/)
* WeeChat: [Relaybot-liipaisin](https://github.com/weechat/weechat/wiki/Triggers#relaybot)

*Joel Lehtonen / OH64K / Zouppen*
