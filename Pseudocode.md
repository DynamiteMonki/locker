---
tags:
  - cs
from: AI
Date: 2025-10-26
---
---
## **What is Pseudocode?**

Pseudocode is a way to **plan out** a program using **plain English** (or any language) mixed with simple programming logic. It's like writing a rough draft of your code in human-readable form before writing the actual code.

Think of it as the **outline** you write before an essay, or **sketch** before a painting.

## **Why Use Pseudocode?**

- **No syntax rules**: Don't worry about semicolons, brackets, etc.
- **Focus on logic**: Think about WHAT to do, not HOW to write it
- **Language independent**: Can be translated to any programming language
- **Easy to share**: Non-programmers can understand it
- **Catch mistakes early**: Easier to spot logical errors

## **Pseudocode vs Real Code**

### **Example: Making Coffee**

**Pseudocode:**

text

```
IF coffee machine is OFF
    Turn on coffee machine
    Wait for it to heat up
END IF

Put coffee in filter
Add water to machine
Press brew button
WHILE coffee is brewing
    Wait
END WHILE
Pour coffee into cup
```

**Real Python Code:**

Python

```python
if coffee_machine.status == "OFF":
    coffee_machine.power_on()
    time.sleep(30)
    
coffee_machine.add_coffee(filter)
coffee_machine.add_water()
coffee_machine.brew()
while coffee_machine.is_brewing():
    time.sleep(1)
cup.pour(coffee_machine.get_coffee())
```

## **Common Pseudocode Keywords**

### **Basic Operations:**

- `SET`, `ASSIGN`: Give a value to something
- `INPUT`, `READ`: Get information from user
- `OUTPUT`, `PRINT`, `DISPLAY`: Show information

### **Decision Making:**

- `IF`, `THEN`, `ELSE`, `END IF`: Make choices
- `SWITCH`, `CASE`: Multiple choices

### **Loops:**

- `WHILE`, `END WHILE`: Repeat while something is true
- `FOR`, `END FOR`: Repeat a specific number of times
- `REPEAT`, `UNTIL`: Keep doing until something happens

## **Real Examples**

### **Example 1: Finding the Largest Number**

text

```
SET largest to first number in list
FOR each number in list
    IF number > largest THEN
        SET largest to number
    END IF
END FOR
DISPLAY largest
```

### **Example 2: ATM Withdrawal**

text

```
DISPLAY "Enter PIN"
READ user_pin
SET attempts to 0

WHILE attempts < 3
    IF user_pin equals correct_pin THEN
        DISPLAY "Enter withdrawal amount"
        READ amount
        IF amount <= account_balance THEN
            Dispense cash
            UPDATE account_balance
            DISPLAY "Transaction complete"
        ELSE
            DISPLAY "Insufficient funds"
        END IF
        EXIT
    ELSE
        INCREMENT attempts
        DISPLAY "Wrong PIN. Try again"
        READ user_pin
    END IF
END WHILE

IF attempts equals 3 THEN
    DISPLAY "Card blocked"
END IF
```

### **Example 3: Simple Game Logic**

text

```
SET player_score to 0
SET computer_score to 0

REPEAT
    DISPLAY "Rock, Paper, or Scissors?"
    READ player_choice
    SET computer_choice to random(rock, paper, scissors)
    
    IF player wins THEN
        INCREMENT player_score
        DISPLAY "You win this round!"
    ELSE IF computer wins THEN
        INCREMENT computer_score
        DISPLAY "Computer wins this round!"
    ELSE
        DISPLAY "It's a tie!"
    END IF
    
    DISPLAY scores
    DISPLAY "Play again? (yes/no)"
    READ answer
UNTIL answer is "no"

DISPLAY "Final scores"
```

## **Tips for Writing Good Pseudocode**

### **DO:**

- ✅ Keep it simple and clear
- ✅ Use consistent indentation
- ✅ Be specific about what happens
- ✅ Use descriptive names (not just x, y, z)
- ✅ Include the main logic flow

### **DON'T:**

- ❌ Worry about perfect syntax
- ❌ Include too much detail
- ❌ Use specific programming language features
- ❌ Make it too technical

## **Simple Analogy**

Pseudocode is like:

- **Directions to a friend's house** - "Turn left at the big tree" instead of "Rotate steering wheel 90° counterclockwise at coordinates 40.7128°N"
- **Recipe notes** - "Mix until smooth" instead of specific mixing machine settings
- **Text messages** - Casual but clear, not formal like business letters

**Remember**: Pseudocode is meant to help YOU think through the problem. There's no "wrong" way as long as it makes sense!
