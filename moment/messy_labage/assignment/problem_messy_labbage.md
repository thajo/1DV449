##Problem
Denna laboration består av tre delar. Du kommer få en webbapplikation som tillhör det röriga slaget. Tanken är att du med din kunskap ska analysera och förbättra denna applikation.

I första delen av laborationen ska du försöka identifiera prestandabovar i applikationen och försöka rätta till dessa.
I andra delen ska du identifiera och rätta till eventuella säkerhetsrisker med applikationen.
I tredje delen ska du implementera antingen en AJAX-lösning för uppdatering eller en Comet-lösning (extrauppgift)

Din kod ska så klart också redovisas på github.

##Om applikationen
I förra laborationen skrapade vi viss data och sparade i en databas. Denna databas har nu används för att skriva en enklare AJAX-driven webbapplikation. Problemet med applikationen är att den inte är speciellt bra skriven, varken ur prestanda-, säkerhets- eller skalbarhetssynvinkel. I denna laboration ska vi främst koncentrera oss på de två första punkterna. Som Du kommer upptäcka är applikationen rörigt uppbyggd. Du kommer få hela källkoden och din uppgift blir att förbättra applikationen samtidigt som du noterar de delar du förändrar i en laborationsrapport.

Applikationen ska ha samma funktion när du är färdig med den.
Fokus på denna laboration ligger inte på att strukturera om koden i en MVC-struktur eller något annat design pattern (även om ni får det om ni vill).
Naturligtvis får du skriva om applikationen helt från grunden men du måste redogöra för vilka delar som .........

TODO - INLOGGNING

Rada upp de bibliotek som ska ingå
Utseendet ska vara det samma - inte ta bort några CSS-regler

FÅR MAN SKRIVA OM HELA APPLIKATIONEN

## Del 1 - Optimering
Applikationen kan optimeras både i front- och back-end (vi bortser från applikationscache och val av databashanterare som såklart påverkar prestandan). Du noterar vilka delar du förändrar och varför. Dela upp varje del i följande punkter, gärna i tabellform:

* Namn på åtgärd Du gjort för att försöka förbättra prestandan
* Teori kring åtgärden (förklara varför du implementerar den)
* Tid det tar för applikationen att rendera sidan mess.php **innan** åtgård (utan browser-cache, medeltal på ett antal testningar)
* Tid det tar för applikationen att rendera sidan mess.php **efter** åtgärd (utan browser-cache, medeltal på ett antal testningar)
* Resonemang kring att testresultatet blev som det blev.


####Tänk på följande:
Server-cachning och gzip är svårt att implementera på servrar man inte har full kontroll över (kan styra php.ini/.htaccess i apache:s fall). I de flesta fall är redan webbservern förinställd på ett bra sätt. TODO - UTVECKLA

Även om din åtgärd **inte** förbättrar resultatet kan den vara intressant att ta med i laborationsrapporten då åtgärden enligt teorin borde förbättrat prestandan men av någon nämnd anledning inte gör detta.

Tänk på att om du kör applikationen lokalt går det väldigt fort och kan vara svårt att upptäcka verkliga förändringar. Testa gärna dina förändringar på en extern server t.ex. ditt webbhotell eller varför inte cloud9 eller någon annan cloudbaserad tjänst.

#### Krav
Du ska implementera minst 5 stycken olika prestandahöjande (ur inladdnings- och renderingssynvinkel) och **tydligt** redogöra för dessa i din laborationsrapport
Fler implementerade åtgärder ses som plus.

#### Tips
Kurslitteraturen går igenom många tips för frontends-optimering.
Tänk på att webbläsaren cache:ar dina förfrågningar.


## Del 2 - Säkerhetsproblem
Applikationen är inte speciellt säker och det finns gott om säkerhetshål att täppa till
BORTSE FRÅN HTTPS - Extra

Du redogör för dina åtgärder i din laborationsrapport.
Dela upp varje del i följande punkter, gärna i tabellform:

* Redogör för det säkerhetshål du hittat.
* Redogör för hur säkerhetshålet kan utnyttjas.
* Vad för skada kan säkerhetsbristen göra?
* Hur du har åtgärdat säkerhetshålet i applikationskoden?

## Del 3 - AJAX eller Long Polling

TODO - Skriv om
Att HTTP-protokellet i sitt orginalutförande har lite begränsningar vet vi om. Kommunikationen mellan webbläsare och webbserver....

En av dessa är möjligheten att ha en kanal öppen till klienten och att från servern kunna skicka data till klienten utan att den senare gjort en request. I dagsläget finns det nyare tekniker så som web socekets och server-side events. Vi ska dock använda en teknik som fungerar med äldre webbläsare och som utnyttjar HTTP-protokollet.

Lösningen brukar kallas [Comet](http://en.wikipedia.org/wiki/Comet_(programming)) och är egentligen ett paraply-begrepp för tekniker där webbservern pushar data till klienten. Det finns ett antal olika varianter för detta men du ska implementera en lösning som stödjer sig på metoden som kallas för **XMLHttpRequest long polling**

Tanken är att du ska skriva om meddelande-hanteringen till en comet-lösning där klienten ligger och lyssnar på nya meddelanden från servern. Applikationen som du fått har implementerat en AJAX-lösning för postning av nya meddelanden men det finns ingen uppdatering när nya meddelanden har skrivits (annat än att ladda om sidan).

Du förklarar din implementation i din laborationsrapport samt reflekterar över de för- och nackdelar som finns med en denna lösning.
Din kod ska så klart också redovisas på github.

[http://www.ibm.com/developerworks/library/wa-reverseajax1/](http://www.ibm.com/developerworks/library/wa-reverseajax1/)

####Krav
Applikationen ska fungera...
Reflektera i din laborationsrapport över brister med denna teknik. Vad bör man tänka på när man gör en liknande implementationer.

### Extrauppgift
Gör en implamentation med någon av de nya teknikerna:
* Web Socket
* Server-sent events 
Jämför med long polling-tekniken och beskriv skillnaderna i din laborationsrapport.