# Debugging Tasks - ChatGPT Introduction

## Overview

This project contains several debugging and documentation tasks using Python, HTML, and JavaScript. The goal is to identify issues in the provided code, fix bugs, improve program behavior, and add proper documentation or error handling where needed.

---

## Task 0 - Python Factorial

**File:** `factorial.py`

### Objective

Fix a Python program that calculates factorial values.

### Problem

The program entered an infinite loop because the value of `n` was never updated inside the `while` loop.

### Solution

Added:

```python
n -= 1
```

This allows the loop to decrease `n` until it reaches 1 and correctly returns the factorial result.

---

## Task 1 - Python Arguments

**File:** `print_arguments.py`

### Objective

Print only command-line arguments without printing the script filename.

### Problem

`sys.argv` includes the Python file name as the first element.

### Solution

Modified the loop to start from index `1`:

```python
sys.argv[1:]
```

This skips the filename and prints only user-provided arguments.

---

## Task 2 - HTML / JavaScript Background Color

**File:** `change_background.html`

### Objective

Change the page background color when clicking a button.

### Problem

The button ID in HTML did not match the ID used in JavaScript.

### Solution

Corrected the button ID from:

```html
colorButon
```

to:

```html
colorButton
```

This allowed JavaScript to properly detect button clicks.

---

## Task 3 - Python Minesweeper

**File:** `mines.py`

### Objective

Implement a winning condition for the Minesweeper game.

### Problem

The game only detected losing conditions when a mine was hit and never checked if the player had successfully revealed all safe cells.

### Solution

Added a `check_win()` method that verifies whether all non-mine cells are revealed. The game now prints:

```text
Congratulations! You've won the game.
```

when the player wins.

---

## Task 4 - Recursive Factorial Documentation

**File:** `factorial_recursive.py`

### Objective

Document the factorial function and correct formatting.

### Problem

The file lacked comments/documentation and contained indentation problems.

### Solution

Added a structured docstring including:

* Function description
* Parameters
* Returns

Also fixed indentation to ensure correct execution.

---

## Task 5 - Python Checkbook Error Handling

**File:** `checkbook.py`

### Objective

Prevent program crashes caused by invalid input.

### Problem

Entering non-numeric values caused a `ValueError` and terminated the program.

### Solution

Implemented:

```python
try / except ValueError
```

for deposit and withdrawal inputs so invalid entries are handled gracefully.

---

## Task 6 - Python Tic Tac Toe

**File:** `tic.py`

### Objective

Fix multiple gameplay and input handling issues.

### Problems Identified

* No validation for non-numeric input
* No range validation for board coordinates
* Incorrect winner announcement
* Missing draw detection
* Insufficient input testing

### Solution

Implemented:

* `try/except` for invalid input
* Coordinate range checking
* Correct winner logic
* Draw detection using a board-full check
* Improved overall game flow and reliability

---

## Conclusion

These debugging tasks demonstrate how to:

* Identify and fix logic errors
* Handle user input safely
* Improve game mechanics
* Add proper documentation
* Build more reliable and maintainable code

