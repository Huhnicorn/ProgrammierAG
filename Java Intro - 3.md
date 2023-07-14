Arrays bzw. Listen sind Datenstrukturen in Java, mit denen du mehrere Werte desselben Datentyps speichern kannst. Arrays haben eine feste Größe, während Listen (z.B. `ArrayList`) dynamisch wachsen können.

## Arrays erstellen und initialisieren

Du kannst ein Array erstellen, indem du den Datentyp der Elemente angibst, gefolgt von eckigen Klammern `[]`, und dann den Array-Namen. Hier ist ein Beispiel für die Erstellung und Initialisierung eines Integer-Arrays:

```java
int[] zahlen = new int[5]; // Erstellt ein Integer-Array mit der Größe 5
```

Alternativ kannst du ein Array auch direkt bei der Deklaration mit Werten initialisieren:

```java
int[] zahlen = {1, 2, 3, 4, 5}; // Erstellt ein Integer-Array und initialisiert es mit den Werten 1, 2, 3, 4, 5
```

## Auf Elemente eines Arrays zugreifen

Die Elemente eines Arrays werden mit einem Index angesprochen. Der Index beginnt bei 0 für das erste Element und erhöht sich um 1 für jedes folgende Element. Hier ist ein Beispiel:

```java
int[] zahlen = {1, 2, 3, 4, 5};

int erstesElement = zahlen[0]; // Zugriff auf das erste Element (Wert: 1)
int drittesElement = zahlen[2]; // Zugriff auf das dritte Element (Wert: 3)
```

## Elemente eines Arrays ändern

Du kannst den Wert eines Elements in einem Array ändern, indem du auf das entsprechende Element zugreifst und ihm einen neuen Wert zuweist. Hier ist ein Beispiel:

```java
int[] zahlen = {1, 2, 3, 4, 5};

zahlen[0] = 10; // Ändert das erste Element auf den Wert 10
zahlen[2] = 30; // Ändert das dritte Element auf den Wert 30
```

## Arrays durchlaufen (iterieren)

Um alle Elemente eines Arrays nacheinander zu durchlaufen, kannst du eine Schleife verwenden. Eine gängige Schleife für die Iteration über ein Array ist die `for`-Schleife. Hier ist ein Beispiel:

```java
int[] zahlen = {1, 2, 3, 4, 5};

for (int i = 0; i < zahlen.length; i++) {
    System.out.println(zahlen[i]); // Gibt jedes Element des Arrays aus
}
```

Die `length`-Eigenschaft eines Arrays gibt die Anzahl der Elemente im Array zurück. In diesem Beispiel wird die Schleife solange durchlaufen, wie der Index `i` kleiner ist als die Länge des Arrays.

## Aufgabe

Schreibe ein Java-Programm, das ein Array von Zahlen enthält und die Summe aller Zahlen berechnet und ausgibt.

## Beispiellösung
```java
public class ArraySumme {
    public static void main(String[] args) {
        int[] zahlen = {1, 2, 3, 4, 5};
        int summe = 0;

        for (int i = 0; i < zahlen.length; i++) {
            summe += zahlen[i];
        }

        System.out.println("Die Summe der Zahlen ist: " + summe);
    }
}
```

Erklärung: In der Lösung wird ein Array von Zahlen erstellt und mit Werten initialisiert. Eine Schleife durchläuft alle Elemente des Arrays und addiert sie zur Variablen `summe` hinzu. Am Ende wird die Summe ausgegeben.


## ArrayList verwenden

Die `ArrayList`-Klasse ist eine dynamische Liste in Java, die Elemente beliebigen Datentyps speichern kann. Im Gegensatz zu Arrays kann eine `ArrayList` ihre Größe dynamisch anpassen.

Um `ArrayList` verwenden zu können, musst du die entsprechende Klasse aus der Java-Bibliothek importieren:

```java
import java.util.ArrayList;
```

Dann kannst du eine `ArrayList` erstellen und mit Werten füllen:

```java
ArrayList<String> namen = new ArrayList<String>(); // Erstellt eine leere ArrayList für Strings

namen.add("Max"); // Fügt einen neuen Namen hinzu
namen.add("Anna");
namen.add("Tom");

System.out.println(namen); // Gibt alle Namen in der ArrayList aus
```

Du kannst Elemente zu einer `ArrayList` hinzufügen und entfernen, auf Elemente zugreifen und deren Werte ändern, ähnlich wie bei Arrays. Weitere Operationen wie das Einfügen an einer bestimmten Position, das Entfernen an einer bestimmten Position usw. sind ebenfalls möglich.

## Aufgabe

Schreibe ein Java-Programm, das eine `ArrayList` von Studenten erstellt und deren Namen ausgibt.

## Beispiellösung
```java
import java.util.ArrayList;

public class StudentenListe {
    public static void main(String[] args) {
        ArrayList<String> studenten = new ArrayList<String>();

        // Studenten zur ArrayList hinzufügen
        studenten.add("Max Mustermann");
        studenten.add("Anna Schmidt");
        studenten.add("Tom Müller");

        // Alle Studentennamen ausgeben
        System.out.println("Liste der Studenten:");
        for (String name : studenten) {
            System.out.println(name);
        }
    }
}
```

Erklärung: In der Lösung wird eine `ArrayList` mit dem Namen `studenten` erstellt, die `String`-Elemente enthält. Mit der `add()`-Methode werden Studentennamen zur ArrayList hinzugefügt. Anschließend wird eine Schleife verwendet, um alle Namen in der ArrayList auszugeben.