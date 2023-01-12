# pPublik Webbplats till BrunchClub :bread: :watermelon: :tea:
 
 ## Grundstruktur
Till uppgfiten har en grundstruktur för webbutveckling skapats med hjälp av Gulp. Strukturen består av en mapp med namn "src" där projektets arbetsfiler ligger. 
Publicerade filer ligger i en mapp med namn "pub". Dessa filer är minifierade och/eller konkatenerade. 

I strukturen sker en automatisk koll om någon arbetsfil ändras och om detta sker så uppdateras även den publicerade filen. Vid ändring av en fil signaleras också till webbläsaren som då uppdateras automatiskt. 
    
 ### De paket som strukturen består av är följande 
    - Browser Sync
    - Gulp - Clean CSS
    - Gulp - Concat
    - Gulp - uglify - es
    - Gulp - sass
    - Gulp - sourcemaps
    - Gulp - browserSync

Paketen avänds i de olika tasks som skapats i abetsmiljöns gulp-fil.

## SASS

Arbetsfilerna för Sass är uppdelade enligt följande: 

+ ### _base.scss : 
Anger grunder såsom font och färg 
+ ### _components.scss : 
Sidan olika komponenter styleas
+ ### main.scss : 
Importeras de två ovanstående filerna

Filerna konverteras till CSS och konkateneras till en enda fil i pub-mappen med namn main.css, detta med hjälp av concat och cleanCSS.


## Javascript 

På den publika webbplatsen används Javascript för att hämta lagrad information från databasen och därefter skiva ut dessa till skärmen. 
Koden har delats upp i två filer: 

+ #### booking.js : 
Gör anrop till API för bokningar. Lagrar bokningar med POST
+ ### main.js : 
Gör anrop till API för menyn. Hämtar lagrade rätter i menyn och skriver ut dessa till skärmen.


De två JS-filerna slås inte ihop i pub-mappen. Däremot minifieras de båda filerna med gulp - uglify.

 ## Länkt till webbplats
https://studenter.miun.se/~sagi1700/writeable/brunchclubwebsite/index.html

