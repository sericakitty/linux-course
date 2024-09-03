# h2 Komentaja Pinviini

### Command line basics revisited
-  **Komentorivi** on tehokas, nopea ja helposti automatisoitava työkalu, jota käytetään laajalti Linux- ja BSD-järjestelmissä.
-  **Peruskomennot** kuten pwd, ls, cd, mkdir, mv, cp, ja rm ovat olennaisia hakemistojen ja tiedostojen hallinnassa.
-  **SSH** mahdollistaa etäyhteyden avaamisen toiseen tietokoneeseen ja tiedostojen siirron turvallisesti.
-  **Man**-komento avaa komennon manuaalisivut, jotka sisältävät yksityiskohtaiset ohjeet sen käytöstä. Lyhyet apuohjeet (--help) tarjoavat nopean tavan saada perustiedot komennosta.
-  **Komentohistorian** käyttö (esim. nuolinäppäimet, history) nopeuttaa työskentelyä ja vähentää virheitä.
-  Tärkeät hakemistot Linuxissa: /, /home/, /etc/, /media/, /var/log/.
-  **Paketinhallinta** (esim. apt-get) on turvallinen tapa asentaa ja poistaa ohjelmistoja Linux-järjestelmissä.

Oma kysymys/huomio:
Miten komentorivin käyttöä voisi tehostaa lisäämällä skriptien tai alias-komentojen käyttöä, jotta toistuvat tehtävät automatisoituvat entisestään?

### Komentoriviohjelmat ja Linux-järjestelmän perusteet


31.8.2024 18:09
<br>
Käynnistin Debian ympäristön virtuaaliboxissa.

