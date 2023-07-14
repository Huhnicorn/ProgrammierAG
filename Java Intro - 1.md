## Überblick über Variablen und Datentypen

In der Programmierung werden Variablen verwendet, um Daten zu speichern und auf sie zuzugreifen. Jede Variable hat einen Namen und einen Wert, der ihr zugeordnet ist. Der Wert einer Variablen kann sich während der Ausführung des Programms ändern.

In Java gibt es verschiedene Datentypen, die angeben, welche Art von Daten in einer Variable gespeichert werden kann. Hier sind einige der häufig verwendeten Datentypen in Java:

- **Ganzzahlige Datentypen**: Diese Datentypen werden verwendet, um ganze Zahlen ohne Dezimalstellen zu speichern. Beispiele hierfür sind `int`, `short` und `long`.
  
  Beispiel:
  ```java
  int alter = 25;
  ```

- **Fließkomma-Datentypen**: Diese Datentypen werden verwendet, um Zahlen mit Dezimalstellen zu speichern. Beispiele hierfür sind `float` und `double`.
  
  Beispiel:
  ```java
  double preis = 9.99;
  ```

- **Zeichen-Datentyp**: Der `char`-Datentyp wird verwendet, um einzelne Zeichen zu speichern, wie Buchstaben oder Sonderzeichen.
  
  Beispiel:
  ```java
  char geschlecht = 'M';
  ```

- **Boolescher Datentyp**: Der `boolean`-Datentyp kann entweder den Wert `true` oder `false` annehmen und wird verwendet, um logische Aussagen darzustellen.
  
  Beispiel:
  ```java
  boolean istAktiv = true;
  ```

- **Zeichenkette (String)**: Der `String`-Datentyp wird verwendet, um eine Folge von Zeichen zu speichern, wie zum Beispiel Namen.
  
  Beispiel:
  ```java
  String name = "Max Mustermann";
  ```

Es ist wichtig, den richtigen Datentyp für eine Variable auszuwählen, da dies die Art der Daten und die möglichen Operationen darauf bestimmt. Die Wahl des richtigen Datentyps kann auch die Speicherplatzanforderungen und die Leistung des Programms beeinflussen.

Variablen können verwendet werden, um Werte zu speichern, Berechnungen durchzuführen und Ergebnisse zu speichern. 

### Beispiel-Programm:

```java
public class Main{
    public static void main(String[] args) {
        String name = "Max Mustermann";
        int alter = 25;
        double groesse = 1.75;
        
        System.out.println("Name: " + name);
        System.out.println("Alter: " + alter);
        System.out.println("Alter nächstes Jahr: " + (alter+1));
        System.out.println("Größe: " + groesse + "m");
    }
}
```

## Aufgaben
1. Schreibe ein Programm, welches deinen Namen, Alter, ... ausgibt
2. Versuche, Rechenaktionen durchzuführen

## Beispiellösung

```java
public class Main {
    public static void main(String[] args) {
        // Rechenoperationen
        int geburtsjahr = 2023 - alter;
        double halbeGroesse = groesse / 2;
        int zehnJahreSpaeter = alter + 10;

        System.out.println("Geburtsjahr: " + geburtsjahr);
        System.out.println("Halbe Größe: " + halbeGroesse);
        System.out.println("Alter in 10 Jahren: " + zehnJahreSpaeter);
    }
}
```

Ausgabe:
```yaml
Name: John Doe
Alter: 30
Alter nächstes Jahr: 31
Größe: 1.8m
Geburtsjahr: 1993
Halbe Größe: 0.9
Alter in 10 Jahren: 40
```
