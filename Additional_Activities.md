# Additional Activities for the Workshop

If you find yourself with extra time during the workshop or are curious to delve deeper into the content, here are some additional activities you can explore.

## Additional Activity 1: Explore the PlaySong Library and program more songs on the buzzer

In this activity, you can explore the PlaySong library provided to you and gain a better understanding of how the buzeer is programmed. You can then create and add more songs to your project using the PlaySong library.

**Steps:**
1. Dive into the playsong.py documentation to understand how the buzzer is programmed using PWM.
3. Utilize the `tones.py` library in combination with `playsong.py` to compose and add new songs to songs.py.



## Additional Activity 2: Add a Timeout to the reaction game

In this activity, you will enhance the reaction game code provided to include a timeout feature for each round.

The goal of this exercise is to modify the existing code for the reaction game to include a timeout for each round. 
You will add a timeout mechanism to each round, where if neither player presses a button within a certain time frame, the round ends, and the game announces a timeout.

Follow these steps to complete the exercise:

**Step 1: Configure the Timeout Timer**
In this step, you will configure a timer to handle timeouts for each round. The timer will trigger a timeout event if neither player presses a button within a specified time frame.

In the `play_round(game_iteration, left_button, right_button)` function configure the timeout timer. Use the `Timer` module to set up the timer.

<code>
timeout_timer = Timer(period=1000, mode=Timer.ONE_SHOT, callback=timeout_callback)
</code>

This code creates a timer that triggers a `timeout_callback` function after 1000 milliseconds (1 second) in one-shot mode. The `timeout_callback` function will handle the timeout event.

**Step 2: Implement the Timeout Callback**
In this step, you will implement the `timeout_callback` function, which will be called when the timeout timer expires. This function will end the current round and announce a timeout.

Add the `timeout_callback` function. This function sets a global flag `timeout_triggered` to `True` when called.

<code>
def timeout_callback(timer):
    global timeout_triggered
    timeout_triggered = True
</code>


**Step 3: Handle Timeout in the Game Round Logic**
Now that you have configured the timer and implemented the timeout callback, you need to modify the game logic to handle timeouts.

Within the while loop inside the `play_round` function, add a condition to check if the `timeout_triggered` flag is set to `True`. If it is, print a message indicating a timeout and break out of the loop.

<code>
while True:
    global fastest_button, player2_wins, player1_wins, timeout_triggered
    
    if timeout_triggered:
        print('Game iteration #' + str(game_iteration + 1) + ' resulted in a timeout')
        break
    # ... (existing code)
</code>

**Step 4: Clear `timeout_triggered` Before Each Round**
Before each round, it's important to clear the `timeout_triggered` variable to ensure that the timeout state from the previous round does not carry over.

In the game loop before calling `play_round()`, add code to set the `timeout_triggered` flag to `False`. This should be done at the beginning of each round.

<code>
timeout_triggered = False
play_round(game_iteration, left_button, right_button)
</code>



