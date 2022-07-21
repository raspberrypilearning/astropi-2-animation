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



--- /task ---


--- save ---