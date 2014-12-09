##Projekt - Webbteknik II

###Inledning
Som avslutning av denna kurs ska Du skriva en komplett applikation som ska sammanfatta vad du lärt dig under kursens gång samt förhoppningsvis tillskansa dig ny kunskap och ny erfarenhet kring hur man utvecklar kompletta webbapplikationer mot befintliga webb-API:r. Projektet är också tänkt att ge dig kunskaper om nya och HTML5-relaterade API:er för JavaScript-klienter samt att bygga applikation med tanke på hur den ska bete sig även ifall den inte har någon uppkoppling (diskuteras i samband med "offline-first")

Vår förhoppning är att du i detta moment utvecklar en egen applikationsidé och som du utan problem skulle kunna visa upp för tilltänkta arbetsgivare när du söker jobb. Det är också klart önskvärt att du låter din egen nyfikenhet och kreativitet som webbutvecklare komma fram. 

##En mashup-applikation
Tanken är att du ska skapa en egen mashup-applikation utifrån en egen idé. Vad applikationen ska hanterar för slags data är upp till dig och din idé. Försök hitta en idé du tycker är intressant och brinner för då arbetet kommer gå betydligt lättare.

Du börjar med att beskriva din idé i ett kort dokument (i md-format) som du publicerar på ditt github-repo som hör till kursen.
Gör detta så fort som möjligt men senast **klockan 13:00, 16:e december**. Skulle kursledningen ha några synpunkter på ditt projekt meddelas det via GitHub senast 17:e december.

Slutlig deadline på projektet då allt ska vara inskickat till kursledning är **15:e januari klockan 13:00**

##Krav på applikation för godkänt (betyg 3)
Vi kommer alltså ha en fri hållning till vad din applikation behandlar för data och du är fri att själv välja tekniken du vill använda men det finns ett antal krav vi kommer ha på applikatinen för godkänt (betyg 3) på projektet.

* Bygg en applikation som hämtar data från *minst två stycken externa API:er*. dessa ska sammankopplas på ett dynamiskt sätt i din applikationskod.

* I din applikation ska du i möjligaste mån utgå från begreppet "offline-first" dvs. applikationen ska fungera på ett bra sätt även om man inte har någon uppkoppling. Det är inte säkert att din applikation helt kan anpassas efter dessa arkitektoriska tankar men avkall från detta bör i så fall återspeglas som en reflektion i din rapport.

* Applikationen ska ha en OAuth-koppling d.v.s. användaren ska kunna logga in via en tredjepartstjänst. Har du ingen anning om vad du ska använda en inloggning till i din applikation så skriv en inställningssida för användaren eller utnyttja de resurser tjänsten som du loggar in emot erbjuder.

* Du ska implementera felhantering till din applikation så att användaren av applikationen blir medveten om t.ex. något av API:erna går ner.

* Applikationen ska vara publicerad och körbar på en publik URL.

* Applikationen ska vara genomarbetad med avseende på design, användarvänlighet, säkerhet och optimering. Designen ska kännas proffsig och genomarbetad. Att inte arbeta med designen är INTE samma sak som "enkel och stilren". 

* Din applikation ska självklart fungera utan buggar eller ohanterade fel. Användaren ska hela tidens veta vad som pågår i applikationen. Krashar din applikation och ej har god felhanteringen underkänns den.

* Din applikation ska eftersträva hög prestanda och bör därför cacha data både på front- och backend. Beskriv din cachningsstrategi i din rapport, Motivera eventuella undantag från detta i din rapport.

* Du redovisar din applikation genom att göra en muntlig och skriftlig redovisning. Rapporten ska tydligt beskriva hur arbetet gått till, vilka tekniker du använt, de reflektioner du gjort samt vad du lärt dig under arbetet (se nedan). Rapporten ska finns på github och vara skriven i md-format.

* Den muntliga redovisningen ska vara inspelad som film. Du ska under minst tre och max fem minuter sälja in din applikation och visa hur den fungerar och vad man kan göra med den. Du väljer själv om du vill publicera den på youtube, vimeo eller som en vanlig mp4-fil. Du redovisar en URL som pekar på din presentationsfilm i ditt repositories readme - där ska också en länk till rapporten och en publika URL:en finnas. Filmerna kommer sedan visas upp på kurshemsidan så att ni kan se varandras applikationer.

* All kod och dokumentation ska nås via ditt github-repo

##Eventuellt betygshöjande funktioner (betyg 4 och 5)

För högre betyg än (G/3) ska applikationen redovisas innan utsatt leveransdatum. Se kurshemsida.

Vi ser såklart gärna att ni utmanar er själva och testar nya grepp och tekniker vilket kan ses som betygshöjande. Här är några förslag som skulle kunna vara betygshöjande funktioner i din applikation. Ju fler som implementeras på ett tillfredsställande sätt ökar chansen till ett högre betyg. Stor del av bedömningen sker också på de reflektioner ni gör i er rapport som påvisar den kunskap och det djup i ämnet ni besitter.

* Inkludera flera relevanta API:er och höj din applikations funktionalitet ytterligare
* Applikationens design ska vara responsiv alltså anpassa sig till enhetens skärmstorlek.
* Inkludera HTML5-relaterade API:er så som geolocation, web workers, web sockets m.m.
* Se bedömningsmatrisen nedan för ytterligare information

## Rapporten
Den skriftliga projektrapporten du lämnar in ska innehålla följande:

