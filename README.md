# STM32 LED Control and Button Interaction Project

This project is a firmware application for STM32 microcontrollers that controls three LEDs (Green, Red, and Blue) and interacts with a button. The project is implemented using STM32Cube HAL and runs on an STM32 microcontroller. The firmware includes various LED patterns and a button-driven menu system to switch between modes. Additionally, it interfaces with peripherals such as GPIO, ADC, UART, and TIM.

## Table of Contents
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Usage](#usage)
- [LED Modes](#led-modes)
- [Peripheral Initialization](#peripheral-initialization)
- [Contributing](#contributing)

## Features

- **LED Control**: Green, Red, and Blue LEDs with various patterns (blinking, wave, opposite wave, etc.).
- **Button Interaction**: Use a button to switch between different LED modes.
- **Random Number Generation**: Implement a simple game using a random number generator.
- **Peripheral Integration**: Interfaces with ADC, UART, RTC, TIM, and GPIO.
- **Debouncing**: Includes logic to debounce the button input.

## Hardware Requirements

- STM32 microcontroller (tested on STM32 series with STM32Cube HAL).
- Three LEDs connected to specific GPIO pins:
  - **Green LED**: GPIOC Pin 7
  - **Red LED**: GPIOA Pin 9
  - **Blue LED**: GPIOB Pin 7
- A button connected to GPIOB Pin 0.

## Usage

Upon powering on the microcontroller, the program starts by blinking the Green LED three times. After initialization, the button on GPIOB Pin 0 can be used to cycle through different LED modes. The following operations are available:

- **Blinker**: Blinks all LEDs together.
- **Wave**: LEDs turn on one after the other from Green to Blue to Red.
- **Opposite Wave**: LEDs turn on in reverse order from Red to Blue to Green.
- **Light**: All LEDs stay on.
- **Winker**: Two LEDs blink alternately.
- **Sea Split**: Middle LED (Blue) turns on, followed by the outer LEDs (Green and Red).
- **Idle**: All LEDs are off.
- **Game**: A simple game where the user has to press the button when the correct LED is lit.

## LED Modes

- **Blinker**: All LEDs blink together at regular intervals.
- **Wave**: LEDs light up sequentially in a wave-like pattern.
- **Opposite Wave**: LEDs light up in reverse wave order.
- **Light**: All LEDs stay on constantly.
- **Winker**: Alternating LED blinking pattern.
- **Sea Split**: Center LED lights up first, followed by the outer LEDs.
- **Game**: Randomly light up LEDs, and the user has to press the button when the correct LED is on.

## Peripheral Initialization

- **GPIO**: Initializes the GPIO pins for LED control and button input.
- **ADC**: Configures the ADC for any analog input reading (not directly used in this implementation).
- **UART**: Sets up UART communication, which can be used for debugging or external communication.
- **RTC**: Initializes the Real-Time Clock for any time-related operations.
- **TIM**: Configures the timer for LED timing and delays.
- **ICACHE**: Enables instruction cache for improved performance.
- **USB**: Configures the USB peripheral for future use cases.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch with a descriptive name.
3. Commit your changes and submit a pull request.


