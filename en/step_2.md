## Design an image

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step you will choose colours for an image and set them as variables in your code, then create an image and play with the colour values until you like it!  
</div>
<div>
<mark>Image, gif or video showing what they will achieve by the end of the step. ![](images/image.png){:width="300px"} </mark>
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

You will now be able to use orange and violet in your image! 

Feel free to add any other colours you like now in the same way.

[[[generic-theory-colours]]]

**Tip:** Make sure you don't double up on variable letters by using the same one twice!

--- /task ---

You can use the LED array on the SenseHAT to display an image by creating a **list** of which colour you want each pixel set to, and calling that list with the `set_pixels` command. 

The examples below are formatted in a grid of 8 values over 8 lines to simulate the way it will look on the SenseHAT (if you squint you might be able to see it!), but they *could* all be on the same line. Each letter in the following lists represents a single pixel on the array and what colour it should show.

--- task ---

**Choose:** Choose one of the images below to copy into your code. The examples include:
+ crab
+ crocodile
+ snake
+ frog
+ skull

--- code ---
---
language: python
filename: crab.py
line_numbers: false
line_number_start: 
line_highlights: 
---

crab = [
b,w,w,b,w,w,b,b,
b,w,n,b,w,n,b,b,
b,r,b,b,r,b,b,b,
b,r,b,b,r,b,b,b,
r,r,r,r,r,b,r,r,
r,r,n,n,r,r,r,b,
r,r,r,r,r,b,r,r,
r,b,r,b,r,b,b,b]

--- /code ---

--- code ---
---
language: python
filename: crocodile.py
line_numbers: false
line_number_start: 
line_highlights: 
---

croc = [
g,g,g,g,g,n,n,n,
g,b,g,b,g,g,g,g,
g,g,g,g,g,g,g,g,
g,g,n,w,n,n,n,w,
g,g,n,n,n,n,n,n,
g,g,n,n,n,w,n,n,
g,g,g,g,g,g,g,g,
g,g,g,g,g,g,g,g]

--- /code ---

--- code ---
---
language: python
filename: snake.py
line_numbers: false
line_number_start: 
line_highlights: 
---

snake = [
n,n,n,n,n,n,n,g,
g,g,g,g,g,g,g,g,
n,g,n,n,n,n,n,n,
n,g,g,g,g,g,n,n,
n,n,n,n,n,g,n,n,
y,g,y,g,g,g,n,n,
g,g,g,n,n,n,n,n,
r,n,n,n,n,n,n,n]

--- /code ---

--- code ---
---
language: python
filename: frog.py
line_numbers: false
line_number_start: 
line_highlights: 
---

frog = [
n,g,g,g,n,g,g,g,
n,g,y,g,n,g,y,g,
g,g,g,g,g,g,g,g,
g,r,r,r,r,r,r,r,
g,g,g,g,g,g,g,g,
g,g,g,g,g,g,g,g,
g,g,g,g,g,g,g,g,
g,g,n,g,g,g,n,g]

--- /code ---

--- code ---
---
language: python
filename: skull.py
line_numbers: false
line_number_start: 
line_highlights: 
---

skull = [
w,w,w,w,w,w,w,w,
w,w,w,w,w,w,w,w,
w,w,w,w,w,w,w,w,
w,n,w,w,w,n,w,w,
w,w,w,n,w,w,w,w,
w,w,w,w,w,w,w,w,
b,w,n,w,n,w,b,b,
b,w,n,w,n,w,b,b]

--- /code ---

--- /task ---

--- task ---

Select the code for the image you want from the examples above and **copy and paste** into your script in Trinket beneath the line reading `#Define image`. The example below uses the `crab` image.

**Tip:** You will need to copy the **entire code snippet** for the image you want to display.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 19
line_highlights: 20-28
---

#Define image
crab = [
b,w,w,b,w,w,b,b,
b,w,n,b,w,n,b,b,
b,r,b,b,r,b,b,b,
b,r,b,b,r,b,b,b,
r,r,r,r,r,b,r,r,
r,r,n,n,r,r,r,b,
r,r,r,r,r,b,r,r,
r,b,r,b,r,b,b,b]

--- /code ---

--- /task ---

Now that you have a list of colours for each LED, you need to run a command to make them light up. 

--- task ---

**Type:** Beneath the line that reads `#Display Image` add: `sense.set_pixels()`

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 31 
line_highlights: 32
---
#Display Image
sense.set_pixels()
--- /code ---

--- /task ---

This command will allow you call any list of 64 values (pixels) and display it as an image. You just now need to tell it which list you want it to show!

--- task ---

**Type:** Inside the brackets of the line you just typed, enter the name of the image you used:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 31 
line_highlights: 32
---
#Display Image
sense.set_pixels(crab)

--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. You should see the pixels light up with your chosen image!

--- /task ---

--- task ---

**Debug:** 
+ What does your error message say? Which line has an error?
+ Does your code match the code above?

--- collapse ---
---
title: NameError
---

+ Have you got the right letters in your list?
+ Have you defined all the colours you are using?
+ Have you spelled the name of your image correctly in `sense.set_pixels(image)`?

--- /collapse ---

--- collapse ---
---
title: SyntaxError
---

+ Have you got commas on the end of each line of your image list?
+ Are you missing any square brackets at the beginning and end of your image list? `[ ]`


--- /collapse ---

--- /task ---

--- save ---
