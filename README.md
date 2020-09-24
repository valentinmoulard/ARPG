# ARPG
 Action RPG project. The inspiration for this project are RPGs in general. The idea is to implement basic feature for a classic RPG game such as a combat system, inventory and shop system, equipement system, skill trees for the different playable classes.
I followed many tutorials to work on this project. Here are the links to their channel.

- Ryan Laley (Unreal engine tutorials) https://www.youtube.com/channel/UCsS5i15vvUbwfr_1JdRKCAA
- DevSquad (Making a RPG in Unreal) https://www.youtube.com/channel/UCz-eYJAUgSE-mqzKtit7m9g
- Astrum Sensei (Creating an Action Role Playing Game in Unreal Engine 4) https://www.youtube.com/channel/UCeaUbzfg8FM8fmx7q_1Xq8w

This current project is not a copy-paste from these tutorials. I try to make the code cleaner, more readable and I try to respect the Solid principles as much as I can so I can extend the current features easily. I often come back on the code I produce as I get more and more experience on this game engine to make the code cleaner, to optimize the code or make the code easier to read and more organized.

Most of the assets come from the Unreal Market place (environment, characters and their animations).


# The Player


 The player can collect ressources (stones or herbs currently), interract with a shop keeper to buy or sell items by pressing the E key to interract with them. The parent class of all character implements an interface called InterractInterface. This one allows to trigger the interract function proper to each objects. Interract with a rock will collect it and put it in the inventory, interract with the shop keeper will display the shop UI and interract with a fire altar will turn on or off the fire.
<p align="center">
  <img src="UE4%20Logs/1.PNG">
</p>


The player can toggle the inventory by pressing the Tab key. For now, this is just a UI to visualize the player's inventory and can't do anything. The player can only click on usable items such as herbs to heal. More items to come later.
<p align="center">
  <img src="UE4%20Logs/2.PNG">
</p>


This is the interface that allows the player to buy or sell items. The shopkeeper has an item table containing the item IDs and their prices. Making different tables will allow to have different shop keeper with different objects in sale and with different prices. The player has the ability to sell items from the inventory or buy from any shop keeper.
<p align="center">
  <img src="UE4%20Logs/3.PNG">
</p>

# Combat System

The player can make combos with auto attacks (This feature was mostly already implemented in the Assets coming with this character model, I just implemented the code in the right place and prepared this character blueprint for the melee combat system such as dealing damage to the enemy, tweaking the attack range, etc).
<p align="center">
  <img src="UE4%20Logs/ComboSystem.gif">
</p>

The player also has abilities he can use (For now most of the abilities have no effects, just visual feedback : animations and UI feedback).
The player can target the nearest enemy by pressing the A key. When an enemy is targeted, the player is allowed to use offensive abilities (damaging abilities or debuffs).
There are 4 types of abilities. The offensive abilities will require a valid target while some non offensive abilities will not.
There are projectiles (fireball damaging the targeted enemy), AOEs (magic circle around the player (not healing the player yet)), Buffs (the buff status appear in the top right corner of the screen) and Debuffs (When the player targets an enemy and cast a debuff, the debuffs status appears under the enemy's health bar).
<p align="center">
  <img src="UE4%20Logs/AbilitySystem1.gif">
  <img src="UE4%20Logs/AbilitySystem2.gif">
</p>

When targeting an enemy, the player's movements will be translated into rotation around the enemy. The player's character will always face the target. When deselecting the target, the player's character will no longer be locked on the enemy. To deselct a target, the player can press the X or W key. The W key is used to target the player's character (disigned for single target buffs).
<p align="center">
  <img src="UE4%20Logs/Target lock and player's movement.gif">
</p>

Targeting an NPC will only lock the player to the target and will display a status bar of the target. The player will move around the target and will always face it.

The player also has the ability to dash forward.
<p align="center">
  <img src="UE4%20Logs/PlayerDash.gif">
</p>


When the player or an enemy dies, they play an animation and it is not possible to interract with them. Their colliders are disabled to prevent blocking passage and it is not possible to lock them or hit them. The dead bodies lay on the ground with simple ragdolls tweaked in the physics assets and turned on when the death animation is finished.
<p align="center">
  <img src="UE4%20Logs/EnemyDead.gif">
</p>
<p align="center">
  <img src="UE4%20Logs/PlayerDead.gif">
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

For now the AI is just following a simple patrol path driven by points set in the world. The AI can loop over these points or stay at the last patrol point. Whenever a player gets in the enemy's sight, the enemy will start to chase the player. The enemy will then get in range to do attacks. 

# Sound

 The current project has many sound effects :
Ambiant music and sounds corresponding to the theme of the environment.
Many SFX like footsteps, sword swings, breathing and voices when attacking.
The two different characters in the game (Shinbi, the player and Yin, the ennemy) have their own sound effects. Shinbi has her own sounds when getting hit, swinging her sword or hitting an ennemy. It's the same for Yin with different sound as they don't have the same voice or weapons. All the sound effects can be tweaked in the viewport by drag and dropping the Cue data containing the sound effects before launching the game.
Every Cue data plays a random sound when played. For exemple, Shinbi has 6 voice lines for getting hit or Yin's whip doing different sound when she hits her opponent.

# Light Environments

 I used light presets to try different result. The project currently use the sunset preset and I did a build with high quality light settings.
<p align="center">
  <img src="UE4%20Logs/Light1.PNG">
  <img src="UE4%20Logs/Light2.PNG">
  <img src="UE4%20Logs/Light3.PNG">
</p>

# Sources

 Musics :
- Ambiant music https://www.youtube.com/watch?v=AY8l-pvTghI
- Ambiant temple sound https://www.soundsnap.com/taxonomy/term/1505/uid:996809
- Various SFX https://opengameart.org/content/fantasy-sound-effects-library / https://opengameart.org/content/3-melee-sounds

Characters :
- Shinbi (character model, textures, voice lines and animations) https://www.unrealengine.com/marketplace/en-US/product/paragon-shinbi
- Yin (character model, textures, voice lines and animations) https://www.unrealengine.com/marketplace/en-US/product/paragon-yin
I worked on the existing animation files to trigger various effects (sounds, particle effects).

Environment :
- Temple https://www.unrealengine.com/marketplace/en-US/product/infinity-blade-temple
I used a premade map level and removed some objects from the scene for performance purposes.
# Coming next

- More feedbacks (visual or sound)
- More abilities
- An additional character to play with different ablities
- Skill tree (a way to enhence abilities)
- Completing the combat system

Currently working on :
- Melee combat system 
