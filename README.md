# Temple of Death
A 2D CLI-Based Game written in C++ for first semester final project
**Note: If you want to play level 2 - The Location Code is: ABCXYZ**

Demo Video: [LinkedIn](https://www.linkedin.com/posts/muhammad-anas-650070281_excited-to-share-my-project-temple-of-activity-7149399926278438912-3i7W?utm_source=share&utm_medium=member_desktop)

![tod](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/935837d6-a8be-449f-b14f-77eb8df01261)
## Game Description
The game is set in a 2D maze, viewed from a side-scrolling perspective, and is divided into two segments: the Temple and the Boss Arena. The Temple features a labyrinth with challenges like burners and chests that require fire to open. Items are collected upon player collision, while contact with enemy projectiles decreases health. Running out of health results in a game over. Players shoot based on their weapon's gauge, which increases over time as stamina is recovered. Different weapons have varying gauge requirements. The player's score rises with interactions such as chest destruction, item collection, and hitting enemies with bullets. The primary objective is to collect scrolls while surviving.
The Boss Arena comprises a bordered area with a weakened seal at the center. Upon spotting the player, the devil initiates random moves, generating obstacles that players must evade while causing damage to the central seal. Once the boss's health is depleted, the devil is sealed, and the player successfully completes the game.
## Background Story
A long time ago, the Devil used to make a lot of trouble, but then four Spirit Magicians sealed him away, bringing peace to the world. Everything was fine until a creepy pool of blood showed up in a temple. The four magicians were found dead with a note saying the Earth would meet the Devil again. People who study spooky stuff thought the magicians might have turned into the Devil to destroy everything.
Only the original four magicians knew where the Devil was sealed, and the temple where they died had a bunch of secrets. Even though many folks tried to figure things out, nobody ever came back. The temple got famous as the 'Temple of Death,' a place where bad things happened, and people who tried to uncover its secrets never made it out.
## Characters
| Character   | Description                                                                                                                                                                                                                                                             |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 👾 Player      | The player is a daring human with magical gloves, allowing them to shoot various projectiles. Their mission is to escape the deadly temple, which has claimed the lives of many adventurers before. The fate of the player in the temple of death is uncertain.                   |
| 🗡️ Barbarian   | Barbarians patrol a given horizontal range quickly, armed with a spear. Brainwashed by the devil, they protect the temple's secrets at all costs. A spear hit from a barbarian results in a drop in the player's health.                                                |
| 🎯 Archer      | Archers, clones of the devil, appear at random locations, facing a specific direction, and shoot arrows at different rates. They guard chests and block the player's path, posing a threat with their deadly arrows.                                                   |
| 🧙 Magicians   | The origin of magicians is unknown, but they are believed to be the evil spirits of four magicians who sealed the devil. These ghostly magicians throw magical orbs, adding another layer of challenge to the player's journey through the temple.                                  |
| 💣 Bombers     | Bombers, also devil clones, are summoned in the boss arena. They chase the player and explode upon getting too close, causing damage and sacrificing themselves. These explosive foes are a formidable challenge in certain parts of the game.                                |
| 👹 Devil       | The devil itself never appears, but its actions and noises emanate from the seal in the boss arena. The transmutation circle with four moves signifies the devil's attempts to hinder the player. Before being spotted, the devil weakened the seal, preparing for a showdown in the arena. |
## Game Objects
Game objects can be divided into three categories; hard objects, collectibles and projectiles. Hard objects are static through which no other object can pass through. Collectibles are also hard objects but the player can collect them, also known as “items”. Projectiles are dynamic objects, which can collide with characters or other hard objects.
| Game Object          | Description                                                                                                                                                                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🧱 Wall**           | Wall is a hard object that provides structure to the maze and acts as a border to the temple and boss arena.                                                                                                                                                         |
| **🌴 Plank**          | Plank is a hard object that appears many times in the temple of death.                                                                                                                                                                                               |
| **💧 Water**          | Water is a hard object (since the player can’t swim) and usually appears in pools along with plants.                                                                                                                                                               |
| **🌿 Plant**          | Plant is a hard object that usually appears with water in the temple. Players can hide behind plants as they block projectiles. Plants can be trees, bushes, or any green object.                                                                                    |
| **🧱 Brick**          | Brick is a hard object sometimes seen in the maze.                                                                                                                                                                                                                   |
| **🗿 Rock**           | Rock is a hard object that players can hide behind as it blocks projectiles. Sometimes, rocks also appear as hurdles.                                                                                                                                               |
| **🛡️ Steel**         | Steel is a hard object usually seen with treasures or burners.                                                                                                                                                                                                      |
| **🔥 Burner**         | Burner is a hard object emitting fire at a set rate and staying for a set duration. Players must avoid the fire emitted by burners.                                                                                                                                  |
| **🔥 Fire**           | Fire is a collectible object emitted by burners. It damages the player upon collection.                                                                                                                                                                            |
| **📦 Chest**          | Chest is a hard object with set durability. When broken, it usually contains an item (collectible object). To break a chest, players need to shoot projectiles towards it.                                                                                           |
| **📜 Scroll**         | Scroll is a collectible item; there are only 7 scrolls in the temple of death. Collecting them is the main objective of the first stage. Once all 7 scrolls are recited by the player, the location of the devil's seal is revealed.                                   |
| **💊 Aspirin**        | Aspirin is a collectible item that increases the player's health.                                                                                                                                                                                                    |
| **⚡ Stamina**        | Stamina is a collectible item that recovers the player's stamina, allowing them to shoot more.                                                                                                                                                                      |
| **👁️‍🗨️ Curse of Devil Eye** | "Curse of devil eye" is a collectible item that damages the player's eyesight. In-game mechanics, it makes the screen flicker in black and gray for a set interval of time.                                                                                       |
| **🌀 Curse of Mirage** | "Curse of mirage" is a collectible item that gives an illusion to the player. In-game mechanics, it inverts the screen vertically, inverting vertical controls and confusing the player.                                                                            |
| **🍂 Curse of Wither** | "Curse of wither" is a collectible item that decreases the player's health over a set interval of time. The curse vanishes after some time.                                                                                                                       |
| **☠️ Curse of Venom**  | "Curse of venom" is a collectible item that poisons the player, sucking out all its stamina, making the player unable to shoot well for some time.                                                                                                                |
| **📌 Bullet**         | Bullet is a projectile that only the player can shoot. It has a low gauge requirement, damage, and range.                                                                                                                                                           |
| **💫 Lazer**          | Lazer is a projectile that only the player can shoot. It has a medium gauge requirement, damage, and range.                                                                                                                                                         |
| **💥 Spread Ball**     | Spread Ball is a projectile that only the player can shoot in a set of 3. It has the highest gauge requirement, damage, and range.                                                                                                                                  |
| **🏹 Arrow**          | Arrow is a projectile that only archers can shoot. It is poisonous, and the player must avoid it.                                                                                                                                                                  |
| **🔮 Orb**           | Orb is a projectile emitted by magicians in a set of 4 and placed by the devil all over the area. Its damage is one of the highest in the game, and it must be avoided at all costs.                                                                             |
| **💣 Dynamite**        | Dynamite is a collectible placed by the devil all over the area, exploding after a set interval. If the player is under the explosion radius, it causes damage.                                                                                                 |

## Player Objective
The game has two main parts. First, players need to get through the Temple of Death, which is a huge maze. They need to dodge obstacles, deal with foes, and open chests. Some chests have bad stuff like curses, some have good things to boost health and stamina, and some got the scrolls. You need to = collect all 7 scrolls to find out where the Devil was sealed. Once you got all the scrolls, a secret code shows up, letting you teleport to the right spot.
Now, at this new location, there's a big showdown waiting for you - a boss fight. You need to face off against the Devil and put him back in his place. It's all about strategy and skill in this part. The Temple and the Boss Arena add a cool and challenging twist to the game.
## Rules and Interactions
Player can move in four different directions (vertical and horizontal), using the Arrow keys and it can switch weapons using Q (left) and E (right) keys, the player can shoot projectiles using the W, A, S, D (keys) each key representing 4 different directions (vertical and horizontal). The player can only move through white spaces or collectible items. Different collision cases are handled differently in the game.

## Curses Preview
#### Curse of Mirage
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/bce53412-0987-4440-a71c-d3bceb3afc1f)
#### Curse of Devil Eye
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/60efd3ba-a365-47d7-b3b0-05c849f7cd64)
#### Curse of Wither
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/7bec86d2-7327-4c80-ace6-42e7243cd02d)
## Boss Fight Preview
#### Explosive Barrage
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/979b7c3f-95cb-4a56-9168-d611c9f394ad)
#### Orb Cyclone
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/4444b2a2-b632-442d-8af3-15b641b94de3)
#### Blow It Up !
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/9bf6f689-12a6-43f7-b6cf-6a021da9a94f)
#### Total Chaos
![image](https://github.com/m-ans-ishfaq/temple-of-death-game/assets/150812466/3e89f9a0-32fc-4260-99c0-fb5507edd646)

**Note: Any kind of music/sound effect doesn't belong to me, I have only used them for my own learning purposes**

Thanks for Reading ❤️
