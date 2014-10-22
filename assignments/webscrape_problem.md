##Problem
I denna uppgift ska du skriva ett **automatiserat script** som skrapar data på en webbplats. Ditt script ska alltså ta ostrukturerad data och göra om till mer strukturerad. Det skrapade datat ska sparas JSON-format.

Du får i denna uppgift mycket gärna välja en egen webbplats att skrapa på information. Dock ska omfattningen på uppgiften vara den samma som nedan beskrivna. Kontakta kursansvarige (twitter: @thajo) och kolla att ditt exempel uppfyller kraven innan du sätter igång.

För er utan fantasi kommer uppgiften att gå ut på att skrapa kursinformation ifrån CoursePress. Sidan ni startar ert script på, http://coursepress.lnu.se/kurser, kommer att innehålla en lista med kurser samt en paginering till fler sidor som fortsätter lista kurserna. Din uppgift blir att skrapa ner viss information (se kraven) om ALLA de kurser som finns på CoursePress.

Skrapningen ska ske på ett så, för servern, skonsamt sätt som möjligt samt ha en utarbetad strategi för cahning.

##Val av teknik
Du är helt fri att välja teknik, programmeringsspråk och servermiljö för att lösa problemet. Fokus ligger i denna uppgift att du löser problemet och att du förstår de koncept som tas upp i samband med uppgiften.

Koden ska redovisas via Github samt att det ska finnas en körbar version för examinatorn att nå via en URL. Uppgiften kommer också redovisas muntligen på examinationspassen. 

##Krav
1. Läs igenom HELA handledningen inan du börjar.
1. Scriptet ska vara helt automatiserat och utgå från URL:en http://coursepress.lnu.se/kurser
2. Informationen som ska skrapas är: 
	* Kursens namn
	* Den URL kurswebbplatsen har
	* Kurskod
    * URL till kursplanen
	* Den inledande texten om varje kurs
	* Senaste inläggets rubrik, författare samt datum/klockslag (på formatet YYYY-MM-DD HH:MM - Kan behöva reguljärt uttryck för att få ut detta)
    * Du ska också låta ditt skript ta reda på viss statistik kring skrapningen genom att att i ditt JSON-dokument inkludera även hur många kurser som skrapats samt en timestamp om när senaste skrapningen gjordes (bör användas vid din cachningsstrategi). 

3. Du ska göra regelbundna commits av din kod och synkronisera denna till GitHub.
4. All data ska sparas på disk i en fil i korrekt JSON-format. Fundera över hur du strukturerar upp din JSON. Använd jsonlint.org eller lämpligt plugin till din editor för att validera json-strukturen du skapar.
5. Om någon av uppgifterna saknas på någon sida ska istället texten "none" anges (t.ex. "author" : "none")
6. Du ska bara skrapa kurser! (dock ej för extrauppgiften) observera att visa sidor hör till ett projekt, ämne eller är en blogg. Hitta ett sätt att särskilja dem!
7. Du ska implementera en enklare cachningsstrategi som gör att om man anropar sidan som kör ditt script ska bara själva skrapningen göras ifall fem minuter har passerat. Det ska dock vara enkelt att kicka igång skrapan vid redovisning genom en enkel ändring i koden.
8. Din skrapas alla HTTP-anrop ska identifiera dig på lämpligt sätt.
9. Du ska skriva ner dina reflektioner i ett dokument i md-format som ska vara enkelt åtkommligt från ditt GitHub-repo.
10. Välj ut två punkter kring din lösning du tycker är värd att diskutera vid redovisningen. Det kan röra val du gjort, tekniska lösningar eller lösningar du inte är riktigt nöjd med.
11. När du anser dig klar med uppgiften gör du en release/tag på GitHub. Döp den liknande L01-v.1.0. Vid eventuella kompletteringar gör du en ny release L01-v.1.1 o.s.v.
  


##Reflektion
Du ska i ditt repositorie skapa en fil (reflektion_lab1.md) i [markdown-format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) där du reflekterar över följande saker:

1. Vad tror Du vi har för skäl till att spara det skrapade datat i JSON-format?
2. Hur har du i din skrapning underlättat för serverägaren?
3. Vilka etiska aspekter bör man fundera kring vid webbskrapning?
4. Vad finns det för risker med applikationer som innefattar automatisk skrapning av webbsidor? Nämn minst tre stycken!
5. Tänk dig att du skulle skrapa en sida gjord i ASP.NET WebForms. Vad för extra problem skulle man kunna få då?
6. Känner du att du lärt dig något av denna uppgift? 


##Extrauppgifter
För er som satsar på högre betyg i kursen finns här ett par extra funktioner för din applikation.

1. Implementera algoritmen för skrapningen via rekursiva anrop.
2. Skrapa även de andra typer av sidorna (project, subject, blogg) och skapa en JSON-fil för varje.
3. Sortera så att kurserna sparas i bokstavsordning på kursnamn i din JSON-fil.


##Redovisning
Redovisning sker på de schemalagda redovisningspassen som finns i schemat.
Laborationen redovisas genom att göra en realease med din kod på ditt github-repositorie samt genom en muntlig redovisning på schemalagt redovisningstillfälle. Redovisningarna sker enskilt. Examinatorn ska kunna nå applikationen via en URL. 

Distansstudenter redovisar genom det virtuella klassrummet.
Campusstudenter redovisar hos någon av de kursansvarigas kontor genom att boka en tid på kursens webbplats. Se till att ha en körbar version man kan nå via en URL.



##Tips
Studera de demonstrationsfilmer som finns på kurshemsidan.

Surfa omkring på webbplatsen med din webbläsare (web inspector) och studera hur den fungerar. Hur är strukturen i sidorna. Hur är sidorna uppbyggda och hur kan de skrapas.

Börja med en sida. Bryt ner problemet i delmängder. Tänk på att det är en skarp server vi nu skrapar mot

Använd handledningspassen och forumet till frågor. 

Behöver du en webbserver att lägga din applikation på. Använd [DigitalOcean](http://digitalocean.com) som du får via [GitHub Student Pack](https://education.github.com/).
