##Projekt - Webbteknik II - 2013/2014

###Inledning
Som avslutning av denna kurs ska Du skriva en komplett applikation som ska sammanfatta vad du lärt dig under kursens gång samt förhoppningsvis tillskansa dig ny kunskap och ny erfarenhet kring hur man jobbar mot befintliga webb-API:r. Projektet är också tänkt att ge dig kunskaper om nya och HTML5-relaterade API:er för JavaScript-klienter.

Vår förhoppning är att du i detta moment utvecklar en egen applikationsidé och som du utan problem skulle kunna visa upp för tilltänkta arbetsgivare när du söker jobb. Det är också klart önskvärt att du låter ditt eget driv och kreativitet som webbutvecklare komma fram här.

##En mashup-applikation
Tanken är att du ska skapa en egen mashup-applikation utifrån en egen idé. Vad applikationen ska hanterar för slags data är upp till dig och din idé. Vi ser gärna att ni utvecklar en applikation kring något du brinner för. Förhoppningsvis jobbar du vidare på din idé från seminarium 3.

Du börjar med att beskriva din idé i ett kort dokument (i md-format) som du publicerar på ditt github-repo som hör till kursen.
Gör detta så fort som möjligt men senast **19:e december 2013**.

##Krav på applikation för godkänt (betyg 3)
Vi kommer alltså ha en fri hållning till vad din applikation behandlar för data och hur du bygger den men det finns ett antal krav vi kommer ha på applikatinen för godkänt (betyg 3) på projektet.

* Bygg en applikation som hämtar data från **minst två stycken externa API:er**. dessa ska såklart sammankopplas på ett dynamiskt sätt i din applikationskod.

* Du ska implementera felhantering till din applikation så att användaren av applikationen blir medveten om t.ex. något av API:erna går ner.

* Klientsidan ska vara en Single Page Applikation
Dina anrop mellan klient och server ska ske helt asynkront.
_(Undantag kan göras för exempelvis autentieringsprocesser via OAuth där synkrona sidomladdningar kan krävas.)_


* Stabilitet och design
Din applikation ska självklart fungera utan buggar eller ohanterade fel. Användaren ska hela tidens veta vad som pågår i applikationen. Designen ska kännas proffsig och genomarbetad. Nej, en ogenomarbetad design är INTE "enkel och stilren".


* Optimering och säkerhet
Det ska framgå av din applikation och rapport att du tänkt på optimering och säkerheten.

* Cachning
Din applikation ska cacha data både på front- och backend. Beskriv din cachningsstrategi i din rapport, Motivera eventuella undantag från detta i din rapport.

* Reflekterande rapport, inspelad redovisning
Du redovisar din applikation genom att göra en muntlig och skriftlig redovisning. Denna gång ska dock den muntliga redovisningen vara inspelad som film. Du ska under minst tre och max fem minuter sälja in din applikation. Du väljer själv om du vill publicera den på youtube eller som en vanlig mp4-fil. Du redovisar en URL som pekar på din presentationsfilm. Filmerna kommer delas ut på kurshemsidan så att ni kan se varandras. 

* All kod och dokumentation ska nås via ditt github-repo

##Eventuellt betygshöjande funktioner (betyg 4 och 5)

För högre betyg än (G/3) ska applikationen redovisas innan utsatt leveransdatum 19 januari 23:59.

Vi ser såklart gärna att ni utmanar er själva och testar nya grepp och tekniker vilket kan ses som betygshöjande. Här är några förslag som skulle kunna vara betygshöjande funktioner i din applikation. Ju fler som implementeras på ett tillfredsställande sätt ökar chansen till ett högre betyg.

* Du ska ha en strategi för att hantera de tillfällen då applikationen inte har en internetuppkoppling (Offline-stöd). De delar av applikation som inte kräver uppkoppling ska fortsätta att fungera även offline. 
* Inkludera flera HTML5-relaterade API:er så som geolocation, web workers, web sockets m.m.
* Inkludera flera externa API:er och höj din applikations funktionalitet ytterligare
* Applikationens design ska vara responsiv alltså anpassa sig till enhetens skärmstorlek. Applikationen ska fungera väl i samtliga fall.
* Det ska gå att bläddra framåt och tillbaka i din applikations state via webbläsarens normala navigation.
* Fundera över SEO och applicera detta där möjligt. Var noga med att i rapporten ta upp din strategi kring detta.

##Bedömning
Din applikation kommer examineras av kursledningen på följande grunder:

* Egen kreativitet. Är din applikation nytänkande och intressant.
* Förmåga att lösa problem.
* Funktionallitet - Hur mycket funktioner har din applikation. Vilket mervärde ger applikationen. Hur väl fungerar applikationen.
* Kvalité på din rapport. Ger din rapport en bra bild av din applikation. Har du reflekterat på ett bra sätt över det du gjort.
* Den inspelade presentationen. Hur väl "säljer du in" och förklarar din applikation i din presentation.
* Uppfyllande av leveransdatum
* Lärdomar utanför laborationskurs. Påvisar din applikation och rapport att du inkluderat och inskaffat ny kunskap som inte tagits upp i laborationskursen.


##Viktiga datum och redovisning
* 19:e december 23:59 - Deadline för att lämna in applikationsidé
* 19:e januari 23:59 - Inlämning av kod (via release på ditt till kursen hörande github-repositorie), rapport (se nedan), URL till körbar version av din applikation och inspelad redovisning. Allt ska finnas att få tag på via github på det repositorie som du har delat med kursens github-konto.

## Rapporten
Den skriftliga projektrapporten du lämnar in ska innehålla följande:

* Inledning där du beskriver vad du gjort och bakgrunden till din applikation
* Inkludera en schematisk bild över applikationens beståndsdelar så att läsaren har enklare att förstå applikationens dataflöde.
* Serversida: Beskriv hur din applikation fungerar på serversidan. Beskriv funktionaliteten och hur den är uppbyggd. Vald teknik/programmeringsspråk/ramverk? Hur fungerar cachningen? Hur sköter du felhanteringen m.m.
* Klientsida: Hur fungerar din applikation på klientsidan. Beskriv på liknande sätt som serversidan.
* Egenreflektion kring projektet: Här tar du upp hur projektet har gått. Vilka eventuella problem har du stött på? Finns det funktioner som du velat implementera men inte hunnit? Hur skulle du vilja jobba vidare med din applikation?
* Risker med din applikation. Reflektera över vilka risker det finns med din applikation; rent tekniskt, säkerhet, etiskt m.m.
* Skriv också om de eventuella delar du anser vara betygshöjande med din applikation. Motivera varför du anser dessa vara betygshöjande.

## Tips
* Använd gärna ramverk, både till klient- och serversidan.
* Dyk upp på handledningspassen om du behöver fråga om något.
* Campus-studenter - *KOM TILL SKOLAN OCH ARBETA HÄR!* Det är enklare att utbyta idéer och tankar vilket förenklar ert arbete.
* Använd diskussionsforumet för att diskutera med varandra
* Börja på rapporten tidigt för att kontinuerligt hålla den uppdaterad

