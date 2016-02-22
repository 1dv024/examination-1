## Skarp beskrivande statistik

>###OBS! OBS! OBS!
- Detta är en __obligatorisk__ och __examinerande__ uppgift som __du ska lösa helt på egen hand__.
- Du måste göra __regelbundna "commits" och "pushes"__ av koden till ditt repositorium för uppgiften för att kursledningen ska kunna följa ditt arbetet med uppgiften.
- Du ska kunna förklara alla konstruktioner och satser som din lösning av uppgiften innehåller.  

Beskrivande statistik (eller _deskriptiv statistik_; eng. "_descriptive statistics_") är ett sätt att reducera stora datamängder för att presentera en sammanfattning av datamängden.

Din uppgift är att skriva en konsolapplikation som tar en JSON-fil med heltal som argument och sammanfattar datamängden i filen och ger lättöverskådlig vy av datat.

Applikationen ska innehålla en statisk metod, `GetDescriptiveResults`, som reducera datamängden i form av en samling med tal (värden av typen `int`) som skickas till metoden och returnera ett anonymt objekt med egenskaper för max- och minvärden, variationsbredd, medelvärde, median samt typvärde (som kan vara en samling med värden), [http://www.matteboken.se/lektioner/matte-1/sannolikhet-och-statistik/medelvarde-median-typvarde-och-variationsbredd](http://www.matteboken.se/lektioner/matte-1/sannolikhet-och-statistik/medelvarde-median-typvarde-och-variationsbredd).

- Applikationen får endast innehålla statiska klasser och medlemmar.

- Anropas applikation med en JSON-fil innehållande `[ 4, 8, 2, 4, 5 ]` ska applikationen presnetera sammanfattningen `{ max: 8, mean: 4.6, median: 4, min: 2, mode: 4, range: 6 }`.

- Anropas applikation med en JSON-fil innehållande `[ 4, 2, 6, 1, 3, 7, 5, 3, 7 ]` ska applikationen presentera sammanfattningen  `{ max: 7, mean: 4.22222222222222, median: 4, min: 1, mode: 3, 7, range: 6  }`.

- Anropas applikation med en JSON-fil innehållande `[ 5, 1, 1, 1, 3, -2, 2, 5, 7, 4, 5, 16 ]` ska applikationen presentera sammanfattningen  `{ max: 16, mean: 4, median: 3.5, min: -2, mode: 1, 5, range: 18  }`.

- Anropas applikation med JSON-filen data.json ska applikationen presnetera sammanfattningen  `{ max: 378, mean: 167.3088, median: 165, min: -42, mode: 31, 87, 228, range: 420  }`.

- Anropas den statiska metoden `GetDescriptiveResults` med argumentet `null`, elelr ett argument som är en tom samling, ska ett undantag av typen `ApplicationException` kastas med meddelandet `"No data to analyze."`.

- Argumentet får inte modifieras på något sätt av den statiska metoden `GetDescriptiveResults`, d.v.s. samlingen som skickas som argument till metoden ska vara opåverkad efter att metoden returnerat.  

> max (maxvärde), mean (medelvärde), median (median), min (minvärde), mode (typvärde), range (variationsbredd)

Skriva inte all kod som krävs för att lösa problemet i en enda statisk klass och/eller metod. Se till att dela upp lösning av problemet i lämpliga statiska klasser och metoder du själv skapar (_"separation of concern"_). Undvik att upprepa kod och bryt därför inte mot principen DRY (_"don't repeat yourself"_).

Vill du verkligen utmana dig själv kan du välja att implementera saknade aggregatsmetoder som så kallade utökningsmetoder (eng. _"extension methods"_).
