> I have a project idea: transform an old analog (world war II era) radio to an internet connect radio hifi, keeping the nice haptic interfaces (button, sliders, etc)
What are the steps, tools and materials needed ? what are the difficulties and downfall ? 
could you provide links to similar project ?

This is a fantastic project. There is something deeply satisfying about bridging the gap between tactile, mid-century industrial design and modern high-fidelity streaming.

Since you are already comfortable with **Raspberry Pi** and **Python**, you have a significant head start. The challenge here isn't just the code; it’s the "mechanical-to-digital" translation.

---

## 🛠 Materials & Tools

### Hardware

*   **The Brain:** Raspberry Pi (A Model 3B+ or 4 is plenty; a Pi Zero 2W is great for tight spaces).
    
*   **Audio Output:** An **I2S DAC HAT** (like Hifiberry or Pimoroni) for true Hi-Fi sound, rather than the noisy onboard 3.5mm jack.
    
*   **The "Feel":** \* **Rotary Encoders:** To replace old potentiometers (volume/tuning) if the originals are too corroded or incompatible.
    
    *   **ADS1115 (ADC):** If you want to keep the *original* analog potentiometers, you’ll need this Analog-to-Digital converter to talk to the Pi.
        
*   **Power:** A 5V power supply for the Pi and potentially a separate supply for the amplifier to avoid ground loop noise.
    
*   **Speakers:** Modern full-range drivers (the original 1940s paper cones are likely brittle or "lo-fi").
    

### Software

*   **OS:** Raspberry Pi OS (Lite).
    
*   **Audio Engine:** **Mopidy** (Python-based, supports Spotify, SoundCloud, Local) or **Volumio**.
    
*   **Interface:** A custom Python script to map GPIO pins to your buttons/sliders.
    

---

## 🏗 The Step-by-Step Process

### 1\. Gutting and Cleaning (The "Archivist" Phase)

Remove the old chassis carefully. WWII-era radios often used heavy transformers and vacuum tubes.

> **⚠️ Safety Warning:** Old tube radios can contain large capacitors that hold a lethal charge long after being unplugged. Discharge them safely before touching.

### 2\. Mechanical Integration

This is the hardest part. You need to connect the original knobs to your electronics.

*   **Tuning Dial:** If it uses a string-and-pulley system, try to attach a rotary encoder to the main spindle so the needle still moves when you turn the knob.
    
*   **Buttons:** Old "clunky" toggle switches are usually easy to wire directly to the Pi's GPIO pins.
    

### 3\. Audio Path

Mount your new speakers. If the radio cabinet is wood, it will actually act as a great acoustic chamber. Line the inside with a bit of foam to reduce "boxiness."

### 4\. Software Mapping

Write a Python service to listen for GPIO interrupts. When you turn the "Tuning" knob, the script tells Mopidy to switch "stations" (which could be different Spotify playlists or internet radio streams).

---

## 🚧 Difficulties & Downfalls

*   **EMI/Static:** High-gain amplifiers inside a small box with a Wi-Fi-enabled Pi can pick up "beeping" interference. Use shielded cables for all audio runs.
    
*   **Logarithmic vs. Linear:** Original volume pots are often logarithmic. If you use an ADC to read them, the volume curve might feel "off" in a digital environment without some math in your Python script.
    
*   **The "Soul" vs. Utility:** It’s tempting to add a screen, but that often ruins the 1940s aesthetic. Consider using the original **Magic Eye** (tuning tube) if it’s still functional—some makers use an Arduino to drive the green glow based on volume levels.
    

---

## 🔗 Inspiration & Similar Projects

These projects range from "modern gut-job" to "high-end restoration":

