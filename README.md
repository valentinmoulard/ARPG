# ARPG
 Action RPG project. The inspiration for this project are RPGs in general. The idea is to implement basic feature for a classic RPG game such as a combat system, inventory and shop system, equipement system, skill trees for the different playable classes.
I followed many tutorials to work on this project. Here are the links to their channel.

https://www.youtube.com/channel/UCsS5i15vvUbwfr_1JdRKCAA - Ryan Laley (Unreal engine tutorials)
https://www.youtube.com/channel/UCz-eYJAUgSE-mqzKtit7m9g - DevSquad (Making a RPG in Unreal)

This current project is not a copy-paste from the tutorials I follow. I try to make the code cleaner, more readable and I try to respect the Solid principles as much as I can so I can extend the current features easily.

Most of the assets come from the Unreal Market place (environment, characters and their animations).


# Current Features


The player can collect ressources, interract with a shop keeper to buy or sell items by pressing the E key.
<p align="center">
  <img src="UE4%20Logs/1.PNG">
</p>


The player can show the inventory by pressing the Tab key
<p align="center">
  <img src="UE4%20Logs/2.PNG">
</p>


This is the interface that allows the player to buy or sell items.
<p align="center">
  <img src="UE4%20Logs/3.PNG">
</p>


The player can make combos with auto attacks (This feature was mostly already implemented in the Assets coming with this character model, I just implemented the code in the right place and prepared this character blueprint for the melee combat system)
<p align="center">
  <img src="UE4%20Logs/ComboSystem.gif">
</p>

The player also has abilities he can use (For now most of the abilities have no effects, just visual feedback : animations and UI feedback).
There are projectiles (fireball damaging the targeted enemy), AOEs (magic circle around the player (not healing the player yet)), Buffs (the buff status appear in the top right corner of the screen) and Debuffs (When the player targets an enemy and cast a debuff, the debuffs status appears under the enemy's health bar).
<p align="center">
  <img src="UE4%20Logs/AbilitySystem1.gif">
  <img src="UE4%20Logs/AbilitySystem2.gif">
</p>

# AI

<p align="center">
  <img src="UE4%20Logs/AI_Patrol.gif">
</p>

# Light Environments

Used light presets to try different result.
<p align="center">
  <img src="UE4%20Logs/Light1.PNG">
  <img src="UE4%20Logs/Light2.PNG">
  <img src="UE4%20Logs/Light3.PNG">
</p>

# Coming next

- More abilities
- An additional character to play with different ablities
- Skill tree (a way to enhence abilities)
- Melee combat system
