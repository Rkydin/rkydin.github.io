---
title: "Background-Oriented Schlieren Imaging"
excerpt: "Making invisible air density gradients visible using optical techniques and Python."
collection: portfolio
layout: portfolio
author_profile: true
share: false
header:
  teaser: https://i.imgur.com/iRkqtU8.gif
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
    <img src="https://i.imgur.com/pJ4EZW5.gif" alt="Normal view - jet lighter" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Standard view - heat distortion invisible</em></p>
  </div>
  <div>
    <img src="https://i.imgur.com/iRkqtU8.gif" alt="BOS view - jet lighter" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
    <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>BOS processing reveals air density gradients</em></p>
  </div>
</div>

### Candle

<div style="margin: 30px 0;">
  <img src="https://i.imgur.com/A5L7gtD.gif" alt="BOS view - candle" style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
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

1. Generate high-frequency background pattern (sine wave)
2. Capture baseline image of undisturbed air
3. Introduce heat source and capture comparison images
4. Calculate pixel shifts between baseline and heated frames
5. Apply image processing to enhance density gradient visualization
6. Map results to color for intuitive interpretation
