---
layout: post
title:  "Minmax trees"
date:   2018-06-11 10:39:54 -0400
categories: ted
---
<p>
The other component to the chess AI is a minmax tree. This is what allows the program to look ahead to see which moves put it in a better position. When the program looks ahead some number of moves in advance, it constructs a tree that represents the next possible moves. After a certain number of moves in the future, the program will cap the tree off with the heuristic value of that node. It is assumed that the program will choose the best possible path for it, and the opponent will choose the worst path for the program. The heuristic for each node that is not a terminal node will be the max or min of its children respectively.
</p>
![figure 1]({{"/assets/ted/chapter2/figure1.png"|absolute_url}})
<p>
Consider the below diagram, where the tree is in the middle of being calculated. One of the paths does not need to be explored, because the only effect it could have on the value of its parent heuristic is to lower it, and its parent’s heuristic is already too low to be considered. It can be skipped. This process is known as alpha-beta pruning, and it eliminates a lot of computation needed, which allows the program to look further ahead. In general, anytime the maximum score that the minimizing player is assured of is greater than or equal to the minimum score that the maximizing player is assured of, that node does not need to be explored. 
</p>
![figure 2]({{"/assets/ted/chapter2/figure2.png"|absolute_url}})
<p>
Each heuristic is expensive to calculate because it involves evaluating a neural network over the chess board. I had to play around with what inputs the neural network received to make it as effective as possible. I started with simply giving each square of the board an input for each piece it could possibly have. This was not feasible because of the number of nodes needed. 
</p>
![figure 3]({{"/assets/ted/chapter2/figure3.png"|absolute_url}})
<p>
The second method I tried was using a convolutional neural network. A convolutional neural network re-uses groups of weights in a moving window over the input, which must be arranged in a grid. 
</p>
![figure 4]({{"/assets/ted/chapter2/figure4.png"|absolute_url}})
<p>
After experimenting with various convolution sizes and approaches, the best solution turned out to be adding another input to the neural network for which pieces were under pressure, or resting on a space that could be attacked by one of the opponents pieces. After that, smaller convolutions were much more effective because they trained faster and executed faster, allowing the program to look further ahead. The solution that reigned supreme was to use a neural network with an input for each kind of piece that could lie on that space, an input for if that space was under pressure, and an input for if that space were guarded. The neural network is evaluated for each square in the grid, and summed up to get the heuristic of the entire grid. 
</p>
![figure 5]({{"/assets/ted/chapter2/figure5.png"|absolute_url}})
<p>
Once a game has completed, the neural network is trained over the last 8 games. The last game has the highest learning rate, with the learning rate tapering off by the 8th to last game, because it is easiest to determine a game’s outcome by later board positions. The program was trained by both playing against itself and also from games collected with a webscraper. 
</p>
![figure 6]({{"/assets/ted/chapter2/figure6.png"|absolute_url}})


<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>
