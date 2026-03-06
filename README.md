<img width="1200" height="400" alt="serpentsTrial_git_banner" src="https://github.com/user-attachments/assets/f391cf55-b050-41b0-968e-66fd8637284a"/>

## Overview

**Serpent's trial is a puzzle platformer in a Greek mythology-inspired setting, where the player controls a Gorgon.**

**He can use a petrification ability to turn enemies into stone and move them around to reach new areas or solve puzzles.**

<p align="center">
	<img alt="serpentsTrial_gameplay" src="https://github.com/user-attachments/assets/79a7746c-7148-48fc-b177-611bbf21333e">
</p>


Serpent's Trial was developed as a **10 week** long, student project at [**School4Games**](https://www.school4games.net) in early 2025. 

**Engine     :** Godot 4.3
**Tools        :** Mercurial (Version Control)
**Team size :** 7 full time (1 producer, 1 game designer, 2 engineers, 3 artists)

Play it [here](https://s4g.itch.io/serpents-trial)

---

## My Responsibilities

I was one of two engineers working on Serpent's Trial. I was primarily responsible for  the core architecture, and the player and the enemy controller, while my [co-engineer](https://github.com/AnubisDev161) was more focused on the main mechanic (the petrifying laser), and how the player uses it to interact with the world.

My main contributions include: 
- Building the **Player & Enemy controller** and their **state machines**
- Implemented an **Interaction systems** to push/pull petrified enemys
- Developing a **Menu Stack** system to allow easier travel, while clicking through menus


---
## Highlights

### Player  
Early in development it became clear that the player would need to handle several different interactions, such as **petrifying enemies** and **moving petrified enemies** to solve puzzles.  
To keep the player logic modular and easier to maintain, I implemented the player controller using a **state machine architecture**.  
  
Each behaviour is handled in its own state, which keeps the logic separated and allows new mechanics to be added without turning the player controller into a large monolithic script.  
  
A very integral mechanic in Serpent's Trial is the ability to **push and pull petrified enemies**. Implementing this system required solving several physics challenges, such as allowing blocks to move smoothly **up and down slopes**, while still being affected by **gravity when moving off platforms**.  
  
This took quite a bit of time and some iterations, to figure out how to ensure the interaction between the player and the movable objects remained stable and predictable.

#### Key Components
- [**State Machine**](https://github.com/superkessi/SerpentsTrial/tree/main/Scripts/Character/State%20Machine)
- [**Player States**](https://github.com/superkessi/SerpentsTrial/tree/main/Scripts/Character/Player/States)
- [**Player**](https://github.com/superkessi/SerpentsTrial/blob/main/Scripts/Character/Player/player.gd) 
