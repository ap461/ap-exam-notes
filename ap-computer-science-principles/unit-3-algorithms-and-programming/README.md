markdown# AP Computer Science Principles Unit 3: Algorithms and Programming

> How algorithms solve problems and how programs are written using variables, loops, conditionals, and functions. This is the largest unit on the AP CSP exam — covering everything from basic Boolean logic to algorithmic efficiency and undecidable problems.

**Practice all Unit 3 questions, flashcards, and Create Task prep →** [apscore5.com/ap-computer-science-principles/unit-3-algorithms-and-programming](https://www.apscore5.com/ap-computer-science-principles/unit-3-algorithms-and-programming)

---

## What is Unit 3 about?

Unit 3 of AP Computer Science Principles is the **biggest and most important unit on the exam** — making up about 30–35% of multiple-choice questions. You'll learn how algorithms solve problems step by step, how programs use variables and lists to store information, how conditionals (IF/ELSE) and loops (REPEAT, FOR) control program flow, and how procedures (functions) make code reusable. You'll also learn algorithmic efficiency, simulations, and the limits of what computers can do (undecidable problems). Strong Unit 3 understanding is essential for both the multiple-choice exam and the Create Performance Task.

---

## Microtopics in this unit

*Microtopic pages are being added. Check back soon, or visit the [full Unit 3 course on apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-3-algorithms-and-programming) for complete content.*

---

## Key concepts to master

### What is an algorithm?

An **algorithm** is a step-by-step set of instructions for solving a problem. Algorithms must be:

- **Clear** — each step is unambiguous
- **Finite** — must end after a number of steps
- **Effective** — each step must be doable

**Examples:** a recipe, directions to a place, sorting numbers, finding the largest number in a list.

---

## AP CSP pseudocode (memorize this)

The exam uses **AP CSP pseudocode**, not Python or Java.

| Concept | Pseudocode |
|---|---|
| **Assignment** | `a ← 5` |
| **Display** | `DISPLAY(value)` |
| **Input** | `INPUT()` |
| **If statement** | `IF (condition) { }` |
| **If/Else** | `IF (condition) { } ELSE { }` |
| **Repeat n times** | `REPEAT n TIMES { }` |
| **Repeat until** | `REPEAT UNTIL (condition) { }` |
| **List** | `myList ← [1, 2, 3]` |
| **List access** | `myList[1]` ← starts at **1**, not 0 |
| **Procedure** | `PROCEDURE name(parameter) { }` |
| **Random** | `RANDOM(min, max)` |

**⚠️ Critical:** AP CSP lists start at index **1**, not 0. This is different from Python and Java.

---

## Variables and data types

| Concept | What it means |
|---|---|
| **Variable** | A named container that holds a value |
| **Assignment** | Putting a value into a variable (`x ← 5`) |
| **Data type** | The kind of value: number, string, Boolean, list |

### Common data types in AP CSP

| Type | Example |
|---|---|
| **Number** | `42`, `3.14` |
| **String** | `"hello"` |
| **Boolean** | `TRUE` or `FALSE` |
| **List** | `[1, 2, 3]` |

---

## Lists (collections)

A **list** stores multiple values in a single variable. Each element has an **index** (position).

### List operations in AP CSP pseudocode

| Operation | Pseudocode |
|---|---|
| **Create** | `myList ← [10, 20, 30]` |
| **Access** | `myList[2]` (gets 20) |
| **Length** | `LENGTH(myList)` |
| **Append** | `APPEND(myList, value)` |
| **Insert** | `INSERT(myList, index, value)` |
| **Remove** | `REMOVE(myList, index)` |

**Index reminder:** AP CSP lists are **1-indexed**. The first element is `myList[1]`, not `myList[0]`.

---

## Conditionals (decision-making)

**IF statements** let a program make decisions based on a condition.

### IF / ELSE structureIF (condition) {
do this
} ELSE {
do that
}

### Nested conditionalsIF (score ≥ 90) {
DISPLAY("A")
} ELSE {
IF (score ≥ 80) {
DISPLAY("B")
} ELSE {
DISPLAY("Below B")
}
}

### Boolean expressions

A **Boolean expression** evaluates to either TRUE or FALSE.

| Operator | Meaning | Example |
|---|---|---|
| **=** | equal to | `a = 5` |
| **≠** | not equal to | `a ≠ 5` |
| **<** | less than | `a < 5` |
| **>** | greater than | `a > 5` |
| **≤** | less than or equal | `a ≤ 5` |
| **≥** | greater than or equal | `a ≥ 5` |

---

## Boolean (logical) operators

Combine Boolean expressions to make complex conditions.

| Operator | Meaning | Result |
|---|---|---|
| **AND** | Both must be true | TRUE only if both are TRUE |
| **OR** | At least one is true | TRUE if either or both are TRUE |
| **NOT** | Reverses the value | NOT TRUE = FALSE |

### Truth tables

**AND:**

| A | B | A AND B |
|---|---|---|
| T | T | T |
| T | F | F |
| F | T | F |
| F | F | F |

