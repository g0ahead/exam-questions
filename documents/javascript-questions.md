## Welche Datentypen werden in JS verwendet?
- Numbers	-> 123, 120.50, etc. 
- Strings -> "This text string"
- Boolean -> true / false 

## Für was werden Variablen gebraucht?
Darin werden Daten gespeichert, auf die später mit dem Variablennamen zugegriffen werden kann

## Was bedeutet case-sensitiv bei Variablennamen?
Groß- und Kleinschreibung werden berücksichtigt -> name != Name

## Sind Variablen in JS case-sensitiv?

## Mit welchen Keywords werden Variablen definiert? 
In JavaScript entstehen Variablen auf dreierlei Weise.
- var 
- let 
- const

## Was sind Prototypen?
Prototypen werden verwendet, um neue Objekte basierend auf vorhandenen zu erstellen. Diese Technik 
wird als prototypische Vererbung bezeichnet. 
Der Prototyp einer Instanz eines Objekts ist über Object.getPrototypeOf (Objekt) oder die Eigenschaft
\__proto__ (interne versteckte Eigenschaft [[Prototype]]) verfügbar.

## Für was wird 'let' verwendet?
Let ist für Variablen, die nur im aktuellen Block verarbeitet werden sollen. 
Es ist zu beachten, dass let in einem verschachtelten Block auch verfügbar ist, da sich ja 
der verschachtelte Block auch im aktuellen Block befindet. Kurz zur Klärung, ein Block ist 
z.B. eine if Bedingung, eine Funktion oder eine Schleife.

## Für was wird 'const' verwendet?
Der Datentype let ist für Variablen, die nur im aktuellen Block verarbeitet werden sollen. 
Es ist zu beachten, dass let in einem verschachtelten Block auch verfügbar ist, da sich 
ja der verschachtelte Block auch im aktuellen Block befindet. Kurz zur Klärung, ein Block 
ist z.B. eine if Bedingung, eine Funktion oder eine Schleife.

## Was ist JSON?
JSON ist ein Textdatenformat, das auf der von Douglas Crockford erfundenen JavaScript-Objektsyntax 
basiert. Es wird zum Übertragen von Daten über das Netzwerk verwendet und hat normalerweise die 
Erweiterung .json.

## Welche Datentypen kennt JSON?
JSON kennt sechs Datentypen: Null-Wert, Boolean, Number, String, Array und Object.
- Null-Wert - Besitzt ein Element keinen Wert, so wird es mit dem Schlüsselwort null belegt.
- Boolean - Boolsche Elemente besitzen den Wert true und false.
- Number - Numerische Elemente werden als Ziffernfolge 0-9 und falls notwendig dem 
           Dezimalpunkt . als Nachkommastellentrenner dargestellt.
- String - Ein Zeichenketten-Element beginnt mit " und endet mit " - dazwischen steht der eigentliche Text.
- Array - Ein Array beginnt mit [ und endet mit ]. Es enthält eine durch Komma 
          getrennte Liste von Elementen gleichen oder verschiedenen Datentyps. Leere Arrays sind erlaubt.
          Ein Array ist eine geordnete Liste, da die Elemente über deren Index angesprochen werden.
- Object - Ein Objekt beginnt mit { und endet mit }. Es enthält eine durch Komma, geteilte Liste
           von Objekt-Eigenschaften. Leere Objekte sind erlaubt.
           Ein Objekt ist eine ungeordnete Liste, da die Elemente über deren Namen angesprochen werden.

## Was macht die Array.slice() -Methode?
Die Slice () -Methode gibt die ausgewählten Array-Elemente als neues Array zurück. Es gibt Elemente 
zurück, die mit dem im ersten Argument angegebenen Index beginnen und mit dem im zweiten optionalen 
Argument angegebenen Index enden, diesen jedoch nicht einschließen. Wenn das zweite Argument fehlt, 
werden alle Elemente abgerufen, die mit dem im ersten Argument angegebenen Index beginnen.
```
	const intValues = [1,2,3,4,5];
	const intSlicesValues1 = intValues.slice(0,2);  // [1,2]
	const intSlicesValues2 = intValues.slice(2,3);  // [3]
   	const intSlicesValues3 = intValues.slice(3);    // [4,5]

```

