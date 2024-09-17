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
