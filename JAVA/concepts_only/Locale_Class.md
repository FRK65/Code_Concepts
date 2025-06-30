
# 1. what is Locale in java explain 

- In Java, the **Locale class** is a part of the **java.util** package and represents a specific geographical, political, or cultural region. 
- It is used primarily for internationalization (i18n), allowing your program to adapt to **different languages, countries, and cultural customs.**
- It helps Java programs:
1. Format dates, times, and numbers.
2. Display messages in different languages.
3. Handle region-specific conventions like currency, sorting order, and case conversion.


| Feature         | Description                                    |
| --------------- | ---------------------------------------------- |
| Class Name      | `java.util.Locale`                             |
| Used For        | Internationalization                           |
| Key Components  | Language, Country, Variant                     |
| Related Classes | `ResourceBundle`, `DateFormat`, `NumberFormat` |

🔹 Basic Syntax:

```java

import java.util.Locale;

Locale locale = new Locale("en", "US");  // English language, United States

```

You can also use predefined constants:

```java
Locale locale = Locale.FRANCE;
```

---

🔹 Constructor:

```java

Locale(String language)
Locale(String language, String country)
Locale(String language, String country, String variant)

```

* **language** – ISO 639 code (e.g., "en" for English, "fr" for French)
* **country** – ISO 3166 code (e.g., "US" for United States, "FR" for France)
* **variant** – Optional for region-specific variations.

---

🔹 Common Use Cases:

 1. **Formatting Numbers**:

```java

NumberFormat nf = NumberFormat.getCurrencyInstance(Locale.US);
System.out.println(nf.format(1000)); // $1,000.00

```

 2. **Formatting Dates**:

```java

DateFormat df = DateFormat.getDateInstance(DateFormat.LONG, Locale.FRANCE);

System.out.println(df.format(new Date()));

```

 3. **Localizing Messages**:

Using `ResourceBundle` with `Locale` to show messages in different languages.



 🔹 Predefined Locales:

Java provides many built-in `Locale` constants:

* `Locale.US`
* `Locale.UK`
* `Locale.JAPAN`
* `Locale.CHINA`
* `Locale.CANADA_FRENCH`
  …and more.



🔹 Example:

```java
import java.util.*;

public class LocaleExample {
    public static void main(String[] args) {
        Locale locale = new Locale("fr", "FR"); // French, France
        System.out.println("Language: " + locale.getLanguage());
        System.out.println("Country: " + locale.getCountry());
    }
}
```

**Output:**

```
Language: fr
Country: FR
```

---

# My Code : 

```java
import java.text.NumberFormat;
import java.time.LocalDate;
import java.util.Locale;
public class Main {
    public static void main(String[] args) {
        
        
        Locale lc = new Locale("en", "US");

        NumberFormat nf = NumberFormat.getCurrencyInstance(lc);

        double amount = 123456.789;
        
        String formattedAmount = nf.format(amount);

        System.out.println(formattedAmount);

    }
}
```

