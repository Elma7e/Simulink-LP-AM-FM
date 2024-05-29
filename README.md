# Simulink Lowpass filter and AM & FM Modeluation & Demodulation!

This repository contains MATLAB and Simulink files for labs focusing on analog filter design, amplitude modulation (AM), and frequency modulation (FM). These labs are designed to help understand the principles of signal processing and modulation techniques used in communication systems.

## Table of Contents

- [Lab 1: Low Pass Filter Design](#lab-1-low-pass-filter-design)
- [Lab 2: Amplitude Modulation](#lab-2-amplitude-modulation)
- [Lab 3: Frequency Modulation](#lab-3-frequency-modulation)
- [Setup and Prerequisites](#setup-and-prerequisites)
- [Usage](#usage)
- [Results](#results)

## Lab 1: Low Pass Filter Design

### Objective
- To understand the design of analog filters.
- To analyze the filter frequency response.
- To understand the role of filters in limiting out-of-band Gaussian noise.

### Procedures
1. **Filter Specifications:**
   - Passband frequency \( f_p = 2 \) Hz
   - Stopband frequency \( f_s = 5 \) Hz
   - Maximum passband ripple \( R_p = 1 \) dB
   - Minimum stopband attenuation \( R_s = 60 \) dB
   - Sampling frequency = 100 Hz

2. **Steps:**
   - Generate a sine wave (message signal) with a frequency of 0.1 Hz, sample time of 0.01 sec, and 5 volts peak using Simulink.
   - Change the frequency of the sine wave and record the amplitude of the output.
   - Sketch the frequency response of the designed filter.
   - Use an out-of-band Gaussian Random source block to generate noise.
   - Combine the message signal (frequency of 1 Hz) and the random noise using an Add block.
   - Display and draw the signals showing axes values and amplitudes.
   - Change the frequency of the message signal upwards and downwards, and comment on the effect.

## Lab 2: Amplitude Modulation

### Objective
- To understand the modulation process and utilize AM to modulate the amplitude of a carrier signal.
- To investigate the effect of multiplying the carrier by the modulating signal and observe the resulting sidebands.

### Procedures

**Task 1: AM Modulation**

**Section 1:**
1. Generate a carrier sine wave signal with a frequency of 20 kHz, sample time of 0.02 sec, and 1V peak.
2. Generate a baseband sine wave signal of frequency 1 kHz, sample time of 0.02 sec, and amplitude of 1V peak.
3. Use a multiplier to obtain the amplitude-modulated signal.
4. Display both inputs and the resulting amplitude-modulated signal on oscilloscopes.
5. Draw the three signals showing axes values and amplitudes.
6. Change the amplitude of the modulating signal upwards and downwards while fixing the amplitude of the carrier, and draw the three signals.
7. Change the amplitude of the carrier while fixing the amplitude of the signal.
8. Display the spectrum of the DSB-SC signal.
9. Comment on the effect of changing the modulation index on the resulting modulated signal.

**Section 2:**
1. Implement the AM (DSB-WC) modulation technique.
2. Change the modulation index from 0.2 to 1 in steps of 0.2, and draw the three signals.
3. Display the spectrum of the AM signal.
4. Compare the results between DSB-SC and DSB-WC modulation techniques.

## Lab 3: Frequency Modulation

### Objective
- To understand the modulation process and utilize FM to modulate the carrier signal.
- To understand the FM demodulation process using a frequency discriminator.

### Procedures

**Task 1: FM Modulation**
1. Generate a sine wave (message signal) with a frequency of 100 Hz, sample time of 0.01 sec, and 2 volts peak using Simulink.
2. Process the message signal using an Integrator block.
3. Use a Gain block to multiply the Integrator output by \( K_f = 10 \) Hz/V.
4. Use a Ramp and constant block ( \( f_c = 25 \) Hz) to produce the term \( f_c t \).
5. Combine the outputs of the Gain block and the Ramp block using an Add block.
6. Apply the combined signal to a Cosine function block to produce the FM signal.
7. Display both inputs and the resulting FM signal on oscilloscopes and spectrum analyzers.
8. Draw the two signals showing axes values and amplitudes.
9. Change the amplitude of the modulating signal and draw the two signals for different frequencies.
10. Repeat the step above by changing the frequency deviation constant.
11. Comment on the effect of changing the signal amplitude and the frequency deviation index on the resulting modulated signal.

**Task 2: FM Demodulation**
1. Implement the FM demodulator model using a frequency discriminator.
2. Modify the filter and the VCO parameters as specified.
3. Change the amplitude of the modulating signal and draw the original and demodulated signals for different frequencies.

## Setup and Prerequisites

- MATLAB and Simulink installed.
- Addons: Signal Processing Toolbox, 
- Basic familiarity with Simulink and MATLAB environment.

## Usage

1. Clone this repository:
   ```sh
   git clone https://github.com/elma7e/Simulink-LP-AM-FM.git
   
## Results
Checkout the report done on these labs [here](./Analog%20Communications%20Report%20%5B210237%5D.pdf)