![image](https://github.com/user-attachments/assets/309c340e-2495-4c5c-8c04-cf3b3efac296)


31.8.2024 18:11
<br>
Kirjauduin sisään järjestelmään.

![image](https://github.com/user-attachments/assets/54547246-1488-4b06-801b-1c565ec87f24)

 
31.8.2024 18:15
<br>
Ensin oli hyvä päivittää järjestelmä ajan tasalle, joten menin terminaaliin ja päivitin järjestelmän.
 
![image](https://github.com/user-attachments/assets/9542d797-1df7-47ca-a1fd-655472a0c0b5)

![image](https://github.com/user-attachments/assets/2eaecf3f-1ba9-4fd0-8eb2-2fe5eb8b8029)

 
31.8.2024 18:17
<br>
Päivityksen jälkeen tarkistin onko muiden päivityksien tarvetta kirjottamalla "sudo apt-get upgrade".

![image](https://github.com/user-attachments/assets/53b48d6f-81b2-4aea-b8aa-c4083ed6cc17)

 
Terminaali kysyi haluanko asentaa päivitykset, ja valitsen kyllä.
 
![image](https://github.com/user-attachments/assets/22534922-f3cd-41a4-80b2-ce26e91cfe75)


31.8.2024 18:21
<br>
järjestelmä oli asentanut päivitykset ja olivat ajan tasalla.

#### a) Micro: Tekstieditorin asentaminen

31.8.2024 18:24
<br>
Seuraavaksi asensin micro tekti editorin syöttämällä komennon "sudo apt-get install micro".

![image](https://github.com/user-attachments/assets/34b00d4b-6168-40dd-b570-2a74a9a8f5b2)


31.8.2024 18:25
<br>
Järjestelmä asensi micro editorin onnistuneesti ja pystyn näkemään sen hakuvalikossa ja avaamaan sen.

![image](https://github.com/user-attachments/assets/9e7c59dd-3ff6-4cac-a50b-0ccaf3332eb9)


![image](https://github.com/user-attachments/assets/c4bd9b76-d4f3-40e5-913b-5d1efb550200)



#### b) Apt: Kolmen uuden komentoriviohjelman asentaminen

31.8.2024 18:53
<br>
Aloitin asentamalla ensimmäisen ohjelman. Valitsin itselleni **htop**-komentoriviohjelman.

![image](https://github.com/user-attachments/assets/61533c9c-97aa-4bde-8b75-53f4a47dbdf3)


31.8.2024 18:54
<br>
Ohjelma asentui onnistuneesti.

31.8.2024 18:55
<br>
Avasin ohjelman kirjoittamalla komentoriville komennon "htop".

![image](https://github.com/user-attachments/assets/a10d8c33-b1a1-466c-b020-9824a117a5a0)


31.8.2024 18:56
<br>
Komentoriville ilmestyi värikäs ja selkeä ohjelma joka kertoi prosessit.

![image](https://github.com/user-attachments/assets/c358f46f-4ce1-4418-94d2-89632a454b52)


31.8.2024 18:56
<br>
Suljin ohjelman oikeassa alanurkassa olevan ohjeen mukaan painamalla F10 painiketta.

31.8.2024 19:00
<br>
Seuraavaksi ohjelmaksi valitsin ohjelman tree. Asensin tämän kirjoittamalla komennon "sudo apt-get install tree".

![image](https://github.com/user-attachments/assets/21cc619e-ec44-4e3d-a59c-54a91b7f26c6)


31.8.2024 19:01
<br>
Komentorivi oli asentanut ohjelman onnistuneesti.

31.8.2024 19:02
<br>
Avansin ohjelman komentorivillä kirjoittamalla komennon ko.hakemistossa käyttämällä komentoa "tree".

![image](https://github.com/user-attachments/assets/503c5e0d-968e-4128-ac08-cb56d02560ae)


Tämä antoi mukavamman visuaalisen kuvan kansiorakenteesta.

31.8.2024 19:05
<br>
Viimeiseksi ohjelma valitisin fzf (fuzzy finder) ohjelman mikä hakee tehokkaasti kansiosta alaspäin kaikki tiedosto ja kansiot ja pystyy hakemaan tiettyä tiedostoa tai kansiota.
Kirjoitin komentoriville komennon "sudo apt-get install fzf".

![image](https://github.com/user-attachments/assets/f9adebd6-1a11-4f85-8ce9-7d18d2a6de23)


31.8.2024 19:06
<br>
Komentorivi oli asentanut ohjelman onnistuneesti.

31.8.2024 19:08
<br>
Olin luonut itselleni testikansion ja testitiedoston Documents kansioon.
Jos haluan löytää jonkin tiedoston helposti ja tietää missä se sijaitsee, pystyin menemään esim “home/{username}/” kansioon ja siellä suorittamaan komennon "fzf".

![image](https://github.com/user-attachments/assets/ef1b2ec6-626f-4cf3-a8b9-3a9eb78463aa)


Tästä hakemistosta pystyin helposti näkemään että missä kyseinen tiedosto sijaitsee.

Nämä kaikki kolme komentoriviohjaa pystyi myös asentaan kerralla kirjottamalla komentorille komennon "sudo apt-get install htop tree fzf".
Tämä komento asentaa kaikki kolme ohjelmaa synkronisesti järjestyksessä.


#### c) FHS: Tärkeiden hakemistojen esittely ja sisältö

31.8.2024 19:16
<br>
Ensimmäisenä hakemistona on root (“/”) kansio eli juurikansio. Juurikansio on ylin kansio mikä sisältää kaikki koneen tiedostosto. Linux järjestelmässä ei ole kirjainta vaan hakemisto alkaa “/”.
Avasin terminaalin ja tarkistan missä olen kirjoittamalla komennon "pwd".

![image](https://github.com/user-attachments/assets/bf90c159-d35e-4ef8-8c7a-3054ed8cc755)


31.8.2024 19:18
<br>
Tiesin että minun pitää päätyä komentorivillä polkuun “/”, joten lähdin etenemään ylöspäin hakemistossa kirjoittamalla seuraavan komennon “cd ../..” tämä hyppää kaksi kansiota ylöspäin.

31.8.2024 19:20
<br>
Tarkistin missä olen kirjoittamalla komennon "pwd".

![image](https://github.com/user-attachments/assets/a1d99a42-8a12-4391-bcb1-ec1b96b91321)


31.8.2024 19:21
<br>
Jos halusin nähdä mitä tämä juurikansio sisältää, kirjoitin komentoriville komennon “ls”.

![image](https://github.com/user-attachments/assets/5d5b9b59-8d47-44d0-8166-df65a9c80544)



31.8.2024 19:22
<br>
Näin että juurikansio sisältää kaikki tärkeät kansiot mitkä ovat väriltään tumman sinisiä ja muutaman tiedoston, mitkä ovat väriltään turkooseja.

31.8.2024 19:23
<br>
 “/home” kansio sisältää kaikki käyttäjät.
pääsin kansioon kirjoittamalla samassa juurikansiossa komennon “cd home”.

![image](https://github.com/user-attachments/assets/3cd9296d-f626-423d-b539-95219895a1cc)


31.8.2024 19:25
<br>
En tarvinnut tällä kertaa tarkistaa pwd komennolla missä olemme koska näin suoraan komentorivillä polun mikä oli muotoa “/home”.

31.8.2024 19:26
<br>
Seuraavaksi kirjoitin komennon “ls” millä näin kansion sisällön.

![image](https://github.com/user-attachments/assets/c2d90734-98ea-400b-9f89-4cd41125ba26)


Näin että home kansio sisältää käyttäjänimellä varustetun kansion, mikä taas sisältää käyttäjälle määritettyjä kansiota tai ohjelmia tai tiedostoja.

31.8.2024 19:28
<br>
Siirryin yhden polun alemmas kirjoittamalla komennon “cd {username}”.

![image](https://github.com/user-attachments/assets/70c5f27b-9e51-4767-a3b9-1e7b530929e7)


31.8.2024 19:29
<br>
Kirjoitin komennon “ls”, millä  näin mitä käyttäjälle suunnattu kansio sisältää.

![image](https://github.com/user-attachments/assets/4d02e739-077d-4727-8e41-2e21304eaeb8)


Olin tehnyt itselleni testikansion mikä näkyy selvästi omassa käyttäjäkansiossani.

31.8.2024 19:31
<br>
Kansio /etc/ sisältää laajasti kaikki järjestelmän asetukset ja ne ovat kirjoitettu tekstimuotoisesti, ihmisen luettavaksi.

Aloitin komentorillä kirjoittamalla “pwd” ja tarkistin missä polussa olen.

![image](https://github.com/user-attachments/assets/08c9072f-be0f-40ec-821a-1f9e573aa3a5)


31.8.2024 19:33
<br>
/etc kansio sijaitsee juurikansiossa, joten minun pitää siirtyä kaksi kansiota ylöspäin jotta pääsen juurikansioon.
Kirjoitin komentoriville komennon “cd ../..” mikä siirtää minut juurikansioon.

![image](https://github.com/user-attachments/assets/02cc1146-bcbf-4cf5-a2e2-4a8a7572903c)


31.8.2024 19:34
<br>
Seuraavaksi kirjoitin komennon “ls” ja tarkistin mitä juurikansio sisältää.

![image](https://github.com/user-attachments/assets/91525985-a108-48bc-a3e5-d3ea74c14f38)


31.8.2024 19:35
<br>
Siirryin /etc kansioon kirjoittamalla komennon “cd etc”.

![image](https://github.com/user-attachments/assets/01ac5562-40b2-4d13-bf4a-b2800b18aa89)


31.8.2024 19:36
<br>
Pääsin näkemään kansion sisältämät tiedostot kirjoittamalla komennon “ls”.

![image](https://github.com/user-attachments/assets/a639bf9d-6b28-4605-bd69-96f3709ae181)


En pystynyt kuvakaappaamaan kaikkea yhteen kuvaan, koska kansio sisältää paljon tiedostoja ja asetuksia.

31.8.2024 19:37
<br>
Kansiotiedosto /media sisältää ulkopuoliset medialukulaitteet esim cdrom tai usbdisk.
Tarkistin komennolla pwd missä olen.

![image](https://github.com/user-attachments/assets/395bf008-8f1e-430f-b0c6-eecaa2d3893a)


31.8.2024 19:39
<br>
Tiesin että /media kansio sijaitsee juurikansiossa joten minun piti siirtyä vain yhden kansion ylöspäin kirjoittamalla komento “cd ..”

![image](https://github.com/user-attachments/assets/8d38679c-6bfe-4dd9-84ce-8670dd4db669)


31.8.2024 19:40
<br>
Kirjoitin komennon “ls”, että näin mitä kansio sisältää.

![image](https://github.com/user-attachments/assets/f8a59fcc-0687-47c9-a3f0-03a98d9c0595)


31.8.2024 19:41
<br>
Siirryn media kansioon kirjoitin komennon “cd media” ja sen jälkeen pystyin kirjoittamaan komennon “ls” millä näin kansion sisällön.

![image](https://github.com/user-attachments/assets/b515e4de-1f28-4a29-b010-ca61c4ad1ad4)


31.8.2024 19:42
<br>
Kansiotiedosto /var/log/ sisältää laajasti järjestelmän lokitiedot ja virhetiedot, esimerkiksi syslog ja auth.log ja erro.log.

Pystyn tarkistamaan missä olen kirjoitin komennon “pwd” komentoriville.

![image](https://github.com/user-attachments/assets/6b495366-b50a-4c60-b518-1391e68b4fe3)


31.8.2024 19:44
<br>
Minun piti päästä juurikansioon ja kirjoittamalla komentoriville “cd ..” pääsin siirtymään yhden kansion ylöspäin juurikansioon ja pystyin sen jälkeen kirjoittaa komennon “ls” millä näin kansion sisällön.

![image](https://github.com/user-attachments/assets/85246f07-2b82-4486-b5f3-c0115b101d12)


31.8.2024 19:46
<br>
Lokitiedot sijaitsevat var kansiossa ja pääsin siirtymään sinne kirjoittamalla komennon “cd var”.

![image](https://github.com/user-attachments/assets/ce7e1809-ac05-4326-bbd5-92acf28a5a44)


31.8.2024 19:47
<br>
Näin komentoriviltä että lokitiedot sijaisivat “log” kansiossa ja pääsin siirtymään sinne komennolla “cd log”.

![image](https://github.com/user-attachments/assets/d8472f2a-5cf0-4a51-8fae-cdeaa8e77298)

31.8.2024 19:48
<br>
Seuraavaksi näin kansion sisällön kirjoittamalla komennon “ls”.

![image](https://github.com/user-attachments/assets/d765679c-c91c-46b1-a741-48a5295e3892)


Näin että kansio sisälti käynnistykseen, virheisiin, järjestemään ja moneen muuhun sisältäviä lokitietostoja.


#### d) The Friendly M: grep-komennon käyttö

31.8.2024 20:00
<br>
En ollut käyttänyt montaa kertaan grep komentoa, mutta kirjoittamalla komentoriville komennon "man grep" sain avatuksi manuaalisivut.

![image](https://github.com/user-attachments/assets/66391b49-9cd8-48fd-b557-2b6aed2298bd)


Kuvaus kertoi että Grep-komento etsii määritettyjä kuvioita (PATTERNS) tiedostoista. Se tulostaa jokaisen rivin, joka vastaa annettua kuviota. Kuvio on yleensä syytä laittaa lainausmerkkeihin, kun grep-komentoa käytetään komentorivillä.
Manuaalisivut eivät avanneet hirveästi minulle miten grep komentoa käytetään joten turvaudun internetistä saataviin ohjeisiin.

31.8.2024 20:05
<br>
Löysin hyvän ohjeartikkelin https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix missä on hyvin esimerkkejä, miten grep komentoa käytetään.

31.8.2024 20:08
<br>
Minulla oli testi tiedosto käyttäjäkansiossa ja kokeilen käyttää grep komentoa siihen.
Tarkistin komentorivillä komennolla ”pwd” missä olin.

![image](https://github.com/user-attachments/assets/bec9b502-1528-40c2-b23d-9e82e1eb4f7a)


31.8.2024 20:09
<br>
Komennolla ”ls” näin kansion sisällön.

![image](https://github.com/user-attachments/assets/7258af40-5401-4001-a626-c8d8eca93eab)


31.8.2024 20:10
<br>
Tiesin että testitiedostoni sijaitsee kansiossa toinentestikansio joten siirryn sinne komennolla ”cd toinentestikansio/”. 
Seuraavaksi kirjoitin komennon ”ls” millä näin kansion sisällön”.

![image](https://github.com/user-attachments/assets/8291cac1-f0f7-42ca-bbd5-e18900099fde)


31.8.2024 20:11
<br>
Kirjoitin komentoriville komennon ”grep -i ”hello world” {tiedostonnimi}” digitalOcenin ohjeiden perusteella, komentoriville printautuu ko.tekstin osa tiedostosta. Parametri -i tarjoittaa että grep hyväksyy minkä sanan koon tahansa.

![image](https://github.com/user-attachments/assets/e2c51231-eee9-484c-8c74-4893e1dc4442)


31.8.2024 20:15
<br>
Pystyin myös grep komennolla muuttaa toisen sanan väriä. Kirjoitin seuraavan komennon ohjeiden perusteella. Parametri -i casesensitive ja --color muuttaa löydetyn sanan värin.

![image](https://github.com/user-attachments/assets/656491df-d5ee-446d-bd5e-afe7b85e29c5)

Tämä väritti ensimmäisen sanan värikkääksi.




#### e) Pipe: putkien käyttö

Jokaisen komennon perään voidaan lisätä merkki “|” eli putki, mikä kertoo komentoriville, että komennon tulostus ohjataan seuraavalle komennolle käsiteltäväksi.

31.8.2024 20:23
<br>
Avasin terminaalin ja tarkistan missä olin.

![image](https://github.com/user-attachments/assets/90190753-aa95-4c68-9a16-61fa8a7e91d2)


31.8.2024 20:25
<br>
Kirjoitin komennon ”ls | less” komentoriville ja se tulosti kansion sisällön käyttämälle less ohjelmaa.

![image](https://github.com/user-attachments/assets/c0840275-4031-4271-b05c-9b3ff96ccb18)






#### f) Rauta: järjestelmän rautatietojen listaus ja analyysi

31.8.2024 20:28
<br>
Näin testaamani koneen raudan komennolla “sudo lshw -short -sanitize”.

![image](https://github.com/user-attachments/assets/3374766c-dc92-4f6d-9231-24c4a982d02e)


Kone pyysi salasanaa ja kirjoitan sen.

31.8.2024 20:30
<br>
Komentorivi ilmoitti ettei minulla ole lshw ohjelmaa.

![image](https://github.com/user-attachments/assets/f47a4279-8bfa-4c76-8ff5-7dc11fc7f66c)


31.8.2024 20:31
<br>
Asensin lshw komennolla “sudo apt-get install lshw”.

31.8.2024 20:32
<br>
Ohjelma asentui onnistuneesti.

31.8.2024 20:33
<br>
Kirjoitin komennon “sudo lshw -short -sanitize” uudestaan komentoriville.

31.8.2024 20:34
<br>
Komentorivi tulosti seuraavat tiedot.

![image](https://github.com/user-attachments/assets/d5684e19-7469-4e63-9e88-04ad1ca76f28)

![image](https://github.com/user-attachments/assets/7255d41a-ef1f-4597-8164-7a7640224ae1)


Lista analysoituna:

Systeemin tiedot:
-	Tietokoneen jäjestelmä on VirtualBox. Tämä tarkoittaa että käyttäjärjestelmä ei toimi fyysisessä koneessa vaan virtuaalikoneessa.
-	Listuksen alussa näkyy Biossin koko, mikä on 128KiB.

Muisti:
-	Järjestelmässä on 10Gt RAM-muistia mikä on jaettu virtuaalikoneelle. Virtuaalikoneelle on asetettu paljon RAM muistia koska sitä on on paljon Host koneella antaa (32Gt), ja jälkikäteen RAM muistin muuttaminen olisi työlästä.
Suuren RAM määrän ansiosta virtuaalikone pystyy suorittamaan raskaitakin ohjelmia.


Prosessori
-	Käytössä on AMD Ryzen 5 7600-prosessori, jossa on 6 ydintä. Tämä on virtuaalikoneelle määritelty prosessori. Tehokas prosessori mahdollistaa virtuaalikoneelle sujuvan moniajon ja suorituskykyisten sovellusten ajamisen.

Kovalevy muisti:
-	/dev/sda on virtuaalinen kiintolevy, ja sen koko on 74Gt. Se on jaettu komeen osioon
o	/dev/sda1 on 68Gt kokoinen EXT4-tiedostojärjestelmä osio mikä sisältää kaikki pääasialliset käyttöjärjestelmän tiedostot.
o	/dev/sda2 on 975Mit laajennettu osio.
o	/dev/sda5 on 975Mt Linux swap osio joka toimii virtuaalimuistina.
Virtuaalikoneelle on hyvä määrittää kunnolla tallennustilaa heti virtuaalikoneen ensimäärittelyssä koska sen muuttaminen jälkikäteen tuottaa enemmän työtä kuin uuden virtuaalikoneen luominen.

Input devices:
-	Erilaiset syöttölaitteet on listattu, kuten näppäimistö (AT Translated Set 2 keyboard), hiiri (ImExPS/2 Generic Explorer Mouse), ja muut syöttölaitteet kuten virtapainike ja unipainike.

Network
  -	**enp0s3**: Verkkosovitin, joka käyttää 82540EM Gigabit Ethernet Controller -laitetta, liitettynä virtuaalikoneeseen

Multimedia.
  -	**card0**: Virtuaalinen ääniohjain (82801AA AC'97 Audio Controller), joka vastaa virtuaalikoneen ääniresursseista.

Listauksen yhteenvedosta voidaan päätellä, että virtuaalikone on hyvin varustettu, ja se näyttää olevan suunniteltu suhteellisen raskaaseen käyttöön, ottaen huomioon sille varattu muisti ja prosessiteho. Tallennustila riittää peruskäyttöön, mutta koska Host koneen omistajana tiedän, että tallennustilaa on jopa 2Tb niin virtuaalikoneelle pystyisi antamaan tarvittaessa enemmänkin.



31.8.2024 21:00
<br>
Virtuaalikoneen sammutus


## Lähteet:
https://terokarvinen.com/linux-palvelimet/

https://terokarvinen.com/2020/command-line-basics-revisited/?fromSearch=command%20line%20basics%20revisited

https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix



 
