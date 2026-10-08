# Assignment 1 — C Fundamentals & Basic Operations (Evidence of Work)

This repository serves as complete evidence and documentation for **Assignment 1**, implemented in **Code::Blocks 25.03**. It covers key C programming topics including arithmetic operations, geometric calculations, string handling, and type conversion.

---

## 📋 Task Overview & Verification Summary

| Task | File Name | Core Objective / Functionality | Evidence Screenshot |
| :--- | :--- | :--- | :--- |
| **Task 1** | `taskfour.c` | Multi-Operation Arithmetic Calculator (`+`, `-`, `*`, `/`, `%`) | `taskone.png` |
| **Task 2** | `tasktwo.c` | Sphere Surface Area Calculation ($A = 4 \pi r^2$) | `tasktwo.png` |
| **Task 3** | `taskthree.c` | String Input Processing (`fgets`) & Length Counting (`strlen`) | `taskthree.png` |

---

## 🧪 Detailed Evidence & Implementation

### Task 1: Basic Arithmetic Calculator (`taskfour.c`)

**Objective:** Prompts the user for two integer values and calculates their sum, difference, product, floating-point quotient, and modulus.

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

#### Verification Evidence
![Task 1 Execution Evidence](/assignmentone/taskone.png)

---

### Task 2: Sphere Surface Area (`tasktwo.c`)

**Objective:** Prompts the user to enter the radius of a sphere, calculates the total surface area using $\text{Surface Area} = 4 \times \pi \times r^2$, and prints the result formatted to 2 decimal places.

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

#### Verification Evidence
![Task 2 Execution Evidence](/assignmentone/tasktwo.png)

---

### Task 3: String Input & Length Determination (`taskthree.c`)

**Objective:** Reads a full line of text safely using `fgets()` and determines the total number of characters using `strlen()`.

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

#### Verification Evidence
![Task 3 Execution Evidence](/assignmentone/taskthree.png)

---


---

## ⚙️ Execution Instructions

1. Clone or download the repository.
2. Open the project file (`.cbp`) in **Code::Blocks 25.03** (or any standard C compiler).
3. Select any desired C file (`taskfour.c`, `tasktwo.c`, or `taskthree.c`).
4. Press **Build and Run** ($F9$).
