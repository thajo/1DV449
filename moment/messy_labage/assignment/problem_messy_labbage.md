##Problem - Messy Labbage
Denna laboration består av tre delar. Du kommer få en AJAX-driven webbapplikation som tillhör det röriga slaget. Tanken är att du med din kunskap ska analysera och förbättra denna applikation.

* I första delen av laborationen ska du försöka identifiera prestandaproblem i applikationen och försöka rätta till dessa.
* I andra delen ska du identifiera och rätta till eventuella säkerhetsrisker med applikationen.
* I tredje delen ska du implementera lösning för meddelande-hantering i applikationen, för godkänt räcker en vanlig AJAX-lösning, för extrauppgiften görs en Comet-lösning.

##Redovisning
Redovisning av denna laboration sker i form av en laborationsrapport och publicering av kod på github.
Laborationsrapporten **ska** vara i anting md-format eller som pdf och finnas publicerad tillsammans med din kod. Där ska också en URL till en körbar version av din omarbetade applikationen finnas med så vi kan testköra den. När du anser dig färdig med din applikation gör du en release via github på den forkade applikationen (se nedan).

##Om applikationen
I förra laborationen skrapade vi viss data och sparade i en databas. Denna databas har nu används för att skriva en enklare AJAX-driven webbapplikation. Problemet med applikationen är att den inte är speciellt bra skriven, varken ur prestanda-, säkerhets- eller skalbarhetssynvinkel. I denna laboration ska vi främst koncentrera oss på de två första punkterna. Att designen på applikationen också är bristfällig struntar vi i till denna laboration. Du kommer få hela källkoden och din uppgift blir att förbättra applikationen samtidigt som du noterar de delar du förändrar i en skriftlig laborationsrapport som denna gång blir redovisningsform. 

Applikationen forkar du på github från adressen: TODO....
Applikationen är skriven i PHP och kräver stöd för SQLite3 och PDO.

Applikationen ska ha samma funktion när du är färdig med den som den har när du får den men förhoppningsvis vara bättre, säkrare och snabbare.
Fokus på denna laboration ligger som sagt på optimering och säkerhet men känner du att du helt eller delvis vill strukturera/skriva om applikationen är du fri att göra detta men i laborationsrapporten måste det **tydligt** framgå vilka prestanda- och säkerhetsförbättringar som förbättrats.

Applikationen fungerar som då att när man väl är inloggad listar den upp producenterna och klickar man på någon av dessa kommer mer information om producenten fram samt en möjlighet att skriva ett meddelande till producenten.
Just nu finns två användarkonton; admin:admin och user:user.

Applikationen använder några javascriptbiblotek samt css-ramverk. Dessa ska finnas kvar vilket innebär att du alltså inte får plocka bort någon javascript- eller css-kod även om det kan vara på sin plats att strukturera eller omarbeta dessa dessa ur optimeringssynpunkt. 


## Del 1 - Optimering
Applikationen bör kunna optimeras både front- och backend (vi bortser från val av databashanterare som såklart också påverkar prestandan). Det kan röra sig om allt från hur resursfiler implementerats till hur anrop till webbserver/databas sköts. Din uppgift blir att analysera applikationen och identifiera eventuella delar som går att optimera bättre. Du skriver om vilka delar du förändrar i din laborationsrapport och berättar också varför. 
Dela upp varje olika del i följande punkter, gärna i tabellform:

* Namn på åtgärd Du gjort för att försöka förbättra prestandan
* Teori kring åtgärden (förklara varför du implementerar den och vad säger teorin om vad denna åtgärd gör). Referens till vart du hittat denna teori ska anges!
* Observation (laddningstid, storlekar av resurser, anrop m.m.) **innan** åtgård (utan webläsar-cache - gärna ett medeltal av ett antal testningar)
* Observation (laddningstid, storlekar av resurser, anrop m.m.) **efter** åtgärd (utan webläsar-cache - gärna ett medeltal av ett antal testningar)
* Reflektion kring att testresultatet blev som det blev.


####Tänk på följande:
HTTP-caching och gzip kan vara svårt att implementera på servrar man inte har full kontroll över (kan styra php.ini / .htaccess i apache:s fall). I de flesta fall är redan webbservern förinställd. Därför kan dessa bortses ifrån i denna laboration men vill man får man gärna observera dessa också.

Även om din åtgärd **inte** förbättrar resultatet kan den vara intressant att ta med i laborationsrapporten om åtgärden enligt teorin borde förbättrat prestandan men av någon nämnd anledning inte gör detta.

Tänk på att om du kör applikationen lokalt går det väldigt fort och kan vara svårt att upptäcka verkliga förändringar. Testa gärna dina förändringar på en extern server t.ex. ditt webbhotell eller varför inte cloud9 eller någon annan cloudbaserad tjänst.

Mindre kodoptimeringar så som att ++variable anses snabbare än variable++ räknas inte i denna laboration utan vi letar efter saker som vi tar upp i kursen så t.ex. antalet requests m.m.


