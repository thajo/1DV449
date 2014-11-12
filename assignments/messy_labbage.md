##Problem - Messy Labbage
Denna laboration består av tre delar. Du kommer få en webbapplikation som kasnke inte är uppbyggd så som du har lärt dig. Det är ganska vanligt att man kommer få "mindre bra" kod i sitt knä som man får jobba vidare med. Tanken med denna uppgift är att du med din kunskap ska analysera och förbättra denna applikation både ur ett prestanda- och ett säkerhetsperspektiv.


* I första delen ska du identifiera och rätta till eventuella säkerhetsrisker med applikationen.
* I andra delen av laborationen ska du försöka identifiera prestandaproblem i applikationen och försöka rätta till dessa.
* I tredje delen ska du implementera lösning för meddelande-hantering i applikationen med en Comet-lösning (long-polling).

Du har ganska stora friheter att ändra i applikationen så länge funktion och utseende inte skalas bort. Fokus på laborationen ligger dock på analys av möjliga optimeringar och att täppa till säkerhetshål.

##Redovisning
Redovisning av denna laboration sker muntligen, i form av en laborationsrapport samt i form av publicering av kod på GitHub. Du kommer få en befintlig applikation att ladda ner som du inkluderar i ditt repositorie. 

Laborationsrapporten **ska** vara i md-format och finnas publicerad tillsammans med din kod i ditt  repositorie. Där ska också en URL till en körbar version av din omarbetade applikation tydligt framgå så vi kan testköra den.

##Om applikationen
Applikationen du får är inte speciellt bra skriven, varken ur prestanda-, säkerhets- eller skalbarhetssynvinkel. I denna laboration ska vi främst koncentrera oss på de två första punkterna. Att designen/strukturen på applikationen också är bristfällig kan vi bortse ifrån. Du kommer få hela källkoden och din uppgift blir att förbättra applikationen samtidigt som du noterar tydligt de delar du förändrar i den skriftliga laborationsrapporten som denna gång blir redovisningsform. 

Applikationen tankar du ner från följande adress: 

Applikationen är skriven i PHP och kräver stöd för SQLite3 och PDO.

Applikationen ska ha samma funktion när du är färdig med den som den har när du får den men förhoppningsvis vara bättre, säkrare och snabbare.
Fokus på denna laboration ligger som sagt på optimering och säkerhet men känner du att du helt eller delvis vill strukturera/skriva om applikationen är du fri att göra detta men i laborationsrapporten måste det **tydligt** framgå vilka prestanda- och säkerhetsförbättringar som du gjort.

Applikationen fungerar som så att:

TODO

Just nu finns två användarkonton; admin:admin och user:user.

Applikationen använder några javascriptbiblotek samt css-ramverk. Dessa ska finnas kvar vilket innebär att du alltså inte får plocka bort någon javascript- eller css-kod även om det kan vara på sin plats att strukturera eller omarbeta dessa dessa ur optimeringssynpunkt. 

## Del 1 - Säkerhetsproblem
Applikationen är inte speciellt säker och det finns gott om säkerhetshål att täppa till. Din uppgift blir såklart att identifiera och fixa till dessa säkerhetshål. Vi kan dock i denna laboration bortse från HTTPS.

Du redogör för dina åtgärder i din laborationsrapport.
Dela upp varje säkerhetsrisk du hittar i följande punkter:

* Redogör för det säkerhetshål du hittat.
* Redogör för hur säkerhetshålet kan utnyttjas.
* Vad för skada kan säkerhetsbristen göra?
* Hur du har åtgärdat säkerhetshålet i applikationskoden?

####Krav
Du ska identifiera **minst fyra** olika och betydande säkerhetsrisker och rätta till dessa samt redogöra för dessa i din laborationsrapport. Plus för de som identifierar och hittar fler.

## Del 2 - Optimering
Applikationen bör kunna optimeras både front- och backend (vi bortser från val av databashanterare som såklart också påverkar prestandan). Det kan röra sig om allt från hur resursfiler implementerats till hur anrop till webbserver/databas sköts. Din uppgift blir att analysera applikationen och identifiera eventuella delar som går att optimera bättre. Du beskriver vilka delar du förändrar i din laborationsrapport och berättar också varför. 
Dela upp **varje olika del** i följande punkter:

* Namn på åtgärd Du gjort för att försöka förbättra prestandan
* Teori kring åtgärden (förklara varför du implementerar den och vad säger teorin om vad denna åtgärd gör). Referens till vart du hittat denna teori ska anges!
* Observation (laddningstid, storlekar av resurser, anrop m.m.) **innan** åtgård (utan webläsar-cache - gärna ett medeltal av ett antal testningar)
* Observation (laddningstid, storlekar av resurser, anrop m.m.) **efter** åtgärd (utan webläsar-cache - gärna ett medeltal av ett antal testningar)
* Reflektion kring att testresultatet blev som det blev.


