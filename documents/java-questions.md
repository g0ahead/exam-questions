## Was ist ein Java-Compiler?
Ein Java Compiler übersetzt Quellcode in Bytecode

## Was ist ein Java-Interpreter?
Ein Java Interpreter wandelt Bytecode in Maschinencode und führt diesen auf der Rechner Plattform aus

## Wie wird ein JDK definiert? Aus welchen Bestandteilen besteht ein JDK?
Java Development Kit; Java Plattform mit einem Java Bytecode Interpreter + Compilter + Klassenbibliotheken

## Was ist eine JRE und wie wird diese definiert?
Java Runtime Environment; wird für die Ausführung von Java-Programmen benötigt

## Warum arbeitet Java mit einem zweistufigem Übersetzungskonzept?
- Bytecode ist hardwarenah
- Java kann auf jeder entsprechenden Rechner-Plattform ausgeführt werden
- Erstellte Bytecodedateien sind kompakt und effizient

## Was sind die zentralen zwei Elemente in der Objektorientierung?
Klassen und Objekte

## Was ist eine Klasse?
Eine Klasse ist ein Bauplan von einem Objekt

## Was ist ein Objekt?
Repräsentiert "Dinge" aus der realen Welt oder aus einem abstrakten Problem: "Der Artikel im Regal"

## Wie verändere ich den Zustand eines Objektes?
Durch Methoden, zB. Setter Methoden

## Was ist eine Mehthode?
Eine Methode definiert das Verhalten von Objekten und was mit den Objekten gemacht wird

## Was ist ein Vorteil der objektorienterter Programmierung?
Man bewegt sich immer in einer Objekt-Welt
  Es entsteht eine adäquate und durchgängige Betrachtungsweise

## Was ist ein Nachteil der objektorienterter Programmierung?
Objekte sind immer eine (starke) Vereinfachung, sie können manchmal sehr Abstrakt werden

## Nenne zwei Synonyme für Objekt
Instanz, Member

## Nenne zwei Synonyme für Klasse
Klassentyp, Typ

## Was kann man machen, um den Überblick über die Klassen zu bewahren (bei vielen und grossen Projekten)?
Die einzelnen Klassen auf Packages aufteilen

## Was verwendet man typischerweise für die Namensgebung eines Packages?
den Reverse Domainname -schwarz.lws.learncards

## Würde man die Klasse Person wie folgt in folgendem Package ablegen?
    Package:    lws.schwarz.learncards
    Klasse:     lws.schwarz.learncards.User
Nein! Ist zwar möglich, aber man verwendet üblicherweise den Reverse Domainname
    Package: schwarz.lws.learncards
    Klasse:  schwarz.lws.learncards.User

## Wie sieht der ideale Aufbau des Klassenrumpfs (innerer Teil der Klasse) aus?
Zuerst die Attribute, dann die Konstruktoren, danach die public Methoden und private Methoden

## Wie werden Attribute deklariert?
Mit einem (oder keinem!) Zugriffsmodifizierer (möglichst private!) einem Datentyp (z.B. int)
  und einem Bezeichner (beginnen immer mit Kleinbuchstaben), gefolgt von einem Semikolon.
    zB. private int articleId;

## Was sind die sieben Hauptmerkmale von Attributen?
- Halten Zustand / Eigenschaften eines Objektes fest (z.B. Grösse eines Rechtecks)
- Jede Instanzvariable dient zum Speichern von Daten und besitzt einen Datentyp.
- Gesamtheit der Datenwerte eines Objektes definiert seinen aktuellen Zustand
- Existieren zeitlebens eines Objektes
- Innerhalb der ganzen Klasse sichtbar/ansprechbar
- Sollten trotz automatischer Initialisierung ggf. explizit initialisiert werden
- Erfordern zur Laufzeit für jedes Objekt Speicherplatz auf dem Heap

## Nenne einige elementaren primitiven Datentypen, welche bei der Initialisierung von Attributen verwendet werden können
double, float, long, int, short, byte, char, boolean

## Was sind Eigenschaften eines Konstruktors?
- Ermöglicht beim Erzeugen eines Objektes das ordentliche Initialisieren dieses Objektes.
- Beinhaltet (meistens) ausführbare Anweisungen
- Wird beim Erzeugen eines Objektes automatisch aufgerufen bzw. abgearbetet
- Initialisiert typischerweise die Instanzvariablen
- Besitzt häufig Parameter (Ohne Parameter: Sogenannter Default-Konstruktor)
- Eine Klasse kann mehrere verschiedenen Konstruktoren besitzen
- Vergleichbar mit einer speziellen Methode ohne Rückgabewert (hat aber immer Klassename!)

