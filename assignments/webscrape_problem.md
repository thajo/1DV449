##Problem
I denna uppgift ska du skriva ett **automatiserat serverscript** som skrapar information på en webbplats. Du ska alltså skapa en egen webbskrapa, med egen kod och inte använda något färdigt verktyg. Din skapa ska producera en eller flera JSON-filer som ska innehålla den skrapade informationen.

Du får i denna uppgift mycket gärna välja en egen webbplats att skrapa på information. Dock ska omfattningen på uppgiften vara den samma som nedan beskrivna. Kontakta kursansvarige (twitter: @thajo_john) och kolla att ditt exempel uppfyller kraven innan du sätter igång.

För er utan fantasi kommer uppgiften att gå ut på att skrapa kursinformation ifrån CoursePress. Din webbskrapa ska utgå ifrån sidan http://coursepress.lnu.se/kurser. Den innehåller en lista med kurser samt en paginering till fler sidor som fortsätter lista kurserna. Din uppgift blir att skrapa ner viss information (se kraven) om ALLA de kurser som finns på CoursePress. Naturligtvis ska ditt skript vara dynamiskt byggt så det kan hantera ifall kurser läggs till eller tas bort.

Skrapningen ska ske på ett, för servern, så skonsamt sätt som möjligt samt ha en utarbetad strategi för caching.

##Val av teknik
Du är helt fri att välja teknik, programmeringsspråk och servermiljö. Fokus på denna uppgift är att du löser problemet och att du förstår de koncept som tas upp i samband med uppgiften.

Koden ska redovisas via Github samt att det ska finnas en körbar version för examinatorn att nå via en URL. Uppgiften kommer examineras muntligen på redovisningspassen. 

##Krav
 
1. Scriptet ska vara helt automatiserat och börja sin skrapning på URL:en http://coursepress.lnu.se/kurser
2. Du ska göra regelbundna commits av din kod och synkronisera denna till GitHub.
3. Informationen som ska skrapas är: 
	* Kursens namn
	* Den URL kurswebbplatsen har
	* Kurskod
    * URL till kursplanen
	* Den inledande texten om varje kurs
	* Senaste inläggets rubrik, författare samt datum/klockslag för detta inlägg (på formatet YYYY-MM-DD HH:MM)
    * Finns inte den aktuella informationen på något av fälten ska de ersättat med texten "no information". T.ex. "coursecode" : "no information". 
    * Du ska också låta ditt skript ta reda på viss statistik kring skrapningen genom att att i ditt JSON-dokument inkludera även hur många kurser som skrapats ner samt en timestamp om när senaste skrapningen gjordes (bör användas vid din cachningsstrategi). 

4. All data ska sparas på disk i en fil i korrekt JSON-format som man ska kunna komma åt via en URL efter skrapningen är gjord. Fundera över hur du strukturerar upp din JSON på ett bra sätt! 
Använd jsonlint.org eller lämpligt plugin till din editor för att validera json-strukturen du skapar.
5. Du ska bara skrapa kurser! (dock ej för extrauppgiften) observera att visa sidor hör till ett projekt, ämne, blogg eller t.ex. är coursepress startsida. Hitta ett enkelt sätt att särskilja dem!
6. Du ska implementera en enklare cachingsstategi som gör att om man anropar sidan som kör ditt script ska bara själva skrapningen göras ifall fem minuter har passerat sedan sista gången. Det ska dock vara enkelt att kicka igång skrapan vid redovisning genom en enkel ändring i koden eller borttagning av JSON-filen.
7. Din webbskrapas alla HTTP-anrop mot coursepress webbserver ska identifiera dig på lämpligt sätt.
8. Du ska skriva ner dina reflektioner (se nedan) i ett dokument i md-format som ska vara enkelt åtkommligt från ditt GitHub-repo.
9. När du anser dig klar med uppgiften gör du en release/tag på GitHub. Döp den liknande L01-v.1.0. Vid eventuella kompletteringar gör du en ny release L01-v.1.1 o.s.v.
  


##Reflektion
Du ska i ditt repositorie skapa en fil (reflektion_lab1.md) **i [markdown-format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)** där du reflekterar över följande saker:

1. Vad tror Du vi har för skäl till att spara det skrapade datat i JSON-format?
2. Olika jämförelsesiter är flitiga användare av webbskrapor. Kan du komma på fler typer av tillämplingar där webbskrapor förekommer? 
3. Hur har du i din skrapning underlättat för serverägaren?
4. Vilka etiska aspekter bör man fundera kring vid webbskrapning?
5. Vad finns det för risker med applikationer som innefattar automatisk skrapning av webbsidor? Nämn minst ett par stycken!
6. Tänk dig att du skulle skrapa en sida gjord i ASP.NET WebForms. Vad för extra problem skulle man kunna få då?
7. Välj ut två punkter kring din kod du tycker är värd att diskutera vid redovisningen. Det kan röra val du gjort, tekniska lösningar eller lösningar du inte är riktigt nöjd med.
8. Hitta ett rättsfall som handlar om webbskrapning. Redogör kort för detta.
9. Känner du att du lärt dig något av denna uppgift? 


##Extrauppgifter
För er som satsar på högre betyg i kursen finns här ett par extra funktioner för din applikation. Du väljer själv hur många du implementerar.

1. Implementera algoritmen för skrapningen via rekursiva anrop.
2. Skrapa även de andra typer av sidorna (project, subject, blogg) och skapa en JSON-fil för varje.
3. När man är inloggad på coursepress kan man även komma åt "mina kurser" Skrapa även ner dessa i en egen JSON-fil. Det kan kräva att scriptet du skriver måste logga in på coursepress för att komma åt sidan.
**STOR VARNING** Tänk efter hur du gö rmed ditt lösenord. LDet får unde ringa omständigheter spridas genom att t.ex. läggas på GitHub. Om du råkar göra det byt genast lösenordet!
4. Sortera så att kurserna sparas i bokstavsordning på kursnamn i din JSON-fil.

##Redovisning
Redovisning sker muntligen på de schemalagda redovisningspassen som finns i schemat. Du kommer dock få boka ett redovisningstillfälle. Se kurshemsidan för denna bokningsmöjlighet!

 Redovisningarna sker enskilt. Distansstudenter redovisar genom det virtuella klassrummet. Campusstudenter redovisar på något av de kursansvarigas kontor. Se till att ha en körbar version av din skrapa man kan nå via en URL.


##Tips
Har du problem att komma igång och vill skriva i PHP kan du studera de demonstrationsfilmer som finns på kurshemsidan om [DomDocument](https://coursepress.lnu.se/kurs/webbteknik-ii/domdocument/) och [cURL](https://coursepress.lnu.se/kurs/webbteknik-ii/curl/)

Surfa omkring på webbplatsen med din webbläsare (web inspector) och studera hur den fungerar. Hur är strukturen i sidorna. Hur är sidorna uppbyggda och hur kan de skrapas.

Börja med en sida. Bryt ner problemet i delmängder. Tänk på att det är en skarp server vi nu skrapar mot så att du är sparsam med dina request!

Använd handledningspassen och forumet till frågor. 

Behöver du en webbserver att lägga din applikation på. Använd [DigitalOcean](http://digitalocean.com) som du får via [GitHub Student Pack](https://education.github.com/).
