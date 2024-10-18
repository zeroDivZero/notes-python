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

## Inheritance Behaviors

Even if child class doesn't implement parent's method, that method still available to child instances **implicitly**.

If child class **overrides** a parent's method, it can completely replace it, or extend parent's functionality by adding logic before or after parent's method.

```python
class Parent(object):
    def implicit(self):
        print('PARENT implicit()')

    def override_replace(self):
        print('PARENT override_replace()')

    def override_extend(self):
        print('PARENT override_extend()')


class Child(Parent):
    def override_replace(self):
        print('CHILD override_replace()')

    def override_extend(self):
        print('CHILD, BEFORE PARENT override_extend()')
        super(Child, self).override_extend()  # or simply super().override_extend()
        print('CHILD, AFTER PARENT override_extend()')


parent = Parent()
child = Child()

# child instance calls parent's method
parent.implicit()  # PARENT implicit()
child.implicit()  # PARENT implicit()

# child instance calls own override method
parent.override_replace()  # PARENT override_replace()
child.override_replace()  # CHILD override_replace()

# child instance calls own override method that calls parent's
parent.override_extend()  # PARENT override_extend()
child.override_extend()
# CHILD, BEFORE PARENT override_extend()
# PARENT override_extend()
# CHILD, AFTER PARENT override_extend()
```
