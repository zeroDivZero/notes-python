# SYNTAX

```python
class GameCharacter:

  # constructor or initializer
  def __init__(self, name, health, pos):
    self.name = name
    self.health = health
    self.pos = pos

  def move(self, by_amount):
    self.pos += by_amount

  def take_damage(self, damage):
    self.health -= damage
    if self.health < 0:
      self.health = 0

  def check_is_dead(self):
    return self.health <= 0
```

Typically instance methods and constructor take `self` as first arg.

## Create Object

```python
game_character = GameCharacter('John', 100, 5)
game_character.move(-2)
game_character.take_damage(20)
print(game_character.check_is_dead())
```
