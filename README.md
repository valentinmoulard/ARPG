# ARPG
 Action RPG project. The inspiration for this project are RPGs in general. The idea is to implement basic feature for a classic RPG game such as a combat system, inventory and shop system, equipement system, skill trees for the different playable classes.
I followed many tutorials to work on this project. Here are the links to their channel.

https://www.youtube.com/channel/UCsS5i15vvUbwfr_1JdRKCAA - Ryan Laley (Unreal engine tutorials)
https://www.youtube.com/channel/UCz-eYJAUgSE-mqzKtit7m9g - DevSquad (Making a RPG in Unreal)
https://www.youtube.com/channel/UCeaUbzfg8FM8fmx7q_1Xq8w - Astrum Sensei (Creating an Action Role Playing Game in Unreal Engine 4)

This current project is not a copy-paste from these tutorials. I try to make the code cleaner, more readable and I try to respect the Solid principles as much as I can so I can extend the current features easily. I often come back on the code I produce as I get more and more experience on this game engine to make the code cleaner, to optimize the code or make the code easier to read and more organized.

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
The player can target the nearest enemy by pressing the A key. When an enemy is targeted, the player is allowed to use offensive abilities (damaging abilities or debuffs).
There are projectiles (fireball damaging the targeted enemy), AOEs (magic circle around the player (not healing the player yet)), Buffs (the buff status appear in the top right corner of the screen) and Debuffs (When the player targets an enemy and cast a debuff, the debuffs status appears under the enemy's health bar).
<p align="center">
  <img src="UE4%20Logs/AbilitySystem1.gif">
  <img src="UE4%20Logs/AbilitySystem2.gif">
</p>

When targeting an enemy, the player's movements will be translated into rotation around the enemy. The player's character will always face the target. When deselecting the target, the player's character will no longer be locked on the enemy.
<p align="center">
  <img src="UE4%20Logs/Target lock and player's movement.gif">
</p>

# AI

A simple patroling AI following a determined route using Unreal engine's behavior tree and DetouredCroudAIController
<p align="center">
  <img src="UE4%20Logs/AI_Patrol.gif">
</p>

When the player is in the enemy field of view, he wil chase the player. And when the enemy is in range, the enemy will attack and do different attack moves.
<p align="center">
  <img src="UE4%20Logs/Enemy AI Chase and Attack Combo.gif">
</p>


# Sound
The current project has many sound effects :
Ambiant music and sounds corresponding to the theme of the environment.
Many SFX like footsteps, sword swings, breathing and voices when attacking. (Only for the player's character at the moment. SFX for NPCs will be added in the future).

# Light Environments

Used light presets to try different result. The project currently use the sunset preset.
<p align="center">
  <img src="UE4%20Logs/Light1.PNG">
  <img src="UE4%20Logs/Light2.PNG">
  <img src="UE4%20Logs/Light3.PNG">
</p>

# Sources

Musics :
- Ambiant music https://www.youtube.com/watch?v=AY8l-pvTghI
- Ambiant temple sound https://www.soundsnap.com/taxonomy/term/1505/uid:996809
- Shinbi voices https://www.nexusmods.com/skyrim/mods/17736?tab=description
- Various SFX https://opengameart.org/content/fantasy-sound-effects-library / https://opengameart.org/content/3-melee-sounds

Characters :
- Shinbi https://www.unrealengine.com/marketplace/en-US/product/paragon-shinbi
- Yin https://www.unrealengine.com/marketplace/en-US/product/paragon-yin

Environment :
- Temple https://www.unrealengine.com/marketplace/en-US/product/infinity-blade-temple

# Coming next

- More abilities
- An additional character to play with different ablities
- Skill tree (a way to enhence abilities)

Currently working on :
- Melee combat system 
