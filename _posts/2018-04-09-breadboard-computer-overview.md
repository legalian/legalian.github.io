---
layout: post
title:  "Breadboard computer overview"
date:   2018-04-09 10:39:54 -0400
categories: breadboard
---
<p>
The computer is broken down into different modules that are connected to each other mostly via the bus.
</p>
![figure 1]({{"/assets/breadboard/chapter1/figure1.png"|absolute_url}})
<p>
My power supply is just a usb 5v power cable that I cut and soldered to breadboard wires. It works fine.
My clock is built from the schematic below. I swap out the capacitor to adjust the speed of the clock. [elaborate] The clock outputs a square wave that keeps the computer going.
Buffers are designed to store one binary word. This is how data is manipulated within the computer- binary operands are stored in buffers A and B so that the bus can be used to place the result of the operation in another location. The address buffer is the same- used for dereferencing pointers. The C buffer, on the other hand, is used for shuffling around data and debugging. Then, there’s the instruction buffer, used for storing the current instruction that is to be executed. 
</p>
![figure 2]({{"/assets/breadboard/chapter1/figure2.png"|absolute_url}})
<p>
The multiplexer is used to switch between accessing the portion of ram addressed by the instruction counter and accessing the portion of ram addressed by the address buffer. This is integral to the operation of the computer; sometimes it needs to access instructions and sometimes it needs to dereference pointers, but both operate on the same ram. 
</p>
![figure 3]({{"/assets/breadboard/chapter1/figure3.png"|absolute_url}})
<p>
The bus is an important concept for the computer. The bus is what allows the computer to arbitrarily move information between different buffers. In other parts of the computer, each wire has an input and one or more outputs. The bus, though, has many inputs and many outputs. At any one time, only one component is outputting to the bus and only one component is accepting input from the bus. The ram and c buffer can input to or output from the ram, but most components only listen to the bus. components can selectively output with tristate buffers- outputs can be high, low, or high impedance.
</p>
![figure 4]({{"/assets/breadboard/chapter1/figure4.png"|absolute_url}})
<p>
Even though the computer is completely self-sufficient, I do have a raspberry PI connected to the bus for the purpose of testing and initialization. When the computer is started, I run a program on the raspberry PI to initialize the computer’s ram to a given set of instructions. To do this, the PI also has outputs that let it temporarily override the computer’s state and control its clock and instruction counter. Ram is set to input, multiplexer is set to listen to the instruction counter, and then the instruction counter counts while the PI sequentially reads the computer’s instructions onto the bus, populating the computer’s ram. Once that is finished, the instruction counter should be initialized to the location of the first instruction in memory. For my computer, that is always 0. 
</p>
![figure 5]({{"/assets/breadboard/chapter1/figure5.png"|absolute_url}})


<div>
{% if page.previous_in_category != nil %}
<a href="{{page.previous_in_category.url}}" style="float:right;">{{page.previous_in_category.title}} &#8250;</a>
{% endif %}
{% if page.next_in_category != nil %}
<a href="{{page.next_in_category.url}}" class="float:left;">&#8249; {{page.next_in_category.title}}</a>
{% endif %}
</div>

