## Design an image

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step you will choose colours for an image and set them as variables in your code, then create an image and play with the colour values until you like it!  
</div>
<div>
Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"}
</div>
</div>

Using the understanding of RGB colour values from the previous project, it is possible to individually set each LED in the array to whatever colour you choose and create a simple image.

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
<span style="color: #0faeb0">Pixel Art</span> is the creation of images by colouring <strong>pixels</strong> one at a time in a specific way. Most digital images you look at are made of pixels, including all of your favourite video games! 
</p>


--- task ---

Open the [starter project](https://trinket.io/python/1ae94097b2){:target="_blank"}. Trinket will open in a new tab.

--- /task ---

You should see the starter script which contains all of the imports required for the SenseHAT, as well as a list of basic colours stored as simple single letter **variables** for you to use in your images:

+ `n` is null (black)
+ `w` is white
+ `r` is red
+ `y` is yellow
+ `g` is green
+ `b` is blue

You are now going to add two more colours to your program; orange and violet. To do this, you need to enter the RGB values for these colours into your variables list. 

--- task ---

**Add:** At the bottom of your code, add the following lines:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 11 
line_highlights: 13-14
---
g=(0,255,0) #green
b=(0,0,255) #blue
o=(255,125,0) #orange
v=(255,0,255) #violet

--- /code ---

You will now be able to use orange and violet in your image! Feel free to add any other colours you like now, or you can easily come back later if you decide you need to.

[[[generic-theory-colours]]]

**Tip:** Make sure you don't double up on variable letters by using the same one twice!

--- /task ---



--- save ---