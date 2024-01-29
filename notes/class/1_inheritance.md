# INHERITANCE

Child class subclassing or extending parent class (*superclass*) to get all parent's functionality and expand upon it.

Can override superclass' implementation, or use `super()` to invoke superclass' version.

```python
class PlayerCharacter(GameCharacter):

  def __init__(self, name, health, pos, num_lives):
    super().__init__(name, health, pos)
    self.max_health = health
    self.num_lives = num_lives

  def take_damage(self, damage):
    self.health -= damage
    if self.health <= 0:
      self.num_lives -= 1
      self.health = self.max_health

  def check_is_dead(self):
    return self.health <= 0 and self.num_lives <= 0
```