* **Inledning** där du kort beskriver vad du gjort och bakgrunden till din applikation. Finns det liknande applikationer redan?
* Inkludera en **schematisk bild över applikationens beståndsdelar** så att läsaren har enklare att förstå applikationens dataflöde.
* **Serversida**: Beskriv hur din applikation fungerar på serversidan. Beskriv funktionaliteten och hur den är uppbyggd. Vald teknik/programmeringsspråk/ramverk? Hur fungerar cachningen? Hur sköter du felhanteringen m.m.
* **Klientsida**: Hur fungerar din applikation på klientsidan. Beskriv på liknande sätt som serversidan.
* **Säkerhet och prestandaoptimering** - Hur har du funderat kring säkerhet och prestanda och vilken teori har du kopplat detta emot.
* **Offline-first**: Hur har du tänkt kring offline-first?
* **Egen reflektion kring projektet**: Här tar du upp hur projektet har gått. Vilka eventuella problem har du stött på? Finns det funktioner som du velat implementera men inte hunnit? Hur skulle du vilja jobba vidare med din applikation?
* **Risker med din applikation**: Reflektera över vilka risker det finns med din applikation; rent tekniskt, säkerhet, etiskt m.m.
* Skriv också om de eventuella delar **du anser vara betygshöjande med din applikation**. Motivera varför du anser dessa vara betygshöjande.

##Examination
Din applikation kommer bedömas av kursledningen främst på följande grunder:

### Hur väl fungerar din applikation. Buggar, användbarhet.
* U - Applikationen innehåller lösningar som inte fungerar
* 3 - Applikationen fungerar utan buggar eller andra konstigheter
* 4 - Som 3 samt; Applikationen är stabil och känns genomtänkt med avseende på funktioner och design. Applikationen är designad så att den fungerar på olika typer av enheter.
* 5 - Som 4 samt; Applikationen känns proffsig och så gott som klar för produktion. 

###Kreativitet och nyfikenhet
* U - Applikationen uppfyller inte de grundkrav som finns och är inlämnad trots att den inte är färdig.
* 3 - Studenten har implementerat grundkraven och använt sig av den teori som tagits upp i kursen kring detta
* 4, 5 - Som 3 samt; Studenten har genom implementationen och rapporten visat prov på att ny kunskap och teori har införskaffats

### Funktionalitet och övergripande intryck av applikationen
* U - Applikationen uppfyller inte de grundkrav som finns
* 3 - Applikationen uppfyller de grundkrav som finns men inte mycket mer
* 4 - Applikationen har en genomtänkt funktionalitet som är lätt att använda och förstå
* 5 - Applikationen har en högre grad genomtänkt funktionalitet som känns klar för leverans.

### Offline-first
* U - Ingen reflektion eller implemntation kring "offline-first"
* 3 - Viss implementation av de terorier kring offline-first som tagits upp i kursen
* 4 - Som 3 samt; tydlig reflektion i rapporten kring hur taktiken kring "offline-first" har implementerats.
* 5 - Som 4 samt; reflekterar kring teorier kring offline-first, sätter dessa emot varandra och kan i rapporten på ett tydligt sätt argumentera för sina val.

### Prestandaoptimering och säkerhet
* U - Applikationen har inte optimerats på något sätt och/eller har uppenbara säkerhetshål
* 3 - Applikationen har optimerats och är fri från uppenbara säkerhetshål
* 4 - Som 3 samt; rapporten visar på studentens arbete och kunskap kring de teorier kring optimering och säkerhet som implementerats i applikationen
* 5 - Som 4 samt; reflekterar kring dessa teorier, sätter dessa emot varandra och kan på ett tydligt sätt argumentera för sina val i rapporten

### Kvalité på rapporten
* U - Rapporten har dålig struktur/dåligt skriftligt språk med vanlig förekommst av grammatik- och stavfel. Rapporten är inlämnad i fel format. Rapporten är pladdrig och innehåller inte relevanta saker.
* 3 - Rapporten ger en godtagbar bild över applikationen och arbetets gång med viss reflektion och hänvisning till teorin
* 4 - Som 3 samt att rapporten visar studentens kunskap genom tydlig koppling till teori. Referenser till teorierna ska anges i rapporten.
* 5 - Som 4 samt; Studenten reflekterar kring olika teorier, sätter dessa emot varandra och kan på ett tydligt sätt argumentera för sina val i rapporten.

### Kod
* U - Koden är ostrukturerad, oindenterad och saknar helt kommentarer
* 3 - Koden är har en tydlig struktur och är delvis kommenterad
* 4, 5 - Som 3 samt; koden är av god kvalité och applikationen känns skalbar och enkel att bygga vidare på. Kommentarer som förenklar kodläsning. Man kan tydligt se hur koden vuxit fram via täta commits på GitHub. Applikationen ska vara fri från återupprepad kod (DRY).

### Den inspelade presentationen 
* U - Ingen inspelad video finns eller går inte att spela upp i en modern webbläsare
* 3 - Publicerad video enligt instruktioner och överstämmer med den publicerade applikationen
* 4, 5 - Som 3 samt; Videoinspelningen ger en tydlig bild av hur applikationen fungerar och vilka funktioner som den har.

### Uppfyllande av leveransdatum. 
* U - Arbetet lämnas in ofullständigt
* 3: Fullständigt arbete lämnas in fast efter fastslagen deadline
* 4, 5: Arbetet lämnas in till fastslagen deadline


## Övrigt
* Du är fri att använda ramverk, både till klient- och serversidan. Val av teknik ska tydligt framgå i rapporten liksom motivering till varför.
* Använd diskussionsforumet
* Börja på rapporten tidigt för att kontinuerligt hålla den uppdaterad
* Gör kontinuerligt commits.
* Testa tidigt att din applikation fungerar på en extern server. testa inte detta dagen innan leverans.
* Testa din kod...testa din applikation. Leverera inte något som inte fungerar!

