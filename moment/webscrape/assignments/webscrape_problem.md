##Problem
I denna uppgift ska du skriva ett automatiserat script som skrapar data på en webbplats.
Du kan i denna uppgift vara kreativ och välja en egen webbplats att skrapa på information (var dock noga med att vara en god skrapare och att uppfylla de generella kraven)
För er utan fantasi finns en färdig webbplats som har samlat ett antal matproducenter. 
Sidan består av en ett inloggningsformulär som leder till en sida med en lista med producenter. Genom att följa dessa länkar via ditt automatiserade skript ska du skrapa alla de undersidor som finns på information och spara i valfri datalagring.

Ditt script ska alltså automatiskt utgå från en URL, automatiskt göra en inloggning och automatiskt följa länkar.

URL:en som inloggningsformuläret finns på är:
[http://vhost3.lnu.se:20080/~1dv449/scrape/](http://vhost3.lnu.se:20080/~1dv449/scrape/)
Användarnamnet är: admin
Lösenordet är: admin

Du är helt fri att välja tekniker, programmeringsspråk och servermiljö för att lösa problemet. Koden ska dock redovisas via github.

##Krav
1. Scriptet ska vara helt automatiserat och utgå den nämnda URL:en
2. Informationen som ska skrapas är: 
	* Producentens namn
	* id till producenten (finns i länken)
	* url:en till producentens hemsida
	* producentens ort
	
3. Din kod ska kontinuerligt commitas upp på github och den slutliga koden ska ligga där tills kursen avslutas.
4. Din data ska sparas undan permanent i en datalagring, på vilket sätt väljer du själv. Du ska spara all skrapad information om producenterna samt även eventuella resurser som inte finns att få tag på. 
	* Döda länkar (404) 
	* Information som eventuellt saknas på producentsidorna t.ex. bilder, ort e.c.t.
5. Gör en snygg och tydlig presentation (från datalagringen) i HTML (ska kommas åt via en URL)
6. Skapa en fil med din reflektioner (se nedan)
7. Din kod ska kontinuerligt pushas upp till github så man kan följa din kodutveckling.
8. När uppgiften redovisas ska man ha gjort en release (tag) på sitt repositorie

##Reflektion
Du ska i ditt repositorie skapa en fil i [markdown-format](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) där du reflekterar över följande saker:

1. Ni är fria att välja sätt att läsa in och extrahera data ur webbsidorna. Motivera ditt val!
2. Vad finns det för risker med applikationer som innefattar automatisk skrapning av webbsidor? Nämn minst tre stycken!
3. Tänk dig att du skulle skrapa en sida gjord i ASP.NET WebForms. Vad för extra problem kan man få då?
4. Vad var svårast med denna uppgift?
5. Vad har du lärt dig av denna uppgift? 


##Extrauppgifter
För er som satsar på högre betyg i kursen finns här ett par extra funktioner för din applikation.

1. De bilder man kan skrapa ska sparas ner lokalt i en egen mapp
2. Utöka datalagringen med information om hur många gånger ditt skript har skrapat en producent och en timestamp om senaste gången informationen skrapades.


##Redovisning
Laborationen redovisas genom att göra en realease med din kod på ditt github-repositorie samt genom en muntlig redovisning på schemalagt redovisningstillfälle.


##Tips
Studera de demonstrationsfilmer som finns på kurshemsidan.

#### Gör en release på din kod
När du genomfört och vill examinera din applikation och för att du senare enkelt ska kunna gå tillbaka och se hur koden såg ut när genomfört laboration 1 ska du göra något som kallas för en tag eller release. 

1. Logga in på GitHub och gå till repositoriet för laborationen.
2. Kontrollera att dina senaste ändringar finns tillgängliga på GitHub.
3. Klicka på "releases" ovanför fillistningen.
4. Välj att skapa en ny release.
5. Se till att "Tag version" blir `L01` (Ludvig, nolla, etta).
Titel och description fyller du i som du själv vill.
![GitHub Release][github-release]
6. Publicera releasen

Se till att i fortsättningen göra ovanstående för samtliga laborationer (tag: L02, L03 etc.) när de är genomförda. Du kan nu fortsätta att arbete på laboration 2 och du har alltid en genväg för att gå tillbaka och se hur laboration 1 såg ut innan förändringarna som laboration 2 innebär.
Kursledningen kan också på ett enkelt sätt överblicka klassens progression på de olika laborationerna.

[github-release]: https://github.com/1ik415/Kursmaterial/raw/master/Laborationer/pics/github-release.png





 
