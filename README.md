# git-oppimispaivakirja

Git-versionhallinta - SOF011AS2A-3002
Janne Airaksinen

Tämä on Git-versionhallintakurssin oppimispäiväkirja.

# Oppimispäiväkirja: Paikallinen git

**Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?**

Vaikeaa oli välillä ymmärtää sanan "talletus" eri merkitykset. Jouduin pohtimaan, tarkoitettiinko talletuksella yksinkertaista tiedoston talletusta ctrl+s vai commitia. Aineiston alun sanasto auttoi tässä. Hämmennys varmaankin johtui siitä, että olen tottunut puhumaan "commiteista" ja "committauksesta" suomenkielisen talletuksen sijaan. Oppimista tuki myös Git cheatsheet (https://education.github.com/git-cheat-sheet-education.pdf) joka kerää gitin tärkeimmät komennot yhteen. Helppoa oli gitin peruskomennot init, config, clone, add, commit, branch ja switch sillä näitä olen käyttänyt jo aiemmilla kursseilla varsin paljon. Komennoista haastavia oli peruutukseen liittyvät komennot sillä nämä olivat minulle entuudestaan tuntemattomia, ja lisäksi ne vielä vastaavat toisiaan varsin paljon (resert, restore ja revert). Kun seuraavan kerran tarvitsen näitä, myönnän joutuvani tarkastamaan niiden tarkan toiminnallisuuden cheatsheetista tai kurssin materiaaleista. Peruutuksiin liittyvä "lopullisuus" tuntuu vielä tässä vaiheessa pelottavalta, kun paljoa kokemusta näiden komentojen käyttämisestä ei ole kertynyt.

Koin, että opin parhaiten tekemällä tehtäviä. Tehtävänannot mielestäni tukivat oppimista siinä, että niissä oltiin vaihe vaiheelta kerrottu mitä tulisi tehdä, ja kehotettu tarkastamaan tilanne status- tai log-komennoilla. Näillä komennoilla muiden komentojen (esim. add, switch, commit) toiminnallisuus selkeytyi. Gitin ymmärtämistä helpottaa myös se, että git myös ehdottaa seuraavia komentoja, esim. commit add-komennon jälkeen.

## Osiossa käyttämäni Git-komennot

| Komento                              | Kuvaus                                                                                                                                        |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| init                                 | git-repositorion alustaminen                                                                                                                  |
| config -list                         | kaikkien git-asetusten tarkastelu                                                                                                             |
| config user.name                     | git-käyttäjätunnuksen tarkastelu                                                                                                              |
| config user.name [käyttäjätunnus]    | git-käyttäjätunnuksen asettaminen                                                                                                             |
| config user.email                    | git-sähköpostiosoitteen tarkastelu                                                                                                            |
| config user.email [sähköpostiosoite] | git-sähköpostiosoitteen asettaminen                                                                                                           |
| clone [git-repositorion osoite]      | git-repositorion kloonaaminen etärepositoriosta paikalliseen repositorioon                                                                    |
| status                               | repositorion tiedostojen tilan tarkastelu (mitä tiedostoja on muutettu, mitkä on lisätty, mitkä ovat staging-alueella, millä haaralla ollaan) |
| log                                  | talletuslokin tarkastelu                                                                                                                      |
| log --stat                           | talletuslokin tarkastelu lisätiedoilla                                                                                                        |
| rm [tiedosto/kansio]                 | tiedoston/kansion poistaminen                                                                                                                 |
| mv [vanha] [uusi/kohde]              | tiedoston/kansion siirtäminen tai uudelleen nimeäminen                                                                                        |
| add [tiedosto]                       | valitun tiedoston muutoksien lisääminen staging-alueelle                                                                                      |
| add .                                | kaikkien tehtyjen muutosten lisääminen staging-alueelle                                                                                       |
| commit                               | staging-alueelle lisättyjen muutosten talletus                                                                                                |
| commit -m [kommentti]                | staging-alueelle lisättyjen muutosten talletus ja kommentin lisäys                                                                            |
| switch [haara]                       | vaihtaminen toiseen haaraan                                                                                                                   |
| switch -c [haara]                    | uuden haaran luominen ja siihen vaihtaminen                                                                                                   |
| branch                               | kaikkien haarojen tarkastelu                                                                                                                  |
| branch -d [haara]                    | haaran poistaminen                                                                                                                            |
| reset [tiedosto]                     | add-komennon peruuttaminen (tiedoston poistaminen staging-alueelta)                                                                           |
| restore [tiedosto]                   | tiedoston tuoreimman version palauttaminen                                                                                                    |
| revert [commit-hash]                 | commitin palauttaminen ja jäljen jättäminen versionhallintaan                                                                                 |

# Oppimispäiväkirja: Hajautettu git

**Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?**

En entuudestaan tarkkaan tiennyt fetch- ja pull-komentojen eroa. Tiesin, että niilä haetaan tietoa etärepositorioista paikalliseen repositorioon, mutta en esim. sitä, että pull-komennolla haetut tiedot yhdistetään paikallisen repositorion haaraan, ja fetchillä taas voi itse päättää haluaako tiedon yhdistää vai ei.

Tähän taitaa vielä liittyä usein kuulemani mutta toistaiseksi tuntematon pull request, jolla ilmeisesti ehdotetaan koodimuutoksia yhdistettäväksi päähaaraan. Pull requestissa olennaista on ymmärtääkseni se, että joku toinen arvioi koodin ja hyväksyy yhdistämisen sen jälkeen kun on varmistettu, että lisättävä koodi täyttää laatuvaatimukset eikä riko aikaisempaa koodia. Pull requestit lienevät opetuksessa harvinaisempia (?), mutta työelämässä yleisempiä.

Jälleen kerran oppimistani tuki käytännön tekeminen. Lisäksi huomaan että aikaisemma git-tiedot tukevat uuden oppimista; minulla on jokin aavistus siitä, mihin asiat liittyvät, mikä helpottaa asioiden ymmärtämistä.

## Osiossa käyttämäni Git-komennot

| Komento                                    | Kuvaus                                                               |
| ------------------------------------------ | -------------------------------------------------------------------- |
| remote                                     | listaa paikallisen repositorion etärepositoriot                      |
| remote add origin [etärepositorion osoite] | määrittää paikalliselle repositoriolle etärepositorion               |
| remote -v                                  | listaa etärepositoriot ja kertoo niistä tietoja                      |
| branch -r                                  | listaa etärepositorion haarat                                        |
| fetch origin                               | lataa etärepositiorion haarat paikalliseen repositorioon             |
| push                                       | työntää paikallisen repositorion muutokset etärepositorioon          |
| push -u origin main                        | työntää muutokset ja asettaa oletusarvoisen haaran etärepositoriossa |

# Oppimispäiväkirja: Git projektissa

**Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?**

Versionhallinnasta on hyötyä, vaikka projektia kehittäisi yksinkin. Ensimmäinen mieleen tuleva asia on ohjelmakoodin tallennus ja säilytys, jolloin aikaisempiin versioihin palaaminen on helppoa jos jokin menee pieleen. Tähän liittyy myös haarat, jolloin voi turvallisesti kokeilla ja kehittää uusia toiminnallisuuksia niin, että ei sotke varsinaista jo toimivaa ja testattua koodia. Lisäksi versionhallinnan käyttäminen yksin on hyvää harjoitusta versionhallinnan käytöstä!

**Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?**

Useamman kehittäjän yhteistyössä versionhallinta auttaa työn jakamisessa. Voimme tiimissä sopia, kuka tekee minkäkin toiminnallisuuden ohjelmaan, ja versionhallinnan avulla voimme kaikki työstää omia toiminnallisuuksiamme yhtä aikaa. Saamme käsiimme myös muiden tekemät muutokset, jolloin myös oma ohjelmakoodimme on ajan tasalla.

**Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.**

Lisätkää kaikki tiimiläiset samaan repositorioon ja kloonatkaa se itsellenne. Sopikaa, kuka työstää mitäkin työjonon toiminnallisuutta. Sopikaa talletusviestien käytännöistä ja varmsita omalta osaltasi, että oikeasti kirjoitat talletusviestejä. Sopikaa koodin formatointikäytännöstä, mikä vähentää turhien muutosten näkymistä versionhallinnassa. Käyttäkää haaroja kokeilemaan ja testaamaan omia toiminnallisuuksianne ja puskekaa niitä vain etärepositorion feature-haaraan; main-haaraan puskeminen voidaan tehdä yhteisen katselmoinnin jälkeen. Kommunikoikaa keskenänne myös päivittäisten kokousten ulkopuolella.

**Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?**

Työmäärä oli sopiva. Muuttaisin ehkä itse materiaalia niin, että suomenkielisten termien lisäksi materiaalissa puhuttaisiin enemmän englanninkielisillä termeillä, sillä nämä tulevat useammin esille oikeassa kielenkäytössä (talletus -> committaus).
