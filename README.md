// Voorbeeld van uitleg over basisprincipes van JavaScript

// Variabelen
var naam = 'John';
let leeftijdd = 25;
const PI = 3.14;

// Gegevenstypen
var naam = 'John';
var leeftijd = 25;
var isStudent = true;
var favorieteKleuren = ['rood', 'blauw', 'groen'];
var persoon = { naam: 'John', leeftijd: 25 };

var stringVoorbeeld = "Dit is een voorbeeld van een string.";
var nummerVoorbeeld = 42;
var booleanVoorbeeld = true;
var arrayVoorbeeld = [1, 2, 3, 4, 5];
var objectVoorbeeld = { naam: "John", leeftijd: 30, stad: "Amsterdam" };
var nullVoorbeeld = null;
var undefinedVoorbeeld;
var symbolVoorbeeld = Symbol("uniek");
var functieVoorbeeld = function () {
    // Code die wordt uitgevoerd wanneer de functie wordt aangeroepen
};

// ____________________________________________________________________________

// Uitleg over berekeningen met variabelen

// Variabelen declareren
var getal1 = 5;
var getal2 = 3;

// Optellen
var som = getal1 + getal2;
console.log("Optellen: " + som); // Output: 8

// Aftrekken
var verschil = getal1 - getal2;
console.log("Aftrekken: " + verschil); // Output: 2

// Vermenigvuldigen
var product = getal1 * getal2;
console.log("Vermenigvuldigen: " + product); // Output: 15

// Delen
var quotiënt = getal1 / getal2;
console.log("Delen: " + quotiënt); // Output: 1.6666666666666667

// Modulus (rest)
var rest = getal1 % getal2;
console.log("Modulus (rest): " + rest);     // Output: 2

// Increment en decrement
var getal = 10;
getal++; // Increment met 1
console.log("Increment: " + getal); // Output: 11

getal--; // Decrement met 1
console.log("Decrement: " + getal); // Output: 10

// ____________________________________________________________________________

// uitleg over functies

// Functies
function begroet(naam) {
    console.log('Hallo ' + naam + '!');
}

begroet('John'); // Output: Hallo John!

// Voorwaardelijke verklaringen
var uur = 15;

if (uur < 12) {
    console.log('Goedemorgen!');
} else if (uur < 18) {
    console.log('Goedemiddag!');
} else {
    console.log('Goedenavond!');
}

// ____________________________________________________________________________

// voorbeeld van iteraties

// for-loop
for (var i = 0; i < 5; i++) {
    console.log(i);
}
// Output: 0, 1, 2, 3, 4

// while-loop
var j = 0;
while (j < 5) {
    console.log(j);
    j++;
}
// Output: 0, 1, 2, 3, 4

// do-while-loop
var k = 0;
do {
    console.log(k);
    k++;
} while (k < 5);
// Output: 0, 1, 2, 3, 4

// forEach-methode
var namen = ["Alice", "Bob", "Charlie"];
namen.forEach(function (naam) {
    console.log(naam);
});
// Output: "Alice", "Bob", "Charlie"

//   break in iteratie
for (var i = 0; i < 10; i++) {
    if (i === 5) {
        break;
    }
    console.log(i);
}

//   Wanneer je dit bestand uitvoert, wordt de for-lus gebruikt om de variabele i te verhogen van 0 tot 9.
//   Bij i === 5 wordt het break-statement uitgevoerd en wordt de lus onmiddellijk verlaten.
//   Als gevolg hiervan worden alleen de getallen 0 t/m 4 weergegeven in de console.

// ____________________________________________________________________________

// Voorbeeld van uitleg over arrays in JavaScript

// Array maken
var kleuren = ['rood', 'blauw', 'groen'];
var getallen = [1, 2, 3, 4, 5];
var mix = ['Hallo', 42, true];

// Toegang tot array-elementen
console.log(kleuren[0]); // Output: rood
console.log(kleuren[1]); // Output: blauw
console.log(kleuren[2]); // Output: groen

