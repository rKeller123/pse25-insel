- **Moderator:** Raphael
- **Recorder:** Yassica
- **Date:** 02/04/2025 08:30 - 09:30
- **Location:** Inselspital, Bettenhochhaus, B121
- **Present Persons:** Raphael Keller, Yanic Bernhard, Elisa Stauffer, Silas Kammler, Yassica Umaparan, Jolan Knüsel, Florin Ackermann, Dr. Waldo Valenzuela

# Agenda
|  | What | Who | Time |
| --- | ---- | --- | ---- |
| 1 | WIP | All | 10 |
| | Presentation of changes since last meeting. | | |
| | - Drag and Drop| | |
| | - Colorpicker | | |
| | - (Partial) Refactor of FourViewer to hold multiple instances| | |
| 2 | Colorpicker Questions | Jolan | 10 |
| | Add second slider for alpha? | | |
| 3 | FourViewer Refactor Questions | Raphael | 10 |
| | Conflicts when scrolling, using the slider on one instance affects the other | | |
| 4 | Brushing Feature | All | 10 |
| | Brushing mechanic, other tasks in parallel to brushing | | |

# WIP
## Drag and Drop
**Feedback:**
Drag and Drop can be implemented without the Component.
Hint for next time: Ask Claude AI for a html code in feature (here: drag and drop).
If we want we can change it.

## Colorpicker 

**Question:** Add second slider for alpha?

 
**Idea:** Is nice to have. Add a interface with brightness and colorpicker.
It is our decision.


## (Partial) Refactor of FourViewer to hold multiple instances
 
**Question:** Conflicts when scrolling, using the slider on one instance affects the other

**Explanation:**
- Clinical viewer: Normally the grid is predefined. Forviewer we have one with 4 grid, as we have now.
The idea is to drop 4 different images into the Fourviewer, with the other perspectives smaller on the bottom side.

    **Source Code** 
- **FourviewerInstance:** We need to create a key to identify one window.
One Component (the ViewerImage2D) should work alone, and different volumes should be able to be drag and dropped in one window.
- **Holder:** How can we get functions from inner component for the upper component? We use the holder, it is used to get information from internal component. 

    We're getting the change done information from one sub component, which requests the other subcomponents to modify the change. 

**Feedback:** This is more complicated, but nice to have.

## Brushing

**Question:** The smoothness through interpolation?

**Idea:** To paint on 2D slice and not on the 3D volume, to have more fluency. In backround, make a screenshot and adapt it later on 3D.
Interpolation is done through the renderer-effect.

## Explanations from Waldo
Use of hook in useEffect: 
1. at the beginning when created, 
2. preparation for the 4 viewer etc. 

## Stories
**High priority:** brushing with size adaptation for the brush

(Simplify the code and understand what happens there)
- create one single 2D Viewer, isolate it as one
- update the brushing feature
    - Painting the 2D without updating the Volume 3D (Note: when scroll the paint will disappear)
    - size adaptation
- Update the interface for Colorpicker, add brightness 

## Next Meeting
- Wednesday, 16.04.2025 at 8:30
- Bettenhochhaus, B121