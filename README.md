## Special Methods (Dunder Methods)

Special methods in Python begin and end with double underscores (e.g., `__init__`). They allow custom classes to hook into Python's built-in syntax and operators, enabling features like custom print outputs, math operations, and collection behaviors.

### Core Examples
*   `__init__(self, ...)`: Runs automatically when a new object is created.
*   `__str__(self)`: Defines a clean text output when using `print()`.
*   `__add__(self, other)`: Configures custom behavior for the `+` operator.

### Quick Syntax Implementation
```python
class Item:
    def __init__(self, name, cost):
        self.name = name
        self.cost = cost

    def __str__(self):
        return f"{self.name}: ${self.cost}"

    def __add__(self, other):
        return self.cost + other.cost

# Usage
item1 = Item("Coffee", 4)
item2 = Item("Cookie", 3)

print(item1)      # Output: Coffee: $4
print(item1 + item2)  # Output: 7
