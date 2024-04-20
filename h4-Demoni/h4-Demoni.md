# h3 Demoni
Neljäs viikkotehtävä, raportin teko alkaa 20.4.2024 klo 12:00. Työskentely tapahtuu omalla kannettavalla tietokoneella, joka on kevyeen pelikäyttöön tarkoitettu, ja opiskeluun täysin riittävä. Nettiyhteys on taloyhtiöethernet varustettuna tarpeeksi suurella lisänopeudella. Raportti sekä tehtävät tulee tehtyä osissa, ja tehtävien tekoajat ovat merkittynä väliotsikoihin.

### Tehtävät (Karvinen, T.2024)
- x) Lue ja tiivistä
- a) Hello SLS! Tee Hei maailma -tila kirjoittamalla se tekstitiedostoon, esim /srv/salt/hello/init.sls
- b) Top. Tee top.sls niin, että useita valitsemiasi tiloja ajetaan automaattisesti, esim komennolla "sudo salt '*' state.apply" tai "sudo salt-call --local state.apply"
- c) Apache easy mode. Asenna Apache, korvaa sen testisivu ja varmista, että demoni käynnistyy.
  - Ensin käsin, vasta sitten automaattisesti.
  - Kirjoita tila sls-tiedostoon.
  - pkg-file-service
  - Tässä ei tarvita service:ssä watch, koska index.html ei ole asetustiedosto
- d) SSHouto. Lisää uusi portti, jossa SSHd kuuntelee.
  - Jos käytät Vagrantia, muista jättää portti 22/tcp auki - se on oma yhteytesi koneeseen. SSHd:n asetustiedostoon voi tehdä yksinkertaisesti kaksi "Port" riviä, molemmat portit avataan.
  - Löydät oikean asetuksen katsomalla SSH:n asetustiedostoa
  - Nyt tarvitaan service-watch, jotta demoni käynnistetään uudelleen, jos asetustiedosto muuttuu masterilla
  - e) Vapaaehtoinen: Apache. Asenna Apache tarjoilemaan weppisivua. Weppisivun tulee näkyä palvelimen etusivulla (localhost). HTML:n tulee olla jonkun käyttäjän kotihakemistossa, ja olla muokattavissa normaalin käyttäjän oikeuksin, ilman sudoa.
- f) Vapaaehtoinen: Caddy. Asenna Caddy tarjoilemaan weppisivua. Weppisivun tulee näkyä palvelimen etusivulla (localhost). HTML:n tulee olla jonkun käyttäjän kotihakemistossa, ja olla muokattavissa normaalin käyttäjän oikeuksin, ilman sudoa.
- g) Vapaaehtoinen: Nginx. Asenna Nginx (lausutaan engine-X) tarjoilemaan weppisivua. Weppisivun tulee näkyä palvelimen etusivulla (localhost). HTML:n tulee olla jonkun käyttäjän kotihakemistossa, ja olla muokattavissa normaalin käyttäjän oikeuksin, ilman sudoa.

### HostOS
- Asus Tuf Gaming A15 FA506QM kannettava tietokone
- Käyttöjärjestelmä: Windows 11 Home
- Prosessori: AMD Ryzen 7 5800H, 8 ydintä 3200GHz
- Muisti: 16 Gt
- Näytönohjain 6144Mt omalla muistilla

### GuestOS
- Debian Bookworm, 64-bit
- 4 prosessoriydintä
- 7981 Mt RAM

### Lähteet
- Karvinen, T. 2024. Tehtävänanto. https://terokarvinen.com/2024/configuration-management-2024-spring/#h4-demoni
