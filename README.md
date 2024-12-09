# Luna
Smarter Speaker

## Key Components

### Main Speaker

[RS125-8 5" Reference Woofer 8 Ohm](https://www.daytonaudio.com/product/94/rs125-8-5-reference-woofer-8-ohm)

This will handle the mids and lows and will be pointed down

![image](https://github.com/user-attachments/assets/310139f0-7841-4700-b8d6-538fee050841)

### Second Speaker

[ND16FA-6 5/8" Neodymium Dome Tweeter 6 Ohm](https://www.daytonaudio.com/product/59/nd16fa-6-5-8-neodymium-dome-tweeter-6-ohm)

This will habndle the highs and will be pointed up

![image](https://github.com/user-attachments/assets/1b7edbc5-ed0f-40df-8333-f6af3881b001)

### Combined Amplifier and DAC

[HiFiBerry Amp 2](https://www.hifiberry.com/shop/boards/dealing-with-blocked-p5-holes-11/)

The Raspberry Pi’s built-in audio can be noisy. A DAC provides much cleaner sound quality.  
Mount it onto the Raspberry Pi and you have a stereo audio system. You only have to connect your loudspeakers. It provides up to 60W power. You only need a single 12V power supply to power the Raspberry Pi and the Amp2. 
It powers the Raspberry Pi, there is no need to add an external 5V power supply to the Raspberry Pi.

![image](https://github.com/user-attachments/assets/d0f9adcb-950a-481a-a303-9c64ab022656)

### Power Supply

A 12V–24V DC power supply for the amplifier (check the amp’s specs).
Step-down converter from the amplifier's supply

### Crossover 

[Dayton Audio XO2W-2.5K 2-Way Crossover 2,500 Hz](https://www.daytonaudio.com/product/593/xo2w-2-5k-2-way-crossover-2-500-hz)

A crossover is an electronic component used in speaker systems to divide the audio signal into separate frequency ranges and send them to the appropriate speaker drivers.

![image](https://github.com/user-attachments/assets/8d0fd1c9-359e-4a70-af0b-32685f81da93)


### Lighting

[DC24V/12V High Density COB Color Chasing Lights Addressable RGB LED Strip](https://www.superlightingled.com/dc24v12v-high-density-cob-color-chasing-lights-addressable-rgb-led-strip-p-4940.html)

Single lighting circle around the speaker - will need configuration somehow/where

## Signal Flow Diagram

1. Raspberry Pi
   - Outputs the digital audio signal.  
2. HiFiBerry DAC+Amp (Amp2)
   - Converts the digital signal to analog (DAC functionality).
   - Amplifies the analog signal for the speakers.  
3. Crossover
   - Input: Receives the full-range amplified audio signal from the Amp2.
   - Outputs:
      - Sends low and mid frequencies to the woofer.
      - Sends high frequencies to the tweeter.  
4. Speakers
   - Woofer: Plays the low and mid-range sounds.
   - Tweeter: Plays the high-frequency sounds.



## Setup

Install PulseAudio or ALSA on the Raspberry Pi for audio management.
Use software EQ (equalizer) to tune the sound based on your setup.
Microphone Integration

The ReSpeaker 2-mic array uses I2S input for audio capture and wake-word detection.
It won’t interfere with the speaker output but will need proper placement to avoid feedback (e.g., place it away from the woofer or inside an acoustic shield).
