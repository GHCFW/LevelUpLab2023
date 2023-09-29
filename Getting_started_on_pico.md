# Flashing MicroPython Firmware on Raspberry Pi Pico

Installing MicroPython involves flashing the MicroPython firmware onto your Raspberry Pi Pico board.
## What is Flashing?

Flashing, in the context of microcontrollers and development boards, is the process of writing a new firmware or software onto the internal storage of the device. It's akin to installing a new operating system on a computer, in that, when you flash a microcontroller like the Raspberry Pi Pico, you are essentially overwriting its existing software with a fresh one.

## Why is Flashing Needed?

Flashing is necessary when you first acquire a Raspberry Pi Pico or if you want to change the programming language or environment on the board. In the case of MicroPython, it involves replacing the existing firmware or software with the MicroPython firmware, which includes the MicroPython interpreter.
Here's what installing MicroPython accomplishes:

- **Flashing the MicroPython Firmware**: Flashing MicroPython firmware, which includes the MicroPython interpreter and essential libraries, onto the Raspberry Pi Pico. This firmware enables your Pico to understand and execute Python code.

- **Preparing for Python Development**: By flashing MicroPython, you prepare your Raspberry Pi Pico for Python development. It allows you to write and run Python code directly on the board, making it a versatile and accessible platform for various projects.

- **Interacting with External Hardware**: With MicroPython installed, your Pico can interface with external hardware components, sensors, and peripherals using Python. This makes it ideal for IoT (Internet of Things) and embedded systems projects.

## Prerequisites

To get started, you'll need the following:

- Raspberry Pi Pico board
- Micro-USB cable
- Thonny IDE installed on your computer

## Step 1: Prepare Your Hardware

1. Locate the BOOTSEL button on your Raspberry Pi Pico board.

![BOOTSEL Button](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/BOOTSEL.jpg)

2. Press and hold the BOOTSEL button while connecting the other end of the micro-USB cable to your computer. This action puts your board into USB mass storage device mode, and it should appear as "RP1-RP2."

   ![RP1-RP2](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/RP1_RP2.jpg)

   Note: If you don't see the device show up, disconnect the board, hold down the BOOTSEL button, and then connect it to the computer while continuing to hold the button.

## Step 2: Configure Thonny IDE

This step configures Thonny to recognize the Raspberry Pi Pico board.

1. Open the Thonny IDE on your computer.

2. Click on the three horizontal lines icon in the bottom right corner of the Thonny IDE.

   ![Configure Interpreter](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_Configure_Interpreter.png)

3. Select "Configure Interpreter."

4. In the dialog that appears, choose "MicroPython for Raspberry Pi Pico" as the interpreter. Keep the remaining options as default.

   ![MicroPython Configuration](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Thonny_MicroPython.jpg)

   Note: You may see this option only when the board is connected to your computer. We connected the board in the previous step.

## Step 3: Install MicroPython Firmware

1. In Thonny, select "Install MicroPython" from the three horizontal lines icon.

   ![Install MicroPython](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Install_MicroPython.jpg)

2. Make sure to select the following options:
   - Target volume: RP1-RP2 (D:) (The drive name may be different for you)
   - MicroPython Family: RP2
   - Variant: Raspberry Pi Pico/Pico H
   - Version: 1.20.0 (or the version you prefer)

   ![MicroPython Installation Details](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/Install_MicroPython_Details.jpg)

3. Click "Install." Thonny will download and install the MicroPython firmware on your Raspberry Pi Pico board.

4. Once it's done, you should see "Done!" in the bottom-left window.

   ![Installation Done](https://github.com/GHCFW/WorkshopExercise23/blob/main/images/MicroPython_Install_Done.jpg)

Congratulations! You've successfully flashed MicroPython firmware onto your Raspberry Pi Pico board. You can now start writing and running MicroPython code on your Pico board.
