---
marp: true
theme: default
paginate: true
---

# CS Hardware - Day 3

## Time

<!-- ### Capacitors, Delay, Oscillation -->

![bg contain right](assets/capacitor-closeup.jpg)

---

# Goal For Today

By the end of today you will:

- Understand what capacitors store
- Learn how capacitors interact with time
- Build an LED delay and fade timer using an RC circuit
- Explore charging and discharging curves
- Build an astable multivibrator oscillator
- Connect timing circuits to real computer hardware

![bg contain right](assets/capacitor-bank.jpg)

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

Today we add a new idea:

# TIME

Some electronic components respond instantly.

Others change slowly over time.

![bg contain right](assets/clock.gif)

---

<!--

TODO: start with problem

- camera flash
- dram memory

-->

---

# Question

How can a circuit:

- wait?
- blink?
- fade?
- remember?
- keep rhythm?

Answer:

# Capacitors

---

# Today's Workflow

1. Learn what a capacitor is
2. Observe charging and discharging
3. Build LED fade/delay circuits
4. Measure timing using RC circuits
5. Build an astable multivibrator oscillator
6. Connect oscillators to computing systems

---

# Why Time Matters In Computing

Computers depend on timing.

Examples:

- CPU clock signals
- RAM refresh cycles
- Network timing
- Audio signals
- Video refresh
- Debouncing buttons
- Startup delays

![bg contain right](assets/cpu-closeup.jpeg)

---

# What Is A Capacitor?

A capacitor stores electrical energy in an electric field.

Think of it like:

- a tiny rechargeable bucket
- a spring for electrons
- short-term memory for a circuit

![bg contain right](assets/capacitor-diagram.png)

---

# Water Analogy

Imagine:

- Voltage = water pressure
- Current = water flow
- Capacitor = stretchy rubber membrane or storage tank

A capacitor slowly fills and slowly empties.

![bg contain right](assets/water-tank-capacitor.png)

---

# Capacitor Basics

Capacitors have:

- two conductive plates
- an insulating material between them

As charge builds:

- voltage across the capacitor increases
- current flow changes over time

![bg contain right](assets/capacitor-cross-section.png)

---

# Units

Capacitance is measured in:

# Farads (F)

Common values:

- microfarad (μF)
- nanofarad (nF)
- picofarad (pF)

![bg contain right](assets/capacitors-variety.jpg)

---

# Polarized Capacitors

Some capacitors have polarity.

Electrolytic capacitors:

- positive (+)
- negative (-)

Connecting backwards can damage them.

![bg contain right](assets/electrolytic-capacitor-polarity.png)

---

# Capacitors Behave Differently

Resistors respond immediately.

Capacitors change over time.

At first:

- capacitor charges quickly

Later:

- charging slows down

Eventually:

- capacitor becomes mostly full

---

# Charging Curve

When charging:

- voltage rises gradually
- current decreases gradually

This creates an exponential curve.

![bg contain right](assets/capacitor-charging-curve.png)

---

# Discharging Curve

When discharging:

- stored energy leaves the capacitor
- voltage falls gradually
- LED brightness fades over time

![bg contain right](assets/capacitor-discharging-curve.png)

---

# RC Circuit

A resistor + capacitor together form an:

# RC Circuit

The resistor controls how fast the capacitor charges/discharges.

![bg contain right](assets/rc-circuit.png)

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

# Demo: LED Fade Circuit

We will build a simple capacitor-powered LED fade circuit.

Observe:

- LED slowly fades out
- capacitor stores energy briefly
- resistor changes fade speed

![bg contain right](assets/led-fade.gif)

---

# What Is Happening?

1. Capacitor charges from the battery
2. Battery disconnects
3. Capacitor releases stored energy
4. LED slowly dims

This is stored electrical energy over time.

---

# Real World Examples

Capacitors are everywhere:

- Camera flashes
- Audio systems
- Phone chargers
- Power supplies
- Motherboards
- WiFi radios
- DRAM memory
- Timing circuits

![bg contain right](assets/motherboard-capacitors.jpg)

---

# Why Motherboards Use Capacitors

Capacitors help:

- smooth voltage
- reduce electrical noise
- stabilize CPU power
- handle sudden current spikes

Without capacitors computers become unstable.

![bg contain right](assets/motherboard-closeup.jpg)

---

# DRAM Memory

Dynamic RAM stores bits using tiny capacitors.

Each capacitor:

- charged = 1
- discharged = 0

But capacitors slowly leak charge.

So DRAM must constantly refresh.

![bg contain right](assets/ram-closeup.jpg)

---

# Demo: Measuring Capacitors

Use the multimeter to:

- measure capacitance (if supported)
- observe charging voltage
- observe discharging voltage
- compare capacitor sizes

---

# Lab Breakout #1

## RC LED Fade Timer

Goal:

Build an LED fade/delay circuit.

Try changing:

- resistor values
- capacitor values
- LED color
- battery voltage

Measure:

- fade time
- capacitor voltage

Start in Tinkercad, then build physically.

---

# Challenge Ideas

Can you:

- make the LED stay on longer?
- make it blink faster?
- make two LEDs alternate?
- create a soft fade-in effect?
- make a pushbutton delay?

---

# Capacitors + Transistors

Yesterday:

- transistors controlled switching

Today:

- capacitors control timing

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

![bg contain right](assets/blinking-led.gif)

---

# Astable Multivibrator

A classic transistor oscillator.

It continuously flips between two states.

Result:

- alternating blinking LEDs
- repeating timing cycle

![bg contain right](assets/astable-multivibrator.png)

---

# How It Works

The capacitors repeatedly:

- charge
- trigger transistors
- discharge
- switch sides

This creates continuous oscillation.

---

# Demo: Astable Multivibrator

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

# Why Oscillators Matter

Computers need clocks.

A clock signal tells circuits:

- when to update
- when to compute
- when to store data

Without timing, CPUs cannot coordinate operations.

![bg contain right](assets/cpu-clock.jpg)

---

# CPU Clock Speeds

Modern processors operate at:

- billions of cycles per second

Example:

- 3 GHz = 3 billion oscillations per second

Those oscillations begin with timing circuits.

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

![bg contain right](assets/debugging.gif)

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

<!-- 

---

# Optional Extensions

Advanced project ideas:

- electronic dice timer
- reaction timer game
- traffic light simulator
- metronome
- Morse code flasher
- capacitor-powered memory demo
- simple synthesizer/noisemaker 

-->

<!-- 
---

# Reflection Questions

- What stores energy in the circuit?
- Why do LEDs fade instead of instantly turning off?
- How do resistors affect timing?
- Why are oscillators important for computers?
- Where do computers depend on timing?

-->

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

<!-- 

---

# Bonus Demo Ideas

Fast demos that work well live:

- giant capacitor powering LED after unplugging
- supercapacitor vs normal capacitor
- button debounce demo
- capacitor smoothing noisy power
- speaker pop from capacitor charging
- slow-motion LED fade challenge 

-->

<!--

---

# Materials

Helpful components:

- 10μF capacitors
- 100μF capacitors
- 1000μF capacitors
- NPN transistors
- assorted resistors
- LEDs
- pushbuttons
- potentiometers
- breadboards
- multimeters

-->
