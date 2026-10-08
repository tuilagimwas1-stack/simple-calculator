# C Fundamentals — Assignment 1 Implementation

A C-based console application project developed in **Code::Blocks 25.03** containing elementary C programming tasks covering geometric calculations, string manipulation, and arithmetic operations.

---

## 📌 Tasks Overview

| File Name | Topic / Task Focus | Key Functions & Concepts |
| :--- | :--- | :--- |
| `tasktwo.c` | **Sphere Surface Area Calculation** | Preprocessor Directives (`#define PI 3.14159`), Geometric Formula $A = 4 \pi r^2$, `scanf` |
| `taskthree.c` | **String Length & Input Processing** | Safe String Input (`fgets`), String Handling Library (`<string.h>`), `strlen()` |
| `taskfour.c` | **Multi-Operation Arithmetic Calculator** | Fundamental Math (`+`, `-`, `*`, `/`, `%`), Explicit Type Casting `(float)` |

---

## 🛠️ Detailed Task Documentation & Code

### Task 2: Sphere Surface Area (`tasktwo.c`)

Calculates the surface area of a sphere based on the user-provided radius value using the mathematical formula $\text{Surface Area} = 4 \times \pi \times r^2$.

#### Source Code

```c
#include <stdio.h>
#define PI 3.14159

int main() {
    float radius, surfaceArea;

    printf("Enter the radius of the sphere: ");
    scanf("%f", &radius);

    surfaceArea = 4 * PI * radius * radius;

    printf("The surface area of the sphere is: %.2f\n", surfaceArea);

    return 0;
}
```

#### Execution Output

```text
Enter the radius of the sphere: 12
The surface area of the sphere is: 1809.56

Process returned 0 (0x0)   execution time : 3.116 s
Press any key to continue.
```

---

### Task 3: String Input & Length Determination (`taskthree.c`)

Reads a string from standard input safely using `fgets()` and calculates its character length using `strlen()`.

#### Source Code

```c
#include <stdio.h>
#include <string.h>

int main() {
    char name[100];

    printf("Enter your name: ");
    fgets(name, sizeof(name), stdin);

    printf("You entered: %s", name);
    printf("Length of the string: %lu\n", strlen(name));

    return 0;
}
```

#### Execution Output

```text
Enter your name: harun
You entered: harun
Length of the string: 5

Process returned 0 (0x0)   execution time : 5.933 s
Press any key to continue.
```

---

### Task 4: Basic Arithmetic Calculator (`taskfour.c`)

Prompts the user for two integer numbers and displays the results of addition, subtraction, multiplication, floating-point division, and modulus.

#### Source Code

```c
#include <stdio.h>

int main() {
    int num1, num2;
    int sum, difference, product, modulus;
    float quotient;

    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    sum = num1 + num2;
    difference = num1 - num2;
    product = num1 * num2;
    quotient = (float)num1 / num2;
    modulus = num1 % num2;

    printf("Addition: %d\n", sum);
    printf("Subtraction: %d\n", difference);
    printf("Multiplication: %d\n", product);
    printf("Division: %.2f\n", quotient);
    printf("Modulus: %d\n", modulus);

    return 0;
}
```

#### Execution Output

```text
Enter two numbers: 2 34
Addition: 36
Subtraction: -32
Multiplication: 68
Division: 0.06
Modulus: 2

Process returned 0 (0x0)   execution time : 6.849 s
Press any key to continue.
```

---



---

## ⚙️ How to Run

1. Clone or download the repository.
2. Open `assignment1.cbp` in **Code::Blocks**.
3. Select any target file (`tasktwo.c`, `taskthree.c`, or `taskfour.c`) in the left-hand workspace navigation tree.
4. Click **Build and Run** ($F9$).
