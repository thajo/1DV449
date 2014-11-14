##Problem - Messy Labbage
Denna laboration består av tre delar. Du kommer få en webbapplikation som kanske inte riktigt är uppbyggd på det sätt du skulle vilja. Det är ganska vanligt att man kommer få "mindre bra" kod i sitt knä som man sedan tvingas jobba vidare med. Tanken med denna uppgift är att du med din kunskap ska analysera och förbättra denna applikation både ur ett prestanda- och ett säkerhetsperspektiv. Applikationen är ganska liten så vi kanske inte kommer se jättestora förändringar i prestandan men vi får i alla fall ett tillfälle att studera de teorier och tips som finns.

* I första delen ska du identifiera och rätta till eventuella säkerhetsrisker med applikationen.
* I andra delen av laborationen ska du försöka identifiera prestandaproblem i applikationen och försöka rätta till dessa.
* I tredje delen ska du implementera lösning för meddelande-hantering i applikationen med en Comet-lösning (long-polling). Som extrauppgift kan man också göra en lösning med WebSockets.

Du har ganska stora friheter att ändra i applikationen så länge funktion och utseende inte ändras. 

##Redovisning
Redovisning av denna laboration sker muntligen, i form av en laborationsrapport samt i form av publicering av kod på GitHub. 

Laborationsrapporten **ska** vara i md-format och finnas publicerad tillsammans med koden i ditt repositorie. Där ska också en URL till en körbar version av din omarbetade applikation tydligt framgå så vi kan testköra den.

##Om applikationen
Applikationen tankar du ner från följande adress: 
<http://orion.lnu.se/pub/education/course/1DV449/ht14/zips/1DV449_L02.zip>

Applikationen är skriven i PHP och kräver stöd för SQLite3 och PDO.

Applikationen ska ha samma funktion när du är färdig med den men förhoppningsvis vara bättre, säkrare och snabbare. Fokus på denna laboration ligger som sagt på optimering och säkerhet men kliar det i fingrarna får du helt eller delvis vill strukturera/skriva om applikationen men i laborationsrapporten måste det **tydligt** framgå vilka prestanda- och säkerhetsförbättringar som du gjort.

Applikationen har en inloggningssida på sin startsida index.php. Just nu finns två användarkonton; *admin:admin och user:user*.
Efter inloggning kommer man till en enkel applikation där man kan skriva meddelanden som dyker upp i en lista. Ni känner nog igen applikationen :) 

Applikationen använder några javascriptbiblotek samt css-ramverk. Dessa ska finnas kvar men det kan vara på sin plats att strukturera eller omarbeta dessa dessa ur optimeringssynpunkt. 

## Del 1 - Säkerhetsproblem
Applikationen är inte speciellt säker och det finns gott om säkerhetshål att täppa till. Din uppgift blir såklart att identifiera och i koden fixa till dessa säkerhetshål. Vi kan dock i denna laboration bortse från HTTPS som man såklart bör implementera på servern i en skarp applikation.

Du redogör för dina åtgärder i din laborationsrapport.
Dela upp varje säkerhetsrisk du hittar i följande punkter:

* Redogör för det säkerhetshål du hittat.
* Redogör för hur säkerhetshålet kan utnyttjas.
* Vad för skada kan säkerhetsbristen göra?
* Hur du har åtgärdat säkerhetshålet i applikationskoden?

Säkerheten tas upp under vecka 3 i självstudier och peer-instructions

## Del 2 - Optimering
Applikationen bör kunna optimeras både front- och backend (vi bortser från val av databashanterare som såklart också påverkar prestandan). Din uppgift blir att analysera applikationen och identifiera eventuella delar som går att optimera bättre. Du beskriver vilka delar du förändrar i din laborationsrapport och berättar också varför. Använd något verktyg som kan mäta laddning av sidan, förslagsvis någon webbläsares "web inspector".
Dela upp **varje olika del** i följande punkter:

