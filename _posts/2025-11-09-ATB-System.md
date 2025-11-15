---
title: UE5 Action Time Battle System
date: 2025-11-09 16:11:52 +0000
categories: [Projects, CPlusPlus, Unreal-Engine]
tags: [portfolio, unreal-engine, blueprints, gameplay]
description: Unreal Engine Gameplay System for Turn Based Games with ATB mechanic
image:
  path: assets/images/ATBSystem/ATB-SystemHUD.png
  alt: Project poster
---

### Overview
Action Time Battle System developed using Blueprints. Started as a group project contribution, the task developed as a standalone system that can be easily integrated inside a pre-existing project. Using **State Trees** for combat flow logic and **UMG Widgets** for player interaction this system takes inspiration from titles such as [***Final Fantasy VII Rebirth***](https://www.youtube.com/watch?v=GL33pUIwZ5U). 

### My role
- Gameplay Programmer (solo)
- Responsibilities: core mechanics, systems integration, prototyping

### What I built
- State Tree driven Combat System 
- Active Time Gauge mechanic to Queue up Combatants
- Component based Combatants
- Simple extendable AI Opponent logic
- Data-Driven Abilities and Ability Sets
- UMG HUB with Dynamic Layout that changes based on Gameplay Triggers

### Technical highlights
- **Engine / Framework**: Unreal
- **Languages**: Blueprints
- **Systems**: State Trees, UMG, DataAssets, Gameplay Framework.

### Challenges & solutions
- One of the team's requirements was for this system to be developed entirely using Blueprints as most of the team, including the team lead were not comfortable dealing with C++, some functionalities had to be reworked to address this limitation as some C++ features as well as some of the UE5 C++ APIs and DSAs couldn't be accessed in Blueprints, which meant that for instance Queues needed to be implementated in Blueprints instead of using UE5 C++'s TQueue data structure. 
- While having past experience working in Blueprints, C++ still remains the preferred choice as it can streamline development without having to worry about point and click over UI and Node manipulation. 
- Creating a Queue that could be pruned based on Combatants states (e.g. Queued up combatant dies before its turn) was something that needed some extra care. 
- Making sure the UI was in sync with the Combatant Manager combat flow. 
- Adding UI art was challenging and required some extra time to get up to speed with texture manipulation and UMG Wdigets setup.  

---

### Links
- Repo: <a href="https://github.com/AbderrahimJami/UE5-Action-Time-Battle-System" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i>
GitHub</a>
- Demo: <a href="https://abderrahimjami.itch.io/thesteroidolympics" target="_blank" rel="noopener noreferrer"><i class="fab fa-itch-io"></i>
Itch.io</a>


---

## Demo

<!-- {% include embed/youtube.html id='' %} -->