####Tänk på följande:
HTTP-caching och gzip kan vara svårt att implementera på servrar man inte har full kontroll över (kan styras via php.ini / .htaccess i apache:s fall). I de flesta fall är redan webbservern förinställd. Därför kan dessa bortses ifrån i denna laboration men vill man får man gärna hantera dessa också.

Även om din åtgärd **inte** förbättrar resultatet kan den vara intressant att ta med i laborationsrapporten om åtgärden enligt teorin borde förbättrat prestandan men av någon nämnd anledning inte gör detta.

Tänk på att om du kör applikationen lokalt går det väldigt fort och kan vara svårt att upptäcka verkliga förändringar. Testa gärna dina förändringar på en extern server t.ex. ditt webbhotell eller varför inte någon molnbaserad tjänst.

Mindre kodoptimeringar så som att ++variable anses snabbare än variable++ räknas inte i denna laboration utan vi letar efter saker som vi tar upp i kursen så som t.ex. antalet requests m.m.


#### Krav
Du ska implementera **minst sex** stycken olika och i teorin styrkta prestandahöjande åtgärder (ur inladdnings- och renderingssynvinkel) och **tydligt** redogöra för dessa i din laborationsrapport. Optimeringar ska köras både i klient- och serverkod.
Fler implementerade åtgärder ses som plus.

#### Tips
Kurslitteraturen går igenom många tips för frontends-optimering.
Tänk på att webbläsaren cache:ar dina förfrågningar.
Använd de utvecklingsverktyg (Developer tools) som finns till din webbläsare för att studera applikationen.




## Del 3 - long-polling
För de som siktar på högre betyg finns ett annat problem definerat i del 4 (och 5) som man istället kan lösa.
För de som endast siktar på godkänt ska man lösa problemet med att man i nuvarande applikation behöver ladda om sidan för att se nya meddelanden man skriver till respektive producent. Detta bör lösas med en AJAX-förfrågan när man vet att meddelandet har skapats och därifrån uppdatera meddelandelistan.  

####Krav

* Sista skrivna meddelandet ska hamna högst upp i meddelandelistan (lägg gärna till tidsangivelse på varje meddelande)
* Applikationen ska förbättras enligt ovan och fungera utan problem.
* Din kod ska redovisas (välkommenterad) på github
* Du ska skriva ner i din laborationsrapport hur du gjorde denna implementation. Det ska där också finnas en länk till en körbar version av din applikation.


## Del 4 - Long Polling - Extrauppgift 1

Att HTTP-protokellet i sitt orginalutförande har lite begränsningar vet vi om. Kommunikationen mellan webbläsare och webbserverar är oftast byggda för att följa en request/response-modell. I och med en webb där vissa tjänster ställer högre krav på realtidsdata finner man ibland denna metod otillräcklig. Man efterfrågan en mer push-baserad metod där servern skickar ut data till kienten när ny data finns.

I dagsläget finns nyare tekniker så som [web sockets](http://en.wikipedia.org/wiki/WebSocket) och [server-sent events](https://developer.mozilla.org/en-US/docs/Server-sent_events/Using_server-sent_events). Vi ska dock i denna laboration studera en teknik som fungerar med äldre webbläsare och som utnyttjar HTTP-protokollet och [XMLHttpRequest](http://en.wikipedia.org/wiki/XMLHttpRequest).

Lösningen brukar kallas [Comet](http://en.wikipedia.org/wiki/Comet_&#40;programming&#41;) och är egentligen ett paraply-begrepp för tekniker där webbservern pushar data till klienten. Det finns ett antal olika varianter för detta men du ska implementera en lösning som stödjer sig på metoden som kallas för **XMLHttpRequest long polling** alternativt **XHR streaming**.

Applikationen du har fått har ju möjlighet att skriva meddelande till de olika producenterna. Tanken är att du ska skriva om meddelande-hanteringen till en comet-lösning där servern meddelar klienten när ett nytt meddelande har skrivits. Du ska alltså kunna ha två webbläsarfönster öppna (med samma valda producent) och när du skriver ett meddelande i det ena ska det dyka upp i båda webbläsarfönstren.


####Krav

* Bara de nya meddelanden som inte tidigare skickas ut till klienten ska skickas ut vid en uppdatering.
* Du förklarar din implementation i din laborationsrapport samt reflekterar över de för- och nackdelar som finns med en denna lösning.
* Koden ska såklart redovisas på ditt github-konto tillsammans med en URL till en körbar version

####Tips
[http://www.ibm.com/developerworks/library/wa-reverseajax1/](http://www.ibm.com/developerworks/library/wa-reverseajax1/)

Testa först implementera din lösning i ett enklare fall så du får ihop metoden och för sedan över den till applikationen

## Del 5 - Extrauppgift 2

För er som vill och hinner finns ytterligare en extrauppgift. Gör en ytterligare en implementation med någon av de nyare teknikerna Web Socket eller Server-sent events. Jämför med long polling-tekniken och beskriv skillnaderna i din laborationsrapport tillsammans med en URL till en körbar version.