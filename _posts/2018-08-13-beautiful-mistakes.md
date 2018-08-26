---
layout: post
title:  "Beautiful Mistakes"
date:   2018-08-13 10:39:54 -0400
categories: voxel
---

<p>
Working on the voxel engine was a difficult process. I've had to do a lot of debugging, and very few even displayed anything abnormal to the screen. When bugs do manifest visually, however, it's a nice change, because it allows you to think more creatively about what the problem could be (and usually solve the problem much faster). I've documented some of the more interesting visual bugs below.
</p>
![figure 5]({{"/assets/vox/bonus/screenshot1.png"|absolute_url}})
<p>
This is what happens when perlin noise is done with nearest-neighbor interpolation. Everything implemented is perfectly functional in this example- the only problem was that the isosurface I specified wasn't the one I had in mind.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot2a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot2b.png"|absolute_url}}"/>
    </div>
</div>
<p>
Here is the block visualization method, but with the scaling on each face too small, and with no skirts.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot3a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot3b.png"|absolute_url}}"/>
    </div>
</div>
<p>
These two screenshots were from before I discovered dual contouring. I had implimented the block method and marching cubes, and I was trying to create a way to bridge the two so that different parts of the world could have different looking features. It involved using the block method but having it connect to vertecies that lie on the edge between two voxels. These screenshots are from the middle of that experiment.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot4a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot4b.png"|absolute_url}}"/>
    </div>
</div>
<p>
These screenshots are the result of the octree being incorrectly stored. Volumes filled with only one type of mass may have to be divided further if a vertex must lie in that volume, i.e. if there is a different type of mass that lies along its edge. If that condition is ignored, then this result is produced. I think it's interesting because you can see the octree in the rendered mesh.
</p>
<div style="display:flex; margin:1em;">
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot5a.png"|absolute_url}}"/>
    </div>
    <div style="flex:45%;">
        <img src="{{"/assets/vox/bonus/screenshot5b.png"|absolute_url}}"/>
    </div>
</div>
<p>
This is the result of a failure when the program is reading from file. In this case, the program was saving the file differently than it was reading it, which manifests in this interesting formation.
</p>






