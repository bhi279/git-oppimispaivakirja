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
