##Problem - Mashup
I denna laboration det meningen att du ska skriva en Mashup-applikation som kombinerar två stycken olika tjänster. Tjänsterna du ska jobba med är dels ett API från sveriges radio samt någon form av karttjänst open streetmap eller google maås.

* [Sveriges radios öppna API](http://sverigesradio.se/api/documentation/v2/index.html)
* [Open streetmap](https://www.openstreetmap.org/)
* [Google Map](https://developers.google.com/maps/documentation/javascript/tutorial). 

Tanken är att du ska bygga en javascript-applikation som ska visa den trafikinformation som Sveriges Radio ger dig och presentera dessa via en webbapplikation som bland annat plottrar ut de positioner som hör till varje trafikmeddelande.

### API:ernas dokumentation
Som en del i uppgiften ingår det att läsa dokumentation av de API som nämns ovan och därifrån förstå hur man implementerar dessa en snyggt utformad webbapplikation. I dokumentationen hittar du hur du anropar API:et, hur du får den data du vill i det format du vill. Hur du implementerar karttjänsterna bör du också kunna hitta information om. Kanske [http://leafletjs.com/](http://leafletjs.com/) kan vara ett tips.


##Krav
* Mashupapplikationen ska visa aktuell trafikinformation och hämta denna information från SR:s API. Dessa ska dels **presenteras på lämpligt sätt på sidan i en lista samt även på en karta med en "marker"** som representerar platsen för den aktuella händelsen. 
* När man klickar på en marker ska mer information om den aktuella händelsen komma upp (titel, datum, beskrivning och kategori - Se API-dokumentationen för mer information) via någon form av popup-fönster. 
* Man ska inte kunna klicka upp flera noteringsrutor så att man döljer information.
* Användaren ska kunna filtrera trafikhändelserna genom att på något sätt ge användaren möjlighet bara visa en specifik kategori: Vägtrafik, Kollektivtrafik, Planerad störning, Övrigt eller Alla kategorier. Se API-dokumentationen för mer information.
* Applikationen ska alltså inte bara vara en karta utan även ha en lista med alla aktuella händelser (alltid sorterad efter tidpunkt - senast högst upp). När användaren klickar på en händelse ska man på något sätt se detta i kartan (markören hoppar eller liknande)
* Naturligtvis ska applikationen se bra ut och vara enkel att använda. Använd gärna ett front-end ramverk för att förenkla detta t.ex. [bootstrap](http://getbootstrap.com/) eller [Foundation](http://foundation.zurb.com/).
* Din applikation ska inte fråga efter data mot API:et i onödan. Implementera en cachningsstrategi som du kan diskutera och försvara vid examinationen. 
* Du ska använda JSON som returformat
* Det är inte tillåtet att använda JSONP

## Reflektionsfrågor
* Vad finns det för krav du måste anpassa dig efter i de olika API:erna?
* Hur och hur länga cachar du ditt data för att slippa anropa API:erna i onödan?
* Vad finns det för risker kring säkerhet och stabilitet i din applikation? 
* Hur har du tänkt kring säkerheten i din applikation?
* Hur har du tänkt kring optimeringen i din applikation?


## Extrauppgift
Trafikinformationen har olika prioritet. Visa detta genom att ge olika utseende på kartans olika markers för de olika prioriteringarna som finns (Mycket allvarlig händelse, Stor händelse, Störning, Information, Mindre störning)


## Redovisning
Redovisning av denna uppgift sker muntligen på de schemalagda redovisningstiderna. Man kommer dock få boka en egen redovisningstid.

