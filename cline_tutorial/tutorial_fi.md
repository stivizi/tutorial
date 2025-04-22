# VS Code, Cline ja OpenRouter: Ensimmäinen tekoälyseikkailusi! ✨

Hei ja tervetuloa! Tämä opas opastaa sinut käyttämään VS Codea Cline-laajennuksen ja OpenRouterin kanssa tutkiaksesi tekoälyagenttien jännittävää maailmaa. Älä huoli, jos et ole koskaan aiemmin koodannut – otamme sen askel kerrallaan.

## Mitä tarvitset aloittamiseen 🚀

* **Tietokone:** Mikä tahansa tietokone (Mac, Windows tai Linux) toimii täydellisesti.
* **Internet-yhteys:** Tarvitset tämän ladataksesi muutaman ilmaisen työkalun.
* **Hymy ja osaava asenne!** Oppiminen on hauskaa, ja olemme täällä auttamassa.

## Vaihe 1: VS-koodin valmistaminen 💻

Visual Studio Code (VS Code) on kuin superälykäs muistilehtiö koodin kirjoittamiseen. Se on ilmainen, ja käytämme sitä puhuaksemme tekoälyn kanssa!

1. **Lataa VS-koodi:** Ajattele tätä sovelluksen hankkimisena. Siirry VS Coden verkkosivustolle ([https://code.visualstudio.com/](https://code.visualstudio.com/)) internetselaimella (kuten Chrome, Safari tai Firefox). Etsi iso painike ladataksesi oikean version tietokoneellesi (Windows, Mac tai Linux).

2. **Asenna VS-koodi:** Tämä on kuin sovelluksen asentaminen tietokoneellesi. 
* **Windows:** Kaksoisnapsauta lataamaasi tiedostoa. Ikkuna avautuu - seuraa ohjeita, napsauta "Seuraava" muutaman kerran ja sitten "Asenna". 
* **Mac:** Kaksoisnapsauta ladattua tiedostoa. Se avaa ikkunan. Vedä VS-koodikuvake "Sovellukset"-kansioon. 
* **Linux:** Asennusprosessi voi vaihdella jakelustasi riippuen. Noudata VS Code -sivustolla olevia ohjeita järjestelmällesi.

3. **Käynnistä VS-koodi:** Etsi VS-koodi tietokoneesi valikosta (yleensä "Sovellukset"-kohdasta Macissa tai "Käynnistä"-valikosta Windowsissa) ja avaa se napsauttamalla sitä. Sinun pitäisi nähdä tervetulonäyttö! 🎉

## Vaihe 2: Clinen lisääminen VS-koodiin (The Magic Wand! ✨)

Cline on kuin taikasauva, jonka avulla VS Code voi puhua tekoälylle. Lisää se seuraavasti:

1. **Avaa VS-koodi:** Jos suljit VS-koodin, avaa se uudelleen.

2. **Etsi Extensions-painike:** Etsi VS-koodin vasemmalta puolelta neliökuvaketta, joka on tehty pienemmistä neliöistä. Sitä kutsutaan "Laajennukset"-näkymäksi. Voit myös avata sen painamalla Ctrl+Shift+X (tai Macissa Cmd+Shift+X).

3. **Hae Cline:** Kirjoita Laajennukset-näkymän yläreunassa olevaan hakukenttään "Cline".

4. **Asenna Cline:** Näet Cline-laajennuksen hakutuloksissa. Sen pitäisi olla Cline-logolla varustettu. Napsauta sen vieressä olevaa "Asenna" -painiketta.

5. **Lataa VS-koodi uudelleen:** Kun Cline on asennettu, VS Code pyytää sinua lataamaan ikkunan uudelleen. Tämä on kuin sovelluksen käynnistäminen uudelleen varmistaaksesi, että Cline on valmis. Napsauta "Lataa uudelleen" -painiketta.

## Vaihe 3: Yhdistäminen OpenRouteriin (The AI ​​Brain! 🧠)

OpenRouter on kuin portti moniin erilaisiin tekoälyaivoihin. Meidän on yhdistettävä Cline OpenRouteriin, jotta se voi esittää kysymyksiä ja saada vastauksia.

1. **Luo OpenRouter-tili:** Ajattele tätä avaimena tekoälymaailmaan. Avaa Internet-selain ja siirry OpenRouter-verkkosivustolle ([https://openrouter.ai/](https://openrouter.ai/)). Napsauta "Rekisteröidy" ja seuraa ohjeita luodaksesi ilmainen tili.

2. **Hanki salainen API-avain:** Kun olet kirjautunut sisään, vie hiiri profiilikuvasi/kuvakkeen päälle (oikeassa yläkulmassa) ja valitse "API-avaimet" tai "Avaimet". Täällä voit luoda salaisen avaimesi. Luo uusi API-avain napsauttamalla painiketta ja anna sille projektiisi tai käyttötapaukseen liittyvä nimi. 
* **Tärkeää:** Tämä avain on kuin salasana, joten säilytä se turvassa äläkä jaa sitä kenenkään kanssa!

3. **Määritä Cline OpenRouterin avulla:** Nyt meidän on määritettävä Cline käyttämään OpenRouteria. Toimi seuraavasti: 

![OpenRouter API -määritysnäyttö](setting_openrouter_api.jpg) 
1. **Aktivoi Cline:** Napsauta Cline-kuvaketta VS Coden sivupalkissa. 

2. **Avaa Cline Settings:** Etsi asetusten rataskuvake Cline-paneelista. 

3. **Valitse OpenRouter:** Valitse avattavasta API Provider -valikosta "OpenRouter". 

4. **Liitä OpenRouter Key:** Kirjoita OpenRouter API -avain sille varattuun kenttään. 

5. **Valitse malli:** Valitse malli avattavasta valikosta. Jos olet vasta aloittamassa, kokeile jotakin ilmaisista malleista. 

6. **Valitse (Ota käyttöön) Suunnittele:** Tämä määrittää vuorovaikutustilan tekoälyn kanssa.



## Vaihe 4: Esitä ensimmäinen kysymyksesi! ❓

Aika katsoa toimiiko kaikki! Esitämme yksinkertaisen kysymyksen ja katsomme, saako Cline vastauksen OpenRouterilta.

1. **Luo uusi tiedosto:** Napsauta VS Codessa viestin syöttöruutua ikkunan vasemmassa alakulmassa. (huom

2. **Kirjoita kysymyksesi:** Kirjoita nyt seuraava kysymys viestin syöttöruutuun: Mikä on Ranskan pääkaupunki?

3. **Kysy Clinelta vastausta:** Napsauta lähetyskuvaketta

4. **Katso vastaus!** Cline lähettää kysymyksesi OpenRouterille, ja OpenRouter käyttää tekoälyä löytääkseen vastauksen. Vastaus tulee näkyviin yllä olevaan viestiketjuun. Sen pitäisi sanoa jotain tällaista: "Ranskan pääkaupunki on Pariisi." 🎉

## Teit sen! 🎉

Taputa itseäsi selkään! Olet onnistuneesti määrittänyt VS Coden, asentanut Clinen, yhdistäted OpenRouteriin ja esitti ensimmäisen tekoälykysymyksesi. Olet virallisesti AI-matkailija!

## Mitä seuraavaksi? 🚀

Nyt alkaa todellinen hauskuus! Tässä on muutamia ideoita oppimisen jatkamiseksi:

* **Kysy lisää kysymyksiä!** Kokeile kysyä Clinelta erilaisia ​​kysymyksiä. Mitä tapahtuu, jos pyydät sitä kirjoittamaan runon? Tai kääntää lause toiselle kielelle?

* **Tutustu erilaisiin tekoälymalleihin:** OpenRouter antaa sinulle pääsyn moniin erilaisiin tekoälyaivoihin. Katso, voitko selvittää, kuinka voit vaihtaa niiden välillä ja vertailla heidän vastauksiaan.

* **Lue Cline Manual:** Clinella on monia muita temppuja hihassaan! Tutustu asiakirjoihin saadaksesi tietoa kaikista hienoista asioista, joita se voi tehdä.

Jatka tutkimista, jatka kysymysten esittämistä ja mikä tärkeintä, pidä hauskaa!