## Gibt es in Java Destruktoren?
Nein! In Java gibt es keine, weil Java den Speicher mit Hilfe des Garbage Collectors verwaltet.
Der Garbage Collector entfernt automatisch nicht mehr benötigte Objekte aus dem Speicher und gibt diesen wieder frei.

## Wie sieht der Aufbau einer Methode in Java aus?
Zugriffsmodifizierer (public, private, etc.), Rückgabewert (void, String, int, etc.), Name, Parameter Liste
    zB. public String translate( String text, String srcLanguage, String destLanguage)

## Was sind Eigenschaften einer Methode?
Zugriffsmodifizierer häufig public oder private
spezieller Rückgabetyp void möglich, d.h. kein Rückgabewert
kann auch keine Parameter besitzen
Innerhalb derselben Klasse müssen alle Methoden in ihrer Signatur unterschiedlich sein!
    dh. Unterschiedliche Methodennamen, oder Parameter mit unterschiedlichen Datentypen,
        oder unterschiedliche Anzahl Paramter

## Können zwei Methoden denselben Namen besitzen?
Ja, wenn ihre Parameter unterschiedliche Datentypen besitzen oder sie eine unterschiedliche Anzahl Parameter haben!

## Wie deklariert man lokale Variablen?
Im Methodenrumpf (oder Konstruktorrumpf). Lokale Variablen sind ab der Zeile ihrer Deklaration bis zum Ende
  ihres umfassenden Blockes sichtbar.

## Was sind Merkmale und Eigenschaften von lokalen Variablen?
Werden innerhalb einer Methode bzw. eines Blocks deklariert.
Müssen explizit mit Werten initialisiert werden! (im Gegensatz zu Attributen nicht automatisch)
Sind nur während der Ausführung des entsprechenden Blocks existent und sichtbar
Erfordern intern Speicherplatz auf dem Call-Stack

## Was kann man machen damit formalen Parametern keine neuen Werte im Ausführungsblock zugewiesen werden kann?
Als final markieren. zB. final String article, final int articleNumber

## Variablen eines elementaren (primitiven) Datentyps enthalten jeweils mehrere Werte?
Nein!

## Welche primitiven Datentypen gibt es für ganze Zahlen?
byte, short, int, long

## Gibt es in Java Unsigned Integer Datentypen
Nein! Alle Integer Datebtypen sind vorzeichenbehaftet, haben also einen negativen und positiven Wertebereich.
  Der Datentype char ist streng genommen auch ein Integer Datentyp der ein einzelnes Zeichen darstellt.

