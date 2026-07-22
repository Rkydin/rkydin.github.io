---
title: "Background-Oriented Schlieren Imaging"
excerpt: "Making invisible air density gradients visible using optical techniques and Python."
category: "Optics"
skills: ["Python", "OpenCV", "NumPy", "Optics"]
date: 2026-02-01
last_updated: 2026-03-11
collection: portfolio
layout: portfolio
author_profile: true
share: false
header:
  teaser: /images/bos-imaging/teaser.jpg
---

<style>
.page__share {
  display: none !important;
}
</style>

**Project Duration:** February 2026  
**Status:** Complete

## Project Overview

Background-Oriented Schlieren (BOS) imaging makes invisible air density gradients visible. When air is heated, its refractive index changes — light bends slightly as it passes through regions of different temperature. BOS exploits this by placing a high-frequency background pattern behind the region of interest and comparing how that pattern appears to shift when a heat source is present versus when the air is undisturbed.

Those tiny apparent shifts in the pattern directly correspond to density gradients in the air, revealing structures like heat plumes, turbulence, and convection that are otherwise invisible to the naked eye.

## Results

### Jet Lighter

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px; margin: 30px 0;">
  <div>
    <video src="/images/bos-imaging/jetlighter-normal.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);"></video>
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Standard view - heat distortion invisible</em></p>
  </div>
  <div>
    <video src="/images/bos-imaging/jetlighter-bos.mp4" autoplay loop muted playsinline style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);"></video>
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>BOS processing reveals air density gradients</em></p>
  </div>
</div>

### Candle

<div style="margin: 30px 0;">
  <video src="/images/bos-imaging/candle-bos.mp4" autoplay loop muted playsinline style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);"></video>
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>BOS reveals heat plume and convection patterns from candle flame</em></p>
</div>

## Technical Implementation

**Core Technologies:**
* Python and OpenCV
* NumPy for array operations
* Procedurally generated sine wave background pattern

**Image Processing Techniques:**
* Background subtraction using `cv2.absdiff`
* Contrast enhancement with thresholding
* Temporal frame averaging with `cv2.addWeighted`
* Gaussian blur for noise reduction
* Inferno colormap visualization
* GIF export using `imageio`

## How It Works

1. Generate high-frequency background pattern
2. Capture baseline image of undisturbed air
3. Introduce heat source and capture comparison images
4. Calculate pixel shifts between baseline and heated frames
5. Apply image processing to enhance density gradient visualization
6. Map results to color for intuitive interpretation