* Namn på åtgärd Du gjort för att försöka förbättra prestandan
* Teori kring åtgärden (förklara varför du implementerar den och vad säger teorin om vad denna åtgärd gör). Referens till vart du hittat denna teori ska anges!
* Observation (laddningstid, storlekar av resurser, anrop m.m.) **innan** åtgård (utan webläsar-cache - gärna ett medeltal av ett antal testningar)
* Observation (laddningstid, storlekar av resurser, anrop m.m.) **efter** åtgärd (utan webläsar-cache - gärna ett medeltal av ett antal testningar)
* Reflektion kring att testresultatet blev som det blev.

Säkerheten tas upp under vecka 4 i självstudier och peer-instructions

####Tänk på följande angående mätningen
HTTP-caching och gzip kan vara svårt att implementera på servrar man inte har full kontroll över (kan styras via php.ini / .htaccess i apache:s fall). I de flesta fall är redan webbservern förinställd. Därför kan dessa bortses ifrån i denna laboration men vill man får man gärna hantera dessa också.

Även om din åtgärd **inte** förbättrar resultatet kan den vara intressant att ta med i laborationsrapporten om åtgärden enligt teorin borde förbättrat prestandan men av någon nämnd anledning inte gör detta.

Tänk på att om du kör applikationen lokalt går det väldigt fort och kan vara svårt att upptäcka verkliga förändringar. Testa gärna dina förändringar på en extern server t.ex. ditt webbhotell eller varför inte någon molnbaserad tjänst.

Mindre kodoptimeringar så som att ++variable eventuellt anses snabbare än variable++ räknas inte i denna laboration utan vi letar efter saker som vi tar upp i kursen så som t.ex. antalet requests m.m.

Den rekommenderade kurslitteraturen går igenom många tips för frontends-optimering.


## Del 3 - Long-polling
Att HTTP-protokellet i sitt orginalutförande har lite begränsningar vet vi om. Kommunikationen mellan webbläsare och webbserverar är oftast byggda för att följa en request/response-modell. I och med en webb där vissa tjänster ställer högre krav på realtidsdata finner man ibland denna metod otillräcklig. Man efterfrågan en mer push-baserad metod där servern skickar ut data till kienten när ny data finns.

Applikationen använder i grundutförande någon underlig variant på AJAX-förfrågan. Du ska nu implementera en äldre variant av realtidslöning som vi kallar för long-polling. I dagsläget kanske man föredrar[web sockets](http://en.wikipedia.org/wiki/WebSocket) och [server-sent events](https://developer.mozilla.org/en-US/docs/Server-sent_events/Using_server-sent_events) (se extrauppgiften) men i många fall har man mer klassisk Long-polling-teknik som fallback.

Det finns ett antal olika varianter för så kallade Comet-tekniker men du ska implementera en lösning som stödjer sig på metoden som kallas för **XMLHttpRequest long polling** alternativt **XHR streaming**.

anken är att du ska skriva om meddelande-hanteringen till en comet-lösning där servern meddelar klienten när ett nytt meddelande har skrivits. Du ska alltså kunna ha två webbläsarfönster öppna och när du skriver ett meddelande i det ena ska det dyka upp i båda webbläsarfönstren.

Long-polling tas upp under vecka 4 i självstudier och peer-instructions

####Krav
* Sista skrivna meddelandet ska hamna högst upp i meddelandelistan 
* Bara de nya meddelanden som inte tidigare skickas ut till klienten ska skickas ut vid en uppdatering.
* Du förklarar din implementation i din laborationsrapport samt reflekterar över de för- och nackdelar som finns med en denna lösning.
* Koden ska såklart redovisas på ditt github-konto tillsammans med en URL till en körbar version


## Del 4 - Extrauppgift 1
För er som vill och/eller satsar på högre betyg finns ytterligare en extrauppgift. Gör en ytterligare en implementation med Web Socket. Implementera applikationen så att long-pollingtekniken automatiskt körs som fallback för eventuella webbläsare som inte stödjer den nya tekniken.

Jämför med long polling-tekniken och beskriv skillnaderna i din laborationsrapport tillsammans med en URL till en körbar version.