# Module `copy`

Assignments don't copy objects, they create bindings between target and object. For collections that are mutable or contain mutable items, sometimes need a copy is to avoid changing original. This module provides generic shallow ([`copy`](./copy.md)) and deep copy ([`deepcopy`](./deepcopy.md)) operations.

Difference between shallow and deep copying only relevant for compound objects (objects containing other objects, like lists or class instances).