## Was sind die Eigenschaften von char?
Ein char enthält genau ein Zeichen und wird mit einfachen Anführungszeichen (') eingefasst.
    zB. char c = 'A';
    Nicht verwechseln mit Strings, das sind Zeichenketten!

## Was ist der Hauptvorteil von byte und short als Datentypen?
Sie können besonders bei grossen Datenmengen viel Platz sparen
    ! Da wir heute über viel Speicher verfügen, lohnt sich eine seriöse Auswahl des geeigneten Datentyps
      nicht (z.B. byte statt int)
## Welche Datentypen gibt es für Gleitkommazahlen?
float und double. Ohne explizite Angabe werden Gleitkommazahlen in Java per Default als double betrachtet

## Was ist Implizite Typumwandlung (Casting)
Java konvertiert den Wert direkt und automatisch bei einer normalen Zuweisung, zB. long value = 1##;

## Was ist die Explizite Typumwandlung (Casting)
Wir geben Java explizit den Befehl, in welchen Typ etwas konvertiert werden soll, z.B. long value = (long) 1##;

## Welches sind die wichtigsten logischen Operatoren?
&& (UND)
|| (ODER
^ (EXKLUSIV-OR)
! (NEGATION, NOT)

## Wenn man eine Variable/Parameter vom Typ boolean hat, kann man dies bei der Bedingung im if-Statement einsetzten?

    boolean isSwitchedOn = true;
    if(isOn) {
        // do something
    }
Ja

## Was ist die Problematik von if-Statements?
Bei logisch etwas komplexeren Abläufen treten if-Statement sehr schnell ineinander verschachtelt auf.
  Schon ab drei Einrückungsebenen empfindet man den Code als sehr unübersichtlich.

## Welche Möglichkeiten hat man, um tiefe Verschachtelungen bei if-Statements zu verhindern?
 In dem man tief verschachtelte if-Statements in eigenständige Methoden auslagert, die man dann aufruft
 Mit else-if-Statements
 Mit switch-Statements

## Was ist der Vorteil eines else-if-Statements?
Kann in manchen Fällen deutlich übersichtlicher sein

## Was ist der Nachteil eines else-if-Statements?
Nur bei voneinander unabhängig formulierten Optionen möglich

## Was ist der Unterschied eines switch-Statements zu einem if-Statement?
Das switch-Statement beschränkt sich auf den Vergleich von absoluten Werten (keine Bedingung)

## Was ist ein Nachteil eines switch-Statements?
Es funktioniert nur mit einer eingeschränkten Menge von Datentypen:
    Primitive: byte, short, char, int (ohne long!)
    Klassen: String und Enumerations-Typen
  Somit nur geeignet für einfache Fallunterscheidungen auf Basis von einzelnen Werten

## Welche verschiedene Schleifen-Anweisungen für unterschiedliche Zwecke und Nutzungen kennt Java?
while-Schleife (Eingangstest)
do-while-Schleife (Ausgangstest)
for-Schleife (Eingangstest)
for-each-Schleife (Iteration über Collection)

## Bei welcher Schleife (Iteration) wird der Schleifenkörper nie ausgeführt, falls die Bedingung false ist?
while-Schleife

## Ist die Anzahl Schleifendurchläufe bei einer while-Schleife (mindestens zum Zeitpunkt der Implementation) bekannt?
Nein

## Was ist die Charakteristik der do-while-Schleifen?
Die Anzahl Schleifendurchgänge ist in der Regel (mindestens zum Zeitpunkt der Implementation) nicht bekannt
Der Schleifenkörper wird ausgeführt, solange die Bedingung true ist
Die Bedingung wird nach jeder Ausführung des Schleifenkörpers geprüft (wird somit immer mindestens einmal ausgeführt!)

## Wozu ist eine for-Schleife ideal?
Für einfache, zählende Schleifen

## Was ist sehr wichtig zu beachten bei den Schleifenbedingungen?
Diese müssen "sicher" formuliert werden, denn tritt eine Bedingung nicht ein, resultiert eine Endlos-Schleife!

## Was sind Checked Unchecked Exceptions?
Java definiert zwei Arten von Ausnahmen:

Checked-Exception (Überprüfte Ausnahmen): 
Ausnahmen, die von der Exception Klasse abgeleitet werden, sind geprüfte Ausnahmen. 
Der Client-Code muss die von der API geworfenen überprüften Ausnahmen entweder in einer Try-Klausel oder durch 
  Weiterleiten mit der Throw-Klausel behandeln. (Beispiele: SQLException, IOxception)

Unchecked-Exception (Ungeprüfte Ausnahmen): 
Alle Ausnahmen, die von RuntimeException erben, werden besonders behandelt. Der Client-Code muss sich nicht mit 
ihnen befassen, und daher werden sie als ungeprüfte Ausnahmen bezeichnet. 
Beispiel ungeprüfte Ausnahmen sind NullPointerException, OutOfMemoryError, DivideByZeroException normalerweise, 
  Programmierfehler.

## Was ist der Unterschied zwischen einer Abstrakten Klasse und einem Interface?
Abstrakte Klassen können einige ausführbare Methoden und Methoden nicht implementieren lassen. Interfaces enthalten 
keinen Implementierungscode.
Eine Klasse kann eine beliebige Anzahl von Interfaces implementieren, aber höchstens eine abstrakte Klasse.
Eine abstrakte Klasse kann nicht abstrakte Methoden haben. Alle Methoden einer Interface sind abstrakt.
Eine abstrakte Klasse kann Instanzvariablen haben. Eine Interface kann nicht.
Eine abstrakte Klasse kann Konstruktor definieren. Eine Interface kann nicht.
Eine abstrakte Klasse kann jede Sichtbarkeit haben: öffentlich, geschützt, privat oder keine (Paket). Die Sichtbarkeit 
einer Interface muss öffentlich oder gar nicht sein (Paket).
Eine abstrakte Klasse erbt von Object und enthält Methoden wie clone () und gleich ().

## Was sind Checked Unchecked Exceptions?
Java definiert zwei Arten von Ausnahmen:

__Checked-Exception__ (Überprüfte Ausnahmen): 
Ausnahmen, die von der Exception Klasse abgeleitet werden, sind geprüfte Ausnahmen. 
Der Client-Code muss die von der API geworfenen überprüften Ausnahmen entweder in einer Try-Klausel oder durch 
Weiterleiten mit der Throw-Klausel behandeln. (Beispiele: SQLException, IOxception)

__Unchecked-Exception__ (Ungeprüfte Ausnahmen): 
Alle Ausnahmen, die von RuntimeException erben, werden besonders behandelt. Der Client-Code muss sich nicht mit 
ihnen befassen, und daher werden sie als ungeprüfte Ausnahmen bezeichnet. 
Beispiel ungeprüfte Ausnahmen sind NullPointerException, OutOfMemoryError, DivideByZeroException normalerweise, Programmierfehler.


## Was ist eine Userdefined Exception (Benutzerdefinierte Ausnahmen)?
Benutzerdefinierte Ausnahmen können implementiert werden durch Definieren einer Klasse, um auf die Ausnahme zu reagieren 
und Einbetten einer Throw-Anweisung in einem Try-Block, in dem die Ausnahme auftreten kann. Der Entwickler kann eine neue 
Ausnahme definieren, indem er sie wie folgt aus der Exception-Klasse ableitet.

Die Throw-Anweisung wird verwendet, um das Auftreten der Ausnahme innerhalb eines Try-Bocks zu signalisieren. Ausnahmen 
werden häufig in derselben Anweisung instanziiert, in die sie mit der Syntax geworfen werden.


## Was ist der Unterschied zwischen C++ und Java?
Wie Bjarne Stroustrup sagt: „Trotz der syntaktischen Ähnlichkeiten sind C++ und Java sehr unterschiedliche Sprachen. 
In vielerlei Hinsicht scheint Java Smalltalk näher zu sein als C++.“
- Java ist multithreaded Java hat keine Zeiger 
- Java hat eine automatische Speicherverwaltung (Garbage Collection) 
- Java ist plattformunabhängig
- Java hat eine eingebaute Unterstützung für Kommentardokumentation 
- Java hat keine Mehrfachvererbung
- Java hat keine Destruktoren

## Was sind Statements in Java?
Statements sind äquivalent zu Sätzen in natürlichen Sprachen. Eine Anweisung bildet eine vollständige Ausführungseinheit. 
Die folgenden Arten von Ausdrücken können in eine Anweisung umgewandelt werden, indem der Ausdruck mit einem Semikolon 
abgeschlossen wird

- Zuweisungsausdrücke ( name = "Christion"; ) 
- Jede Verwendung von ++ oder -- 
- Methodenaufrufe 
- Objekterstellungsausdrücke (new String("Konrad");)

Diese Arten von Anweisungen werden als Ausdrucksanweisungen bezeichnet. Zusätzlich zu diesen Arten von Ausdrucksanweisungen 
gibt es noch zwei weitere Arten von Anweisungen. 
Eine Deklarationsanweisung deklariert eine Variable. Eine Ablaufsteuerungsanweisung regelt die Reihenfolge, in der 
Anweisungen ausgeführt werden. 
Die for-Schleife und die if-Anweisung sind beide Beispiele für Ablaufsteuerungsanweisungen.


##)  Was ist eine JAR Datei?
Java-Archive Dateien ist eine Sammlung von Java-Klassen, Bildern, Audio usw., die zu einer einfachen, kleineren Datei. (Zip-Format)


## Was ist JNI?
JNI ist ein Akronym für Java Native Interface. Mit JNI können wir Funktionen aufrufen, die in anderen Sprachen von Java 
geschrieben sind. Im Folgenden sind seine Vor- und Nachteile aufgeführt.

Vorteile: 
- Vorhandene Bibliothek verwenden, die zuvor in einer anderen Sprache geschrieben wurde. 
- Aus der Windows-API-Funktion aufrufen. 
- Aus Gründen der Ausführungsgeschwindigkeit. 
- Die API-Funktion eines Servers aufrufen, das sich in C oder C++ vom Java-Client befindet. 
  
Nachteile:
- 'write once run anywhere' funktioniert hier nicht, auf Grund der Systemabhänigkeiten 
- Schwierig zu debuggender Laufzeitfehler im nativen Code. 
- Potentielles Sicherheitsrisiko.

## Was ist Serialization?
Ein ganzes Java-Objekt in einen und aus einem Byte-Strom zu lesen oder zu schreiben. Es ermöglicht die Codierung von 
Java-Objekten und -Primitiven in einen Byte-Strom, der für das Streaming zu einer Art Netzwerk oder zu einem 
Dateisystem oder allgemeiner zu einem Übertragungsmedium oder einer Speichereinrichtung geeignet ist. 
Ein seralisierbares Objekt muss die serilisierbare Schnittstelle implementieren. 
Wir verwenden ObjectOutputStream, um dieses Objekt in einen Stream zu schreiben, und ObjectInputStream, um es aus dem 
Stream zu lesen.

## Warum gibt es in Java eine Nullschnittstelle? Was heißt das ?
Null-Schnittstellen fungieren als Markierungen. Sie teilen dem Compiler nur mit, dass die Objekte dieser Klasse anders 
behandelt werden müssen. 

Einige Markierungsschnittstellen sind: 
- Serializable
- Remote
- Cloneable

## Ist 'synchronised' ein Modifikator, Bezeichner oder was ist sonst?
Es ist ein Modifikator. Synchronisierte Methoden sind Methoden, die verwendet werden, um den Zugriff auf ein 
Objekt zu steuern. Ein Thread führt eine synchronisierte Methode erst aus, nachdem er die Sperre für das Objekt oder 
die Klasse der Methode erworben hat. Synchronisierte Anweisungen ähneln synchronisierten Methoden. 
Eine synchronisierte Anweisung kann nur ausgeführt werden, nachdem ein Thread die Sperre für das Objekt oder die Klasse 
erworben hat, auf die in der synchronisierten Anweisung verwiesen wird.

##  Was ist eine Singleton Klasse, für was wird sie benötigt?
Singleton ist ein Entwurfsmuster, das eine und nur eine Instanz eines Objekts bereitstellen soll. 
Andere Objekte können über eine statische Methode eine Referenz auf diese Instanz erhalten (der Klassenkonstruktor wird 
privat gehalten). 
Warum brauchen wir ein Singleton? Manchmal ist es notwendig und oft ausreichend, eine einzelne Instanz einer bestimmten 
Klasse zu erstellen. Dies hat Vorteile bei der Speicherverwaltung und bei Java bei der Garbage Collection. 
Darüber hinaus kann es aus technologischen oder geschäftlichen Gründen erforderlich oder wünschenswert sein, die Anzahl 
der Instanzen zu beschränken. Beispielsweise möchten wir nur eine einzige Instanz eines Pools von Datenbankverbindungen.

##)  Was ist eine Compilation Unit?
Die kleinste Einheit von Quellcode, die kompiliert werden kann, d.h. eine .java-Datei.

##  Ist String eine Wrapper Klasse?
String ist eine Klasse, aber keine Wrapper-Klasse. Wrapper-Klassen wie (Integer) existieren für jeden primitiven Typ. 
Sie können verwendet werden, um einen primitiven Datenwert in ein Objekt umzuwandeln und umgekehrt.

##  Warum hat Java keine Mehrfachvererbung?

Das Java-Designteam war bestrebt, Java nach folgenden:

- Einfach, objektorientiert
- Robust und sichere Architektur 
- Neutral und portabel 
- Hochperformant interpretiert, threaded und dynamisch 

Die Gründe für das Weglassen der Mehrfachvererbung in der Java-Sprache ergeben sich hauptsächlich aus dem Ziel 
„einfach, objektorientiert und vertraut“. Als einfache Sprache wollten die Entwickler von Java eine Sprache, 
die die meisten Entwickler ohne umfangreiches Training verstehen können. Zu diesem Zweck arbeiteten sie daran, 
die Sprache C++ so ähnlich wie möglich (vertraut) zu machen, ohne die unnötige Komplexität von C++ zu übertragen. 
Nach Meinung der Designer verursacht Mehrfachvererbung mehr Probleme und Verwirrung, als sie löst. Sie schneiden 
also die Mehrfachvererbung aus der Sprache ab (genauso wie sie das Überladen von Operatoren abschneiden). 
Die umfassende C++-Erfahrung der Designer lehrte sie, dass Mehrfachvererbung die Kopfschmerzen einfach nicht wert war.

## Warum ist Java nicht 1##% OOPS (Objekt-Orientiert)?
Viele Leute sagen das, weil Java primitive Typen wie int, char, double verwendet.

## Was ist ein Resource-Bundle?
In seiner einfachsten Form wird ein Resource-Bundle durch eine Textdatei dargestellt, die Schlüssel und einen Textwert 
für jeden Schlüssel enthält. 

## Was ist eine Transient-Variable?
Transiente Variable kann nicht serialisiert werden. Wenn beispielsweise eine Variable in einer serialisierbaren Klasse 
als transient deklariert und die Klasse in einen ObjectStream geschrieben wird, kann der Wert der Variablen nicht in 
den Stream geschrieben werden, stattdessen wird beim Abrufen der Klasse aus dem ObjectStream der Wert der Variablen Null.

## Was ist die Collection-API?
Die Collection-API ist ein Satz von Klassen und Schnittstellen, die den Betrieb von Sammlungen von Objekten unterstützen. 
Diese Klassen und Schnittstellen sind flexibler, leistungsfähiger und regelmäßiger als die Vektoren, Arrays und 
Hashtabellen, wenn sie effektiv ersetzt werden. (Beispiele: HashSet HashMapArrayList LinkedList TreeSet TreeMap)

## Ist ein Iterator eine Klasse oder ein Interface, für was wird es benutzt?
Iterator ist ein Interface, die zum schrittweisen Durchlaufen der Elemente einer Sammlung verwendet wird.

## Was ist die Gemeinsamkeit/Unterschied zwischen einer abstrakten Klassen und einem Interface?
Gemeinsamkeiten:

Weder abstracte Klassen noch Interfaces können instanziiert werden.

Unterschiede:

Interfaces bieten eine Form der Mehrfachvererbung. Eine Klasse kann nur eine andere Klasse erweitern.
Interfaces sind auf öffentliche Methoden und Konstanten ohne Implementierung beschränkt. Abstrakte Klassen können 
eine teilweise Implementierung, geschützte Teile, statische Methoden usw. haben.
Eine Klasse kann mehrere Interfaces implementieren. Im Falle einer abstrakten Klasse kann eine Klasse jedoch nur eine 
abstrakte Klasse erweitern. Interfaces sind langsam, da zusätzliche Einrückung erforderlich ist, um die entsprechende 
Methode in der tatsächlichen Klasse zu finden.

## Was ist eine Transient-Variable?
Eine vorübergehende Transient-Variable ist eine Variable, die möglicherweise nicht serialisiert wird.

## Welche Container benutzt ein Border-Layout als Standardlayout? (Swing UI)
Die Klassen Window, Frame und Dialog verwenden ein Border-Layout als Standardlayout.

## Warum blockieren Threads I/O Operationen?
Threads blockieren I/O (dh gibt den Wartezustand ein), sodass andere Threads ausgeführt werden können, 
während die I/O-Operation ausgeführt werden.

## Wie werden Observer und Observable verwendet?
Objekte, die die von Observable Klasse abgeleitet snd, führen eine Liste von Beobachtern. Wenn ein beobachtbares Objekt 
aktualisiert wird, ruft es die update()-Methode jedes seiner Beobachter auf, um die zu benachrichtigen.

Observer, dass es den Zustand geändert hat. Die Observer-Interface wird von Objekten implementiert, 
die beobachtbare Objekte beobachten.

## Was ist Synchronization und warum ist es wichtig?
In Bezug auf Multithreading ist die Synchronisierung die Möglichkeit, den Zugriff mehrerer Threads auf gemeinsam 
genutzte Ressourcen zu steuern. Ohne Synchronisierung kann ein Thread ein freigegebenes Objekt ändern, während 
ein anderer Thread den Wert dieses Objekts verwendet oder aktualisiert. Dies führt häufig zu erheblichen Fehlern.

## Kann ein Lock für eine Klasse erworben werden??
Ja, eine Klasse kann gesperrt werden. Diese Sperre wird für das Class-Objekt der Klasse erworben.

##  Was ist neu an den Methoden stop(), suspend() und resume() in JDK 1.2?
Die Methoden stop(), suspend() und resume() sind in JDK 1.2 veraltet (deprecated).

## Ist null ein Schlüsselwort?
Der null-Wert ist kein Schlüsselwort.

## Was ist die preferred size (bevorzugte Größe) einer Komponente?
Die preferred size einer Komponente ist die minimale Komponentengröße, die eine normale Anzeige der Komponente ermöglicht.

## Was ist das Ergenis von der Division 1.1 / 0.0 
Infinity -> keine ArithmeticException: / by zero

## JPA Wie muss ein Datenobjekt annotiert werden dass es von JPA verwaltet werten kann?
- @Entity 
- @Id ( @GeneratedValue @SequenceGenerator @TableGenerator @GenericGenerator)