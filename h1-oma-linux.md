# Oma Linux -raportti

### Raportin kirjoittaminen:

- Raportin tulee olla sellainen että toinen henkilö voi toistaa tehdyt toimenpiteet ja saada saman tuloksen. Ympäristö jossa testi tehtiin tulee myös raportoida tarkasti.
  
- Raportissa pitää myös ilmoittaa tarkasti annetut komennot tai klikatut kohteet sekä tulokset joita saatiin. Tämä sisältää esimerkiksi kellonajat ja vikailmoitukset. Jos komennot onnistuivat tai epäonnistuivat tulee seuraavat toimenpiteet myös kirjoittaa. Raportti tulee kirjoittaa menneessä aikamuodossa.
  
- Raportti kannattaa kirjoittaa huolellisesti ja selkeästi. Väliotsikoiden käyttö ja kieliopillisesti oikein kirjoittaminen parantavat raportin luettavuutta.
  
- Viittaukset osoittavat perehtyneisyyttä ja ovat akateeminen tapa. Haaga-Helian lähdeviittaukset löytyvät sivulta: https://libguides.haaga-helia.fi/lahdeviittaamisen-tueksi/tekstiviitteet-ja-lahdeluettelo.
  
- Raportteihin voidaan liittää vakiotekstejä kuten lisenssiehtoja jotka määrittelevät dokumentin käyttöoikeuden.
  
- Viimeisenä mutta ei vähäisempänä mokien välttäminen raportissa. Vältä sepittäminen plagiointi ja luvattomien kuvien käyttö. Niiden sääntöjen rikkominen voi johtaa vakaviin seuraamuksiin kuten syytöksiin vilpistä.
  
### Free Software Foundation: FSF Free Software Definition

- Vapaus 0: Vapaus ajaa ohjelmaa mihin tahansa tarkoitukseen
  
- Vapaus 1: Vapaus tutkia ohjelman lähdekoodia ja muokata sitä tarpeen mukaan. Lähdekoodin saatavuus on edellytys.
  
- Vapaus 2. Vapaus levittää ohjelman kopioita edelleen muille
  
- Vapaus 3: Vapaus levittää omia muokattuja versioita ohjelmasta jotta muutkin hyötyisivät muutoksista.
  
- Vapaa ohjelmisto voi olla kaupallista: Vapaa ohjelmisto ei tarkoita ettei sillä voisi tehdä liiketoimintaa. On tärkeää että kaupallinen käyttö kehitys ja jakelu ovat sallittuja
  
- Copyleft ja lisenssit: Tietyt säännöt kuten copyleft mikä takaa että ohjelmisto tai sen muutetut versiot pysyvät vapaina. Se käyttää tekijänoikeutta suojatakseen käyttäjien oikeuden muokata jakaa ja käyttää ohjelmisto estäen sen muuttamisen suljetuksi.

### 1. Johdanto

Tämä raportti käsittelee Linux-käyttöjärjestelmän asentamista VirtualBox-virtuaalikoneeseen sekä joitakin Linuxin peruskäyttöön liittyviä toimenpiteitä. Raportti on laadittu osana Linux-palvelimet - ICI003AS2A-3010-opintojaksoa ja sen tavoitteena on antaa opiskelijalle perustaidot Linuxin käyttöönotosta ja käytöstä. Käytetty Linux-jakelu on Debian 12 (debian-12.6.0-amd64-netinst.iso) ja asennus suoritetaan VirtualBox-ympäristössä. (Karvinen 2024)

#### 1.1. Ympäristön kuvaus

- Host-käyttöjärjestelmä: Windows 10 pro
- Virtuaalikoneohjelmisto: VirtualBox 7.0
- Tietokoneeni laitteisto:
  - Prosessori: AMD Ryzen 5 700 6-core 3801 MHz 12 logiikka prosessoria
  - Emolevy: MSI MPG B650 EDGE WIFI emolevy AMD B650 pistoke AM5 ATX
  - Grafiikkakortti: Nvidia GeForce RTX 3060 Ti
  - RAM: Corsair Vengeance RGB DDR5 5200 MHz 32Gt
  - Ulkoinen muisti: Kingston Technology KC300 M.2 2048 Gt PCI Express 4.0 3D TLC NVMe
  - Virtalähde: Asus ROG loki 850w