1.  **[The Phono-Pi](https://www.google.com/search?q=https://www.instructables.com/Vintage-Radio-Raspberry-Pi-Internet-Radio/):** A classic Instructable that covers the basics of using a Pi with vintage hardware.
    
2.  **[Bob’s Vintage Radio (Volumio)](https://www.google.com/search?q=https://community.volumio.com/t/vintage-radio-restoration-project/10452):** A great look at how to integrate a modern Hi-Fi DAC into an old wooden housing.
    
3.  **[Pimoroni’s Pirate Radio:](https://www.google.com/search?q=https://learn.pimoroni.com/article/build-your-own-pi-zero-radio)** While a small kit, their software tutorials for internet radio are excellent for beginners.
    

https://www.youtube.com/watch?v=7NESVK89Rho



https://retrotechnique.org/


https://www.instructables.com/1970-Flirt-Pi-Internet-Radio/


## Modern Hardware

What are modern maker of great haptic buttons and selectors ?

Finding "great" haptics in 2026 often means looking beyond the standard plastic buttons found in budget electronics. For a WWII radio project, you likely want components that feel **intentional, heavy, and mechanical.**

Here are the modern makers currently leading the field in high-quality tactile interfaces:

### 1\. The "Gold Standard" for Mechanical Feel

If you want that satisfying "clunk" or a perfectly weighted rotation, these industrial-grade manufacturers are the go-to for high-end audio and aerospace:

*   **Elma Electronic:** Famous for their "Swissclick" technology. Their rotary switches and encoders are used in high-end studio gear. They feel incredibly precise and are rated for millions of cycles.
    
*   **Grayhill:** A favorite in the maker community for "overbuilt" components. Their **51 Series** rotary switches are legendary for having a distinct, crisp detent (the "click" between positions) that feels much more substantial than cheap alternatives.
    
*   **NKK Switches:** Known for their rugged, high-quality toggles and pushbuttons. If you need a heavy-duty toggle switch that feels like it belongs in a cockpit, NKK is the answer.
    

### 2\. High-Tech "Smart" Haptics

If you want to move beyond simple mechanical clicks into programmable resistance (e.g., making a knob feel like it has 5 positions for one app and 50 for another):

*   **XeelTech (HAPTICORE):** They produce "smart" rotary actuators. These use electromagnetic resistance to create virtual detents. You can program exactly how the knob "feels"—from smooth friction to heavy clicks—via software. https://www.xeeltech.com/hapticore/
    
*   **Titan Haptics:** They specialize in wide-frequency haptic motors (LMR architecture) that can simulate textures or complex vibrations through a solid surface or button.
    

### 3\. Boutique & Enthusiast Favorites

For projects where aesthetics and "finger-feel" are paramount:

*   **Burrows (and other Mechanical Keyboard brands):** Don't overlook high-end mechanical keyboard switches (like **Gateron Oil Kings** or **Gazzew U4T**). Makers often use these as individual "reset" or "function" buttons because the tactile "thock" is so well-engineered. https://www.gateron.co/
    
*   **LoveMySwitches:** A boutique distributor specifically for pedal builders and synth makers. They curate switches (like the **Alpha 1P12T**) specifically for their "heaviness" and durability. https://lovemyswitches.com/toggle-switches/
    

---

### Comparison Table: Which one for your Radio?

| **Interface Type** | **Best Maker** | **Why it fits a WWII Radio** |
| --- | --- | --- |
| **Main Tuning Knob** | **Elma** or **Grayhill** | Provides the heavy, "expensive" torque feeling of 1940s gear. |
| **Power/Toggle** | **NKK Switches** | Authentic "snap" that matches the era's industrial aesthetic. |
| **Volume/Sliders** | **Bourns** | Their "Pro Audio" line of potentiometers has a smooth, damped travel. |
| **Hidden Functions** | **Gateron (Tactile)** | Use a mechanical keyboard switch for a hidden "sync" button. |

### Pro-Tip for your Project:

Since you’re doing a "reconversion," look for **"High-Torque"** versions of encoders. Most standard encoders (like the common EC11) are very light and feel "plasticky." A high-torque Grayhill encoder will make the radio feel like a piece of professional laboratory equipment rather than a toy.


https://fr.rs-online.com/web/c/interrupteurs/commutateurs-rotatifs-et-accessoires/commutateurs-rotatifs/



# Hardware choice

You are right to worry about boot times. If you have to wait 30–45 seconds for a Linux kernel to initialize and connect to Wi-Fi every time you flip the physical switch, the "magic" of the analogue experience disappears.


### 1\. The "True Instant-On" Choice: ESP32 (Microcontroller)

If you want the radio to play music almost the moment you flip the switch (within 2–5 seconds), an **ESP32** is much better than a Raspberry Pi. It doesn't run a heavy OS; it just runs your code.

*   **How it works:** You use an ESP32 board paired with an **I2S DAC** (to get high-quality audio out) and a small **Class-D Amplifier** to drive the original radio speaker.
    
*   **Software:** Use the **Squeezelite-ESP32** firmware. It turns the ESP32 into a "Squeezebox" player.
    
*   **The Spotify/Deezer Link:** You would run a small server in your house (like a Docker container of **Logitech Media Server - LMS**) which handles the Spotify/Deezer API. The radio itself just acts as a lightweight receiver.
    
*   **Pros:** Extremely fast boot, very low power (you could run it on a battery for a long time), and no risk of SD card corruption if you just "pull the plug" to turn it off.
    

### 2\. The "Modern Smart" Choice: Raspberry Pi Zero 2 W

If you prefer a standalone solution where the radio handles everything itself without an external server, a Pi is the way to go, but you'll need to optimize it.

*   **Hardware:** Use a **Pi Zero 2 W** (small enough to fit in any vintage shell) + a **HiFiBerry DAC+ Zero** or a **Pimoroni Pirate Audio** board.
    
*   **Fast Boot Strategy:**
    
    *   **DietPi OS:** Use this instead of Raspberry Pi OS. It’s ultra-minimal.
        
    *   **Read-Only Mode:** Set the OS to "read-only" so you can cut the power safely without shutting down properly.
        
    *   **Optimization:** By disabling HDMI, Bluetooth, and unused services, you can get a Pi to boot and start a Spotify stream in about **15–20 seconds**.
        
*   **Software:** **Raspotify** (for Spotify Connect) or **pleezer** (an open-source headless Deezer player).
    

---

### Summary Comparison

| **Feature** | **ESP32 + LMS** | **Raspberry Pi Zero 2 W** |
| --- | --- | --- |
| **Boot Time** | 2–5 seconds | 15–30 seconds |
| **Setup Complexity** | High (Needs a separate server) | Medium (Standalone) |
| **Stability** | Rock solid (no OS to crash) | Good (if configured read-only) |
| **Audio Quality** | Excellent (via I2S DAC) | Excellent (via HAT DAC) |

### My Recommendation

Since you value the **physicality and "feeling"** of the radio, I would go the **ESP32** route. There is a specific hardware line called **"Esparagus"** (by Sonocotta) designed specifically for this—it's an ESP32 with the DAC and Amp already on one tiny board. It boots nearly instantly, and you can map the old radio's potentiometers (knobs) to the ESP32's pins to control volume and "tuning" (skipping tracks) physically.

👉 https://sonocotta.com/esparagus-hifi-medialink/




## Host Radio Transistor

https://www.leboncoin.fr/ad/collection/3079777179


# marque
- Sonolor
  - RANGER
  - Vogue
  - Vero54
- Reela
- Telefunken
- Optalix
  - TO99, TO100
  - TO305
- Radiola
- Philips
- Schneider