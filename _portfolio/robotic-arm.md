---
title: "Surgical-Inspired Robotic Arm"
excerpt: "Building an affordable teleoperated robotic arm with 7 degrees of freedom for precise human-like movements."
collection: portfolio
layout: portfolio
author_profile: true
share: false
header:
  teaser: /images/roboticarm/prototype2.1.png
---

<style>
.page__share {
  display: none !important;
}
</style>

**Project Duration:** August 2025 - Present

## Project Overview

Building an affordable robotic arm intended to mimic precise human arm movements through teleoperation. The goal is to create a 7 DOF (degrees of freedom) robot that acts similar to a human arm and can be teleoperated intuitively - a cheap way for precision robotics at home.

## Design Evolution

### Prototype 1.1 - Initial Concept

Early CAD design exploring the general concept with available tools and components.

<div style="margin: 30px 0;">
  <img src="/images/roboticarm/prototype1.1.png" alt="Prototype 1.1 - Initial assembly concept" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Initial assembly concept showing overall design approach</em></p>
</div>

**Key Features:**
- Two servos and differential gear set for shoulder rotation and elevation
- Stepper motor mounted to linkage for elbow flexion
- Servo on elbow for forearm rotation
- Cable-driven end effector

### Prototype 1.2 - Linkage Mechanism

Close-up of the early linkage controlled by stepper motor. This mockup revealed critical interference issues that limited movement range.

<div style="margin: 30px 0;">
  <img src="/images/roboticarm/prototype1.2.png" alt="Prototype 1.2 - Stepper-controlled linkage" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Early linkage mechanism showing interference challenges</em></p>
</div>

**Shoulder Joint Design:**
- Bevel gear differential for dual-axis rotation
- Combination of up/down movement and rotational control
- Mounted stepper motor driving elbow linkage

**Issues Identified:**
- Part interference limiting range of motion
- Need for design refinement in subsequent iterations

### Prototype 1.3 - Cable-Driven Gripper

Initial end effector design.

<div style="margin: 30px 0;">
  <img src="/images/roboticarm/prototype1.3.png" alt="Prototype 1.3 - End effector gripper" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Cable-driven gripper for precise manipulation</em></p>
</div>

**Design Approach:**
- Cable-driven actuation using Bowden cables
- Designed for precise manipulation at small scale

---

## Prototype 2 - Refined Design

More nuanced and thoroughly planned iteration addressing lessons learned from Prototype 1.

### Prototype 2.1 - Differential Shoulder Joint (In Progress)

Redesigned differential gear system and hub for the shoulder joint.

<div style="margin: 30px 0;">
  <img src="/images/roboticarm/prototype2.1.png" alt="Prototype 2.1 - Differential gears and hub" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Redesigned differential gears and shoulder hub (work in progress)</em></p>
</div>

**Key Improvements:**
- Stepper motors with pulley system to transfer weight away from the arm
- Improved differential gear design for shoulder actuation
- More robust hub structure
- Better weight distribution for enhanced precision

---

## Technical Approach

**Mechanical Design:**
- Multiple joints and linkages to reproduce key arm motions
- Differential gear sets for joint actuation
- Bowden cables to drive small end-effector gripper
- 7 DOF for human-like movement capability

**Development Tools:**
- SolidWorks for CAD design and assembly
- 3D printing for rapid prototyping
- C++ for control software
- Stepper motors and servo actuators

**Design Goals:**
- Affordable precision robotics for home use
- Intuitive teleoperation interface
- Human arm-like kinematics
- Precision control at accessible cost

---

## Current Status

🚧 **In Active Development**

Currently refining Prototype 2 design with focus on:
- Optimizing differential gear geometry
- Improving weight distribution through pulley systems
- Developing control software for teleoperation
- Testing joint ranges of motion and precision

---

## Future Development

- Complete Prototype 2 mechanical design
- Integrate full 7 DOF control system
- Develop teleoperation interface
- Implement precision control algorithms
- Add force feedback capability
- Expand end effector capabilities
