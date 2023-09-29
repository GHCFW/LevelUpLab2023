# The Power of Firmware: Bringing Your Hardware to Life

## Workshop Overview
Welcome to the GHC 2023 "The Power of Firmware" level-up lab! In this 1-hour session, you will learn key firmware development concepts. You will have the opportunity to practice these concepts using an online simulator called Wokwi as well as real hardware, the Raspberry Pi Pico board.

## Prerequisites
To participate in this level-up lab, please make sure to bring your laptop and have Thonny, Python IDE, installed on it. The installation should only take a couple of minutes. Below, you'll find detailed installation instructions for Thonny:

[Prerequisites Guide](https://github.com/GHCFW/LevelUpLab2023/blob/main/Prerequisites.md)

Any prior knowledge of programming languages or firmware is not necessary to participate in this workshop.

## Workshop Activities

### **Activity 1. Play the reaction game on Raspberry Pi Pico board <br>**
   **Goal of the game**<br>
   This is a game of quick reflexes! <br>
    &nbsp; &nbsp; * It is a 2-player game, create groups of 2 on your table. <br>
    &nbsp; &nbsp; * The game consists of three rounds where the on-board LED turns on and off as the stimulus. <br>
    &nbsp; &nbsp; * The first player to press their button as soon as the LED goes off wins a point. <br>
    &nbsp; &nbsp; * The player with the most points at the end of three rounds wins the game. <br>
    &nbsp; &nbsp; * The LED has been configured to stay on for an arbitary amount of time. Button presses while the LED is still on will be ignored. <br>

   We have setup the Pico board along with 2 switches for you. The firmware has been flashed on the board. All you need to do for this step is: <br>
     &nbsp; &nbsp; a. Connect the board to your computer <br>
     &nbsp; &nbsp; b. Open Thonny IDE <br>
     &nbsp; &nbsp; c. Connect the board to run with Thonny (check the link below for step by step instructions) <br>
     &nbsp; &nbsp; d. Open and run the code saved on Pico <br>
     &nbsp; &nbsp; e. Play the game!! <br>
     &nbsp; &nbsp; f. Ensure everyone on the table gets a chance to play the game once!! <br>

   Visit [Activity 1](https://github.com/GHCFW/LevelUpLab2023/blob/main/Activity_1.md) for detailed instructions
   
### **Activity 2. Update the reaction game to play victory music on the simulator <br>**
   We will start with this exercise on the simulator (Wokwi) before trying the code on the board. <br>
   **Goal** <br>
   You have been provided with a song library with song options: 'player1_victory_song', 'player2_victory_song'. <br>
   Update the existing code to play the corresponding victory tone when a player wins the round. <br>

   Visit [Activity 2](https://github.com/GHCFW/LevelUpLab2023/blob/main/Activity_2.md) for detailed instructions

### **Activity 3. Play the reaction game with the buzzer on the Pico board <br>**
   **Goal** <br>
   The goal of this exercise is to play the same victory music on the board!

   a. Connect the buzzer to the board (check the link below for instructions) <br>
   b. Open and run the code saved on Pico <br>
   c. Play the game! <br>

   Visit [Activity 3](https://github.com/GHCFW/LevelUpLab2023/blob/main/Activity_3.md) for detailed instructions


## Resources

* You bought a new Pico board. What next? See how to flash micorpython and setup the new board [here](https://github.com/GHCFW/LevelUpLab2023/blob/main/Getting_started_on_pico.md).
* If you want to explore more, checkout the additional activities listed [here](https://github.com/GHCFW/LevelUpLab2023/blob/main/Additional_Activities.md)


