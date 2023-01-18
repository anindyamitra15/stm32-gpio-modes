# GPIO Modes/Functions on STM32F103

## Introduction
Experimenting with the plethora of GPIO modes and functionalities which are available on STM32F103C8T6.

## Contents
```
|_ adc_cpu_poll
|_ digital_input
|_ pin_interrupts
```
1. [ADC Poll for Conversion Mode](./adc_cpu_poll/): In this project, a GPIO is used as analog input to the ADC. `HAL_ADC_PollForConversion` is used to obtain the ADC reading. Here the CPU waits for the sampling and conversion process inside the microcontroller ADC unit. This is the simplest implementation useful for infrequent ADC readings. 

<br/>
<figure>
<img src="./adc_cpu_poll/Results/output.png" width="350" alt="Demo"/>
<figcaption>Output is shown on Arduino's Serial Plotter via UART1 of STM32 through FTDI breakout</figcaption>
</figure>
<br/>
<br/>

2. [GPIO as Digital Input](./digital_input/): This is a very basic functionality of GPIO, digital input.

<br/>
<figure>
<img src="./digital_input/Results/output.png" width="350" alt="Demo"/>
<figcaption>PuTTY serial shows the logic at the GPIO input</figcaption>
</figure>
<br/>
<br/>

3. [External Interrupt through GPIO](./pin_interrupts/): A falling edge interrupt was configured, which when triggered, toggles a boolean flag, which enables or disables the blinking of an LED on another GPIO.

<br/>
<figure>
<img src="./pin_interrupts/Results/output_gif.gif" height="350" alt="Demo"/>
<figcaption>Working shown in GIF</figcaption>
</figure>
<br/>

<hr>

# Other experiments:

Also checkout my other works with STM32F1: [STM32F103 RTOS](https://github.com/anindyamitra15/stm32-rtos), [STM32F103 UART](https://github.com/anindyamitra15/stm32-uart) and, [STM32F1 PWM Modes](https://github.com/anindyamitra15/stm32-pwm)
