**BufferedReader**, which is another way to read input from the user in Java. It's a bit more low-level than `Scanner`, 
but it's **faster** and more **flexible**, especially for reading **strings or characters**.

---

## ✅ Step 1: Setup

To use `BufferedReader`, you need to import and set it up like this and very IMP add **"throws IOException"** in method signature.

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;
```

```java
BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
```

---

## 🟦 Important Points

* `BufferedReader.readLine()` always returns a **String**.
* To read other data types like `int`, `double`, etc., you must **convert (parse)** them manually using `Integer.parseInt()`, `Double.parseDouble()`, etc.
* It throws `IOException`, so your code must handle it.

---

## 🔹 1. Reading **Primitive Data Types**

| Type      | Read as      | Then Parse Using         |
| --------- | ------------ | ------------------------ |
| `int`     | `readLine()` | `Integer.parseInt()`     |
| `double`  | `readLine()` | `Double.parseDouble()`   |
| `long`    | `readLine()` | `Long.parseLong()`       |
| `float`   | `readLine()` | `Float.parseFloat()`     |
| `boolean` | `readLine()` | `Boolean.parseBoolean()` |

### Example:

```java
System.out.print("Enter an int: ");
int i = Integer.parseInt(reader.readLine());

System.out.print("Enter a double: ");
double d = Double.parseDouble(reader.readLine());
```

---

## 🔹 2. Reading **String and Character**

| Type     | Method                        |
| -------- | ----------------------------- |
| `String` | `reader.readLine()`           |
| `char`   | `reader.readLine().charAt(0)` |

### Example:

```java
System.out.print("Enter a word or line: ");
String text = reader.readLine();

System.out.print("Enter a character: ");
char ch = reader.readLine().charAt(0);
```

---

## 🔹 3. Reading **Wrapper Objects**

Just like with primitives, you can read them as strings and convert (parse) them:

```java
System.out.print("Enter an Integer object: ");
Integer myInteger = Integer.valueOf(reader.readLine());

System.out.print("Enter a Boolean object: ");
Boolean myBool = Boolean.valueOf(reader.readLine());
```

---

## 🔹 4. Full Example with All Types

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        System.out.print("Enter an int: ");
        int i = Integer.parseInt(reader.readLine());

        System.out.print("Enter a double: ");
        double d = Double.parseDouble(reader.readLine());

        System.out.print("Enter a long: ");
        long l = Long.parseLong(reader.readLine());

        System.out.print("Enter a float: ");
        float f = Float.parseFloat(reader.readLine());

        System.out.print("Enter a boolean: ");
        boolean b = Boolean.parseBoolean(reader.readLine());

        System.out.print("Enter a string (line): ");
        String line = reader.readLine();

        System.out.print("Enter a character: ");
        char ch = reader.readLine().charAt(0);

        System.out.println("\nYou entered:");
        System.out.println("int: " + i);
        System.out.println("double: " + d);
        System.out.println("long: " + l);
        System.out.println("float: " + f);
        System.out.println("boolean: " + b);
        System.out.println("line: " + line);
        System.out.println("char: " + ch);
    }
}
```

---

## 🔚 Summary: `BufferedReader` vs `Scanner`

| Feature            | `BufferedReader`           | `Scanner`                     |
| ------------------ | -------------------------- | ----------------------------- |
| Input type         | String only (`readLine()`) | Direct types like `nextInt()` |
| Needs parsing      | ✅ Yes                      | ❌ Not always                  |
| Exception handling | Needs `IOException`        | No exception needed           |
| Performance        | Faster                     | Slightly slower               |
| Suitable for       | Large input, file input    | Interactive console input     |

---

# F.1 My code to read primitive int data types
```java
import java.io.BufferedReader;
import java.io.InputStreamReader;

import java.io.IOException;


public class Main {
    
    public static void main(String args[]) throws IOException
    {
        BufferedReader bf = new BufferedReader( new InputStreamReader(System.in));
        
        System.out.println("Enter an int");
        int i = Integer.parseInt(bf.readLine());
        
        System.out.println("Enter an long");
        long l = Long.parseLong(bf.readLine());
        
        System.out.println("Enter an Double");
        double d = Double.parseDouble(bf.readLine());
        
        System.out.println("Enter an float");
        float f = Float.parseFloat(bf.readLine());
        
        System.out.println("Enter an boolean");
        boolean b = Boolean.parseBoolean(bf.readLine());
        
        System.out.println("Enter an int "+i);
        System.out.println("Enter an long "+l);
        System.out.println("Enter an double "+d);
        System.out.println("Enter an long "+f);
        System.out.println("Enter an Boolean" +b);
         
        
    
    }
}
```

# F.2 My code to read Integer, Boolean etc Object. 
```java
import java.io.BufferedReader;
import java.io.InputStreamReader;

import java.io.IOException;


public class Main {
    
    public static void main(String args[]) throws IOException
    {
        BufferedReader bf = new BufferedReader( new InputStreamReader(System.in));
        
        System.out.println("Enter an int");
        Integer i = Integer.parseInt(bf.readLine());
        
        System.out.println("Enter an long");
        Long l = Long.parseLong(bf.readLine());
        
        System.out.println("Enter an Double");
        Double d = Double.parseDouble(bf.readLine());
        
        System.out.println("Enter an float");
        Float f = Float.parseFloat(bf.readLine());
        
        System.out.println("Enter an boolean");
        boolean b = Boolean.parseBoolean(bf.readLine());
        
        System.out.println("Enter an int "+i);
        System.out.println("Enter an long "+l);
        System.out.println("Enter an double "+d);
        System.out.println("Enter an long "+f);
        System.out.println("Enter an Boolean " +b);
         
        
    
    }
}
```

# F.3 My code to read char, word and String 
```java
import java.io.BufferedReader;
import java.io.InputStreamReader;

import java.io.IOException;


public class Main {
    
    public static void main(String args[]) throws IOException
    {
        BufferedReader bf = new BufferedReader( new InputStreamReader(System.in));
        
        System.out.println("Enter an char");
        char ch = bf.readLine().charAt(0);
        
        System.out.println("Enter an Word");
        String word = bf.readLine();
        
        System.out.println("Enter an Line");
        String line = bf.readLine();
        
        System.out.println("Enter an Line but read only word");
        String wordline = bf.readLine().split(" ")[0];
        
        
        System.out.println("Enter an char: "+ch);
        System.out.println("Enter an word: "+word);
        System.out.println("Enter an Line: "+line);
        System.out.println("Enter an word from line: "+wordline);
        
    
    }
}
```