// Array-lengte
console.log(kleuren.length); // Output: 3

// Array-bewerkingen
kleuren.push('geel'); // Element toevoegen aan het einde van de array
console.log(kleuren); // Output: ['rood', 'blauw', 'groen', 'geel']

kleuren.pop(); // Laatste element verwijderen
console.log(kleuren); // Output: ['rood', 'blauw', 'groen']

kleuren[1] = 'geel'; // Element wijzigen
console.log(kleuren); // Output: ['rood', 'geel', 'groen']

// ____________________________________________________________________________

// Uitleg over objects in JavaScript

// Object maken met objectliteralen
var persoon = {
    naam: "John Doe",
    leeftijd: 30,
    stad: "Amsterdam"
};

// Eigenschappen benaderen met dot-notatie en vierkante haakjes-notatie
console.log(persoon.naam); // Output: "John Doe"
console.log(persoon["leeftijd"]); // Output: 30

// Eigenschappen toevoegen, wijzigen en verwijderen
persoon.email = "john@example.com"; // Eigenschap toevoegen
persoon.leeftijd = 31; // Eigenschap wijzigen
delete persoon.stad; // Eigenschap verwijderen

// Geneste objecten
var auto = {
    merk: "BMW",
    model: "X5",
    eigenaar: {
        naam: "Jane Doe",
        leeftijd: 35
    }
};

console.log(auto.eigenaar.naam); // Output: "Jane Doe"

// Objectmethoden
var rechthoek = {
    breedte: 10,
    hoogte: 5,
    berekenOppervlakte: function () {
        return this.breedte * this.hoogte;
    }
};

console.log(rechthoek.berekenOppervlakte()); // Output: 50

// ____________________________________________________________________________

// voorbeeld van een class

// Definitie van een class genaamd "Persoon"
class Persoon {
    // Constructor-methode voor het initialiseren van objecten
    constructor(naam, leeftijd) {
        this.naam = naam;
        this.leeftijd = leeftijd;
    }

    // Methode voor het begroeten van een persoon
    begroeten() {
        console.log(`Hallo, mijn naam is ${this.naam} en ik ben ${this.leeftijd} jaar oud.`);
    }
}

// Instantiëren van een object van de class "Persoon"
var persoon1 = new Persoon("Alice", 30);

// Gebruik van objectmethoden
persoon1.begroeten(); // Output: Hallo, mijn naam is Alice en ik ben 30 jaar oud.

// ____________________________________________________________________________

// Voorbeeld van gegevens doorsturen via een link in JavaScript

// Voorbeeld 1: Een enkele waarde doorsturen
var naam = 'John';
var leeftijd = 25;

var link1 = 'pagina.html?naam=' + naam + '&leeftijd=' + leeftijd;

// Voorbeeld 2: Een array doorsturen
var kleuren = ['rood', 'blauw', 'groen'];

var link2 = 'pagina.html?kleuren=' + encodeURIComponent(kleuren.join(','));

// Voorbeeld 3: Objectgegevens doorsturen
var persoon = {
    naam: 'John',
    leeftijd: 25,
    stad: 'Amsterdam'
};

var link3 = 'pagina.html?' + Object.entries(persoon).map(([key, value]) => key + '=' + encodeURIComponent(value)).join('&');

// ____________________________________________________________________________

// Voorbeeld van gegevens doorsturen vanuit een formulier in JavaScript

// Event listener voor het formulier
document.getElementById('mijnFormulier').addEventListener('submit', function (event) {
    event.preventDefault(); // Voorkomt dat het formulier wordt verzonden

    // Gegevens ophalen uit het formulier
    var naam = document.getElementById('naam').value;
    var leeftijd = document.getElementById('leeftijd').value;

    // Link samenstellen met gegevens
    var link = 'pagina.html?naam=' + encodeURIComponent(naam) + '&leeftijd=' + encodeURIComponent(leeftijd);

    // Navigeer naar de link
    window.location.href = link;
});

// ____________________________________________________________________________

