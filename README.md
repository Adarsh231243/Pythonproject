# Pythonproject
How to play the Game?

1.You should have installed python along with two libraries called pygame (pip install pygame) and mediapipe (pip install mediapipe) on your device.
2.To play the game you have first run code on your pc then show your palm of one of your hand to your web cam.
4.Move your palm on the mosquito closing the fingers from top to bottom in forward direction consecutively.
5. If you kill the mosquito you’ll get the points but if you kill the bees your points will be deducted.
Game Description:
The game consists of mosquitoes and bees flying in the center of the screen. Every time you swat a mosquito you get 1 point and every time you swat a bee you lose 1 point. Everything must be done within a certain number of seconds as mentioned above. Our game is based on the concept of computer vision.
This game consists of 11 different modules along with two libraries pygame and mediapipe. 
Pygame:It is ais a set of python modules designed for writing video games. Pygame adds functionality on top of the excellent SDL library. This allows you to create fully featured games and multimedia programs in the python language.
Mediapipe: It is responsible for detecting different body movements

Construction of the game

The game is made up of within 11 different modules. The explanation of major modules is given below:
background.py
It will display the background of the game along with loading the background image in specific resolution in specific position.
mosquito.py
This file consists of a mosquito class which consists of different functions designed for different functionality like:
For spawning the mosquito
defdefine_spawn_pos(self, size)
This function will span the mosquito in different position
For animating the mosquito:
This will the changes the frame of the mosquito when needed.
 defanimate(self)

Similarly, we have used functions for movement of the mosquito, killing the mosquito and so on

main.py
In this file there are the main startup functions of pygame and this is the page to use to start the game. If you just want to change some settings open the settings.py file. You can many modifications like you can change the time duration of the game, difficulty level etc.

game.py
This is the file to manage the events of the game and it includes in addition to various libraries, also the files for the management of the hand such as a cursor, bee.py, and mosquito.py

hand_tracking.py
This module will scan your hands and detect your movements with the help of media pipe library. E.g. defscan_hands(self, image):



The major logic used behind the game:
Add hand as controller (Computer Vision)
As we mentioned in the introduction, this part of the project was made with mediapipe. First, we install the library, and the command is:
pip install mediapipe
According to the Mediapipe documentation, it manages to generate a 3d map of 21 points of the hand as follows:


 

The idea is to use landmark points, as we can see the highest point of the hand is the number 12 and immediately before the palm of the hand there is the number 9. When point number 12 is lower than 9 we can say that the hand is closed, always open in the other case.
To explain it in a simpler way, as you can see in the image when the red dot is lower than the green one the hand is closed so send the click command.
How you’ll be able to kill mosquito?
We put rectangles on each element to better explain the concept. When two rectangles overlap, that of the hand and the mosquito or bee, an event is associated.
How game will differentiate between whether you are killing mosquito or bees?
It’ll track your hand movement position and mosquito or bee’s position. If your hands position will overlap with mosquito it’ll remove(kill) the mosquitoes and if it overlaps with bees it’ll remove (Kill) bees. Bees and mosquito are all already defined by the modules itself.
Note: For detailed understanding of each line of the code please visit every section of the modules of the game and read the comments.











