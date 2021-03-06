CMPE/CISC 457 Assignment 1

Due Friday, October 8 at noon.

In this assignment you'll build an image editor that applies
translation, scaling, and rotation to images.

Undergraduates may work in groups of two. Graduate students must work
individually.

1. ~~Get the main.py code running. READ ALL OF THE CODE AND UNDERSTAND
   HOW IT WORKS.~~

2. ~~Modify transformImage() to apply backward projection according to
   the comments in that code. Once this is done, test it by trying to
   translate the image by moving the mouse with the left button held
   down. You'll find that Python performs the translation slowly.~~

3. ~~Modify scaleImage() according to the comments in that code. Test
   with the mouse.~~

4. ~~Modify rotateImage() according to the comments in that code. Test
   with the mouse.~~

5. Modify the code so that multiple transformations do not cause parts of
   the image to be lost. Do not do this part until the transformations
   (above) are working.

   You can do this in eight lines of code. Think about this a long
   time before starting to implement. Poor implementations will lose
   marks, even if they work.

   To do this, you will need to apply your transformations to the
   _initially-loaded_ image, not to the current image.

   But ... in addition to the current transformation being made by the
   mouse, you will have to transform that initially-loaded image by
   all the _other_ transformations that took place before the current
   transformation. So you will need to store a global 'accumulated
   transformation' which is all the transformations that have already
   been applied. Then transformImage() will include the already-
   accumulated transformations with the current transformation before
   doing its backward projection.

   Once the current transformation is complete (i.e. when the mouse
   button is released), you will have to include the current
   tranformation with the already-accumulated transformations and
   store that as the _new_ accumulated transformations.

To submit:

Submit two files with EXACTLY THESE NAMES.

     README.txt - containing the name, student number, and netID of each
                  person working on the assignment.  Include here any
                  comments you have for the TA.

     main.py    - the modified code, well commented.

YOU WILL LOSE MARKS IF YOU DO NOT SUBMIT TWO FILES WITH EXACTLY THE
NAMES ABOVE.

IN A GROUP OF TWO, ONLY ONE PERSON MAY SUBMIT THE ASSIGNMENT. IF
YOUR GROUP SUBMITS TWO ASSIGNMENTS, YOU WILL LOSE MARKS.

For marking, we will read your code for correctness, clarity, and
quality, and we will run your code.