## Was macht die Array.splice() -Methode?
Die splice () -Methode wird verwendet, um Elemente zu oder von einem Array hinzuzufügen oder zu entfernen. 
Das erste Argument gibt die Startposition für das Hinzufügen oder Entfernen von Elementen an, das zweite 
optionale Argument gibt die Anzahl der zu entfernenden Elemente an. 
Jedes nachfolgende Argument (drittes usw.) wird dem Array hinzugefügt.

```
let arrayOriginal1 = [1, 2, 3, 4, 5]
let arrayOriginal2 = [1, 2, 3, 4, 5]
let arrayOriginal3 = [1, 2, 3, 4, 5]

let array1 = arrayOriginal1.splice(0, 2);               //  [1, 2];   = [3, 4, 5]
let array2 = arrayOriginal2.slice(3); 	                //  [4, 5];   = [1, 2, 3]
let array3 = arrayOriginal3.slice(3, 1, 'a', 'b', 'c'); //  [4];      = [1, 2, 3, 'a', 'b', 'c']
```

## Was ist der Unterschied zwischen Array.slice() und Array.splice()?
Array.slice()
- Ändert das ursprüngliche Array nicht	
- Gibt ein Subarray des ursprünglichen Arrays zurück
- Wird verwendet, um Elemente aus einem Array abzurufen	
Array.splice()
- Ändert das ursprüngliche Array
- Gibt die entfernten Elemente als Array zurück
- Dient zum Hinzufügen / Entfernen von Elementen zu / von einem Array

## Was ist der Unterschied zwischen den Operatoren "==" und "==="?
JavaScript bietet zwei Möglichkeiten zum Vergleichen von Werten: 
- strict (=== ,!==) 
- abstract (== ,!=). 
In einem strengen Vergleich werden die Werte so verglichen, wie sie sind, und in einem laxen Vergleich
wird erforderlichenfalls eine implizite Konvertierung (Umwandlung) von Werttypen durchgeführt. 

- Zwei Zeichenfolgen sind streng gleich, wenn sie denselben Zeichensatz, dieselbe Länge und dieselben Zeichen an denselben Positionen haben
- Zwei Zahlen sind streng gleich, wenn ihre Werte gleich sind. Es gibt zwei Sonderfälle:
	- NaN ist nichts, einschließlich NaN
	- Positive und negative Nullen sind gleich
- Boolesche Werte sind streng gleich, wenn beide wahr oder falsch sind, d.h. richtig oder falsch
- Zwei Objekte sind streng gleich, wenn sie sich auf dasselbe Objekt beziehen (Speicherort).
- null === undefined gibt false zurück und null == undefined gibt true zurück

```
0 == false 			// true
0 === false 		// false
1 == "1" 			// true
1 === "1" 			// false
null == undefined 	// true
null === undefined 	// false
'0' == false 		// true
'0' === false 		// false
[] == [] 			// true 
[] === [] 			// false      
{} == {} 			// true 
{} === {} 			// false      
```

## Was sind Lambda oder Pfeilfunktionen?
Pfeilfunktionen sind eine Kurzform zum Schreiben von Funktionsausdrücken. Sie haben nicht ihre eigenen Argumente, 
super und new.target. Diese Funktionen dienen als gute Alternative zu Funktionen, die keine Methoden haben, aber 
nicht als Konstruktoren verwendet werden können.

## Was ist ein Virtual DOM
Das virtuelle DOM (VDOM) ist ein Programmierkonzept, bei dem eine ideale oder “virtuelle” Darstellung der 
Benutzerschnittstelle (UI) im Speicher gehalten und mit dem “echten” DOM mittels einer Bibliothek names 
ReactDOM synchronisiert wird. 
Dieser Prozess wird Abgleich (engl. reconcilation) genannt.





