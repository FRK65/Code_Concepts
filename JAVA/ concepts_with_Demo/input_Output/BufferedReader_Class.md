**BufferedReader**, which is another way to read input from the user in Java. It's a bit more low-level than `Scanner`, 
but it's **faster** and more **flexible**, especially for reading **strings or characters**.

---

## ✅ Step 1: Setup

To use `BufferedReader`, you need to import and set it up like this:

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

Let me know if you want to try reading from files using `BufferedReader` too!