## 2. Debianin lataaminen koneelle.

- Menin osoitteeseen https://www.debian.org/ ja etusivulta klikkasin ”download”-nappia minkä jälkeen selain latasi minulle debian-12.6.0-amd64-netinst tiedoston koneelle. (Debian 2024)
<br>
<img width="243" alt="image" src="https://github.com/user-attachments/assets/a1e5bdc1-b73c-4772-becd-c30bd15f7fa7">
<br>

### 3. Debianin asentaminen VirtualBoxiin

#### 3.1 VirtualBoxin asennus ja konfigurointi

##### Vaiheet:

  1. Virtualboxin lataaminen ja asentaminen
  - Menin verkko-osoiteeseen https://www.virtualbox.org/ ja painoin    vasemmasta laidasta ”downloads”-välilehden painiketta.

  <img width="200" alt="image" src="https://github.com/user-attachments/assets/85257800-8e17-4bcd-89d4-2cb1eb46798e">
  <br><br>

  - Tämän jälkeen valitsin seuraavalta sivulta ” VirtualBox 7.0.20 platform packages Windows hosts”.
  <img width="452" alt="image" src="https://github.com/user-attachments/assets/3d3e008e-6470-4572-9d4b-495e243d0373">
  <br><br>

  - Viimeisenä selain latasi koneelleni ohjelman ja latauksen jälkeen asensin VirtualBox ohjelman koneelleni noudattamalla asennusohjeita. (VirtualBox 2024)

  2. Uuden virtuaalikoneen luominen
  - Avasin VirtualBox ohjelman ja aloitin painamalla ”machine” välilehdeltä ”new” mikä aloittaa uuden virtuaalikoneen luomisen. Toinen vaihtoehto olisi oikeasta laidalta valita painike jossa lukee ”New”.
  <img width="396" alt="image" src="https://github.com/user-attachments/assets/1e62b19a-def3-40b5-b413-b16fb7bbf0c2">
  <br><br>

  - Asennusvalikossa valitsin Virtuaalikoneelleni nimen tyypin version sekä ISO-kuvan.
    - Annoin nimeksi ”Debian 12”
    - Valitsin tyypiksi ”Linux” sekä versioksi ”Debian (64-bit)”
    - Seuraavaksi valitsin ISO-kuvaksi lataamani ISO-tiedoston minkä latasin Debian sivulta.
    <br>
    <img width="338" alt="image" src="https://github.com/user-attachments/assets/478ce504-8465-4a2a-8917-504c0685e24d">
    <br><br>

  - Seuraavassa vaiheessa konfiguroin valitsemani henkilökohtaisen käyttäjänimen ja salasanan. Tässä on hyvä muistaa että käyttäjänimi on pienellä. Salasana pitää myös muistaa tai kirjoittaa tarvittaessa ylös jonnekin turvalliseen paikkaan.
  - Seuraavaksi valitsin virtuaalikoneeseeni ram muistin sekä prosessoreiden määrän.
    - Valitsisin ram muistiksi noin 10Gt.
    - Valitsin prosessoreiden lukumääräksi 4 kpl.
    <br>
    <img width="341" alt="image" src="https://github.com/user-attachments/assets/39a17469-c45d-46d1-8114-b63596119232">
    <br><br>

  - Seuraavassa vaiheessa valitsin virtuaalikoneeseeni noin 60Gt ulkoista virtuaalimuistia.

  <img width="328" alt="image" src="https://github.com/user-attachments/assets/25e04ae6-3b0f-40f2-8165-f1db8cdb371d">
  <br><br>

  - Viimeisessä ikkunassa oli yhteenveto suoritettavasta asennusprosessista minkä jälkeen painoin ”finish” painiketta. Tämän jälkeen virtuaalikone avasi uuden ikkunan ja asensi Debian käyttöjärjestelmän VirtualBoxiin.

  <img width="381" alt="image" src="https://github.com/user-attachments/assets/ea645b62-d5b3-4c25-826e-a726fb9593a6">
  <br><br>

  - Kun asennus valmistui oli VirtualBoxin näkymä Debianin kirjautumissivulla:

  <img width="321" alt="image" src="https://github.com/user-attachments/assets/560e1071-0e24-4f8c-942d-fa6d935a825f">
  <br><br>

  3. Debianin konfigurointi 

  - Kun kirjauduin käyttöjärjestelmään seuraavana vuorossa oli yleisten asetusten valitseminen.
  - Valitsin kieleksi ”English (United States)”.
  - Seuraavaksi valitsin näppäimistöksi ”Finnish (Windows)”.
  - Tämän jälkeen estin paikalliset palvelut ja viimeisenä hyppäsin yli ”connect your online accounts” osion.
  - Ja viimeisenä valitsin vihreän aloita Debianin käyttö painikkeen mistä siirryin suoraan Debianin työpöydälle.

  <img width="322" alt="image" src="https://github.com/user-attachments/assets/61611417-91bd-440e-8a4b-5c68f0bfb8ef">
  <br><br>

