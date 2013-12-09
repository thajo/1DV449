##Problem - Mashup
I denna laboration det meningen att du ska skriva en Mashup-applikation som kombinerar två stycken olika tjänster. Tjänsterna du ska jobba med är:

* [Sveriges radios öppna API](http://sverigesradio.se/api/documentation/v2/index.html) 
* [Google Map](https://developers.google.com/maps/documentation/javascript/tutorial). 

Tanken är att du ska bygga en applikation som ska visa trafikinformation som Sveriges Radio ger dig och presentera dessa via en karta från Google.

### API:ernas dokumentation
Som en del i uppgiften ingår det att läsa dokumentation av de API:er som nämns ovan och därifrån förstå hur man implementerar dessa en snyggt utformad webbapplikation. I dokumentationen hittar du hur du anropar API:et, hur du får den data du vill i det format du vill. Googles kart-API är ett javascript-API och det finns gott om guider på deras sida för att se hur man använder detta.


##Krav
Mashupapplikationen ska hämta de senaste 100 posterna (finns det färre ta alla) av trafikinfo från SR:s API. Dessa ska presenteras på lämpligt sätt på sidan samt även på en karta på sidan med en "marker" som representerar platsen för den aktuella händelsen. När man klickar på en marker ska mer information om den aktuella händelsen komma upp (titel, datum, beskrivning och kategori - Se API-dokumentationen för mer information) via ett infowindow (se google maps dokumentation).

Användaren ska kunna filtrera trafikhändelserna genom att på något sätt ge användaren möjlighet bara visa en specifik kategori: Vägtrafik, Kollektivtrafik, Planerad störning, Övrigt eller Alla kategorier. Se API-dokumentationen för mer information.

Naturligtvis ska applikationen se bra ut. Använd gärna ett front-end ramverk för att förenkla detta t.ex. [bootstrap](http://getbootstrap.com/).

##Extrauppgift
Trafikinformationen har olika prioritet. Visa detta genom att ge olika utseende på kartans olika markers för de olika prioriteringarna som finns (Mycket allvarlig händelse, Stor händelse, Störning, Information, Mindre störning)

##Redovisning
Redovisning av denna uppgift sker muntligen på de schemalagda redovisningstider som finns i ert schema v.51

