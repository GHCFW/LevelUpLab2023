## Activity 2: Run the game on a simulator and play the victory song

To get started, let's understand the existing code for the reaction game and make the necessary modifications to add some music! We will utilize an online simulator, Wokwi to develop and verify the code.

Click on the following link to open your project in the Wokwi simulator: [Wokwi Simulator - Exercise 2]( https://wokwi.com/projects/377160264606827521).

Once the simulator is open, you can explore the code files:

- `main.py`: The main script for the game, which includes code for button handling and determining the winner. This is what we used in Exercise 1. 
- `playsong.py`: Contains functions for playing songs and sound effects.
- 'songs.py`: A list of different songs options to choose from for the victory music.
- `tones.py`: A dictionary of musical note frequencies that we'll use for playing the buzzer.

In the schematics, we have already connected the buttons as well as the buzzer to the Pico.

### Step 1: Configure the Buzzer
Raspberry Pi Pico has a PWM module that we can utilize to play different sounds by changing the duty cycle, frequency and the duration each note plays for. We will use an external buzzer to play musical notes. 

We first need to initialize the PWM object for the buzzer.

**EXERCISE 2.1:**
In the `playsong.py` file, replace the comment that says `# Exercise 2.1: Instantiate a buzzer object, which is a PWM-type GPIO pin` with code to initialize the GPIO pin that the buzzer is connected to in GPIO out mode. In other words, what should `buzzer_pin` be set to? 

```python
###################################################################
# Exercise 2.1: Instatiate a buzzer_pin object, which is a GPIO pin
# We want this pin to be an output pin
# buzzer_pin = Pin(<pin_number>, <pin_direction>)
###################################################################
BUZZER_GPIO_PIN_NUMBER = 14
buzzer_pin = Pin(BUZZER_GPIO_PIN_NUMBER, Pin.OUT)
buzzer = PWM(buzzer_pin)
```

We are connecting the buzzer to Pico's GPIO Pin #14 and defining it as a PWM pin.

## Step 2: Adding Sound Effects

Now, let's add sound effects to announce the winner. In the `main.py` file, you will find a section where the winner is determined. Your task is to add function calls to play sound effects for the players.

Here's what you need to do:

**EXERCISE 2.2:**
- When **player 1** wins, add a function call to `playsong()` with whichever song you choose to play for player 1 victory from the options provided in song.py.
  
``` python
        if fastest_button is left_button:
            print('Game interation #' + str(game_iteration + 1) + ', player 1 won')
            ###################################################################
            # Exercise 2.2 Call the playsong API with your choice of song
            # from the songs library for player1 victory song
            ###################################################################
            playsong(victory_song_option_1)
            player1_wins += 1
            fastest_button = None
            break
```

- When **player 2** wins, add a function call to `playsong()` for player 2 vicotry song.

``` python
        elif fastest_button is right_button:
            print('Game interation #'+ str(game_iteration + 1) + ', player 2 won')
            ###################################################################
            # Exercise 2.2 Call the playsong API with your choice of song
            # from the songs library for player2 victory song
            ###################################################################
            playsong(victory_song_option_2)
            player2_wins += 1
            fastest_button = None
            break
```


## Step 3: Testing on Wokwi

Before porting your code to the Raspberry Pi Pico, it's a good practice to test it quickly on the Wokwi simulator. This allows you to verify that your code is functioning as expected without the need for physical hardware.

To do this, make sure you have made the changes mentioned above in Steps 1 and 2 and test your game in the simulator to ensure that the sound effects work correctly.

## Answer Key

[Exercise 2 Wokwi Answer Key](https://wokwi.com/projects/377161844132496385)
