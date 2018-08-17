---
layout: post
title:  "Generating Interesting Isosurfaces"
date:   2018-08-13 10:39:54 -0400
categories: voxel
---
<p>
- Now that we have a reliable way to sample and render isosurfaces, we need some interesting isosurfaces to render. Most good methods start with a base of some volumetric noise combined with the voxel’s vertical coordinate. I’m generating multiple different 3d samplers filled with random noise, and adding them together with different frequencies and amplitudes just like perlin noise for my volumetric noise function. I’m just doing linear interpolation, though, and its a fascinating thing because the interpolation method I’m using is clearly visible in the generated mesh. (See the attached example) the flatish parts that clearly change direction at each grid point is very distinctive of linear interpolation. In addition to subtracting the voxel’s vertical coordinate, I also subtract the voxel’s vertical coordinate truncate divided by 16 and then multiplied by 16 to give it those shelf-looking features. Because I’m not seeding the pseudorandom number generator, and I haven’t changed the generation algorithm much since ive started, ive become very familiar with the valley structure pictured.
</p>

