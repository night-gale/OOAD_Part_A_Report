# Project SAM: SUSTecher And Monster
### Project part A report
### Member: 11812301 王浩, 11811408 李昶, 11811410 李奇隆, 11812925 黄子健, 11812622 杨佳雨
## **Project Abstract**
Inspired by the one of the most classical and famous player-made game map *Troll and Elves* from *WarCraft 3*, we plan to develop a "Tower Defense" game that inherits some of the interesting and exciting features of it, and, on top of that, includes more fancy and fantastic functionalities along with additional interaction between players that share a same side or play as opponents to exploit more fun out of it. The basic and also the key game mode of our game would be a online, multi-player and imbalanced combat game also known as Asymmetric Battle Arena Game. Players would be divided into two sides. While one of them play as "Monster" to attack, the others act as "SUSTech" to build **tower** and walls to defend themselves from "Monster". To achieve that, a fairly good understanding about the APIs of the game engine--unreal that we are going to adopt is critical and vital. Moreover, the game experience largely depends on our design and understanding of network synchronization.
## **Description**
### Motivation

* What's the problem?
  + We need to design a fun tower defense gameplay and some interesting game background
  + We need to design a complete game system
  + We need a clear plan and division of labor to complete our game
  + We need to choose a suitable game engine
* What's your vision for solving the problem?
  + discuss to determine the specific gameplay of the game, as well as the background design
  + represent the whole system by drawing UML diagrams
  + compare Unity and Unreal engine, choose better
* What's your solution
  + We spent some time in discussion and made a timetable for whole project
  + We decided a one-to-many gameplay to make our tower defense game fun
  + We drew cases diagram and class diagram to reprsent our system
  + We learn both two engines and final choose Unreal to Implement our project

### Feature Description 

* User stories
Story1:
You can’t image how excited I am when I know we would create a game as our project. I started playing game when I was just four years old. Game is my favorite. In the following years, I played so many different games, such as *WarCraft 3*, *Overwatch*, *Plant VS Zombie* et al. What's more, game is one part of reason for what I learn computer science.But I never think I could create a game as an undergraduate. By this chance, I want to create a game like Trolls and elves which is not popular now but very creative and interesting. Our group will also insert some features of Sustech to make it familiar to us teachers and students. Create an Sustech’s Tower Defense game. 
Story2:
I like playing games but just several games. Maybe I am not a game fan but I would like to create a game. It will be a hard but great process, where I will learn a lot things useful.
* UML use cases 
  <div>
    <img src = "Diagram/use_case.jpg" width=400></br>
  </div>

The whole system is composed of 5 main parts, 
  * Start game (Online/Offline)
  * Load/Save game (For offline)
  * Configurations
  * Account manage system that handles the online game player

### Requirements

* Functional Requirements
  1. A Top-down multi-player online tower defense game
  2. 1 monster vs at most 4 Sustechers
  3. Sustecher will build different kinds of towers to defend and attack the monster
  4. Monster will attack the towers and gain gold to buy equipments
  5. Buildings have multiple levels and functions
  6. Player controller system
  7. Account management system
  8. User friendly interface
  9. (Optional) offline game mode (play with AI or story mode)
  10. (Optional) Not bad character modeling
  11. (Optional) SUSTech-like designed map
* Performance
  * Network: Low-latency online gameplay experience
  * Graphics: Not bad graphics

### Design Document

* Class Diagrams
  * Player
    <div>
      <img src = "Diagram/Player.jpg" width=400></br>
    </div>

    **Class Player**
    > User can choose one of the Player to play in game \
    > Move:  Move Player to where right-click event is generated \
    > UseSkill: Use a specific skill on a selected target

    **Class Sustecher** 
    > Can have multiple Sustechers in one game \
    > Build: Building a specific building on where left-click event is generated

    **Class Monster**
    > Only one in each game \
    > Attack: Dealing damage to a Sustecher or a SustecherBuilding and will give monster an amount of gold according to the magnitude of damage
    
  * Building
    <div>
      <img src = "Diagram/Building.jpg" width=400></br>
    </div>

    **Class SustecherBuilding**
    > The buildings that Sustecher can build and monster can attack
    > Upgrade: Raise the level of the building by 1
    > Destory: Destory the building

    **Class House**
    > The most important building of Sustecher
    > The only source of gold in the early stages of game
    > ProduceGold: Give a specific amount of gold to Sustecher

    **Class Mine**
    > The building that give major gold resource to Sustecher in the mid to last stages of game
    > ProduceGold: Give a specific amount of gold to Sustecher

    **Class WoodFactory**
    > The building that give major wood resource to Sustecher in the mid to last stages of game
    > ProduceWood: Give a specific amount of wood to Sustecher

    **Class Market**
    > The only way that Sustecher can get wood resource in the early stages of game
    > BuyWoods: Give Sustecher an amount of wood by taking an amount of gold from Sustecher
    > BuyGolds: Give Sustecher an amount of gold by taking an amount of wood from Sustecher

    **Class Castle**
    > Some high-level buildings can be built only after this building being built

    **Class Tower**
    > The major building that Sustecher used to attack the monster
    > Attack: Dealing damage to a monster

    **Class Wall**
    > The major building that Sustecher used to defense the attack of monster
    > Defense: Reduce the incoming damage by a certain percentage

    **Class MonsterBuilding**
    > The building that monster can interact with
    > Be built in the beginning of the game
    > Cannot be destroyed

    **Class MonsterShop**
    > The building where monster can use gold to buy equipments to improve itself
  
  	<div>
    	<img src = "Diagram/Skill.jpg" width=400></br>
    </div>

  * Skill
    **Class Skill**
    
> ApplyTo: Apply a selected skill on a selected target
    
    **Class Enwind**
> Limit the monster's movement for a few seconds
    
    **Class Silence**
> Keep the monster from using its skills for a few seconds
    
    **Class Undamageable**
> Keep the SustecherBuilding from being destroyed by the monster
    
    **Class Repair**
> Sustecher can repair the HP of SustecherBuilding in a certain speed
    
    **Class DetectMap**
> Make an area become visible to the monster for a few seconds
    
    **Class BackHome**
> After casting for a few seconds, monster can teleport to a place near the MonsterShop
    
    **Class Hiding**
    
    > Keep the monster from being detected by a Sustecher or a SustecherBuilding for a few seconds

### Feasibility

* Why we can achieve it?
  * Unreal engine provides us a complete system for game development
  * Github can help us accomplish tasks efficiently
  * Good analysis of the game mechanism ensure the efficient development of the game
  * Reasonable timeline guarantees the whole project in an order manner
  * Suitable work load ensures that development of every parts of the game goes on smoothly
  >* ****


