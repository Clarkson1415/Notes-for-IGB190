# IGB190 Game Mechanics Implementation

Grace Clarkson

# Contents
- [igb190 Game Mechanics Implementation](#igb190-game-mechanics-implementation)
- [Contents](#contents)
- [Weekly outline](#weekly-outline)
- [Teaching team](#teaching-team)
- [Class times](#class-times)
- [Assignments](#assignments)
- [Lecture 1](#lecture-1)
  - [Low level game design](#low-level-game-design)
  - [igb 190](#igb-190)
  - [Major Topic C# scripting and Unity](#major-topic-c-scripting-and-unity)
  - [Melee Combat Systems](#melee-combat-systems)
  - [animation driven systems](#animation-driven-systems)
  - [on hit events](#on-hit-events)
  - [RPG mechanicss](#rpg-mechanicss)
  - [assignment 1 Part A](#assignment-1-part-a)
  - [assignment 1 part B](#assignment-1-part-b)
- [Wk 2: Unity Scripting](#wk-2-unity-scripting)
- [Lecture 2](#lecture-2)
  - [the game loop](#the-game-loop)
  - [Data Types](#data-types)
  - [Arrays, Lists etc](#arrays-lists-etc)
  - [Logic and Conditionals](#logic-and-conditionals)
  - [for loops](#for-loops)
  - [quick activity using arrays for loops](#quick-activity-using-arrays-for-loops)
  - [methods](#methods)
  - [Args and Parameters](#args-and-parameters)
  - [Structs](#structs)
  - [Class](#class)
  - [Inheritance](#inheritance)
  - [Unity C# public variables](#unity-c-public-variables)
  - [unity intantiate()](#unity-intantiate)
  - [unity GetComponent()](#unity-getcomponent)
  - [Assignment 1 Part B Questions](#assignment-1-part-b-questions)
- [Workshop wk2](#workshop-wk2)
  - [Nav Mesh Surface](#nav-mesh-surface)
  - [**Unity Prebuilt Methods**](#unity-prebuilt-methods)
  - [**Variables and Variable Types**](#variables-and-variable-types)
  - [Mouse and Keyboard Input](#mouse-and-keyboard-input)
  - [GetComponent](#getcomponent)
- [Wk3: Principles of Game Mechanics](#wk3-principles-of-game-mechanics)
    - [MDA Framework?](#mda-framework)
    - [Mechanics, dynamics, aesthetics](#mechanics-dynamics-aesthetics)
    - [Game dev vs mda](#game-dev-vs-mda)
    - [Rules → mechanics → systems](#rules--mechanics--systems)
  - [Rules are simple mostly](#rules-are-simple-mostly)
  - [Mechanics are intricate](#mechanics-are-intricate)
  - [Systems are complex](#systems-are-complex)
  - [FPS mechanics ray casting](#fps-mechanics-ray-casting)
  - [**Raycasting in C# \& Unity**](#raycasting-in-c--unity)
  - [platformer mechanics](#platformer-mechanics)
  - [platformer mechanics edge leyway](#platformer-mechanics-edge-leyway)
  - [platformer mech - ballistics](#platformer-mech---ballistics)
  - [ballistic equations](#ballistic-equations)
  - [Ballistic Equation in C# and unity](#ballistic-equation-in-c-and-unity)
  - [Input Queuing](#input-queuing)
  - [2**Input Queue in C# \& Unity**](#2input-queue-in-c--unity)
  - [Portal - Portal Gun](#portal---portal-gun)
  - [Object Collider Interactions and Events](#object-collider-interactions-and-events)
- [Workshop wk3](#workshop-wk3)
  - [Animations](#animations)
  - [Wk3 Questions](#wk3-questions)
- [Wk4 Lecture notes: designing gameplay Interactions](#wk4-lecture-notes-designing-gameplay-interactions)
  - [Animation Events](#animation-events)
  - [collider interactions](#collider-interactions)
  - [What is a collider](#what-is-a-collider)
  - [on hit events](#on-hit-events-1)
  - [Unity and C# colliders and on hit events](#unity-and-c-colliders-and-on-hit-events)
  - [activity collider event](#activity-collider-event)
  - [Fighting games](#fighting-games)
  - [Hit boxes and Hurtboxes](#hit-boxes-and-hurtboxes)
  - [Startup, active and recovery](#startup-active-and-recovery)
  - [blocking and parry](#blocking-and-parry)
  - [blockstun and hitstun](#blockstun-and-hitstun)
  - [activity](#activity)
  - [frame data analysis](#frame-data-analysis)
  - [frame data analysis](#frame-data-analysis-1)
  - [frame advantage and footsies](#frame-advantage-and-footsies)
  - [and in other games](#and-in-other-games)
  - [animation driven systems](#animation-driven-systems-1)
- [Workshop wk4](#workshop-wk4)
  - [Player and Enemy Combat](#player-and-enemy-combat)
  - [Interfaces](#interfaces)
  - [Change the name of build or its ICON](#change-the-name-of-build-or-its-icon)
- [Lecture 5 Game devs are liars](#lecture-5-game-devs-are-liars)
  - [Player Experience PX](#player-experience-px)
  - [Design pillars](#design-pillars)
  - [Using PX to define gameplay](#using-px-to-define-gameplay)
  - [Target audiences](#target-audiences)
  - [My game is like dark souls](#my-game-is-like-dark-souls)
  - [jump buffering implementation](#jump-buffering-implementation)
  - [Corner Correction](#corner-correction)
  - [Input Buffering](#input-buffering)
  - [Movement assist](#movement-assist)
  - [Networked Movement](#networked-movement)
  - [Tension mechanics](#tension-mechanics)
    - [Enemies scripted to Miss](#enemies-scripted-to-miss)
    - [Health Bar manipulation](#health-bar-manipulation)
    - [Example implementation health bar In Unity](#example-implementation-health-bar-in-unity)
    - [Last Pixel Comebacks](#last-pixel-comebacks)
    - [Wow, that was close other ways](#wow-that-was-close-other-ways)
  - [Dynamic Difficulty Adjustment DDA](#dynamic-difficulty-adjustment-dda)
  - [Forgiveness Mechanisms](#forgiveness-mechanisms)
    - [Give another chance](#give-another-chance)
    - [did you mean this button instead](#did-you-mean-this-button-instead)
  - [Resource Compensation](#resource-compensation)
  - [Hidden RNG Bias](#hidden-rng-bias)
  - [Catchup Mechanisms](#catchup-mechanisms)
  - [Stealth Help](#stealth-help)
  - [Aim assist implementation](#aim-assist-implementation)
    - [if cant see it cant hurt you](#if-cant-see-it-cant-hurt-you)
  - [Direction check implementation](#direction-check-implementation)
  - [Satisfying Reloads](#satisfying-reloads)
  - [psychological triclks](#psychological-triclks)
  - [loading screens](#loading-screens)
  - [so fast!](#so-fast)
  - [New player Performance](#new-player-performance)
  - [Multiplayer games Fake](#multiplayer-games-fake)
  - [implied Depth](#implied-depth)
- [Wk6](#wk6)
- [Lecture 6 - Improving look and feel](#lecture-6---improving-look-and-feel)
  - [game is only as strong as its weakest part](#game-is-only-as-strong-as-its-weakest-part)
  - [game is only as strong as weakest part](#game-is-only-as-strong-as-weakest-part)
  - [Stuff Not to DO](#stuff-not-to-do)
    - [Lighting](#lighting)
  - [Motion](#motion)
    - [Make everything Bigger](#make-everything-bigger)
  - [Juicing](#juicing)
- [Lecture 7:](#lecture-7)
  - [Assignment2](#assignment2)
  - [Assignment 2 Design Pillars](#assignment-2-design-pillars)
  - [RPG Mechanics and Itemisation](#rpg-mechanics-and-itemisation)
  - [Origins of RPG mechanics](#origins-of-rpg-mechanics)
  - [Types of RPGs](#types-of-rpgs)
  - [Roles and Classes](#roles-and-classes)
  - [Stats](#stats)
  - [Levelling](#levelling)
  - [Skill Trees](#skill-trees)
  - [Abilities](#abilities)
  - [Ability Mechanics](#ability-mechanics)
  - [RPG Itemisation](#rpg-itemisation)
  - [Item Generation](#item-generation)
  - [Item Sets](#item-sets)
  - [Itemisation and RPG Development](#itemisation-and-rpg-development)
  - [Player Decision Making](#player-decision-making)
  - [Item 'economy'](#item-economy)



# Weekly outline

![Untitled](Untitled.png)

# Teaching team

![Untitled](Untitled%201.png)

# Class times

![Untitled](Untitled%202.png)

# Assignments

![Untitled](Untitled%203.png)

# Lecture 1

## Low level game design

- Elden ring character attack breakdown

![Untitled](Untitled%204.png)

- Basic Rules and mechanics don’t happen naturally
- all discussed need to be carefully considered and implemented

## igb 190

- low-level concepts discussion education

## Major Topic C# scripting and Unity

- coming up

## Melee Combat Systems

- heavy exploration and emphasis on mechanics of melee combat, events and frame data

## animation driven systems

## on hit events

- potential for complicated interesting gameplay mechantics
- animation, collider controls and C# events
- will explore fascinating industry examples

## RPG mechanicss

- using formulae to control
    - levelling curves
    - gear/enemy scaling
    - dealing damage
    - taking damage

## assignment 1 Part A

- setup basic ARPG game with minor customisable elemnts
- player controller, camera, basic abilities, enemy spawner, object, level design
- scaffolded and guided
- not carry into assignment 2

## assignment 1 part B

- short edited video designed to answer a tailored question given to you exploring game mechanics and systems
- e.g. why is chun li considered top teir in sf3
- write response, record voice use and find pics and footage to compile your answer as a video adobe Premiere pro or similar software - DaVinci Resolve

# Wk 2: Unity Scripting
# Lecture 2

- recap start() update()
    - inherits from MonoBehaviour
    - start() - hook into object initialisation
    - update() - hook called every frame

## the game loop

- most important
- game logic loops

## Data Types

- Generic value data types (i.e. C# native)
    - Int – 4 bytes
    - long - 8 bytes - whole numbers
    - Float – 4 Bytes - stores fractional numbers up to 7 decimals
    - Double – 8 Bytes - stores fractional numbers, sufficient for up to 15 decimal digits
    - char - 2 bytes - single quotes ‘ ‘
    - String - sequence of chars double quotes “ ”
    - Bool – 1 bit
    - Enums, Structs etc

## Arrays, Lists etc

- reference data types
- Arrays – indexable sequenced data structure. Can be multidimensional ([,], [][], [1,2,3,4], etc)
- E.g. int[] selection;
- Lists – more nuanced data structure orientated towards searching, removing, re-sorting etc
- Dictionary – less sequenced, unordered data with expandable ‘key’ lookup functionalities

## Logic and Conditionals

```csharp
Less than: a < b
Less than or equal to: a <= b
Greater than: a > b
Greater than or equal to: a >= b
Equal to a == b
Not Equal to: a != b
```

## for loops

- For loops – when you know exactly how many times you want to loop through a block of code. Typically partnered with Arrays for index utility
- 
- Foreach loops – when you don’t know how many times you wish to loop. Useful for finding or exempting container elements, e.g. within IEnumerable Lists
- 
- While loops – when you don’t care(?) how many times you wish to loop. Typically utilized with caution and assurances – while loop error = system hang. Find answer in 1 frame territory.

## quick activity using arrays for loops

- Our Game requires you to have have a space-ship that fires lasers from multiple locations at the same time (i.e. broadside)
- How would you use an array and loop to facilitate this?
- How would you tweak this to fire sequentially?
- How would you explain both firing patterns in a Game Design Document?

## methods

- Method – block of code containing logical statements, typically segregated uniquely for efficiency and for running multiple times
- Method usage creates branching logical pathways to occur per object each game loop
- Most methods should be written to be reusable in some way. Important methods should be called from the Update() function in your scripts – e.g. PlayerControls()

## Args and Parameters

- Methods can have parameters and return types for varying degrees of functionality and purpose
- Methods can then be called with varying arguments to accommodate multiple use cases, or even objects, doing the same thing
- AStarNavigation(gameObject, pointA, pointB);
- Method header parameters can be written differently – overloading*

## Structs

- Sometimes you just need a ‘container’ that can hold multiple degrees of information
- Struct – cheap value type data structure for small, self-contained processing. Useful for things that need to be cloned/copied. Can contain methods.
- “This enemy really needs an instanceable data structure for storing information about target acquisition. Not every enemy needs this…”
- Note: don’t use structs for anything requiring inheritance or potentially containing null references

## Class

- If a Struct can’t cut it, use a Class
- Class – less cheap reference type data structure, necessary for more complex, object-oriented design
- Have significantly more functionality. Can ‘inherit’ from other classes
- With Unity, contains your hooks into Start() and Update() and doesn’t require constructors

## Inheritance

- Complicated domain. Relates directly to the OOP nature of C#

- Child classes inherit information from a parent class – less information necessary in child classes

- Useful for ‘storing’ universal functionality but also differentiating between nuanced objects

- Child classes can utilize polymorphism and have virtual, override & abstract methods

## Unity C# public variables

- allows to access within unity inspector
- inspector values take priority

## unity intantiate()

- Method for spawning new object instances (prefabs) into the game world. Enemies, Effects, Audio etc
- Massive Tip: Said objects can be manipulated immediately! E.g.
- GameObject thisObject = Instantiate(abc, a.position, a.location);
- **thisObject.GetComponent<MyScript>().value = whatever;**
- Consider using object pooling for handling many repeated instances…

## unity GetComponent()

- Almost any Unity component (i.e. something you add to a game object) can be manipulated
- This is not just limited to the object’s transform and scripts!
- Adjusting other components on objects is useful for manipulating colliders, physics, animations, materials etc at runtime
- Result = even more dynamic object interactions

## Assignment 1 Part B Questions

- In Doom Eternal, what do the designers refer to as "The Fun Zone"? How do you think this design would impact your own enjoyment of the game?
    - doom clone, 2D top down version (lauren)
    - and recreate doom levels - how to fix the vertical level fun in 2d?
    - there is a 2d sidescrolling DOOM already
- What is 'Coyote Time' and why is it considered important in platform games? How could this concept improve a gameplay experience you have encountered that lacks this phenomenon?
    - platformer demo player can adjust coyote Time amount

[IGB190 assignment 1](https://www.notion.so/IGB190-assignment-1-8d74853957cf4dfb977208fcc8844255?pvs=21)

# Workshop wk2

## Nav Mesh Surface

- Bake each time change level layout

## **Unity Prebuilt Methods**

Unity has many other methods that are called by the game loop (if they exist in your script). You can find a complete description of these functions on Unity’s website [here](https://forum.unity.com/threads/1381647/). If you add a method to your script with an **exactly matching** name ****(they are case sensitive!), Unity will run that method under the specified conditions. The most important of these are:

- **Awake**: Called **once**, **immediately** after the object is created.
- **Start**: Called **once**, at the beginning of the frame after this object is created.
- **Update**: Runs **every frame**.
- **LateUpdate**: Runs **every frame**, after Update methods have been called on all objects.
- **OnDestroy**: Runs **once**, when the GameObject with this script attached is destroyed.
- **OnEnable**: Runs **every time** the attached GameObject is enabled.
- **OnDisable**: Runs **every time** the attached GameObject is disabled.

There are also methods related to physical collisions between GameObjects:

- **OnCollisionEnter**: Called whenever the GameObject **starts colliding** with another GameObject.
- **OnCollisionExit**: Called whenever the GameObject **stops colliding** with another GameObject.
- **OnCollisionStay**: Called **every frame** that the GameObject **is colliding** with another GameObject.

In a game, there can also be non-physical collisions (e.g., playing a sound when a player enters an invisible hitbox). In Unity, these are handled with **Trigger Colliders** and there are separate methods for those collisions:

- **OnTriggerEnter**: Called whenever the GameObject **starts colliding** with another GameObject.
- **OnTriggerExit**: Called whenever the GameObject **stops colliding** with another GameObject.
- **OnTriggerStay**: Called **every frame** that the GameObject is colliding with another GameObject.

*Note: There are also 2D variants of all these collision functions (e.g., OnCollisionEnter2D) if you are making a 2D game with 2D colliders instead.*

## **Variables and Variable Types**

Variables are used in programming to store data. You can store a value to them, and then retrieve or modify that value later. In C#, variables are strongly typed. This means that when you define a variable, you must state the type of information it will be storing. There are four important **primitive** types you should know about for game development, **string**, **bool**, **int**, and **float**:

- **string**: Stores **text**. The text must be surrounded by quotation marks.
    - public string enemyName = “Skeleton”;
- **bool**: Stores a **True/False** property.
    - public bool isRunning = True;
- **int**: Stores a **whole number**.
    - public int enemiesAlive = 5;
- **float**: Stores a **decimal number**. Floats are a special format for storing numbers that allow for very fast calculations, which are important for game development. When specifying a float, you must always put an **f** after the number.
    - public float movementSpeed = 3.5f;

## Mouse and Keyboard Input

There is no event which triggers when the user presses a button in the game. Instead, you must check to see if the user is holding a key on that specific frame. This means that all input related code should go in the Update method (or a method which is called from the Update method). These are the important functions related to input:

- Input.GetKey: Checks to see if the user is currently holding down the specified key.
- Input.GetKeyDown: Checks to see if the user started holding down the specified key this frame.
- Input.GetKeyUp: Checks to see if the user released the specified key this frame.
- Input.GetMouse: Checks to see if the user is currently holding down the specified mouse button.
- Input.GetMouseDown: Checks to see if the user started holding down the specified mouse button this frame.
- Input.GetMouseUp: Checks to see if the user released the specified mouse button this frame.

Each of these functions returns a bool. This means that if you are trying to execute code if the correct input conditions are met, you should put the method in an if statement. For example:

`if (Input.GetKeyDown(KeyCode.Space))`

`{`

`// Perform actions.`

`}`

If you want to check for a different key, change the key highlighted in the code above. The keys have sensible names (e.g.  KeyCode.W would check if the W key was pressed). You can find the complete list in Unity’s documentation [here](https://docs.unity3d.com/ScriptReference/KeyCode.html).

---

## GetComponent

To access the variables and methods in one script from another, you need to get a reference to that script. One of the most common ways of doing this is to use the GetComponent method.

The GetComponent method searches only the GameObject you specify and returns the component of the type you specified (or null if it doesn’t exist). In this case, we are searching for the NavMeshAgent component on the same GameObject as the Player.

In this case, we use the GetComponent method to access and control the NavMeshAgent component we created earlier.

Instead of using the GetComponent method, we instead use the GetComponentInChildren method to find the Animator. This is because the Animator component isn’t attached to the Player, but is instead on the Barbarian Model (which is a child).

Here is an example using GetComponent in the bullet collision method of a hypothetical FPS game to damage an enemy:

```csharp
private void OnTriggerEnter(Collider other)
{
Enemy enemy = other.GetComponent<Enemy>();
if (enemy != null)
	{
	enemy.TakeDamage(10);
	Destroy(gameObject);
	}
}
```

In this case, whenever something collides with the bullet, the game checks to see if the object has an Enemy component. If it does, it calls the TakeDamage method on the enemy and destroys the bullet, otherwise it does nothing.

---

# Wk3: Principles of Game Mechanics

### MDA Framework?

- Mechanics, Dynamics, and aesthetics
- Hunicke, R., LeBlanc, M., & Zubek, R. (2004).
- 

### Mechanics, dynamics, aesthetics

- Mechanics - fundamental components, of a game. rules, systems and algorithms
- dynamics - interaction of mechanics and systems during gameplay, player behaviours
- aesthetics - emotional responses and experiences the game elicits.

### Game dev vs mda

- play testing is required

### Rules → mechanics → systems

- consider early staege rules and mechanics and hor contribute to systems design
- Rule: jump on space
- mechanic: double jump
- system: player traversal system

## Rules are simple mostly

- simple can constrain gameplay
- player controls -
- resouce collection
- taking damage
- define what you can do and what happens

## Mechanics are intricate

- mechanics utilize or build upon multiple rules. e.g.
    - double jump
    - aim down sights
    - drifting
- can be emergent, multiple rules or not

## Systems are complex

- systems consist multiple mechanics
- juggle combo - string together attack inputs
- player traversal
- combat resource loop

## FPS mechanics ray casting

- Ray-casting used for many purposes. Derived
- from calculating how light travels in simulations
- based on realistic lighting models
- In FPS games, primarily used for ballistic weapon hit detection
- Also heavily used for Line-of-Sight calculations in Game AI and Game Logic, generally
- Very cheap and simple technique for ‘shooting’mechanics in video games. Just vector math!

## **Raycasting in C# & Unity**

- calculate ray from weapon to object on its x-axis

```csharp
void Shoot(){
	RaycastHit hit;
	// create a ray from objects pos in direction facing
	Ray ray = new Ray(thisObject.transform.position, this Object.transform.foward);
	
	if(Physics.Raycast(ray, out hit, range)}{
	// If ray hits within range
	// apply damage
	Health health = hit.collider.GetComponent<Health>();
	if(health != null){
		health.TageDamage(damage);
		}
	}
}
```

## platformer mechanics

- double or mario gravity when player reaches jump apex
- player accellerates upwards quickly. when falling accelleration constant
- result weightlessness rapid descent forgiving air control.
- also super meat boy

## platformer mechanics edge leyway

- e.g. coyote time

## platformer mech - ballistics

- jump feels natural like earth parameters
- jump arcs that are predictable and calculated

## ballistic equations

- projectiles too

$\Large y = xtan(A) - \frac{Gx^2}{2\cdot V^2 cos^2(A)}$

A = angle in radians

G = gravity 

V = velocity

## Ballistic Equation in C# and unity

![Untitled](Untitled%205.png)

## Input Queuing

- not all mechanics are visible
- Input Queue - A mechanism that temporarily records recent player input and parses it for validity. Valid inputs are deciphered

## 2**Input Queue in C# & Unity**

1. Create a queue that captures input
2. Analyse this queue over time every few

milliseconds

1. Attempt to match the current string to an

existing case (with some leniency)

1. Add any valid cases to a shorter list which

may override player input

1. Repeat from 2

![Untitled](Untitled%206.png)

## Portal - Portal Gun

- teleport mechanic

## Object Collider Interactions and Events

- fundamental process
- often with animation driven system
- complex: utilisation, hitboxes, hurtboxes, events
- next week

# Workshop wk3

## Animations

- Create new Animator Controller
- add animations to the animator
- attatch Animator Controller to character model
- create animation transitions and conditions as desired within the animator window tab
- HasExitTime off if I have a condition

## Wk3 Questions

1. What is the main function of the Start method in Unity scripts?

a) To initialize variables and set up the initial state when the GameObject is created

3. How frequently does the game loop run in Unity?

Once every second, regardless of game content

4. What is a "frame" in the context of game development?

d) One iteration of the game loop, representing a single update and render cycle

5. How often does the Update method run in Unity?

Every frame

1. What is the purpose of using Instantiate in a script?

a) To create a new GameObject from a Prefab at runtime

1. What does the Input.GetKeyDown(KeyCode.Space) method check for in Unity?

a) If the spacebar key is pressed down during the current frame

10. In which method should you put your code if you want it to run when an object is removed from the scene in

Unity?

b) OnDestroy

1. What does the IsTrigger property on a collider do in Unity?

 It allows the collider to detect overlaps without generating a physical collision

12. What is the difference between GetKey and GetKeyDown in Unity?

d) GetKey checks if a key is being held down, and GetKeyDown checks if a key was pressed down in the current frame

13. You have written a script with some variables representing player stats, but when you update the script with new

variable values and recompile, it keeps using the old values. What might have gone wrong?

c) The script is using the current inspector values instead

14. What in-built Unity method should you use if you want the code to run immediately after a prefab is instantiated?

c) Awake

● d) OnEnable

Explanation: Both Awake and OnEnable run immediately after a prefab is instantiated, while Start runs at the start of the

next frame. Use OnEnable if the startup code needs to run every time the object is re-enabled, or Awake otherwise

15. When should you use FixedUpdate instead of Update in Unity?

c) When you need to handle physics calculations

16. When should you use LateUpdate instead of Update in Unity?

b) When you want to update the object after all other object updates are completed

7. What is the Unity Mecanim system used for?

The Mecanim system is used to control and animate characters and objects in Unity. You will likely need to

use the Mecanim system in every Unity project you ever work on. You should become very familiar with it!

18. Can you create animations for one character and apply them to a different character in Unity?

b) Yes, if both characters use the same rig, such as Unity's default humanoid rig

19. What are animation parameters in Unity, and how are they used?

a) Variables that control the properties of animations, such as transitions and speed

20. What is the significance of the 'Entry' node in the Animator window?

a) It represents the starting point of the animation state machine

21. What is the function of the 'Any State' node in the Animator window?

b) To allow the transitions to occur from any state in the animator

22. Why is it important to disable 'Has Exit Time' for certain animation transitions?

d) To allow the transition to occur immediately

23. What is the role of the Animator.SetFloat method in controlling animations?

b) To set the value of a numerical parameter in an animator

Explanation: Animator.SetFloat is used to set the value of a numerical parameter in an animator, which can control

aspects like animation speed, remaining health, or other values which may affect animations in some way.

24. In Unity, what is a Trigger parameter used for in animations?

b) To activate a one-time transition between animation states

25. How does the Unity Animator component interact with scripts you write?

a) Scripts can update animation parameters and play or stop animations

1.  How do you modify the speed of an animation in Unity?

b) By adjusting the speed parameter in the animation clip or animator node

1.  Why is it important to have a clean layout in the Animator window?

c) It simplifies understanding and debugging the animator logic

1. What is the role of the Animator Override Controller?

b) To customize animations for different models using the same template

29. How can you debug animations in Unity when the game is running?

b) By selecting the GameObject with the Animator component and observing the Animator window

30. What is a NavMesh in Unity, and how is it used?

d) A navigation system that allows GameObjects to find paths and move through the game world

31. Which component must be added to an enemy GameObject to enable pathfinding and movement in Unity?

NavMeshAgent

32. How do you prevent dynamic objects, such as enemies placed in the level, from being included as NavMesh

blockers during baking in Unity?

b) By setting the objects to a layer that is not included in the baking

# Wk4 Lecture notes: designing gameplay Interactions

## Animation Events

- tied to animation driven systems
- events tied to animations of objects in video games
- at particular frame, activate an engine feature, or call a method in script.
- if animations do not get to said frame, said events do not occur

## collider interactions

- process driving mechanics and systems in action-based games
- every frame, physics engine calculates what collider volumes are overlapping and ajusts
- unity, OnEnter, Exit Stay events for colliders and triggers can be utilised on objects of interest

## What is a collider

- defines shape for physical collisions and interactions
- Box, sphere, capsule or mesh
- usually mesh is not needed not idea

## on hit events

- using collider interactions
- scripting

## Unity and C# colliders and on hit events

- attach colliders to segments of model
- automate collider to attach to animations for accuracy

## activity collider event

- animation, collider interaction, on hit event
- at specific frame, animation calls event with box collider, collider enters another and must take damage
    - how to make collider only interact with new object colliders every frame?

## Fighting games

- 70s become popular in 80s and 90s
- intricate controls, rules, mechanics and combo systems
- high skill floor and ceiling

## Hit boxes and Hurtboxes

- A hitbox is usually associated with some form of attack, and describes where that attack is effective.
- A hurtbox is usually associated with a character (or any other "hittable" object in your game).

## Startup, active and recovery

- startup - frames before hurtbox spawns, long startup bad
- active - frames hurtbox is active for
- recovery - frames to return to neutral state long recovery really bad

## blocking and parry

- counter the effects of active hurtboxes
- block - hit effects are minimised
- parry - timed mechanic, hit effects are even further minimised.

## blockstun and hitstun

- blockstun - won’t get a change to attack but better than being hit
- hitstun - you are taking damage and recovering slower, not getting to attack

## activity

- how could consideration of frame data assist with perforamcne
- would you wish to change said frame data and if so how

## frame data analysis

- most fighting games have basic moves of varying speed and utility
- street fighter, tekken

## frame data analysis

- compare move frame data, to pick best moves
- typically in fighting games

![image.png](image.png)

## frame advantage and footsies

- being hit puts you in a longer animation than block or parry
- frame advantage means have the opportunity to hit again - combo
- footsies of fighting games is looking for opportunities to gain frame advantage over opponent
- spamming is not a good strategy for experienced players who can block and parry or frame advantage etc.

## and in other games

- Elden Ring - weapon choice influence hitbox size range speed

## animation driven systems

- Animation blending
- animation cancels
- timing mechanics
- buffering & input queues
- masking, rigging etc.
- 

# Workshop wk4

## Player and Enemy Combat

## Interfaces

## Change the name of build or its ICON

If you want to change the name of your game or its icon, you need to do this in Player Settings. There is a shortcut to access the

player settings by pressing the ‘Player Settings’ button at the bottom left of the Build Settings window.

- Changing the ‘Company’ will change how some files are named, particularly on mobile.
- Changing the ‘Product Name’ will change the name of the executable.
- Changing the default icon will change the icon of the built executable.

# Lecture 5 Game devs are liars

- your job isn’t to beat the player you control everything
- if players enjoyed or had the intended experience - you won

## Player Experience PX

- consider the intended experience
    - how challenging
    - what emotions
    - how much autonomy

## Design pillars

- easy to learn, difficult to master
    - Hearthstone
- competitive integrity
    - league of Legends
- speed and fluidity
    - Doom quake
- challenge and reward
    - dark souls, elden ring

## Using PX to define gameplay

- league of legends
    - focuses on fair competition. minimal randomness
- Hearthstone
    - emphasises fun interactions
- Yogg-Saron randomness decided a 250k world championship match.

## Target audiences

- should inform your design
    - what games and genres does your target audience play
    - what experience
    - what features
    - what will be familiar

## My game is like dark souls

- its easy to make a hard game - the challenge is to make it satisfying

## jump buffering implementation

- if when player pressed jump within small threshold and touching the ground

![image.png](image%201.png)

## Corner Correction

- Celeste Corner correction
    - If player hits a corner, push them towards the nearest free direction
- super smash bros
    - if a player

## Input Buffering

- Critical players feel movement system in game feels responsive and correct.
- Input Buffering:
    - if player tries to do something but doesn’t meet requierments, do asap

## Movement assist

- Spiderman

## Networked Movement

- Client-side prediction
    - player thinks theyve started moving but they havent
    - 

## Tension mechanics

- want to increase tension, but not difficulty
- Lego star wars
    - large number of enemies can appear, but noly a subset of them act at once
- Uncharted
    - enemies are unable to hit during acrobatics, climbing ziplining
- to make in seem like you’re more likely to be hurt when you actually can’t be

### Enemies scripted to Miss

- Far cry 3 enemies must miss first shot if player hasn’t seem or shot them yet
- Lego star wars

### Health Bar manipulation

- increase tension by having player think they’re low on health

![image.png](image%202.png)

### Example implementation health bar In Unity

![image.png](image%203.png)

### Last Pixel Comebacks

- same as non linear bar but modified when low

![image.png](image%204.png)

### Wow, that was close other ways

- instead of health bar manipulation
    - enemies deal less damage if you are low on health
    - boarderlands 2 Funzerker
        - the player deals more damage when low on health

## Dynamic Difficulty Adjustment DDA

- the flow state
    - balance skill against challenge
    - players are different

![image.png](image%205.png)

DDA

- given players arying skill how do you keep everyone in flow state
- left for dead 2
    - AI director will ramp up enemies until player might be overwheled
- RE4
    - if you fail too much, the game will slide you into a lower difficulty e..g remove some enemies

## Forgiveness Mechanisms

- checkpoints and autosave systems
- shields and health Regeneration

### Give another chance

- hit zero but dont die
    - boarderlands 2 fight for your life - kill enemy to revive
    - elden ring rune recovery
    - Tekken - chip damage recovery - after losing helath player may recover hp is dmage opponent

### did you mean this button instead

- portal 2: you place correct portal, even if you press the wrong button

## Resource Compensation

- last of us
    - likely to find ammo if you are almost out
- dead cells
    - players more likely to find health pickups when near death
    - one line if check if player within low threshold, drop health

## Hidden RNG Bias

- playres don’t trust randomness true randomness feels unfair
    - hit with a 1% change youre awsom
    - miss with 99% chace game is broken
- XCOM
    - 85% change to hit may be 95% to hit
- Diablo 3, boardlands 3, path of exile
    - longer it =s been since last good loot drop higher chance will be.

## Catchup Mechanisms

- cames feel fun if close
- Rubber banding need for speed
    - if youre behind you get a speed bost
- mario cart
    - quality of powerups you get dpeneds on houw well you’re performing

## Stealth Help

- Aim Assist
    - players frustrated if they keep missing shots
    - Most console FPS

## Aim assist implementation

- compare look vector of the player and the vector from player to enemy, if they’re close, apply aim assist

![image.png](image%206.png)

### if cant see it cant hurt you

- halo 2 and 3,
    - enemies avoid shooting the player in the back, they move closer instead
- Bioshock Infinite
    - enemy move slower if cant see it

## Direction check implementation

![image.png](image%207.png)

![image.png](image%208.png)

- if player cant see enemy slow down else go fast and attack

## Satisfying Reloads

- Gears of War - last bullet in a clip does bonus damage
- half life 2 - 1st shot after reload is perfectly accurate

## psychological triclks

## loading screens

- Mass effect - load screen elevator
- dark souls - heavy doors - animation slower if computer bad - for loading
- crawl space loading events

## so fast!

- mass effect
    - sprint didnt change speed - instead FOV and camera position
    - dragon age inquisition
        - sprint doesnt increase only changes fov and wind particles

## New player Performance

- new players more likely to quit if lost 1st match

## Multiplayer games Fake

- IO games [slither.io](http://slither.io) fake against bots but player thinks against players

## implied Depth

- telltale
    - game will tell player characters will remember an action, but they actually don’t
- Dante’s infermer
    - health pickups don’t increase the players health just the size of bar
- car games
    - stats don't reflect in the game
- Visual Tricks
    - billboards and imposters
        - fake complicated geometry
    - Imposter romos
        - eg spidersman

# Wk6

# Lecture 6 - Improving look and feel

## game is only as strong as its weakest part

## game is only as strong as weakest part

- do Workshop week 6

## Stuff Not to DO

- don’t use copyrighted materials duh
- don't leave default assets in game
    - Font
    - skybox
    - UI
    - particl
    - mode
    - sicon
    - demo assets
- Z fighting
    - when surfaces occupy same space

![image.png](image%209.png)

- Texture Stretching
- Poorly Tiled Textures
- Pixel Light Count - how many lights can contribute to the lighting of a surface
- Common UI Mistakes
    - too many decimals
    - timers negative
    - stretched
    - spelling
    - selectrion hover errors
    - colliders blocking buttons
- Volume Balances
    - balance, too low is better than too high
- Project Naming
    - naming and Crypt Crawl
- Screen Resolution
    - change to scale with screen size
    - and match with height
- Shadow Resolution
    - edit / project settings/ quality/ shadow distance
- Colour Palette
    - Gradients
    - use colour picker
- Fonts are Important
    - custom
    - legible
- Music
- Custom Skyboxes
    - downloadonline
    - window / rendering/lighting / environmental / skybox material
- Colour Space
    - linear: correct brightness and contrast at higher computation
    - gamma: is fast but too bright
    - in unity: edit / project settings / player / other settings / color space / linear
- anti-aliasting
    - unity: post-process later on the camera choose antialias mode you want
- Ambient Occlusion
    - fakes correct lighting by darkening obscured objects
- Bloom
- Depth of field
- Color grading
- post-processing greyscale
    - good for death effects or low health

### Lighting

- lighting improves game feel
- add more static lights
    - 
- or dynamic lights
    - particle effects
    - emissive
- light baking
    - in unity: window, rendering, lighting, environment, generate lightmaps
- Volumetric Lighting
    - tries to simulate real-world lighting conditions
    - unity needs to be in HDRP

## Motion

- Moving backgrounds
- Grass
    - add grass, skybox, wind audio loop
- God Rays
    - light shafts make a prefab and use in all future projects
- Boids
    - simular group of objects flocking together
    - There are free Boiding systems in unity
- fog and pulsing glows
    - unity window, animation, animation
    - make some pulsing moving stuff
- Dynamic camera
    - use unity cinemachine
- Action Feedback
    - e.g. tetris
        - each time block line completed in a row pitch of sfx goes up
- UI animations
- Custom Cursor Design
- Screen fades
- Blurring the game in menus easy and looks good
- SFX
    - SFXR
    - GDC free sounds
    - freesound
- Text and dialogue Boxes
- Scene Transitions
    - Free asset available

### Make everything Bigger

- if player like it add more of it
- like shooting
    - make it faster
- player like weapon kickback
    - double it

## Juicing

https://www.youtube.com/watch?v=AJdEQ

- The art of screenshake
- [https://www.youtube.com/watch?v=AJdEqssNZ-U](https://www.youtube.com/watch?v=AJdEqssNZ-U)
- Juice it or lose it
- [https://www.youtube.com/watch?v=Fy0aCDmgnxg](https://www.youtube.com/watch?v=Fy0aCDmgnxg)

- How to design with feedback and game feel in mind
- [https://www.youtube.com/watch?v=yCKI9T3sSv0](https://www.youtube.com/watch?v=yCKI9T3sSv0)

- Best Practices for fast game design in Unity
- [https://www.youtube.com/watch?v=NU29QKag8a0](https://www.youtube.com/watch?v=NU29QKag8a0)

# Lecture 7:

## Assignment2

- design and justification Document
    - detail low-level designs in intricate detail (rules, mechanics, systems) with rationale
    - some iteration and playtesting expected and documented briefly

## Assignment 2 Design Pillars

1. Challenge and Competence
- the game is appropriately challenging and that they are competent at the experience
2. Player Empowerment
- game systems should make player feel powerful, as they progress
3. Buliding Anticipation
   - player should feel a sense of anticipation throughought
4. meaningful bulid choicing
- feel they can create unique gameplay dynamics and playstyles
## RPG Mechanics and Itemisation
- part 1/2 on RPG Mechanics
- Lec 7 focus on concepts and mechanics of RPGs
- Why?
  - these drive RPG games 
  - contain logic for complex and rich game design
## Origins of RPG mechanics
 - Dungeons and Dragons 1974 TTRPG
 - Warhammer TTRPG
 - dnd 1975 rpg game
 - rogue 1980 - video game
 - Ultima 1981 - video game

## Types of RPGs
- Turn based RPG - darkest Dungeon
- ARPG
- MMORPG
- Tactical RPG TRPG - XCOM
- contain interaction, conbat and RNG

## Roles and Classes
- allow some degree of initial character choice or ongoing customisation
- Typical Archetypes
  - Tank
  - Damage
  - Support
- other
  - Necromancer
  - sniper
- Define items, abilities, and interactions

## Stats
- impact abilities and performance
- items, armour, buffs, debuffs can effect

## Levelling
- Progression Mechanic of most RPGs
- Gain Experinece from Tasks
- Increase CHaracter SKill as reward
  - stats
  - skill point
  - gear, areas, quests

## Skill Trees
- Character Progression
- not always important - debatable
- often too complex or not rewarding enough per skill point

## Abilities
- Directly connected to class
- Serve Function, damage, heal, buff

## Ability Mechanics
- Formulae control how stats contribute
- impact general movement and attack speed
- Intricately Designed

## RPG Itemisation
- varies
- give bonuses
- major progression point
- Item Quality as a function of player level
  - can  shift player stats
  - farming for max quality items is an endgame objective for RPG players

## Item Generation
- stat ranges created server-sise - loot tables
- item generation database

## Item Sets
- add interest in farming specific items for additional bonuses or change player archetype

## Itemisation and RPG Development
- stats, levelling, abilities and items, needs to be designed and tested

## Player Decision Making
- Often Neccessary to formulaically design mechanics in a way that encourages varied decision making

## Item 'economy'
- can't have everything at max stats forever. items rolls prohibit it
- Limitations, caps, diminishing returns etc.
- This is a form of min maxing
