---
marp: true
theme: default
paginate: true
---

# CS Hardware - Day 3

## Time

<!-- ### Capacitors, Delay, Oscillation -->

<!-- ![bg contain right](assets/capacitor-closeup.jpg) -->

---

# Goal For Today

By the end of today you will:

- Understand what capacitors do
- Learn how capacitors interact with time
- Build an LED delay and fade timer using an RC circuit
- Explore charging and discharging curves
- Build an astable multivibrator oscillator
- Connect timing circuits to real computer hardware

<!-- ![bg contain right](assets/capacitor-bank.jpg) -->

---

# Review From Day 2

Yesterday we learned:

- Transistors act like switches
- Small signals can control larger signals
- Logic gates are built from transistors
- Computers use binary ON/OFF states
- Billions of transistors power modern CPUs

---

# Review From Day 1

We also learned:

- Voltage pushes current
- Resistance limits current
- LEDs have polarity
- Ohm's Law: **V = I × R**
- Multimeters help us debug circuits

---

# Today

Today we add a new idea: **TIME**

- Some electronic components respond instantly.
- Others change slowly over time.

<!-- ![bg contain right](assets/clock.gif) -->

---

# Today's Workflow

1. Learn what a capacitor is
2. Observe charging and discharging
3. Build LED fade/delay circuits
4. Measure timing using RC circuits
5. Build an astable multivibrator oscillator
6. Connect oscillators to computing systems

---

![bg contain](assets/100-dollar.jpg)

<!-- INSTRUCTOR NOTES:

Ben Franklin was a electricity enthusiast and experimenter. Electricity was a curiosity at the time. People didn't yet understand how it worked, though they could observe natural phenomeon like lightning and static electric shocks.

-->

---

![bg contain](assets/18th-century-electricity-experiment-bildagentur-onlinetschanz.jpg)

<!-- INSTRUCTOR NOTES:

Electrician comes from magician. People went around doing demonstrations with electricity like magic tricks.

-->
---

![bg contain](assets/18th-century-electrical-experiment-sheila-terry.jpg)

<!-- INSTRUCTOR NOTES:

people studied electricity to try and understand it and shocked themselves often

One of Franklin's favorite experiments was the "circle shock." In the circle shock, a group of people hold hands and one person at the end of the human chain holds the outside of the Leyden jar, while the person on the other end of the human chain touches the inner conductor. If there is enough charge in the jar, every person in the circle will feel a shock.

-->

---

![bg contain](assets/franklin-electrostatic-machine.jpg)

<!-- INSTRUCTOR NOTES:

Franklin developed this machine to generate static electricity.

-->

---


---

![bg contain](assets/franklin-current.avif)

<!-- INSTRUCTOR NOTES:

Franklin did experiements with electricity to help with health (eg depression, paralysis, pain, etc.)

It didn't actually cure anything, but we still have electric therapies for depressiojn

-->

---

![bg contain](assets/leyden-battery.jpg)

<!-- INSTRUCTOR NOTES:

-->

---

![bg contain](assets/leyden-jar.png)

<!-- INSTRUCTOR NOTES:

The original Leyden jar held water as the inner conductor. Early electrical experimenters thought that the charge was held in the water. However, Benjamin Franklin was the first person to figure out that the charge in the Leyden jar is located where the insulator meets the electrode (in this case, the water). Thus, water is not required and can be replaced by attaching an electrode, such as aluminum foil, to the inside of the jar. Franklin also connected several Leyden jars together and created what he called a battery. This is not a battery like we know today, but it was a way to store lots of charge for Franklin's electrical experiments.


# is this true?
Franklin intuited (positive and negative charge) as a build up (and lack of) electrons. 

He actually mistaked that electricity flowed positive to negative (which is wrong and took 100+ years to figure out). So we have "conventional current" but it actually flows negative to positive

-->

---

![bg contain](assets/how-capacitors-work.gif)

<!-- INSTRUCTOR NOTES:


-->

---

# Why do we need to store a charge?

Computers and circuits often need to store a charge

- Camera flashes
- Audio systems
- Phone chargers
- Power supplies
- Motherboards
- WiFi radios
- DRAM memory
- Timing circuits

<!-- TODO: image -->

---

# What Is A Capacitor?

A capacitor stores electrical energy in an electric field.


| Component | Energy Storage | Charge / Discharge |
| --------- | -------------- | ------------------ |
| Battery   | Chemical       | Slow               |
| Capacitor | Electric Field | Fast               |

<!-- INSTRUCTOR NOTES:

Think of it like:

- a tiny rechargeable bucket
- a spring for electrons
- short-term memory for a circuit

-->

<!-- TODO: image -->
<!-- ![bg contain right](assets/capacitor-diagram.png) -->

