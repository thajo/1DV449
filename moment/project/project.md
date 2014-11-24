##Projekt - Webbteknik II - 2013/2014

###Inledning
Som avslutning av denna kurs ska Du skriva en komplett applikation som ska sammanfatta vad du lärt dig under kursens gång samt förhoppningsvis tillskansa dig ny kunskap och ny erfarenhet kring hur man jobbar mot befintliga webb-API:r. Projektet är också tänkt att ge dig kunskaper om nya och HTML5-relaterade API:er för JavaScript-klienter. 

Vår förhoppning är att du i detta moment utvecklar en egen applikationsidé och som du utan problem skulle kunna visa upp för tilltänkta arbetsgivare när du söker jobb. Det är också klart önskvärt att du låter ditt eget driv och kreativitet som webbutvecklare komma fram här. Applikationen ska vara av sådan kvalité att den ska kunna köras skarpt.

##En mashup-applikation
Tanken är att du ska skapa en egen mashup-applikation utifrån en egen idé. Vad applikationen ska hanterar för slags data är upp till dig och din idé. Vi ser gärna att ni utvecklar en applikation kring något du brinner för. Förhoppningsvis jobbar du vidare på din idé från seminarium 3.

Du börjar med att beskriva din idé i ett kort dokument (i md-format) som du publicerar på ditt github-repo som hör till kursen.
Gör detta så fort som möjligt men senast **19:e december 2013**.

##Krav på applikation för godkänt (betyg 3)
Vi kommer alltså ha en fri hållning till vad din applikation behandlar för data och hur du bygger den men det finns ett antal krav vi kommer ha på applikatinen för godkänt (betyg 3) på projektet.

* Bygg en applikation som hämtar data från **minst två stycken externa API:er**. dessa ska sammankopplas på ett dynamiskt sätt i din applikationskod.

* Applikationen ska ha en OAuth-koppling d.v.s. använderen ska kunna logga in via en tredjepartstjänst. Har du ingen anning om vad du ska använda en inloggning till i din applikation så skriv en inställningssida för användaren där man t.ex. kan ändra på offline-stödet elle rnågot annat i applikationen. 

* Du ska implementera felhantering till din applikation så att användaren av applikationen blir medveten om t.ex. något av API:erna går ner.

* Applikationen ska vara publicerad och körbar på en publik URL.

* Applikationen ska vara genomarbetad med avseende på design, användarvänlighet, säkerhet och optimering. Designen ska kännas proffsig och genomarbetad. Nej, en ogenomarbetad design är INTE "enkel och stilren".

* Stabilitet och design
Din applikation ska självklart fungera utan buggar eller ohanterade fel. Användaren ska hela tidens veta vad som pågår i applikationen. Krashar din applikation och ej har god felhanteringen underkänns den.

* Applikationen ska utgå ifrån begreppen "Offline first" och Mobile first"

* Cachning
Din applikation ska cacha data både på front- och backend. Beskriv din cachningsstrategi i din rapport, Motivera eventuella undantag från detta i din rapport.

* Reflekterande rapport, inspelad redovisning
Du redovisar din applikation genom att göra en muntlig och skriftlig redovisning. Rapporten ska tydligt beskriva hur arbetet gått till, vilka tekniker du använt, de reflektioner du gjort samt vad du lärt dig under arbetet.

Denna gång ska dock den muntliga redovisningen vara inspelad som film. Du ska under minst tre och max fem minuter sälja in din applikation. Du väljer själv om du vill publicera den på youtube eller som en vanlig mp4-fil. 

Du redovisar en URL som pekar på din presentationsfilm i ditt repositories readme - där ska också en länk till rapporten och en publika URL:en finnas. Filmerna kommer delas ut på kurshemsidan så att ni kan se varandras. 

* All kod och dokumentation ska nås via ditt github-repo

##Eventuellt betygshöjande funktioner (betyg 4 och 5)

För högre betyg än (G/3) ska applikationen redovisas innan utsatt leveransdatum. Se kurshemsida.

Vi ser såklart gärna att ni utmanar er själva och testar nya grepp och tekniker vilket kan ses som betygshöjande. Här är några förslag som skulle kunna vara betygshöjande funktioner i din applikation. Ju fler som implementeras på ett tillfredsställande sätt ökar chansen till ett högre betyg.

* Inkludera HTML5-relaterade API:er så som geolocation, web workers, web sockets m.m.
* Inkludera flera externa API:er och höj din applikations funktionalitet ytterligare
* Applikationens design ska vara responsiv alltså anpassa sig till enhetens skärmstorlek. Applikationen ska fungera väl i samtliga fall.
* Det ska gå att bläddra framåt och tillbaka i din applikations state via webbläsarens normala navigation.
* Fundera över SEO och applicera detta där möjligt. Var noga med att i rapporten ta upp din strategi kring detta.

##Bedömning
Din applikation kommer examineras av kursledningen på följande grunder:

* Krativitet och nyfikenhet. Är din applikation nytänkande och intressant samt har du utmanat dig själv.
* Förmåga att lösa problem.
* Hur väl fungerar din applikation. Buggar, användbarhet.
* Funktionallitet - Hur mycket funktioner har din applikation. Vilket mervärde ger applikationen. 
* Kvalité på din rapport. Ger din rapport en bra bild av din applikation. Har du reflekterat på ett bra sätt som visar den kunskap du besitter i ämnet.
* Den inspelade presentationen. Hur bra lyckas du förmedla bilden av din applikation.
* Uppfyllande av leveransdatum. 
* Lärdomar utanför laborationskurs. Påvisar din applikation och rapport att du inkluderat och inskaffat ny kunskap som inte tagits upp i laborationskursen.


## Rapporten
Den skriftliga projektrapporten du lämnar in ska innehålla följande:

* Inledning där du beskriver vad du gjort och bakgrunden till din applikation. Finns det liknande applikationer redan?
* Inkludera en schematisk bild över applikationens beståndsdelar så att läsaren har enklare att förstå applikationens dataflöde.
* Serversida: Beskriv hur din applikation fungerar på serversidan. Beskriv funktionaliteten och hur den är uppbyggd. Vald teknik/programmeringsspråk/ramverk? Hur fungerar cachningen? Hur sköter du felhanteringen m.m.
* Klientsida: Hur fungerar din applikation på klientsidan. Beskriv på liknande sätt som serversidan.
* Egenreflektion kring projektet: Här tar du upp hur projektet har gått. Vilka eventuella problem har du stött på? Finns det funktioner som du velat implementera men inte hunnit? Hur skulle du vilja jobba vidare med din applikation?
* Risker med din applikation. Reflektera över vilka risker det finns med din applikation; rent tekniskt, säkerhet, etiskt m.m.
* Skriv också om de eventuella delar du anser vara betygshöjande med din applikation. Motivera varför du anser dessa vara betygshöjande.

## Tips
* Du är fri att använda ramverk, både till klient- och serversidan.
* Använd diskussionsforumet för att diskutera med varandra
* Börja på rapporten tidigt för att kontinuerligt hålla den uppdaterad
* Gör kontinuerligt commits
* Testa tidigt att din applikation fungerar på en extern server. testa inte detta dagen innan leverans.
* Testa din kod...testa din applikation. Leverera inte något som inte fungerar!

