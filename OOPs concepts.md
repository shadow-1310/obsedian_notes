
### variable types
- instance variable (belongs to object)
- class/static variable (belongs to class)
## Method types
Instance Method
- accessor (e.g. getattr)
- mutator (e.g. settattr)
Class Method
- access class variable
- need to use classmethod decorator
- pass <code>cls</code>
Static Method
- doesnot deal with neither instance variable nor class variable
- kind of like helper function within the class
- no need to pass any argument like self or cls in the method
## Design Patterns
- Factory
- Builder
- Singleton

#### Behavioral pattern
- observer
- iterator
- strategy
### Abstract class
- this class defines a structure which each of its subclass must follow. It serves as an blueprint
- in the folllowing example abc - Abstract Base Class
```python
from abc import ABC, abstractmethod

class GameObject(ABC):  # Abstract class for game objects
    def __init__(self, x, y):
        self.x = x
        self.y = y

    @abstractmethod
    def draw(self):
        pass

class Player(GameObject):  # Concrete subclass representing a player character
    def draw(self):
        print(f"Drawing player at ({self.x}, {self.y})")

class Enemy(GameObject):  # Concrete subclass representing an enemy
    def __init__(self, x, y, strength):
        super().__init__(x, y)
        self.strength = strength

    def draw(self):
        print(f"Drawing enemy at ({self.x}, {self.y}) with strength {self.strength}")

# Creating objects of concrete subclasses
player = Player(10, 20)
enemy = Enemy(30, 40, 50)

player.draw()  # Output: Drawing player at (10, 20)
enemy.draw()   # Output: Drawing enemy at (30, 40) with strength 50

```
- This abstract class ensures that all game objects, whether they are players or enemies or any other type, must have a `draw()` method, which is essential for rendering them in the game world.


## Inheritance
- syntax in C++
```cpp
class BaseClass { // Base class members and methods };

class DerivedClass : access-specifier BaseClass { };
```
message passing - interaction of one object with another
access specifier 
- private 
- public
- protected

Encapsulation
- It is a way of combining various data members and member functions that operate on those data members into a single unit

Constructor
- only one constructor should be defined