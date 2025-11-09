---
title: First Placeholder post
date: 2025-11-09 12:32:52 +/-0000
categories: [Blogging, Demo]
tags: [getting-started, writing]     # TAG names should always be lowercase
description: This is my first blog post! 🙌
image:
  path: https://images.pexels.com/photos/1107717/pexels-photo-1107717.jpeg?cs=srgb&dl=pexels-fotios-photos-1107717.jpg
  alt: Landscape image to use for Placeholder post 🌳
mermaid: true
---



# Hello World!

This is a quick placeholder you can edit as you practice writing, formatting, and publishing with Jekyll.

---

This is my first post, I've never really used this before, but I'm confident I'll pick it up in not time 💪!

This is me practicing a simple checklist
- [ ] First Checklist item
- [ ] second checklist with **bold formatting**
- [ ] Third checklist item with [***Multiplayer.it***](http://multiplayer.it/)
- [ ] Fourth checklist item with `inline code` 

---

### Youtube embed
{% include embed/youtube.html id='l1fTbQV5J2A' %}



### Mermaid diagram 
```mermaid
classDiagram
%% ===================== UI ROOT =====================
class BP_EnemyController {
  <<AI Controller>>
  %% Context Information
  +BP_PatrolPath* PatrolPathRef
  +Overlay* TurnQueueAnchor
  +VerticalBox* PartyBarsAnchor
  +VerticalBox* EnemyBarsAnchor
  +SizeBox* CommandMenuAnchor
  --
  %% Public API
  +AddTurnQueue(queue: WBP_TurnQueue)
  +AddCommandMenu(menu: WBP_CommandMenu)
  +HideCommandMenu()
  +AddATBBarForParty(bar: WBP_ATBBar)
  +AddATBBarForEnemy(bar: WBP_ATBBar)
  +PlaceWidgetOnCanvas(w: UUserWidget, anchorsMin, anchorsMax, align, pos, size, z)
}

%% ===================== Enemy Character =====================
class BP_EnemyCharacter {
  <<Character>>
  +ScrollBox* ListPanel   %% BindWidget
  +TArray~WBP_QueueEntry*~ Pool_Free
  +TMap~UCombatantComponent*, WBP_QueueEntry*~ Pool_Active
  --
  +RefreshFromReadyQueue(ReadyQueue: TArray~UCombatantComponent*~, Current: UCombatantComponent*)
  +AcquireEntry() : WBP_QueueEntry
  +ReleaseEntry(entry: WBP_QueueEntry)
  +HighlightCurrent(comp: UCombatantComponent*)
}

class StateTreeEnemyBrain {
  <<UserWidget>>
  +UCombatantComponent* CompRef
  +Image* Portrait
  +TextBlock* NameText
  --
  +BindCombatant(comp: UCombatantComponent*)
  +UnbindCombatant()
  +SetIsCurrent(b: bool)
  +SetIsDead(b: bool)
  +PlayAppear()
  +PlayDisappear()
}

%% ===================== BARS =====================
class WBP_ATBBar {
  <<UserWidget>>
  +UCombatantComponent* Comp
  +ProgressBar* ATBProgress
  --
  +BindCombatant(comp: UCombatantComponent*)
  +SetPercent(p: float)
  +PulseReady()
  +FadeOut()
  +UnbindCombatant()
}

%% ===================== COMMAND MENU =====================
class WBP_CommandMenu {
  <<UserWidget>>
  +UCombatantComponent* OwnerComp
  +TArray~DA_Ability*~ Abilities
  +PanelWidget* OptionsList
  --
  +SetOwnerCombatant(comp: UCombatantComponent*)
  +PopulateAbilities(comp: UCombatantComponent*)
  +BuildAndConfirm()
  +Cancel()
  --
  <<Dispatchers>>
  +OnConfirm(action: FQueuedAction)
  +OnCancel()
}

%% ===================== Relationships =====================
WBP_HUD_Root o--> WBP_TurnQueue : owns
WBP_HUD_Root o--> WBP_CommandMenu : owns
WBP_HUD_Root o--> WBP_ATBBar : owns many (party/enemy)

WBP_TurnQueue o--> WBP_QueueEntry : pools many
WBP_QueueEntry ..> UCombatantComponent : binds to
WBP_ATBBar ..> UCombatantComponent : binds to
WBP_CommandMenu ..> UCombatantComponent : reads abilities
WBP_CommandMenu ..> FQueuedAction : emits OnConfirm

```




### Tiny example content
This is an example of a short paragraph using lorem ipsum
Cupidatat cupidatat voluptate mollit quis exercitation. Adipisicing irure ut reprehenderit ullamco non nostrud nulla eiusmod. Cillum consectetur laboris culpa cillum sunt ullamco officia deserunt velit labore cupidatat deserunt enim. Anim excepteur sunt nulla commodo laboris. Dolor in ipsum incididunt magna aliquip qui Lorem quis esse aliquip. Ea aliqua commodo irure pariatur minim est eiusmod sunt. Duis ad cupidatat ea eiusmod Lorem incididunt occaecat occaecat id laborum ullamco.

---


### Code block

Example code block:
```bash
# start local server
./tools/run.sh
```
  