[Video: Capacitors Explained](https://www.youtube.com/watch?v=X4EUwTwZ110)

---

# Capacitor Basics

Capacitors have:

- Two conductive plates
- An insulating material between them
- As charge builds voltage across the capacitor increases
- *Some* capacitors have polarity
<!-- ![bg contain right](assets/capacitor-cross-section.png) -->

---

# Units

Capacitance is measured in **Farads (F)**

- microfarad (μF)
- nanofarad (nF)
- picofarad (pF)

<!-- Named after Faraday -->
<!-- ![bg contain right](assets/capacitors-variety.jpg) -->

---

# Charging Curve

When charging:

- voltage rises gradually
- current decreases gradually

This creates an exponential curve.

<!-- ![bg contain right](assets/capacitor-charging-curve.png) -->

<!-- INSTRUCTOR NOTES:

Resistors respond immediately.

Capacitors change over time.

At first capacitor charges quickly
Later charging slows down
Eventually capacitor becomes mostly full

-->

---

# Discharging Curve

When discharging:

- stored energy leaves the capacitor
- voltage falls gradually
- LED brightness fades over time

<!-- ![bg contain right](assets/capacitor-discharging-curve.png) -->

---

# RC Circuit

- A resistor + capacitor together form an: **RC Circuit**
- The resistor controls how fast the capacitor charges/discharges.

<!-- ![bg contain right](assets/rc-circuit.png) -->

---

# Demo: LED Fade Circuit

<!-- Demo charging capacitor, then adding an led? -->
We will build a simple capacitor-powered LED fade circuit.

<!--

Observe:

- LED slowly fades out
- capacitor stores energy briefly
- resistor changes fade speed
- capacitor blocks dc

-->

<!-- ![bg contain right](assets/led-fade.gif) -->

---

# What Is Happening?

1. Capacitor charges from the battery
2. Battery disconnects
3. Capacitor releases stored energy
4. LED slowly dims

This is stored electrical energy over time.

---

# Time Constant

The timing behavior is controlled by:

# τ = R × C

Where:

- R = resistance
- C = capacitance
- τ (tau) = time constant

Larger resistor = slower
Larger capacitor = slower

---

# Intuition

| Component | Effect |
| --- | --- |
| Bigger resistor | Slower charging |
| Bigger capacitor | More stored charge |
| Smaller resistor | Faster charging |
| Smaller capacitor | Faster fading |

---

# Demo: Measuring Capacitors

Use the multimeter to:

- measure capacitance (if supported)
- observe charging voltage
- observe discharging voltage
- compare capacitor sizes

---

# Lab Breakout #1

## RC LED Fade + Delay Timer Circuits

Goal: Build an LED fade/delay circuit.

Try changing:

- resistor values
- capacitor values
- LED color
- battery voltage

Measure:

- fade time
- capacitor voltage

Start in Tinkercad, then build physically.

<!-- 

---

TODO: move to lab?

# Challenge Ideas

Can you:

- make the LED stay on longer?
- make it blink faster?
- make two LEDs alternate?
- create a soft fade-in effect?
- make a pushbutton delay? 

-->

---

# Capacitors + Transistors

Yesterday: transistors controlled switching

Today: capacitors control timing

Together they create:

- oscillators
- clocks
- timers
- memory systems

---

# Oscillators

An oscillator repeatedly switches between ON and OFF.

Examples:

- blinking LEDs
- clock circuits
- alarm sounds
- CPU clocks
- radio signals

<!-- TODO: measured in Hz? -->

<!-- ![bg contain right](assets/blinking-led.gif) -->

---

# Why Oscillators Matter

Computers need clocks. A clock signal tells circuits:

- when to update
- when to compute
- when to store data

Without timing, CPUs cannot coordinate operations.

Modern processors operate at billions of cycles per second (3 GHz = 3 billion oscillations per second)

<!-- ![bg contain right](assets/cpu-clock.jpg) -->

---

# Demo: Astable Multivibrator

A classic transistor oscillator. It continuously flips between two states.

The capacitors repeatedly:

- charge
- trigger transistors
- discharge
- switch sides

Observe:

- alternating LEDs
- timing changes
- capacitor charge/discharge behavior

<!--

Questions:

- What changes blink speed?
- What happens with larger capacitors?
- What happens with larger resistors?

-->

---

# Debugging Timing Circuits

If your circuit does NOT work:

- check capacitor polarity
- verify resistor values
- check transistor orientation
- inspect loose wires
- verify power rails
- test LEDs individually

Timing circuits can fail in subtle ways.

<!-- ![bg contain right](assets/debugging.gif) -->

---

# Lab Breakout #2

## Astable Multivibrator

Goal:

Build a two-transistor blinking LED oscillator.

Try:

- changing capacitor values
- changing resistor values
- mismatched timing components
- measuring blink frequency

---

# Key Takeaways

<!--

- Capacitors store electrical energy
- Capacitors introduce TIME into circuits
- RC circuits create delays and fades
- Timing depends on resistance and capacitance
- Oscillators repeatedly switch states
- Computers depend heavily on timing circuits
- Memory systems often use capacitors

-->