**OR:**

| A | B | A OR B |
|---|---|---|
| T | T | T |
| T | F | T |
| F | T | T |
| F | F | F |

---

## Iteration (loops)

Loops repeat a block of code multiple times.

### Types of loops in AP CSP

| Loop type | What it does |
|---|---|
| **REPEAT n TIMES** | Run a block exactly n times |
| **REPEAT UNTIL (condition)** | Run until the condition becomes TRUE |
| **FOR EACH** | Run once for each item in a list |

### Common loop pitfalls

| Pitfall | What it means |
|---|---|
| **Off-by-one error** | Loop runs one too many or too few times |
| **Infinite loop** | Loop never exits (condition never becomes TRUE) |
| **Wrong loop type** | Used REPEAT n TIMES when REPEAT UNTIL was needed |

---

## Procedures (functions)

A **procedure** is a named block of code that performs a task. Procedures make code reusable and easier to read.

### Procedure structurePROCEDURE name(parameter1, parameter2) {
// body
RETURN value
}

### Key procedure concepts

| Concept | What it means |
|---|---|
| **Procedure** | A reusable block of code |
| **Parameter** | A variable in the procedure definition (a placeholder) |
| **Argument** | The actual value passed to the procedure when called |
| **Return value** | The value the procedure sends back |
| **Procedural abstraction** | Hiding the details of a procedure behind a name |

### Why procedures matter

- **Reusability** — write once, use many times
- **Clarity** — give a long process a meaningful name
- **Easier debugging** — fix one place, fix everywhere
- **Required by Create Task** — you must write at least one student-developed procedure with sequencing, selection, and iteration

---

## Sequencing, selection, and iteration

The three building blocks of all programs.

| Building block | What it means | Example |
|---|---|---|
| **Sequencing** | Steps run in order, one after another | Each line of code |
| **Selection** | Choosing between paths | IF/ELSE statements |
| **Iteration** | Repeating a step | Loops (REPEAT, FOR EACH) |

**Create Task requirement:** your student-developed procedure must include all three.

---

## Algorithms (the bigger picture)

### Common algorithms

| Algorithm | What it does |
|---|---|
| **Linear search** | Check each item one by one until found |
| **Binary search** | Repeatedly halve a sorted list |
| **Sorting (e.g., bubble sort)** | Arrange items in order |
| **Sum / count** | Total or count items meeting a condition |
| **Find max / min** | Find largest or smallest |

### Linear vs binary search

| Feature | Linear search | Binary search |
|---|---|---|
| **Requirement** | Works on any list | List must be **sorted** |
| **Time** | Slow on big lists | Fast even on huge lists |
| **How it works** | Check items one at a time | Halve the list each step |

**Example:** Finding a name in a phone book.
- Linear: read every name from start.
- Binary: open in the middle, see if name is before or after, and repeat.

---

## Algorithmic efficiency

Some algorithms are much faster than others — efficiency matters as data grows.

### Reasonable vs unreasonable time

| Type | Description | Examples |
|---|---|---|
| **Reasonable time** | Time grows polynomially (manageable as input grows) | Linear, quadratic, logarithmic |
| **Unreasonable time** | Time grows exponentially or factorially (impossible at scale) | Trying every possible password, exhaustive routes |

**Key idea:** an algorithm that runs "reasonably" on small data may take **billions of years** on large data if it's exponential.

### Heuristics

A **heuristic** is a "rule of thumb" — an approach that gives a good (but not always perfect) solution faster.

**Examples:**
- GPS finding a "good enough" route, not the absolute shortest
- Spell-check suggesting likely fixes
- Game AI evaluating positions without checking every possibility

---

## Simulations

A **simulation** uses a program to model real-world situations.

### Why use simulations

- Real experiment is too expensive (test pilots, drug trials)
- Real experiment is too dangerous (nuclear reactor failure)
- Real experiment is too slow (climate change over 100 years)
- Real experiment is impossible (alien planet)

### Examples

| Domain | Simulation |
|---|---|
| **Science** | Climate models, particle physics, molecular dynamics |
| **Engineering** | Crash tests, aerodynamics |
| **Medicine** | Drug interaction, surgery training |
| **Games** | Sports, weather in flight simulators |
| **Social** | Traffic, epidemic spread |

### Limitations of simulations

- They are **simplifications** — real world has more variables
- They depend on the accuracy of inputs and assumptions
- They can be biased by the developers' choices
- Random factors are often introduced via `RANDOM()`

---

## Undecidable problems

Some problems **cannot be solved by any algorithm**, no matter how powerful the computer.

### Famous example: the halting problem

There is no general algorithm that can determine, for any program with any input, whether the program will eventually stop or run forever.

**Why it matters:** computing has fundamental limits. Some questions don't have algorithmic answers.

---

## Decidable vs undecidable

| Type | Definition |
|---|---|
| **Decidable** | An algorithm can give a yes/no answer for every input |
| **Undecidable** | No algorithm exists that can give a yes/no answer for every input |

