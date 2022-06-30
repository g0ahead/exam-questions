## Was hat ein String mit einer Liste zu tun? 
Eine String ist eine Liste von einzelnen Zeichen 

## Welche Schleifenarten gibt es in Python
In Python gibt es zwei Schleifentypen: die while-Schleife und die for-Schleife. 
Die meisten Schleifen enthalten einen Zähler oder ganz allgemein Variablen, die 
im Verlauf der Berechnungen innerhalb des Schleifenkörpers ihre Werte ändern.

## Was sind List Comprehension?
List Comprehensions oder Listen-Abstraktionen sind syntaktische Gefüge, die beschreiben, 
wie vorhandene Listen oder andere iterierbare Objekte verarbeitet werden, um aus ihnen 
neue Listen zu erstellen. 

## Welche Collection Typen gibt es in Python?
- Listen -  Eine Liste wird mit eckigen Klammern definiert und besteht aus einer Folge von Elementen. (auch mit unterschiedlichen Typen)
- Tuple - Tupel werden mit runden Klammern initialisiert und können anschliessend nicht mehr verändert werden. (immutable)
- Mengen - Mengen enthalten eindeutige Elemente, also keine doppelten Einträge, und sind nicht geordnet. 
  Im Gegensatz zu Listen oder Tupel können wir die Elemente nicht mit einem Index abrufen. Mengen werden 
  in Python mit geschweiften Klammern gebildet.  

## Was ist ein Tupel
Ein Tuple ist eine geordnete, sequenzielle Sammlung. Es kann Daten aller Typen aufnehmen, 
die über einen Index erreichbar sind. Ein Tuple kann im Gegensatz zu einer Liste nicht 
geändert werden. 
Sobald ein Element in das Tuple eingefügt wurde, kann es nicht mehr verändert oder gelöscht werden,
somit ist ein Tuple immutable.

## Was ist ein Namedtuple ?
User = namedtuple('User', ['firstName', 'lastName', 'age'])
user = User('John', 'Doe', 42)

## Was ist in Python ein Generator
Mit Generatorfunktionen können Sie eine Funktion deklarieren, die sich wie ein Iterator verhält, 
d.h. sie kann in einer for-Schleife verwendet werden.