- **Moderator:** Raphael
- **Recorder:** Yassica
- **Date:** 16/04/2025 08:30 - 09:30
- **Location:** Inselspital, Bettenhochhaus, B121
- **Present Persons:** Raphael Keller, Yanic Bernhard, Elisa Stauffer, Silas Kammler, Yassica Umaparan, Jolan Knüsel, Dr. Waldo Valenzuela


|  | What | Who | Time |
| --- | ---- | --- | ---- |
| 1 | Review last iteration | | 10 |
|  | PaintingLayer + semi-working Rendering Pipeline | |  |
|  | ViewerImage2D, InitRenderWindow2D | |  |
| 2 | Still to do: | | 10 |
|  | Select color | |  |
|  | Mouseposition to pixelposition is happening at the wrong place | |  |
|  | Fixed radius | |  |
|  | Select color | |  |
|  | ImageData is rendered with wrong properties (direction, origin, spacings, ...)  | |  |
| 3  | Next Iteration | | ~ |
|  | Points from above | |  |
|  | background process write paintingdata into Segmentation | |  |

## Review last Ieration
**PaintingLayer + semi-working Rendering Pipeline**

*Feedback Waldo:* 

**seperated paintinglayer:**
we need to get the actor of the reslicer (initReslicer2D). The resliceMapper will give the exact position.
What we need to do is reproduce the actor and match.
Tipp: ask ClaudeAI 

**coloring smoothness:**
The coloring isn't smooth, because we don't have a buffer. 
We need a seperate handle class, which handles the painting, the class contains the code for the calculation, buffer.
This is done to avoid further code in another class and to have a clear presentation and better understanding of the code.

*TO DO:*
From the parent class: catch mousemovement and press, which is our object (all that .onMouseMove() should be moved)

## Still To Do
**Select color:** Focus on painting.

**Fixed radius**
Where on the UI do you want the radius changing?
S on Keyboard + Scroll on Mouse and add to the colorpicker a slide


## Till End of Iteration

1. paint on top of image
2. seperate class for coloring

## Next Meeting
- Wednesday, 30.04.2025 at 8:30
- Bettenhochhaus, B121