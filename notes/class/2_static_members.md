# STATIC MEMBERS

Static variables or methods shared across all instances of class.

When defining, use class name rather than `self` keyword.

```python
class GameCharacter:

  speed = 1.0

  # static method to update static variable, no `self`
  def change_speed(to_speed):
    GameCharacter.speed = to_speed

  # remaining implementation

# usage
print(GameCharacter.speed)  # 1.0
GameCharacter.change_speed(2.0)
print(GameCharacter.speed)  # 2.0
```
