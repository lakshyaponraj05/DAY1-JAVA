# DAY1-JAVA
# 📘 Java Calculator Program

This is a simple **Java console-based calculator** that performs the following operations:

* Addition
* Subtraction
* Multiplication
* Division

The program uses **Object-Oriented Programming (OOP)** principles by defining a `Calculator` class with methods for each arithmetic operation.

---

## 🔹 Program Explanation

### 1. **Calculator Class**

```java
class Calculator {
    int a, b;

    Calculator(int a, int b) {
        this.a = a;
        this.b = b;
    }
```

* The class has two integer variables `a` and `b` which store the user input numbers.
* The constructor initializes these values when a new `Calculator` object is created.

---

### 2. **Methods**

Each arithmetic operation is defined in a separate method:

```java
public String addition() {
    int sum = a + b;
    return "Addition = " + sum;
}

public String subtraction() {
    return "Subtraction = " + (a - b);
}

public String multiplication() {
    return "Multiplication = " + (a * b);
}

public String division() {
    if (b == 0) {
        return "Invalid (division by zero)";
    } else {
        return "Division = " + ((float) a / b);
    }
}
```

* `addition()` → returns the sum of `a` and `b`.
* `subtraction()` → returns the difference.
* `multiplication()` → returns the product.
* `division()` → checks for division by zero. If `b == 0`, it returns an error message, otherwise it returns the division result as a `float`.

---

### 3. **Main Method**

```java
Scanner sc = new Scanner(System.in);

System.out.print("Enter first number: ");
int x = sc.nextInt();
System.out.print("Enter second number: ");
int y = sc.nextInt();

Calculator calc = new Calculator(x, y);
```

* The program takes two numbers from the user using `Scanner`.
* A `Calculator` object is created with these numbers.

---

### 4. **Switch Case (Menu-Driven Program)**

```java
System.out.println("1) Addition");
System.out.println("2) Subtraction");
System.out.println("3) Multiplication");
System.out.println("4) Division");
System.out.print("Enter your choice: ");
int choice = sc.nextInt();

switch (choice) {
    case 1: System.out.println(calc.addition()); break;
    case 2: System.out.println(calc.subtraction()); break;
    case 3: System.out.println(calc.multiplication()); break;
    case 4: System.out.println(calc.division()); break;
    default: System.out.println("Invalid choice");
}
```

* The program displays a menu with 4 options.
* The user selects an operation.
* The corresponding method is executed, and the result is printed.

---

## 🔹 Sample Output

```
Enter first number: 10
Enter second number: 5
1) Addition
2) Subtraction
3) Multiplication
4) Division
Enter your choice: 4
Division = 2.0
```

---

## ✅ Key Features

* Uses **OOP concepts** (class, constructor, methods).
* Handles **division by zero** gracefully.
* Simple **menu-driven interface** with `switch` statement.
* Beginner-friendly Java example for practicing classes and methods.

---
