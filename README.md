# Luna
Smarter Speaker

Key Components
Amplifier Board

Recommended: TPA3116D2  amplifier modules (up to 50W/channel) are affordable and provide clean sound.
Why: The Dayton RS125-8 is an 8-ohm speaker that requires proper amplification to drive it at decent volume and clarity.
Connection: Use the Raspberry Pi’s 3.5mm audio output or a USB DAC to feed the amplifier.
Digital-to-Analog Converter (DAC)
https://www.amazon.ca/TPA3116D2-Class-Stereo-5V-24V-Digital/dp/B08NFCCGC2
![image](https://github.com/user-attachments/assets/8be45fbc-d058-405f-9f53-500b237ac233)


Recommended: HiFiBerry DAC+ for Raspberry Pi.
Why: The Raspberry Pi’s built-in audio can be noisy. A DAC provides much cleaner sound quality.
Connection: Mount it on the Raspberry Pi’s GPIO header or use a USB DAC.
Enclosure Design
https://www.amazon.ca/HiFiBerry-DAC-Light-Raspberry-Pi/dp/B017L75824
![image](https://github.com/user-attachments/assets/793efac4-ba48-4084-a1f1-47a01b9fd177)


Sealed Box (recommended for simplicity):
Volume: ~3–4 liters (internal space) for good bass response.
Material: MDF or 3D-printed plastic with proper bracing.
Ported Box:
Requires precise tuning and design to match the speaker’s Thiele-Small parameters.
Use software like WinISD to calculate dimensions for optimal bass performance.
Power Supply

A 12V–24V DC power supply for the amplifier (check the amp’s specs).
A separate 5V supply for the Raspberry Pi (or a step-down converter from the amplifier's supply).
Crossover (Optional)

If you're adding a tweeter for better high-frequency sound, use a passive crossover (e.g., 2.5 kHz at 2nd-order) to split the audio signal between the woofer and tweeter.
Audio Configuration



Install PulseAudio or ALSA on the Raspberry Pi for audio management.
Use software EQ (equalizer) to tune the sound based on your setup.
Microphone Integration

The ReSpeaker 2-mic array uses I2S input for audio capture and wake-word detection.
It won’t interfere with the speaker output but will need proper placement to avoid feedback (e.g., place it away from the woofer or inside an acoustic shield).