### 4. Suosikkiohjelmani Linuxilla

Tässä osiossa valitsin kokeiltavakseni Debianissa olevan Text Editor-ohjelman. Debianissa ei ole montaa ohjelmaa asennettuna valmiiksi mutta Text Editor on hyvä kirjoitusohjelma joten valitsin sen.
- Painoin vasemmasta yläreunasta ”Activities” painiketta

<img width="340" alt="image" src="https://github.com/user-attachments/assets/cb5f9aa0-aeaf-4460-aa34-05f54c1dfb4d">
<br><br>

- Seuraavaksi kirjoitin hakukenttään ”text” ja valitsin Text Editor -ohjelman

<img width="408" alt="image" src="https://github.com/user-attachments/assets/5d7168e6-6b98-4b78-9c78-387295912360">
<br><br>

- Text Editorissa kirjoitin yksinkertaisen python komennon<br>

`print(”Hello World”);`

<br>
<img width="452" alt="image" src="https://github.com/user-attachments/assets/6a50709c-1c04-48c2-90f3-b08f18ba4b62">
<br><br>

- Seuraavaksi tallensi tiedoston työpöydälle nimellä "print_hello.py"
<br>

<img width="452" alt="image" src="https://github.com/user-attachments/assets/353f7518-1723-4256-b3d2-98ff3aaa68b2">
<br>
<img width="452" alt="image" src="https://github.com/user-attachments/assets/aed5be8c-29a9-43b0-aa6a-5bdf81944154">
<br><br>

- Tämän jälkeen valitsin ohjelmista terminaalin ja avasin sen.
<br>
<img width="285" alt="image" src="https://github.com/user-attachments/assets/09f2091a-d012-4f8c-bf27-ad29fb22f484">
<br><br>

- Seuraavaksi menin terminaalin hakemistossa työpöydälle ja tarkistan että tiedosto löytyy sieltä.
<br>
<img width="452" alt="image" src="https://github.com/user-attachments/assets/1f8da8ae-8481-4f7b-8192-97c088d26df8">
<br><br>

- Tiedostoilla ei ollut automaattisesti suoritusoikeutta joten annoin tiedostolle suoritusoikeuden seuraavalla komennolla<br>
`chmod +x print_hello.py`.
<br>

<img width="406" alt="image" src="https://github.com/user-attachments/assets/5f0a01e8-b398-4447-9ef7-8cc4c038154b">
<br><br>

- Viimeisenä ajan tiedoston kirjoittamalla komennon<br>
  `python3 print_hello.py`
  <br>

<img width="356" alt="image" src="https://github.com/user-attachments/assets/c4963c39-d450-4cce-9c3a-ab77e55dc859">
<br><br>

Text Editor toimii erittäin hyvin skriptien kirjoittamiseen.

### 5. Yhteenveto ja havaitut ongelmat.

VirtualBoxin ja Debianin asennus onnistui sujuvasti seuraamalla asennusohjeita sekä hyödyntämällä aiempaa osaamista. Asennusprosessissa ei ilmennyt ongelmia eikä virheilmoituksia tullut esiin.

### Lähteet

- Karvinen Tero 2024: Linux palvelimet https://terokarvinen.com/linux-palvelimet/ Luettu: 23.8.2024
- Debian – The Universal Operation System. https://www.debian.org/ Luettu: 23.8.2024
- Oracle VM VirtualBox. https://www.virtualbox.org/ Luettu: 23.8.2024
