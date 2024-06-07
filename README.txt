# Harjoitustyö2_Peliohjelmointi

This project was made using Unreal Engine version 5.3.2 and Microsoft Visual Studio 2022.

This was a simple twin-stick shooter designed for controller, made on Unreal Engine.
This was also my first 3D game, and my first Unreal Engine game!

Download:
Simply launch the TwinStickShooter.exe from the windows folder to run the game!
Keep in mind the game is packaged in Developer mode!

The Gameplay:
Try and survive as long as possible while gaining score from defeated enemies.

Controls:
WASD / Left Joystick = Move
ARROW KEYS / Right Joystick = Turn and Shoot

Documentation:

I tried to first make the project on UE 4.8, but it was too outdated and required Visual Studio 2017, which can no longer be used.
Upon importing the project into UE 5.3.2, I ran into a lot of trouble with Visual Studio. I spent the first 8 hours of the project trying to fix the issues and get the editor working as intended.
The main issue was that I couldn't do any C++ scripting as it couldn't find Visual Studio or make the class in the content drawer. I had to manually rebuild the project, which ultimately didn't fix the issue either.
I then decided to restart the entire thing, but ran into the same problem. I got the issue fixed by trying to rebuild and save the source myslef, then changing the Visual Studio version inside the editor, and finally remaking everything again.

This was my first time using Unreal Engine so it took quite a while to get used to it, but i was slowly following the tutorials. It was also pretty challenging at times to figure out how to do the same things in a newer version.
Some of the blueprints and actors had to be made slightly differently as it didn't work lik eit did in the tutorials, so it took a bit of time getting used to making things in new ways.

Another weird issue popped up at the middle of developement, that I couldn't fix even at packaging. The bool for isDead was for some reason inverted, so false = true and vice versa.
I checked the code and everything multiple times, but all was as intended on those. The default variable was for some reason locked to true, and when the player or enemies health went to 0, it would go to false, so I just worked with it inverted for the time being.
Thoough even after researching and attempting to fix it I never found a solution, and it wasn't a big enough problem for me to restart everything again.
But after packaging the game it turns out that the isDead works as intended on the .exe, but even after i changed the isDead variables to true, the death animation would always be playing.
I spent nearly 4 hours of work trying to fix the isDead bool so that the characters weren't always just dead whether I attached the Dead animation to false or true.
Finally the way I fixed it was instead of using the original isDead variable, I made a new variable that was DeadTrue since Dead and isDead were taken, which became true from Health <= 0.
I then attached this to the Dead animation transition and after packaging the game it worked as intended!

I wanted to add some unique aspects to the game like 2 levels to choose from and maybe some different types of enemies (faster but weaker, slower but stronger jne), but I had so many different issues and problems I didn't have much time to add those. 
Another thing i was going to add based on the tutorial 23 was sound, but I finished the project on the 25th, and i was really tired + I had to finish another project by monday for a course redo, so I decided to skip taht part.

I did learn a lot though and the blueprint system in UE can clearly be used to make a game without any C++ coding by the developer, so over the summer I want to try and make a new project in UE.
The animating also seems easier then in Unity as you can just put the different animations in and the character will smoothly transform from one animation to another.

A little secret here, the original plan was to change the projectile and the characters, to make the game be about a business boss shooting all the workers asking for promotions, not sure where I got the idea from.

Overall if I'm honest I enjoyed and also really hated making this project on Unreal because of all the issues, but I did learn a lot for the future projects I'll be making on UE.