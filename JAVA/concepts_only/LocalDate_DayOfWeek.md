## 📆 What is `LocalDate` in Java?

✅ Definition:

* `LocalDate` is a **class** in the `java.time` package.
* It represents a **date only** (no time or timezone), like `2025-06-30`.
* It is a **final class**, so it **cannot be extended**.
* Implements the `Temporal`, `ChronoLocalDate`, and `Comparable` interfaces.

✅ When to Use:

* When you only need the **year, month, and day** (e.g., birthdays, holidays, deadlines).
* For date calculations: adding/subtracting days, comparing dates, etc.

✅ Example:

```java
LocalDate date = LocalDate.of(2025, 6, 30);
System.out.println(date); // 2025-06-30
```

---

## 📅 What is `DayOfWeek` in Java?

✅ Definition:

* `DayOfWeek` is an **enum** in `java.time` package.
* It represents the **seven days of the week**: `MONDAY`, `TUESDAY`, ..., `SUNDAY`.
* It is an **enum**, not a class or interface.
* Each constant (`MONDAY`, `TUESDAY`, etc.) has an associated **numeric value** (1 to 7).

 ✅ When to Use:

* When you want to **find out the day of the week** for a given date.
* Useful in scheduling, business rules (e.g., "only run on weekdays"), or UI display.

✅ Example:

```java
LocalDate date = LocalDate.of(2025, 6, 30);
DayOfWeek day = date.getDayOfWeek();  // MONDAY
System.out.println(day);              // MONDAY
System.out.println(day.getValue());   // 1 (Monday = 1, Sunday = 7)
```

---

✅ Summary Table:

| Feature     | `LocalDate`               | `DayOfWeek`         |
| ----------- | ------------------------- | ------------------- |
| Type        | Class (final)             | Enum                |
| Package     | `java.time`               | `java.time`         |
| Represents  | Date (year, month, day)   | Day of the week     |
| Example Use | `LocalDate.of(2025,6,30)` | `MONDAY`, `TUESDAY` |

---

# Code Example :
You are given a date. You just need to write the method, , which returns the day on that date. To simplify your task, we have provided a portion of the code in the editor.
```java
import java.time.LocalDate;
import java.time.DayOfWeek;

 public static String findDay(int month, int day, int year)
{
        LocalDate date = LocalDate.of(year, month, day);

        DayOfWeek dayOfWeek = date.getDayOfWeek();

        return dayOfWeek.toString();
}
```

