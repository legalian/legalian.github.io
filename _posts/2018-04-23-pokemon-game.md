---
layout: post
title:  "Pokemon Game"
date:   2018-04-16 10:39:54 -0400
categories: pokemon
---
<p>
The plan was to use 2d perlin noise to randomly generate the continent. To do this, a series of smoothed random noise functions with increasing frequencies and decreasing amplitudes are summed together to produce a fractal noise texture. Then, that noise is interpreted as a heightmap and colored appropriately, with the lowest values corresponding to the ocean. For more about procedural generation with peril noise, see the voxel engine project. 
</p>
![figure 1]({{"/assets/pokemon/figure1.png"|absolute_url}})
<p>
Road layout could easily be generated with a modified random walk. A starting position for the player is chosen somewhere in the map, and then the algorithm takes random steps of varying lengths outward from this position. Extra care is taken so that the step does not land in the water or cross another road. The algorithm may branch out a set number of times. In game, each branch only allows the player to go down one path until they find an ability or key to unlock the other branch.  
</p>
![figure 2]({{"/assets/pokemon/figure2.png"|absolute_url}})
<p>
Finally, the full list of Pokémon is partitioned into different biomes so that they can be assigned to different groups of roads. Since there are too many of each type of Pokemon to just sort them by their primary type, I create random clusters with the following method: clusters are started with 2 random Pokemon each. Then, each remaining Pokemon is randomly assigned to a cluster. Pokemon are more likely to be assigned to a cluster if it has Pokemon of similar types or egg groups. 
</p>
![figure 3]({{"/assets/pokemon/figure3.png"|absolute_url}})
<p>
Then, each cluster is randomly assigned to a road. Roads close to the coast are most likely to accept clusters with many water pokemon and roads in the mountains are more likely to accept rock, ground, or fire pokemon. Grass and normal pokemon most likely show up in the height values in between. For other types, the only criteria is that clusters are more likely to be assigned to roads next to roads with similar clusters. 
</p>
![figure 4]({{"/assets/pokemon/figure4.png"|absolute_url}})
<p>
The list of Pokémon, however, could not be randomly generated or manually implemented in a reasonable amount of time. I wanted every Pokémon to appear in game, but I didn’t have the time to compile a sprite sheet with every single one. Spritesheets online either would have missing Pokémon or duplicates when the Pokémon had different male and female sprites, preventing me from indexing into the sheet sequentially. I also needed a file with all of the base stats, names, and other attributes of each Pokémon. All of this information was available on serebii.net, so I wrote a web scraper to extract this information and save it. The source of this webscraper is written in python and is very small, so I’ve made it available below.
</p>


<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>
