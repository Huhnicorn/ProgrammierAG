Nachdem du Variablen deklariert und initialisiert hast, gibt es verschiedene Aktionen, die du mit Variablen durchführen kannst:

1. **Werte zuweisen**: Du kannst den Wert einer Variablen ändern, indem du ihr einen neuen Wert zuweist. Zum Beispiel:
   ```java
   int zahl = 5;
   zahl = 10; // Wert von zahl wird auf 10 aktualisiert
   ```

2. **Operationen durchführen**: Du kannst arithmetische Operationen (wie Addition, Subtraktion, Multiplikation und Division) auf numerischen Variablen durchführen. Zum Beispiel:
   ```java
   int a = 5;
   int b = 3;
   int summe = a + b; // Addition
   int differenz = a - b; // Subtraktion
   int produkt = a * b; // Multiplikation
   int quotient = a / b; // Division
   ```

3. **Variablen miteinander kombinieren**: Du kannst Variablen miteinander kombinieren oder sie in Ausdrücken verwenden. Zum Beispiel:
   ```java
   int alter = 25;
   String name = "Max";
   String satz = "Ich bin " + name + " und ich bin " + alter + " Jahre alt.";
   ```

4. **Variablen ausgeben**: Du kannst den Wert einer Variablen mit Hilfe der Ausgabefunktionen (z.B. `System.out.println()`) auf der Konsole ausgeben. Zum Beispiel:
   ```java
   int zahl = 10;
   System.out.println("Die Zahl ist: " + zahl);
   ```

5. **Bedingungen überprüfen**: Du kannst Bedingungen überprüfen und Entscheidungen basierend auf dem Wert von Variablen treffen. Zum Beispiel:
   ```java
   int alter = 18;
   if (alter >= 18) {
       System.out.println("Du bist volljährig.");
   } else {
       System.out.println("Du bist minderjährig.");
   }
   ```

6. **Schleifen verwenden**: Du kannst Schleifen (wie z.B. `for`- oder `while`-Schleifen) verwenden, um bestimmte Aktionen wiederholt auszuführen, möglicherweise unter Verwendung von Variablen als Zähler oder Bedingungen. Zum Beispiel:
   ```java
   for (int i = 0; i < 5; i++) {
       System.out.println("Schleifendurchlauf " + i);
   }
   int a = 1;
   while (a < 4){
	   System.out.println(a);
	   a++;
	   }
   ```

## Aufgabe

Schreibe ein Java-Programm, das die Zahlen von 1 bis 10 ausgibt. Verwende dazu eine Schleife.

## Beispiellösung
```java
public class ZahlenAusgeben {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            System.out.println(i);
        }
    }
}
```


## Scanner

Der `Scanner` ist eine Klasse in Java, die es ermöglicht, Eingaben von Benutzern über die Konsole oder andere Eingabequellen zu lesen. Mit dem `Scanner` können verschiedene Datentypen wie ganze Zahlen, Gleitkommazahlen, Zeichenketten und andere eingelesen werden.

Um den `Scanner` zu verwenden, muss zuerst eine Instanz der Klasse erstellt werden. Dazu wird die `Scanner`-Klasse aus der Java-Bibliothek importiert, und ein neues `Scanner`-Objekt wird mit dem gewünschten Eingabestrom (z.B. `System.in` für die Konsole) erstellt. Hier ist ein Beispiel für die Erstellung eines `Scanner`-Objekts:

```java
import java.util.Scanner;

public class ScannerBeispiel {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        // Weitere Code-Zeilen ...
    }
}
```

Nachdem der `Scanner` erstellt wurde, können verschiedene Methoden verwendet werden, um Eingaben zu lesen. Einige häufig verwendete Methoden sind:

- `nextInt()`: Liest eine ganze Zahl von der Eingabe.
- `nextDouble()`: Liest eine Gleitkommazahl von der Eingabe.
- `nextLine()`: Liest eine Zeichenkette (bis zum Zeilenumbruch) von der Eingabe.

Hier ist ein Beispiel, das den `Scanner` verwendet, um eine ganze Zahl von der Benutzerin oder dem Benutzer einzulesen und sie anschließend auszugeben:

```java
import java.util.Scanner;

public class ScannerBeispiel {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Gib eine ganze Zahl ein: ");
        int zahl = scanner.nextInt();

        System.out.println("Die eingegebene Zahl ist: " + zahl);
    }
}
```

Es ist wichtig zu beachten, dass der `Scanner` nach dem Einlesen einer Eingabe im Puffer verbleibt. Wenn weitere Eingaben gelesen werden sollen, muss der `Scanner` erneut verwendet werden. Nachdem alle Eingaben eingelesen wurden, sollte der `Scanner` mit der `close()`-Methode geschlossen werden, um Ressourcen freizugeben.


## Aufgabe

Schreibe ein Java-Programm, das die Summe aller geraden Zahlen von 1 bis zu einer gegebenen Zahl berechnet. Verwende dazu eine Schleife und bedingte Anweisungen.

## Beispiellösung
```java
import java.util.Scanner;

public class SummeGeraderZahlen {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Gib eine Zahl ein: ");
        int zahl = scanner.nextInt();
        int summe = 0;

        for (int i = 2; i <= zahl; i += 2) {
            summe += i;
        }

        System.out.println("Die Summe aller geraden Zahlen von 1 bis " + zahl + " ist: " + summe);
    }
}
```

Erklärung: In der Lösung wird eine Schleife verwendet, um alle geraden Zahlen von 1 bis zur gegebenen Zahl zu summieren. Die Schleife erhöht den Zähler `i` bei jedem Durchlauf um 2, um sicherzustellen, dass nur gerade Zahlen berücksichtigt werden. Die Summe wird in der Variable `summe` akkumuliert und am Ende ausgegeben.