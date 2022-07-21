## Make an animation

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
In this step you will create a copy of your image, edit it to be slightly different and display your new frames in order to make an animation.
</div>
</div>
<div>
<iframe src="https://trinket.io/embed/python/e1a3182c3c?outputOnly=true&runOption=run&start=result" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>
</div>

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
<strong>Animation</strong> is created by swapping images (called frames) in front of your eyes very quickly. The rate at which the images are swapped is known as the <strong>frame rate</strong>, and it is measured in <strong>frames per second</strong> (how many pictures are shown to you each second). Normal TV and movies are usually shown at 24fps - that means each frame is only shown for 0.04 seconds! 
</p>

To create an animation, you need at least two frames or images which you can swap quickly. To do this, you will first create a copy of your image from the previous step, then edit it slightly.

<mark>
1. Design another image/ more images
2. Call images in order
3. End the loop before 28s
</mark>

--- task ---

**Copy:** Select the entire list you created for your image, including the name and the final square bracket. Copy the list using `Ctrl+C` and paste the copy beneath the first using `Ctrl+V`:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 19
line_highlights: 32-41
---
#Define image
image = [
    o,o,o,o,o,o,o,o,
    o,w,w,o,o,w,w,o,
    o,b,w,o,o,b,w,o,
    o,o,o,o,o,o,o,o,
    o,r,o,o,o,o,r,o,
    o,o,r,o,o,r,o,o,
    o,o,o,r,r,o,o,o,
    o,o,o,o,o,o,o,o
    ]


image = [
    o,o,o,o,o,o,o,o,
    o,w,w,o,o,w,w,o,
    o,b,w,o,o,b,w,o,
    o,o,o,o,o,o,o,o,
    o,r,o,o,o,o,r,o,
    o,o,r,o,o,r,o,o,
    o,o,o,r,r,o,o,o,
    o,o,o,o,o,o,o,o
    ]


--- /code ---

--- /task ---

--- task ---

**Edit:** Change the name of your second list by adding a `1` to the end of the name:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 19
line_highlights: 32
---
#Define image
image = [
    o,o,o,o,o,o,o,o,
    o,w,w,o,o,w,w,o,
    o,b,w,o,o,b,w,o,
    o,o,o,o,o,o,o,o,
    o,r,o,o,o,o,r,o,
    o,o,r,o,o,r,o,o,
    o,o,o,r,r,o,o,o,
    o,o,o,o,o,o,o,o
    ]


image1 = [
    o,o,o,o,o,o,o,o,
    o,w,w,o,o,w,w,o,
    o,b,w,o,o,b,w,o,
    o,o,o,o,o,o,o,o,
    o,r,o,o,o,o,r,o,
    o,o,r,o,o,r,o,o,
    o,o,o,r,r,o,o,o,
    o,o,o,o,o,o,o,o
    ]

--- /code ---

This will allow us to call our two frames separately. 

**Tip:** If you make more frames, remember to change the name for each one!

--- /task ---

At the moment your frames are identical, so won't have the appearance of movement if we swap them. You need to change some of the pixels in your image. In this example, we will make the face's eyes look from side to side.

--- task ---

**Edit:** Change some of the pixels in your images by deleting and replacing them. In this example, we will be moving the blue pixels designated with a `b` one space to the right:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 19
line_highlights: 35
---
#Define image
image = [
    o,o,o,o,o,o,o,o,
    o,w,w,o,o,w,w,o,
    o,b,w,o,o,b,w,o,
    o,o,o,o,o,o,o,o,
    o,r,o,o,o,o,r,o,
    o,o,r,o,o,r,o,o,
    o,o,o,r,r,o,o,o,
    o,o,o,o,o,o,o,o
    ]


image = [
    o,o,o,o,o,o,o,o,
    o,w,w,o,o,w,w,o,
    o,w,b,o,o,w,b,o,
    o,o,o,o,o,o,o,o,
    o,r,o,o,o,o,r,o,
    o,o,r,o,o,r,o,o,
    o,o,o,r,r,o,o,o,
    o,o,o,o,o,o,o,o
    ]


--- /code ---

**Tip:** Make sure all the lines in your list end in a comma and have eight terms. (It should be easy to spot if something is off, thanks to your clever formatting!)

--- /task ---

The next thing to do is to call the images one after another to create the sense of motion. You do this by calling the first image, waiting for a fraction of a second using `sleep`, then calling the second image for the same amount of time and repeating this process over and over. 

[[[generic-python-sleep]]]

--- task ---

**Type:** At the end of your code, add the following:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 44
line_highlights: 46-48
---
#Display Image
sense.set_pixels(image)
sleep(0.5)
sense.set_pixels(image1)
sleep(0.5)

--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. This should call your two images one after another, for half a second each. It will look like your image changes, but it won't *keep* moving as we haven't coded our **loop** yet.

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

--- collapse ---
---
title: My image isn't changing
---

Have you called both images in turn, or are they both `image`? 

--- /collapse ---

--- /task ---

A **loop** is a section of code that repeats over and over again. You're going to use a **loop** now to make your images switch quickly over and over again.

[[[generic-python-for-loop]]]

--- task ---

**Type:** Add a blank line beneath the line that reads `#Display Image`. On the new line type `for i in range(10):'. This will create a **for loop** which will run **10 times**.

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 44
line_highlights: 45
---
#Display Image
for i in range(10):
sense.set_pixels(image)
sleep(0.5)
sense.set_pixels(image1)
sleep(0.5)

--- /code ---

--- /task ---

Now that you have created our loop, we need to **indent** the parts of the code you want to be looped: everything underneath what you just typed.

--- task ---

**Edit:** At the beginning of every line of code **beneath** the line you just added, press the `Tab` key to insert four spaces and create an **indented block** of code:

--- code ---
---
language: python
filename: main.py
line_numbers: true
line_number_start: 44
line_highlights: 45
---
#Display Image
for i in range(10):
    sense.set_pixels(image)
    sleep(0.5)
    sense.set_pixels(image1)
    sleep(0.5)

--- /code ---

--- /task ---

--- task ---

**Test:** Run your code. You should see your images switch back and forth.

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

--- collapse ---
---
title: My image isn't changing
---

Have you called both images in turn, or are they both `image`? 

--- /collapse ---

--- /task ---



--- save ---