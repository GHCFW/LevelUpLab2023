## Activity 1: Play the reaction game on the Pico board

   **Goal of the game**<br>
    This is a game of quick reflexes! <br>
    * It is a 2-player game, create groups of 2 on your table. <br>
    * The game consists of three rounds where the on-board LED turns on and off as the stimulus. <br>
    * The first player to press their button as soon as the LED goes off wins a point. <br>
    * The player with the most points at the end of three rounds wins the game. <br>
    * The LED has been configured to stay on for an arbitary amount of time. Button presses while the LED is still on will be ignored. <br> <br>
      A key objective of this exercise is to ensure that every group has a system that is set up for the subsequent exercises and can connect to the Raspberry Pi Pico board. 


   We have setup the Pico board along with 2 switches for you. The micropython firmware as well as the game firmware has been flashed on the board.
   
   ### Step 1. Verify bread-board setup <br> <br>
  Check the picture below to verify your bread-board setup matches the below expectations. These connections are already done for you. If you have moved the components on your board, look at the picture below to connect them back. <br>

  ![Exercise 1: Board Setup](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Exercise_1_Board_Setup.jpeg)

  The button we are using has 2 pins, one end of which is connected to Pico's GPIO pin and the other end is connected to a 3V rail. <br>
      - Player 1 (blue button) button connections: GPIO Pin 15, which is connected to the bread-board via #20 <br>
      - Player 2 (white button) button connections: GPIO Pin 16, which is connected to the bread-board via #40 <br>

  Pico's 3V is GPIO Pin 36, which is connected to the bread-board via #5 to the bread-board's +rails.<br>
  It does not matter which + rail pin on the bread-board you connect to as long as the + rails on both sides of the bread-board are connected.

  Reference <br>
      [Raspberry Pi Pico pinout diagram](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf?_gl=1*1ish86u*_ga*MTc0NDY1MTcyMC4xNjk0MDQ3NTcw*_ga_22FD70LWDS*MTY5NDA1MTUwNC4yLjAuMTY5NDA1MTUwNS4wLjAuMA..)


 ### Step 2. Connect the board to your computer <br> <br>
  Use the USB cable to connect the board to your computer. <br>
  The host computer supplies power to the board, but it also provides a mechanism to run the firmware.

 ###  Step 3. Open Thonny & connect the board to run with Thonny <br> <br>
  3a. By default Thonny will open a Python shell, such as the one shown in the picture below.
     
  ![Thonny Home](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Home.jpg)
 
  3b. We want to switch the shell to run with MicroPython instead of Python. Locate the three horizontal lines icon in the bottom right window of Thonny. Click and select "MicroPython (Raspberry Pi Pico) @ [drive that the board is mounted on]."

  - Example: "MicroPython (Raspberry Pi Pico) Board CDC @ COM3" (OR) "MicroPython (Raspberry Pi Pico) Board in FS Mode @ /dev/..."
  - This shows that the board is connected to a specific port (e.g., COM3), but the port number may vary depending on your computer.

    ![Pico COM Port on Windows](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_COM.jpg)

  3c. Verify that the shell has been updated to the MicroPython version you selected, and it shows "Raspberry Pi Pico with RP2020." <br> <br>
      ![RP2040 Shell](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/rp2040_shell.jpg) <br>
  
  You are all set to run MicroPython code on your board!
  
 ### Step 4. Open the code uploaded on Thonny <br>
  Before we can play the game, open the files that are already uploaded on Thonny so that we can run that firmware. To do this, go to File -> Open ... -> Raspberry Pi Pico -> main.py

  ![Open File](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Open_File_On_Thonny.png)

  If you didn't see Raspberry Pi Pico as an option to open the file from:
     - Your board is not recognized by Thonny. Go back to steps 2 & 3 and ensure that those were successful by verifying you were able to switch the shell to MicroPython v1.20.0; Raspberry Pi Pico with RP2040
     - See our [troubleshooting guide]((https://github.com/GHCFW/WorkshopExercise23/blob/main/Troubleshooting.md) if you still can't get it to work. 

 ### Step 5. Play the game!! <br>
  Once you have the firmware code up, click anywhere on main.py and let's start the game!

  Click on the run button (or press F5) as highlighted in purple below. You should see the shell update with some game messages and the game is on!!

  ![Start the Game](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Exercise_1_Hit_Play.png)

  At the end of the game, the shell should reflect the player who won!!

  ![End Game](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Winning_Shell.png)
     

