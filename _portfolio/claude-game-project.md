---
title: "Game Project Built with Claude"
excerpt: "A first-person co-op melee game I'm building in Godot 4 with Claude. This page tracks its progress."
category: "Game Dev"
skills: ["Godot 4", "GDScript", "Claude Code", "Game Design", "Multiplayer Architecture"]
date: 2026-11-02
last_updated: 2026-11-04
collection: portfolio
layout: portfolio
author_profile: true
share: false
header:
  teaser: /images/claude-game-project/teaser.jpg
---

<style>
.page__share {
  display: none !important;
}
</style>

**Started:** November 2026  
**Status:** In progress  
**Latest update:** Devlog 001, November 4, 2026

## About the Project

A first-person melee game for online co-op, made in Godot 4. You guard in one
of four directions, attack from your guard, and block or parry enemy attacks
by guarding the side they come from.

I'm building it with Claude Code. Each milestone gets a devlog entry below.

## How It's Built

* **Engine:** Godot 4, GDScript
* **AI:** Claude Code edits scenes live in the Godot editor through a plugin
* **Project rules:** a CLAUDE.md file keeps context between sessions
* **Devlog media:** a showcase scene plays the mechanics and records itself
* **Multiplayer:** built for online co-op from the start; the host decides every hit

## Progress

| Milestone | Status |
|---|---|
| First-person movement | Done |
| Four-direction guards and swings | Done |
| Blocking, bracing and parrying | Done |
| Training dummy that attacks | Done |
| Hit, block and parry effects | Done |
| Health and stamina | Next |
| Enemy that blocks back | Planned |
| Online play | Planned |
| Real weapons and sounds | Planned |

## Devlog

### 001: Guard, Strike, Parry
*November 4, 2026*

First playable version: guard in four directions, attack, and block or parry
a training dummy.

<div style="margin: 30px 0;">
  <video src="/images/claude-game-project/001-showcase.mp4" autoplay loop muted playsinline style="width: 100%; max-width: 800px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);"></video>
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>All four guards and swings, then a hit, a block, a braced block and a parry</em></p>
</div>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <img src="/images/claude-game-project/001-pose-left.png" alt="Left guard" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Left guard</em></p>
  </div>
  <div>
    <img src="/images/claude-game-project/001-pose-up.png" alt="Up guard" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Up guard</em></p>
  </div>
  <div>
    <img src="/images/claude-game-project/001-pose-down.png" alt="Down guard" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Down guard</em></p>
  </div>
  <div>
    <img src="/images/claude-game-project/001-pose-right.png" alt="Right guard" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #666;"><em>Right guard (also the rest pose)</em></p>
  </div>
</div>

**What's new**

* Four guard directions you can switch anytime
* Swings start from your current guard and leave a trail
* Blocks only work if you guard the side the hit comes from; hits from behind can't be blocked
* Hold right click to brace (stronger block, slower movement); tap it right before a hit to parry
* Training dummy shows which side it will attack from and flashes orange before it hits
* Every hit, block and parry has its own effect: flashes, sparks, dust, optional blood, damage numbers and screen-edge warnings

**Problems solved**

* **Blocks sometimes picked the wrong side.** Fast swings could register from the opposite side. Hits are now judged by where the blade first touches you.
* **Parrying was too easy.** You could parry by spamming guard switches. Parry now has its own button, and missed presses briefly disable it.
* **Inputs got lost mid-swing.** Presses during a swing were ignored. The game now saves your last press and uses it when the swing ends.
* **The overhead swing trail was invisible.** A straight-down swing lined up with the camera. Overhead swings now come down slightly off center.
