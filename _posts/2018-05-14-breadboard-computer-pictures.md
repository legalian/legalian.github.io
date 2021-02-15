---
layout: post
title:  "Breadboard computer pictures"
date:   2018-05-14 10:39:54 -0400
categories: breadboard
---


![figure 1]({{"/assets/breadboard/chapter5/fig18.png"|absolute_url}})
<p>
An image of the whole thing, albeit not connected together.
</p>

![figure 2]({{"/assets/breadboard/chapter5/fig19.png"|absolute_url}})
<p>
The clock- a 555 IC in astable configuration
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig17.png"|absolute_url}})
<p>
This component is a series of multiplexers that handle bitwise shifting. I thought it would be cool to make it circular, since it eliminates any wires having to travel back to the other side of the board, but I ended up feeling very silly wiring the thing up when all the breadboards were inaccessible.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig16.png"|absolute_url}})
<p>
Two registers- the address register that controls what word of memory is being accessed by RAM, and another, general purpose register that can be used for rearranging data in other registers.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig15.png"|absolute_url}})
<p>
Here you can see the RAM, and also the multiplexers that head into the RAM that decide between listening to the address register, for accessing program memory, and listening to the instruction counter, for accessing the next instruction that should be executed.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig14.png"|absolute_url}})
<p>
MOSFETS to allow the raspberry PI to initialize the machine state.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig13.png"|absolute_url}})
<p>
Again, I 3D printed a setup that I thought would be cool, and then it bit me during wiring when I realized that none of the breadboards were accessible. This is the full adder/subtraction circuit. It also allows the computer to perform bitwise binary operators (except for bitwise shifting.)
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig12.png"|absolute_url}})
<p>
A cleaner view of the registers that feed into the ALU. All binary operations are performed on the values stored in these registers.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig10.png"|absolute_url}})
<p>
This is the doodad I would use to test parts of the circuit. They would act as a pulldown resistor, which would sometimes disrupt the circuit if I was measuring an intermediate step in the circuit, so I had to test everything modularly.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig9.png"|absolute_url}})
<p>
This is the instruction buffer and the decoder that I used to decode certain instructions.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig9.png"|absolute_url}})
<p>
This is the instruction buffer and the decoder that I used to decode certain instructions.
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig7.png"|absolute_url}})
<p>
Overall view of the RAM and instruction handling portion
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig6.png"|absolute_url}})
<p>
Decoders used to select input and output registers during the appropriate instructions
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig5.png"|absolute_url}})
<p>
The program counter (and inverters because the carry signal was active low)
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig4.png"|absolute_url}})
<p>
Correct operation of a small portion of the bitwise shifting circuit
</p>

![figure 3]({{"/assets/breadboard/chapter5/fig2.png"|absolute_url}})
<p>
A series of OR gates and a latch. This stores whether or not the last operation was nonzero, for the purposes of conditional branching. The conditional skip operation uses this to determine whether or not to skip.
</p>

<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>