---

## Common AP exam mistakes

- **Forgetting that AP CSP lists start at index 1** (not 0 like Python/Java)
- **Mixing up REPEAT n TIMES and REPEAT UNTIL** — REPEAT n is fixed count; REPEAT UNTIL is condition-based
- **Confusing parameters and arguments** — parameters are in the definition; arguments are passed when calling
- **Tracing AND/OR incorrectly** — AND requires both true; OR requires at least one
- **Off-by-one errors in loops** — runs one too many or too few times
- **Mixing up linear and binary search** — binary requires a **sorted** list
- **Calling exponential algorithms "fast"** — exponential = unreasonable time as input grows
- **Saying every problem can be solved** — the halting problem and other undecidable problems prove this is false
- **Confusing decidable and undecidable** — decidable = an algorithm exists; undecidable = none can exist

---

## How Unit 3 connects to other units

- **Unit 1 (Creative Development)** — algorithms are designed and tested through the development process
- **Unit 2 (Data)** — algorithms operate on data; lists store data
- **Unit 4 (Computer Systems)** — efficient algorithms are critical for networks and distributed computing
- **Unit 5 (Impact of Computing)** — algorithmic bias is a major societal concern
- **Create Performance Task** — every concept in this unit is tested in your project

---

## Top exam topics to prepare

1. **Tracing pseudocode** — predict what a program outputs
2. **List operations** — INSERT, REMOVE, APPEND with correct indices
3. **Boolean logic** — evaluate AND, OR, NOT expressions
4. **Loop logic** — predict how many times a loop runs
5. **Procedure calls** — track parameters and return values
6. **Linear vs binary search** — when each can be used
7. **Algorithmic efficiency** — recognize reasonable vs unreasonable time
8. **Heuristics and simulations** — explain why and when they're used
9. **Undecidable problems** — explain that some problems can't be solved by any algorithm

---

## Frequently asked

**How much of the AP exam is Unit 3?**
Unit 3 is the **biggest unit** on the exam — about 30–35% of multiple-choice questions. Combined with Unit 5 (Impact of Computing), these two units cover over half the exam. If you only have time to focus deeply on one unit, focus on Unit 3.

**What's the difference between linear and binary search?**
Linear search checks each item one at a time from the start — works on any list but can be slow. Binary search repeatedly halves a **sorted** list, eliminating half the possibilities at each step — much faster on large data, but requires the list to be sorted first.

**Why does AP CSP use 1-indexed lists?**
Most real programming languages (Python, Java, C) start lists at index 0. AP CSP intentionally uses 1-indexing to keep things simple for students who may not have prior programming experience — it matches how humans naturally count ("the first item," not "the zeroth item"). On the exam, always start counting list positions at 1.

**What's the difference between a parameter and an argument?**
A parameter is a placeholder in a procedure's definition: `PROCEDURE add(a, b)` — `a` and `b` are parameters. An argument is the actual value you pass when calling the procedure: `add(3, 5)` — `3` and `5` are arguments. The argument is what fills in the parameter.

**What does "reasonable time" mean for an algorithm?**
An algorithm runs in reasonable time if its running time grows as a polynomial of the input size (linear, quadratic, etc.). Algorithms that grow **exponentially** or **factorially** are considered unreasonable — they may finish on small inputs but take billions of years on large ones. This is why we use heuristics for some hard problems instead of trying to find perfect solutions.

**What is a heuristic?**
A heuristic is a "rule of thumb" — an approach that finds a good answer quickly without guaranteeing the best possible answer. GPS apps use heuristics to find quick routes that may not be the absolute shortest. Heuristics let us solve practical versions of problems that are too hard to solve perfectly.

**What is the halting problem?**
The halting problem asks: can we write a single program that, given any program and input, decides whether that program eventually stops or runs forever? Alan Turing proved in 1936 that no such program can exist. The halting problem is the most famous example of an **undecidable** problem — it shows there are limits to what algorithms can do.

**Why are simulations useful?**
Simulations let us model situations that are too expensive, dangerous, slow, or impossible to study in the real world — climate change, plane crashes, disease outbreaks, surgical training, traffic patterns, alien planets. They use programs to predict outcomes based on input variables and rules. But simulations are simplifications, so they depend heavily on the quality of their assumptions.

**Why is procedural abstraction important?**
Procedural abstraction lets you call a procedure by its name without worrying about how it works inside. This is how complex programs stay manageable — once a procedure is written and tested, you can use it anywhere without re-thinking the details. You use procedural abstraction every time you call a built-in function like `RANDOM()` or `LENGTH()`.

---

## Practice this unit

- [Full Unit 3 guide on apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-3-algorithms-and-programming) — 50+ questions, flashcards, Create Task prep
- [Browse all AP CSP units](../)
- [AP CSP course overview](../../ap-computer-science-principles/)

---

*Notes synced from [apscore5.com](https://www.apscore5.com/ap-computer-science-principles/unit-3-algorithms-and-programming). Last updated: May 2026.*
