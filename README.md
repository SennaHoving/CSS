# CSS 
## Week 1
Maak een digitale 3d rubiks cube. Voor de benodigde css technieken die ik hierbij denk nodig te hebben zijn: 
- 3D transform
- Perspective
- Rotate
- En misschien custom properties? 

De grootste challenge voor deze opdarcht light denk bij het zo dynamisch mogelijk maken van de rubiks. Ik denk dat het opzetten van de rubiks nog redelijk makkelijk is, maar om dan vervolgens de draaien uit te werken is de grootste uitdaging.  


### wo 18/02
vandaag begonnen met de kickoff introductie opdracht voor css. Met het team ingelezen over de selector `:has()`, vervolgens hiervoor de darkmode en anchor links gemaakt. 

In de ochtend ben ik bezig geweest met de kickoff en daarna het het inlezen over de selector. De middag ben ik ongeveer 15 minuten bezig geweest met de dark mode, en verder aan de anchor links en de presentatie. 

Ik heb geleerd over de `:has()` selector, en de features die daar bij horen, dus of `:is()` en `:where()` selectoren en de targets. 

Morgen de presentatie geven en dan kickoff eindproject css. 

### do 19/02
Checkout met Kerr
Vandaag presentatie over :has(), en daarna kickoff opdrach css. Begonnen aan de eindopdracht, gekeken naar nodige technieken en uberhoudt hoe 3d werkt in css.

Presentateis gegeven in de ochtend, duurde tot 12:00. Vervolgens de kickoff voor het eindproject, en daarna gelezen over de mogelijke technieken en hoe ik zou moeten beginnen. En uiteindelijke nog de weekly geek om 16:00. 

Bij de introductie presentatie heb ik over verschillende nieuwe css functies geleerd, de functies die voor mij vooral nieuw en interresant waren waren: containers, scrollen en anchors. En ook vandaag veel geleerd over hoe perspective precies werkt in css, en hoe dat ook werkt in combinatie met rotates.  

Morgen verder voorbereiden van de rubiks opdracht, misschien schetsen maken en de weekly checkout. 

### feedback 20/03
Voor deze feedback session vroeg ik mij vooral af of het echt mogelijk is om een volledige dynamische rubiks te maken. Dat is dus eigenlijk niet echt mogelijk / haalbaar, om een beetje een idee te geven was de verste tot 7 draaien gekomen. Dit gaf mij iniedergeval een beter idee van hoe ik het aan wou pakken. 

