# Project SAM: Sustecher And Monster
### Project part A report
### Member: 11812301 王浩, 11811408 李昶 11811410 李奇隆
## **Project Abstract**
## **Description**
* Motivation
  * What's the problem?
  * What's your vision for solving the problem?
  * What's your solution
* Feature Description 
  * 2-4 user stories
  * UML use cases (Graph Done, description TODO)
* Requirements
  * Functional Requirements
  * Performance
    * network
    * Graphics
* Design Document
  * Class Diagrams
    * Player
      <div>
        <img src = "Diagram/Player.jpg"></br>
      </div>

      **Class Player**
      > Move:  Move Player to where right-click event is generated \
      > UseSkill: Use a specific skill on a selected target

      **Class Sustecher** 
      > Build: Building a specific building on where left-click event is generated

      **Class Monster**
      > Attack: Dealing damage to a Sustecher or a SustecherBuilding
        
    * Building
      <div>
        <img src = "Diagram/Building.jpg"></br>
      </div>

      **Class SustecherBuilding**
      > Upgrade: Raise the level of the building by 1 \
      > Destory: Destory the building

      **Class House & Class Mine**
      > ProduceGold: Give a specific amount of gold to Sustecher

      **Class WoodFactory**
      > ProduceWood: Give a specific amount of wood to Sustecher

      **Class Market**
      > Get10Woods: Give Sustecher 10 woods by taking an amount of gold from Sustecher \
      > Get100Woods: Give Sustecher 100 woods by taking an amount of gold from Sustecher \
      > Get10Golds: Give Sustecher 10 golds by taking an amount of wood from Sustecher \
      > Get100Golds: Give Sustecher 100 golds by taking an amount of wood from Sustecher

      **Class Tower**
      > Attack: Dealing damage to a monster

      **Class Wall**
      > Defense: Reduce the incoming damage by a certain percentage

    * Skill
      <div>
        <img src = "Diagram/Skill.jpg"></br>
      </div>

      **Class Skill**
      > ApplyTo: Apply a selected skill on a selected target

      **Class Enwind**
      > Limit the monster's movement for a few seconds

      **Class Silence**
      > Keep the monster from using its skills for a few seconds

      **Class Undamageable**
      > Keep the SustecherBuilding from being destroyed by the monster

      **Class Repair**
      
      **Class DetectMap**

      **Class BackHome**
      > 
      **Class Hiding**
      > Keep the monster from being detected by a Sustecher or a SustecherBuilding for a few seconds

* Feasibility
  * Why your can achieve it?
  * Or how?


