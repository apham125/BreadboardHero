# BreadboardHero
CS120B Introduction to Embedded Systems Final Project

## Complexities/Build Upons
Complexity 1: Creating menus and implementing custom characters
>https://drive.google.com/file/d/1371Pp8gQtxMftL4qZOR3Cy3TNaJsfC7J/view?usp=sharing 

Complexity 2: Implementing 5x8 LED matrix with shift register 
>https://drive.google.com/file/d/118g5zl80c4tX_8tITvpPc-mhhgVNgqEL/view?usp=sharing  

Complexity 3: Using eeprom to save scores, adding music, and adding hit/miss messages on lcd
>https://drive.google.com/file/d/19rsqHC7MYtDOMAPzVz88VDO68wRqH_hR/view?usp=sharing  

## Final Demo
>https://drive.google.com/file/d/1DIfTntr68jKMNHNXrstmexbi18DRqp1Z/view?usp=sharing 



## PROJECT DESCRIPTION:
For this project, I created a rhythm game similar to guitar hero. Falling notes
appear on an LED matrix and when the notes reach the bottom of the matrix, the player
must click the corresponding button underneath it to score points. The player has a
choice between two songs with two difficulty settings each, normal and hard. Levels
labeled hard have their notes fall faster than the levels labeled normal. Three buttons
are used to navigate menus, choose which level to play and for tapping the falling
notes. Music is played during the game. A forth button is used to restart and start the
game from the title menu. Menus, scores and combo numbers are displayed on the
LCD screen. High scores can be saved as well.

## Rules and Controls:
The game starts off on the title screen. Press the reset/start button (the button on the far
right) to start the game. You will now be displayed with the song selection menu. The
left and right buttons (the first and second buttons from the left) are used to choose
which song you want to play. Pick a song using the selection button (the third button
from the left). After selecting your preferred song, you will be brought to the difficulty
menu. Use the left and right and selection buttons to choose which difficulty you would
like to play. Upon pressing the selection button, the level will start. Falling notes will
appear on the LED matrix and music will start playing. When the notes reach the last
row of the matrix, click the button that corresponds to the column it is in. If you time it
correctly, you will earn a hit and win points. If you don’t, you will earn a miss and get no
points. When the song ends you are shown your final score and your combo number
that you had. To play another song, press the selection button to go back to the song
selection menu. At any point of the game, you may press the reset/start button to go
back to the title menu. Press the reset/start button again to resume playing the game as
usual.

## SPECIAL CONSIDERATIONS:
I noticed that if you hold the correct button the whole time while the note is falling, as
long as the button is held when the note reaches the button, you will earn a hit on that
note. This would make the game very easy since you could just hold the buttons instead
of doing a single press. I did not know how to adjust this without affecting the combo
counter. However, if you don’t hold the buttons until the notes reach the bottom row, the
game will function as intended and be based on timing. Other than that, I did not notice
any errors with my code.

## SOURCE FILES:
* io.c/io.h- Custom char function obtained from
https://www.electronicwings.com/avr-atmega/lcd-custom-character-display-using-atmega-16-32-
* Shift.h- used to configure shift register. Code obtained from
https://embedds.com/interfacing-shift-register-with-avr/
* Main.c- main code that contains all tasks
* Beatmap.h - code that contains the beatmaps of the songs
* Variables.h - declares all variables and sm states I used
* PWM.h - code that contains PWM configuration provided from class
* Scheduler.h - scheduler struct provided form class
* Timer.h - timer provided from class
* simAVRHeader.h - provided from class

## TECHNOLOGIES USED/LEARNED:
* Avr studio 6
* ATmega1284p
* 4 buttons
* 16x2 LCD screen
* 5x8 LED Matrix with shift register
* Speaker
* EEPROM
>This project made me learn how to implement an LED matrix with a shift register. With
the shift register, I only needed to use 3 output pins from the microcontroller rather than
8 which allowed me to save some pins. I learned how to write to the matrix through the
shift register and how to display the falling dots. I was also able to learn how to write to
individual pixels and create my own custom characters on the LCD screen and use the
eeprom to save data.

## COMPONENT VISUALIZATION
![wiring](https://user-images.githubusercontent.com/72577619/160269382-78cc5bd2-3e0b-450c-b260-0e5e62665ff5.png)

## Task Diagram
![taskDiagram](https://user-images.githubusercontent.com/72577619/160269400-4d7df4be-2625-4946-82c9-2822bbc445c2.png)

