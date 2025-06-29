In Java, to read input from the user and print output, you commonly use these built-in classes:

## ✅ 1. Scanner (Most Common for Input)
# 🔹 1. First Step basic setup

```java

import java.util.Scanner;
Scanner sc = new Scanner(System.in);  // Create Scanner object

}
```
Once you create a `Scanner` object, you can use different methods to read different types of data.

---

## 🔹 2. Read **Primitive Data Types**

| Type      | Method          | Example Input  |
| --------- | --------------- | -------------- |
| `int`     | `nextInt()`     | `42`           |
| `double`  | `nextDouble()`  | `3.14`         |
| `long`    | `nextLong()`    | `1234567890`   |
| `boolean` | `nextBoolean()` | `true`/`false` |
| `float`   | `nextFloat()`   | `2.5`          |

### Example:

```java
int myInt = scanner.nextInt();

double myDouble = scanner.nextDouble();

boolean myBool = scanner.nextBoolean();
```

---

## 🔹 3. Read **String and Character**

| Type            | Method             | Notes                              |
| --------------- | ------------------ | ---------------------------------- |
| `String` (word) | `next()`           | Reads until space                  |
| `String` (line) | `nextLine()`       | Reads full line (including spaces) |
| `char`          | `next().charAt(0)` | Reads first character of input     |

### Example:

```java

String word = scanner.next();

System.out.print("Enter a full line: ");
scanner.nextLine(); // to consume leftover newline
String line = scanner.nextLine();

System.out.print("Enter a character: ");
char ch = scanner.next().charAt(0);
```

---

## 🔹 4. Read **Wrapper Classes** (Objects like `Integer`, `Double`, etc.)

* You still read as a primitive, but you can **box** into objects manually:

```java
System.out.print("Enter an Integer: ");
Integer myInteger = scanner.nextInt(); // auto-boxes to Integer

System.out.print("Enter a Double: ");
Double myDouble = scanner.nextDouble(); // auto-boxes to Double

System.out.print("Enter a Boolean: ");
Boolean myBoolean = scanner.nextBoolean(); // auto-boxes to Boolean
```
> Java automatically converts between primitives and wrapper objects (called *autoboxing*).
---

## 🔹 5. Full Example: Read All Types

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter an int: ");
        int i = scanner.nextInt();

        System.out.print("Enter a double: ");
        double d = scanner.nextDouble();

        System.out.print("Enter a long: ");
        long l = scanner.nextLong();

        System.out.print("Enter a boolean: ");
        boolean b = scanner.nextBoolean();

        System.out.print("Enter a float: ");
        float f = scanner.nextFloat();

        System.out.print("Enter a single word: ");
        String word = scanner.next();

        scanner.nextLine(); // clear newline left in buffer

        System.out.print("Enter a full line: ");
        String line = scanner.nextLine();

        System.out.print("Enter a character: ");
        char c = scanner.next().charAt(0);

        System.out.println("\nYou entered:");
        System.out.println("int: " + i);
        System.out.println("double: " + d);
        System.out.println("long: " + l);
        System.out.println("boolean: " + b);
        System.out.println("float: " + f);
        System.out.println("word: " + word);
        System.out.println("line: " + line);
        System.out.println("char: " + c);

        scanner.close();
    }
}
```
---

# F.1 My Code to Read only primitive data types 

```java
import java.util.Scanner;

public class Main {
    
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter char :");
        char ch = sc.next().charAt(0);
        
        System.out.println("Enter int:");
        int x = sc.nextInt();
        
        System.out.println("Enter Boolean:");
        boolean t = sc.nextBoolean();
        
        System.out.println("Enter Double:");
        double d = sc.nextDouble();
        
        System.out.println("Enter Float:");
        float f = sc.nextFloat();
        
        System.out.println("Enter Long:");
        long l = sc.nextLong();
        
        
        System.out.println("char :"+ch);
        System.out.println("int :"+x);
        System.out.println("boolean :"+t);
        System.out.println("double :"+d);
        System.out.println("float :"+f);
        System.out.println("long :"+l);
        
    }
}
```

# F.2 My code to Read Object of Integer 
```java
import java.util.Scanner;

public class Main {
    
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter char :");
        char ch = sc.next().charAt(0);
        
        System.out.println("Enter int:");
        Integer x = sc.nextInt();
        
        System.out.println("Enter Boolean:");
        Boolean t = sc.nextBoolean();
        
        System.out.println("Enter Double:");
        Double d = sc.nextDouble();
        
        System.out.println("Enter Float:");
        Float f = sc.nextFloat();
        
        System.out.println("Enter Long:");
        Long l = sc.nextLong();
        
        
        System.out.println("char :"+ch);
        System.out.println("int :"+x);
        System.out.println("boolean :"+t);
        System.out.println("double :"+d);
        System.out.println("float :"+f);
        System.out.println("long :"+l);
        
    }
}
```
# F.3 My code to Read char and String and word
```java
import java.util.Scanner;

public class Main {
    
    public static void main(String args[])
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a CHAR :");
        Character CHAR = sc.next().charAt(0); 
        
        
        System.out.println("Enter a char :");
        char ch = sc.next().charAt(0);
        
        System.out.println("Enter a String ");
        sc.nextLine();
        String str1 = sc.nextLine();
        
        System.out.println("Enter a Word ");
        
        String str2 = sc.nextLine();
        
        System.out.println("CHAR "+CHAR);
        System.out.println("char "+ch);
        System.out.println("str1 "+str1);
        System.out.println("str2 "+str2);
       
    }
}
```


