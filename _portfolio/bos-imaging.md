---
title: "Background-Oriented Schlieren Imaging"
excerpt: "Making invisible air density gradients visible using optical techniques and Python."
collection: portfolio
layout: portfolio
author_profile: true
share: false
header:
  teaser: /images/bos/BOS.gif
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

### Normal View

<div style="margin: 30px 0;">
  <img src="/images/bos/normal.gif" alt="Normal camera view" style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>Standard camera view - heat distortion invisible</em></p>
</div>

### Schlieren Imaging

<div style="margin: 30px 0;">
  <img src="/images/bos/BOS.gif" alt="BOS processed view" style="width: 100%; max-width: 600px; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.3);">
  <p style="text-align: center; margin-top: 10px; font-size: 0.9em; color: #999;"><em>BOS processing reveals invisible air density gradients</em></p>
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
