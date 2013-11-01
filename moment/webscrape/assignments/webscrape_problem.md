##Problem
I denna uppgift ska du skriva ett automatiserat script som skrapar data på en webbplats.
Du kan i denna uppgift vara kreativ och välja en egen webbplats att skrapa på information (var dock noga med att vara en god skrapare och att uppfylla de generella kraven)
För er utan fantasi finns en färdig webbplats som har samlat ett antal matproducenter. 
Sidan består av en ett inloggningsformulär som leder till en sida med en lista med producenter. Genom att följa dessa länkar via ditt automatiserade skript ska du skrapa alla de undersidor som finns på information och spara i valfri datalagring.

Ditt script ska alltså automatiskt utgå från en URL, automatiskt göra en inloggning och automatiskt följa länkar.

URL:en som inloggningsformuläret finns på är:


Du är helt fri att välja tekniker, programmeringsspråk och servermiljö.

##Krav
1. Scriptet ska vara helt automatiserat och utgå den nämnda URL:en
2. Informationen som ska skrapas är: 
	* Producentens namn
	* id till producenten (finns i länken)
	* url:en till producentens hemsida
	* producentens ort
	
3. Din kod ska kontinuerligt commitas upp på github
4. Din data ska sparas undan permanent i en datalagring, på vilket sätt väljer du själv. Du ska spara all skrapad information om producenterna samt även eventuella resurser som inte finns att få tag på. 
	* Döda länkar (404) 
	* Information som eventuellt saknas på producentsidorna t.ex. bilder, ort e.c.t.
5. Gör en presentation (från datalagringen) i HTML ex)
	ID|Namn|Ort|Hemsida|BildURL|
	8|Bredervall|Kalmar|http://www.dn.se|http://www.dn.se/secure/images/bild.jpg
6. Skapa en fil med din reflektion

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
Tänk på att det är ett skript du skriver och inte en hel webbapplikationsarkitektur.




 