// Voorbeeld van het ophalen van gegevens uit een URL in JavaScript

// Functie voor het ophalen van een queryparameterwaarde uit een URL
function getQueryParameterValue(url, parameter) {
    parameter = parameter.replace(/[\[\]]/g, '\\$&');
    var regex = new RegExp('[?&]' + parameter + '(=([^&#]*)|&|#|$)');
    var result = regex.exec(url);
    if (!result) return null;
    if (!result[2]) return '';
    return decodeURIComponent(result[2].replace(/\+/g, ' '));
}

// Voorbeeldgebruik
var url = 'pagina.html?naam=John&leeftijd=25';
var naam = getQueryParameterValue(url, 'naam');
var leeftijd = getQueryParameterValue(url, 'leeftijd');

console.log(naam); // Output: John
console.log(leeftijd); // Output: 25

// ____________________________________________________________________________

// Uitleg over document.addEventListener("DOMContentLoaded", function() {})

// De DOMContentLoaded-gebeurtenis
    document.addEventListener("DOMContentLoaded", function() {})
// Deze methode wordt gebruikt om een functie uit te voeren zodra het DOM volledig is geladen en klaar is om te worden gemanipuleerd.
// Het wordt vaak gebruikt om ervoor te zorgen dat JavaScript-code correct wordt uitgevoerd op het juiste moment.

// Voorbeeldgebruik:
document.addEventListener("DOMContentLoaded", function () {
    // Code die wordt uitgevoerd nadat het DOM volledig is geladen

    // Elementen selecteren en manipuleren
    var mijnElement = document.getElementById("mijnElement");
    mijnElement.innerHTML = "DOM is volledig geladen!";
});

// ____________________________________________________________________________

// Uitleg over document.getElementById
var uitleg = `document.getElementById
// Deze methode wordt gebruikt om een DOM-element te selecteren op basis van het ID-attribuut.
// Het retourneert het geselecteerde element als een object.

// Voorbeeldgebruik:
//HTML: <div id="mijnElement">Dit is mijn element</div>
var element = document.getElementById('mijnElement');
console.log(element); // Output: <div id="mijnElement">Dit is mijn element</div>
`;

// Voorbeeld van het wijzigen van de inhoud van een element

// Het wijzigen van de inhoud van een element
var element = document.getElementById('mijnElement');
element.innerHTML = 'Nieuwe inhoud';
console.log(element.innerHTML); // Output: Nieuwe inhoud


// Voorbeeld van het wijzigen van stijlen van een element

// Het wijzigen van stijlen van een element
var element = document.getElementById('mijnElement');
element.style.color = 'red';
element.style.fontSize = '20px';

// ____________________________________________________________________________

// uitleg over gebeurtenissen

// klikgebeurtenis

var button = document.getElementById("myButton");
button.addEventListener("click", function () {
    // Code die wordt uitgevoerd wanneer er op de knop wordt geklikt
    console.log("De knop is geklikt!");
});

// Toetsaanslaggebeurtenis

document.addEventListener("keydown", function (event) {
    // Code die wordt uitgevoerd wanneer er een toets wordt ingedrukt
    console.log("Er is een toets ingedrukt: " + event.key);
});


//   mouseover-gebeurtenis

var element = document.getElementById("myElement");
element.addEventListener("mouseover", function () {
    // Code die wordt uitgevoerd wanneer de muis over het element beweegt
    element.style.backgroundColor = "red";
});

// formulier gebeurtenis

var form = document.getElementById("myForm");
form.addEventListener("submit", function (event) {
    event.preventDefault(); // Voorkomt dat het formulier wordt verzonden

    // Code die wordt uitgevoerd wanneer het formulier wordt ingediend
    var input = document.getElementById("myInput");
    console.log("Invoerwaarde: " + input.value);
});

// window load gebeurtenis

window.addEventListener("load", function () {
    // Code die wordt uitgevoerd wanneer het venster volledig is geladen
    console.log("Het venster is volledig geladen!");
});
