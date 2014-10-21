##Problem
I denna uppgift ska du skriva ett automatiserat script som skrapar data på en webbplats d.v.s skapar strukturerad data av ostrukturerad.

Du får i denna uppgift mycket gärna vara kreativ och välja en egen webbplats att skrapa på information. Dock ska omfattningen på uppgiften vara den samma som nedan beskrivna. Kontakta kursansvarige och kolla av innan.

För er utan fantasi kommer uppgiften att gå ut på att skrapa kursinformation ifrån coursepress. Sidan ni startar ert script på kommer att innehålla en lista med kurser samt en pagenering till fler sidor med kurser. Din uppgift blir att skrapa ner alla kurser samt viss information om varje.

Sidan består av en ett inloggningsformulär som leder till en sida med en lista med producenter. Genom att följa dessa länkar via ditt automatiserade skript ska du skrapa alla (möjliga) undersidor på information och spara i valfri datalagring.

Ditt script ska alltså automatiskt utgå från en URL, http://coursepress.lnu.se/kurser och utifrån denna automatiskt skrapa ner efterfrågad information och presentera denna i ett mer strukturerat (maskinläsbart) format.

Du är helt fri att välja tekniker, programmeringsspråk och servermiljö för att lösa problemet. Fokus ligger i denna uppgift att du löser problemet och att du förstår de koncept som tas upp i samband med uppgiften.

Koden ska dock redovisas via Github samt vara körbar för examinatorn via en URL. Uppgiften kommer också redovisas muntligen på examinationspassen. 

##Krav
1. Scriptet ska vara helt automatiserat och utgå den nämnda URL:en
2. Informationen som ska skrapas är: 
	* Kursens namn
	* Den URL kurswebbplatsen har
	* Kurskod
	* Den inledande texten om varje kurs
	* Senaste inläggets rubrik, författare samt datum/klockslag (på formatet YYYY-MM-DD HH:MM - Kan behöva reguljärt uttryck för att få ut detta)


	
3. Du ska göra regelbundna commits av din kod och synkronisera denna till GitHub.
4. All data ska sparas på disk i en fil i korrekt JSON-format. Fundera över hur du strukturerar upp din JSON.
5. Om någon av uppgifterna saknas på något ska istället texten "none" anges (t.ex. "author" : "none")
6. Du ska bara skrapa kurser! observera att visa sidor hör till ett projekt, ämne eller person. Hitta ett sätt att särskilja dem!
7. 


##Reflektion
Du ska i ditt repositorie skapa en fil (reflektion_lab1.md) i [markdown-format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) där du reflekterar över följande saker:

1. Ni är fria att välja sätt att läsa in och extrahera data ur webbsidorna. Motivera ditt val!
2. Vad finns det för risker med applikationer som innefattar automatisk skrapning av webbsidor? Nämn minst tre stycken!
3. Tänk dig att du skulle skrapa en sida gjord i ASP.NET WebForms. Vad för extra problem skulle man kunna få då?
4. Har du gjort något med din kod för att vara "en god webbskrapare" med avseende på hur du skrapar sidan?
5. Vad har du lärt dig av denna uppgift? 


##Extrauppgifter
För er som satsar på högre betyg i kursen finns här ett par extra funktioner för din applikation.

1. Implementera algoritmen för skrapningen via rekursiva anrop.
2. Skrapa även de andra typer av sidorna och skapa en JSON-fil för varje.


##Redovisning
Redovisning sker på de schemalagda redovisningspassen som finns i schemat.
Laborationen redovisas genom att göra en realease med din kod på ditt github-repositorie samt genom en muntlig redovisning på schemalagt redovisningstillfälle. Redovisningarna sker enskilt. Examinatorn ska kunna nå applikationen via en URL. 

Distansstudenter redovisar genom det virtuella klassrummet.
Campusstudenter redovisar hos någon av de kursansvarigas kontor. Se till att ha en körbar version man kan nå via en URL.


##Tips
Studera de demonstrationsfilmer som finns på kurshemsidan.

Surfa omkring på webbplatsen med din webbläsare (web inspector) och studera hur den fungerar. Hur är strukturen i sidorna. Hur är sidorna uppbyggda och hur kan de skrapas.

#### Gör en release på din kod
När du genomfört och vill examinera din applikation och för att du senare enkelt ska kunna gå tillbaka och se hur koden såg ut när genomfört laboration 1 ska du göra något som kallas för en tag eller release. 

1. Logga in på GitHub och gå till repositoriet för laborationen.
2. Kontrollera att dina senaste ändringar finns tillgängliga på GitHub.
3. Klicka på "releases" ovanför fillistningen.
4. Välj att skapa en ny release.
5. Se till att "Tag version" blir `L01_v.1.0`.
Titel och description fyller du i som du själv vill.
![GitHub Release][github-release]
6. Publicera releasen


[github-release]: https://github.com/1ik415/Kursmaterial/raw/master/Laborationer/pics/github-release.png





 