#### Krav
Du ska implementera **minst sex** stycken olika och betydande prestandahöjande åtgärder (ur inladdnings- och renderingssynvinkel) och **tydligt** redogöra för dessa i din laborationsrapport. Optimeringar ska köras både i klient- och serverkod.
Fler implementerade åtgärder ses som plus.

#### Tips
Kurslitteraturen går igenom många tips för frontends-optimering.
Tänk på att webbläsaren cache:ar dina förfrågningar.
Använd de utvecklingsverktyg (Developer tools) som finns till din webbläsare för att studera applikationen.


## Del 2 - Säkerhetsproblem
Applikationen är inte speciellt säker och det finns gott om säkerhetshål att täppa till. Din uppgift blir såklart att identifiera och fixa till dessa säkerhetshål. Vi kan dock i denna laboration bortse från HTTPS.

Du redogör för dina åtgärder i din laborationsrapport.
Dela upp varje säkerhetsrisk du hittar i följande punkter, gärna i tabellform:

* Redogör för det säkerhetshål du hittat.
* Redogör för hur säkerhetshålet kan utnyttjas.
* Vad för skada kan säkerhetsbristen göra?
* Hur du har åtgärdat säkerhetshålet i applikationskoden?

####Krav
Du ska identifiera **minst fyra** olika och betydande säkerhetsrisker och rätta till dessa samt redogöra för dessa i din laborationsrapport. Plus för de som identifierar och hittar fler (beroende på storlek av förändring)

## Del 3 - AJAX
För de som siktar på högra betygen finns ett annat problem definerat i del 4 (och 5) som man istället kan lösa.
För de som endast siktar på godkänt ska man lösa problemet med att man i nuvarande applikation behöver behöver ladda om sidan för att se nya meddelanden man skriver till respektive producent. Detta bör lösas med en AJAX-förfrågan när man vet att meddelandet har skapats och därifrån uppdatera meddelandelistan.

####Krav
Applikationen ska förbättras enligt ovan och fungera utan problem.
Din kod ska redovisas (välkommenterad) på github
Du ska skriva ner i din laborationsrapport hur du gjorde denna implementation. Det ska där också finnas en länk till en körbar version av din applikation.


## Del 4 - Long Polling - Extrauppgift 1

Att HTTP-protokellet i sitt orginalutförande har lite begränsningar vet vi om. Kommunikationen mellan webbläsare och webbserverar är är oftast byggda för att följa en request/response-modell. I och med en webb där vissa tjänster ställer högre krav på realtidsdata finner man ibland denna metod otillräcklig. Man efterfrågan en mer push-baserad metod där servern skickar ut data till kienten när ny data finns.

I dagsläget finns nyare tekniker så som [web sockets](http://en.wikipedia.org/wiki/WebSocket) och [server-sent events](https://developer.mozilla.org/en-US/docs/Server-sent_events/Using_server-sent_events). Vi ska dock i denna laboration studera en teknik som fungerar med äldre webbläsare och som utnyttjar HTTP-protokollet och [XMLHttpRequest](http://en.wikipedia.org/wiki/XMLHttpRequest).

Lösningen brukar kallas [Comet](http://en.wikipedia.org/wiki/Comet_&#40;programming&#41;) och är egentligen ett paraply-begrepp för tekniker där webbservern pushar data till klienten. Det finns ett antal olika varianter för detta men du ska implementera en lösning som stödjer sig på metoden som kallas för **XMLHttpRequest long polling**

Applikationen du har fått har ju möjlighet att skriva meddelande till de olika producenterna. Tanken är att du ska skriva om meddelande-hanteringen till en comet-lösning där servern meddelar klienten när ett nytt meddelande har skrivits. Du ska alltså kunna ha två webbläsarfönster öppna och när du skriver ett meddelande i det ena ska det dyka upp i båda webbläsarfönstren.


####Krav
Applikationen ska använda tekniken XMLHttpRequest long pooling, du ska alltså kunna ha två webläsare öppna där när du skriver ett meddelande i den ena ska bådas meddelandekö uppdateras.

För godkänt räcker det med att när ett nytt meddelande finns skickas alla meddelanden tillhörande den aktuella producenten ut. För extra plus skickas bara de *nya* meddelanden som inte tidigare skickas ut till klienten (se extrauppgift).
Du förklarar din implementation i din laborationsrapport samt reflekterar över de för- och nackdelar som finns med en denna lösning.
Koden ska såklart redovisas på ditt github-konto.

####Tips
[http://www.ibm.com/developerworks/library/wa-reverseajax1/](http://www.ibm.com/developerworks/library/wa-reverseajax1/)
Testa först implementera din lösning i ett enklare fall så du får ihop metoden och för sedan över den till applikationen

## Del 5 - Extrauppgift 2

För er som vill och hinner finns ytterligare en extrauppgift. Gör en ytterligare en implementation med någon av de nyare teknikerna Web Socket eller Server-sent events. Jämför med long polling-tekniken och beskriv skillnaderna i din laborationsrapport tillsammans med en URL till en körbar version.