Verder had ik ook [deze bron](https://miocene.io/post/3d-cube-with-css/) gevonden voor het maken van een 3d kubus in css, alleen zou [deze bron](https://css-tricks.com/css-in-3d-learning-to-think-in-cubes-instead-of-boxes/) van Jhey Tompkins minder verwarrend zijn / worden. 

Ook heb ik het hierbij nog gehad over de form van de opdracht. En dat je meer dingen kan doen dan alleen het traditioneel uit te werken. Zo is er een voorbeeld laten zijn van een soort rubiks met een hypnose effect over de zijkanten, of een voorbeeld over de algoritmes van een rubiks.

Aan het einde van hierbij kwam ook nog naar voren dat het hetzelfde werkt om een 2x2 uit te werken. En dit bracht mij op het idee om voor mijn concept de verschillende algoritmes uit te werken van een 2x2x2, dit zijn er volgensmij namelijk maar 13 in totaal. 

<!-- misschien nog een schets?  -->

## Week 2 
### wo 04/03 
Checkout met Lisa
Vandaag ben ik begonnen met maken van een enkele kubus, waarbij het met de bron best goed te doen was. Vervolgens heb ik daar 8 blokjes van gemaakt en die goed om het midden geplaatst. En als laatste nog één kant gedraaid.  

In de ochtend was er een weekly geek, en vervolgens ook nog in de ochtend de eerste kubus in elkaar kunnen zetten. Vervolgens grootendeels van de middag de 8 blokjse naast elkaar geplaatst, en op het laatst nog de draai animatie toegevoegd.

Vandaag veel geleerd over transform en translate3D, hoe het werkt en dat je er mee kan roteren, positioneren en wat er eigenlijk allemaal mee mogelijk is. Dat bij de translate het ook uitmaakt of je de rotates voor of na te positionering uitvoert, en dat je hiermee wel of niet om het centrale anchor punt kunt draaien. Ook nog over custom `@property` waar je je eigen properties kunt aanmaken wat erg handig is voor keyframes.

Morgen aan de slag met de 2de draai, en als dat lukt nog verder. 

### do 05/03 
Checkout met Alisha
Vandaag verder gegaan met de tweede turn, hier heb ik vrij lang bij vast gezeten omdat ik alle 4 de blokjes hetzelfde wou animeren. Maar uiteindelijk de keyframes opgesplits en tot bijna 3 draaien gekomen. En workshop layouts gevolgd, die opzicht wel interresant was, maar sommige dingen wist ik al en toch niet super aansluitend op deze opdracht. 

In de ochtend een presentatie, daarna verder gewerkt aan de 2de draai. Toen in het begin van de middag een workshop over layouts, grid, flex, flex grow. 2de draai afgemaakt, begonnen aan 3de draai. 

Vandaag geleerd over flex grow en de prioriteiten van selectoren in de workshop. En niet nieuws over rotates, maar rotates zijn na vandaag wel een stuk logischer geworden. 

Morgen feedback gesprek, kijken naar hoe nu verder, wil ik nog meer draaien uitwerken of iets anders? 

### Feedback 06/03
De code werkt nu als volgd met apparte keyframes voor alle individuele blokjes: 
```
@keyframes c1 {
    0% {
        --rotateY: 0deg; 
    } to {
    } 33% {
        --rotateY: 90deg; 
        --rotateX: 0deg;
    } 66% {
        --rotateY: 90deg; 
        --rotateX: 90deg;
        --rotateZ: 0deg;
    } 100% {
        --rotateZ: 90deg;
        --rotateY: 0deg; 
        --rotateX: 0deg;
    }
}
```

En met deze variabelen verandert de transform van de 8 blokjes: 
```
body > div > div:nth-child(n) {
    transform: var(--translate) rotateX(var(--rotateX)) rotateY(var(--rotateY)) rotateZ(var(--rotateZ)) translate3d(calc(var(--offset-x) * var(--position)), calc(var(--offset-y) * var(--position)), calc(var(--offset-z) * var(--position)));
}
```

Screenshot kubus derde draai: 
![kubus derde draai](/screenshots/week2.png)

Verder is het is het voor nu niet heel anders om nog meer draaien uit te werken, en is het misschien nuttiger / leuker om te kijken naar verschillende manieren om de kubus te stylen (hypno voorbeeld). En verder is het ook nog goed om te kijken naar de overall criteria.  


## Week 3
### 11/03
Checkout met Jacco
Vandaag zat ik een beetje vast op het concept en waar ik naartoe wou. Het eerste concept van de 13 verschillende algoritmes van de 2x2x2 uitwerken voelt niet als het meest nuttige. Of aan de hand van de feedback van vorige week, nu verder te focussen op de styling. Maar uiteindelijk ben ik toch nog net iets verder gegaan met het draaien om een loopje te kunnen maken. Hierbij was het plan om het volgende algoritme uit te werken: `R U F L D B B' D' L' F' U' R'`. Dus daarmee ben ik vandaag de heledag bezig geweest. Hiervoor moest uiteindelijk een tweede zelfde rotate toevoegen aan de transform van een cube, wat ervoor zorgte dat ik niet meer de variabelen kon gebruiken, en hierdoor alles moest veranderen naar de transforms binnen de keyframes. 

Eigenlijk de heledag bezig geweest met het uitwerken van het bovenstaande algoritme. 

geleerd dat je dus dubbel kan roteren in een tranform / translate3D, en dat keyframes de begin en eindpositie moeten kunnen berekenen om het te kunnen animeren. 

Ik ben vandaag tot de 8ste draai gekomen, dus morgen de resteren daarien maken en daarnaa kijken naar een effect om toe te voegen aan de kubus. 

### 12/03 
Checkout met Nienke
Vandaag heb ik de animatie loop afgerond. In de ochtend kwam de container queries naar boven, wat mij op het idee bracht op een soort hyper cube te maken. 

Kickoff over css wiskunde, vervolgens de rest van de ochtend de animatie afgerond. En daarna de rest van de middag ingelezen over container queries en container style queries, en daar begonnen met het maken van de hypercube eerst in een enkele apparte kubus. 

Vandaag veel geleerd over de wiskunde binnen css, en dat het vooral goed is om bewust te zijn van wat er is, en weten wat er mogelijk is met de wiskunde binnen css. En daarnaast ook veel over container queries, dat de container queries eigenlijk een waarde is binnen de parent container. Het werkt het zelfde als viewport height / width, alleen dan de parent container als max in plaats van de viewport. Wat denk opzich wel nuttig is, alleen binnen dit project waarbij een kubus altijd vierkant is, komt de container queries altijd op hetzelfde neer als dat je percentages gebruikt. 

Morgen feedback gesprek, vragen naar randvoorwaarden container queries. 

### Feedback 13/03
Gekeken naar randvoorwaarden, dus ik heb container querie styles gebruikt voor de theming: 
```
@container style(--theme: base) {
}

@container style(--theme: hyper) {
    body > div > div > div:nth-child(n) {
        background-color: transparent; 
    }

    body > div > div > div::before {
        content: ""; 
        display: block; 
        width: 0cqw;
        height: 0cqh;
        border: 5px red solid;
        position: absolute;
        --position: -45px; 
        top: 50%; 
        left: 50%; 
        transform: translate(-50%, -50%) translateZ(var(--position)); 
        animation: hyper 5s infinite linear; 
    }

    body > div > div > div:is(:nth-of-type(2), :nth-of-type(4), :nth-of-type(6))::before {
        --position: 45px; 
    }
}
``` 

En heb gekeken naar css nesting, bijvoorbeeld voor het plaatsen van de individuele blokjes: 
``` 
body > div > div {
    --height: 100px; 
    --width: 100px; 
    --depth: 100px; 
    --position: calc(100px + 10px);  
    --translate: translate(-50%, -50%);
    --rotateDeg: 0deg; 
    height: var(--height);
    width: var(--width);
    position: absolute; 
    transform-style: preserve-3d;

    &:nth-of-type(1) {
        --offset-x: -0.5;
        --offset-y: -0.5;
        --offset-z: 0.5; 
        animation: c1 15s infinite; 
        opacity: 1  ;
    }

    &:nth-of-type(2) {
        --offset-x: 0.5;
        --offset-y: -0.5;
        --offset-z: 0.5; 
        animation: c2 15s infinite; 
        opacity: 1  ;
    }
}
```

Kubus met algoritme: 
![kubus met algoritme](/screenshots/week3-base.png)

Enekele kubus met hyper cube concept: 
![Enkele hyper kubus](/screenshots/week3-hyper.png)

Verder kwam hierbij nog uit dat de titel nog belangrijks was, en interactie toe te voegen.  

## Week 4
### 18/03
Checkout met Nienke
Vandaag ben ik begonnen met het toevoegen van de titel, waarbij het idee was om de letters random te laten draaien. Alleen omdat je random niet kan gebruiken binnen animaties, en alleen op safari werkt moest dit ook met keyframes, en dan so random mogelijk.

Begonnen met het toevoegen van de titel, hier de ochtend mee bezig geweest. Verder de rest van de middag bezig geweest met de readme. 

Geleerd over random, uiteindelijk niet gebruikt. Verder niet heel veel nieuwe dingen vandaag. 

En morgen eindgesprek. 

Huide kubus nu: 
![Huidige kubus](/screenshots/week4-base.png)

Met de hyper layout: 
![Hyper kubus](/screenshots/week4-hyper.png)

### Reflectie 
Voor het uiteindelijk resultaat ben ik best tevreden, vooral aan het begin had ik geen idee hoe ik dit tot werking kon maken en het wel gelukt. Ik denk dat ik toen ik eenmaal beginnen was, wat bronnen had gelezen over transform en perspective dat het in elkaar zetten een enkele kubus erg mee viel. En daarna het draaien van de rubiks viel in het begin wel mee, maar toe ik eenmaal in de derde week was begonnen met het uitwerken van het algoritme, waarvoor ik alle apparte kubussen los animerde was het toch wel uitdagend en anders denken om de draaien te laten werken. 

Met het uiteindelijk resultaat ben ik denk het meest trots op de uiteindelijke keyframes. Dit was toch wel even puzzelen om goed te laten werken, maar is uiteindelijk goed gelukt: 
```
@keyframes c2 {
    ...
    33.333% {
        transform: var(--translate) rotateX(90deg) rotateY(90deg) rotateZ(90deg) translate3d(calc(var(--offset-x) * var(--position)), calc(var(--offset-y) * var(--position)), calc(var(--offset-z) * var(--position)));
    }
    41.666% {
        transform: var(--translate) rotateX(90deg) rotateY(90deg) rotateZ(90deg) rotateY(-90deg) translate3d(calc(var(--offset-x) * var(--position)), calc(var(--offset-y) * var(--position)), calc(var(--offset-z) * var(--position)));
    }
    50% {
        transform: var(--translate) rotateX(90deg) rotateY(90deg) rotateZ(90deg) rotateY(-90deg) rotateZ(-90deg) translate3d(calc(var(--offset-x) * var(--position)), calc(var(--offset-y) * var(--position)), calc(var(--offset-z) * var(--position)));
    }
    ...
}
```

En ik ben ook trots op de styling van het hyper effect, ik denk dat dat uiteindelijk ook een goed gelukt experiment is geworden. Het is misschien niet de meest complexe code geweest, maar creeërde dat wel het effect waar ik een beetje naar opzoek was: 
```
    body > div > div > div::before {
        content: ""; 
        display: block; 
        width: 0cqw;
        height: 0cqh;
        border: 5px red solid;
        position: absolute;
        --position: -45px; 
        top: 50%; 
        left: 50%; 
        transform: translate(-50%, -50%) translateZ(var(--position)); 
        animation: hyper 5s infinite linear; 
    }

    body > div > div > div:is(:nth-of-type(2), :nth-of-type(4), :nth-of-type(6))::before {
        --position: 45px; 
    }
```

Het enige dat echt nog niet is gelukt is de soort 'squeez' in de 6de en 7de rotate eruit te halen. Bij deze draai stack ik de rotates en draait die niet meer over de center maar komt die wel op de juist plaats. Dus in de tijd ben ik hier niet achter gekomen, had ik met meer tijd nog willen fixed. 

Verder zou ik ook nog willen kijken naar de bruikbaarheid van deze css buiten het maken van een rubiks, maar meer hoe ik het ook kan inzetten in een website format. Dus nu ik snap hoe ik bepaalde elementen kan animeren met de transform en rotates, en dat dan implementeren tijdens het maken van wat 'echtere' sites. 

Als laatste vond ik het toepassen van css nesting ook super nuttig. Het is soms nog een beetje zoeken naar wanneer het wel goed is om te gebruiken, en wanneer je er te ver in gaat en het alleen maar onoverzichtelijker maakt. Maar overall is het een super handige techniek die voor mij het schrijven van bepaalde componenten of deelen veel logischer maakt en voor veel meer overzichtelijk zorgt. 

## Bronnen
https://css-tricks.com/almanac/rules/k/keyframes/
https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@property
https://css-tricks.com/css-in-3d-learning-to-think-in-cubes-instead-of-boxes/
https://codepen.io/h20x/pen/YQYrOa
https://stackoverflow.com/questions/4359627/stopping-a-css3-animation-on-last-frame
https://robertcelt95.medium.com/responsive-typography-that-actually-works-beyond-font-size-clamp-acf592b79774
https://chatgpt.com/share/69ba8145-af1c-800a-ac1b-6ccb9e8ceeff 