The Game is a text—based role-playing game in which the player controls a character, fights enemies,
collects items, and completes levels. The code has been refactored using SOLID principles to make it more understandable, flexible, and extensible.

Why is this project useful?
Uses clean and structured code based on SOLID principles.
Easily add new enemies, items, and levels.
It is suitable for teaching object-oriented programming (OOP) and good code.



We've redesigned the game's code to make it cleaner, more convenient, and easier for
further changes. The SOLID principles were used for this.
1. The principle of single responsibility (SRP)
Previously, one class could do too much, now everyone is responsible only for their task.:
Player — manages the player's health, experience, and items.
CombatManager — responsible for the battles.
ItemManager — manages items and their effects.
LevelManager — tracks the player's level.
Enemy and its descendants (Skeleton, Zombie, Vampire) — describe enemies.
This makes the code clearer, and if something breaks, it's easier to find the error.
2. The Open/Closed Principle (OCP)
Now you can easily add new enemies or items without changing the old code. For example, if
you want to add a new monster, you just need to create a new class that inherits from Enemy.
3. The Lisk Substitution Principle (LSP)
All classes of enemies (Skeleton, Zombie, Vampire) behave the same way, but they attack in
different ways. This means that you can easily replace one enemy with another without any
problems.
4. The principle of interface Separation (ISP)
We didn't make huge classes with a bunch of unnecessary methods. For example, the Player has
only the methods he needs, and the ItemManager deals only with items.
5. The principle of dependency inversion (DIP)
Instead of classes depending on each other directly, they work through abstractions (for example,
through Enemy). This makes the code more flexible and easier to change
