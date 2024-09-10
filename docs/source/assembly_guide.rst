Assembly Guide for Redding Drone Show Drones
============================================

This guide provides detailed instructions for assembling drones for internal use at Redding Drone.

Parts List
----------

**Core Components:**

- **F9P RTK Module**: High-precision GPS for positioning.
- **Pixhawk 6C Mini Flight Controller**: Main control system for the drone.
- **5000mAh 4C LiPo Battery**: Powers the entire drone.
- **3DR WiFi Module**: Provides wireless communication for drone control.
- **TGY-IA6B Radio Receiver**: Receives control inputs from the remote.
- **S500 Drone Frame / Motor Kit**

.. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/WIFI.png
  :width: 400
  :alt: Basic Hardware Overview

**Additional Hardware:**
  
- **Metric Screwdriver: M2.5, M2.**

Wiring Configuration
--------------------

- **F9P RTK Module** → **GPS 1** on Pixhawk
- **PM02 Power Module** → **POWER** on Pixhawk
- **3DR WiFi Module** → **TELEM 1** on Pixhawk
- **TGY-IA6B Radio Receiver** → **PPM/SBUS RC** on Pixhawk
  - **Yellow wire**: Signal (top pin)
  - **Black wire**: Ground (bottom pin)
- **ESCs** → **I/O PWM OUT**

.. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/ReceiverWiring.png
  :width: 400
  :alt: Receiver Wiring Example

Assembly Steps
--------------

**1. Landing Gear Installation**

.. image:: https://docs.px4.io/main/assets/s500_fig1.NawTu5yB.jpg
  :width: 250
  :alt: S500 Landing Gear

*Tools & Materials:*

- Metric Hex Bit (2.5mm)
- 2x Landing Gear
- 2x Vertical Pole

*Steps:*

1. Unscrew the clamp on the Landing Gear.
2. Insert the Vertical Pole into the Landing Gear.
3. Align the flat base so that the Vertical Pole is symmetrical with the Landing Gear.
4. Tighten the clamp on the Landing Gear.

.. image:: https://docs.px4.io/main/assets/s500_fig2.DUocALWg.jpg
  :width: 250
  :alt: S500 assembled landing gear

**1.5. Solder Battery Adapter to Frame PDB 

*Tools & Materials:*

- Pliers/scissors (to cut wires)
- Wire Strippers
- Soldering Station
- Solder
- PM02 V3 Power Module

*Steps:*

- Start by cutting the male end (as close to the connector to not waste wire)
.. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/cutPower.png
  :width: 250
  :alt: Cut diagram for PM02D
    *make sure battery is disconnected*
- Seperate the two connections, striping off ~1.5cm of shielding on each
- Pre-tin the tips of both ends
- Pre-solder a generouis amount on each pad (+ & -)
- Solder connections appropriatley (Red to + | Black to -)
.. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/SolderPoints.jpg
  :width: 250
  :alt: Already Soldered Ends on PDB
- *End Results*

**2. Attaching Landing Gear to Frame PDB**

.. image:: https://docs.px4.io/main/assets/s500_fig3.5YUW7iL9.jpg
  :width: 250
  :alt: S500 landing gear attached to frame

*Tools & Materials:*

- M3*8 Screws (8x Black)
- Metric Hex Bit (2.5mm)
- 2x Assembled Landing Gear

*Steps:*

1. Place the landing gear on the frame's PDB (Power Distribution Board).
2. Secure the gear using M3 screws, threading them through the PDB into the gear’s attachment points.
   - **Tip**: cross tighten the screws one by one, to reduce the chance of stripping, and even tolerance.

**3. Attaching the Arms to the Frame**

*Tools & Materials:*

- M2.5*6 Screws (8x)
- Metric Hex Bit (M2)
- PDB Board with Landing Gear attached
- 4x Drone Arms

*Steps:*

1. Place each arm on the frame, aligning the screw holes.
2. Secure each arm with 2 M2 screws through the PDB into the arm’s threads.
3. Route the ESC wires through the center of the arm to the board.

**4. Mounting the Motors to the Arms**

*Tools & Materials:*

- M3*7 Screws (16x Silver)
- Metric Hex Bit (M2.5)
- 4x Motors
- 4x Zip Ties

*Steps:*

1. Identify motor placement (e.g., black motors on the back arms, white on the front).
2. Secure each motor to the corresponding arm using 4 M3 screws.
3. Route the motor wires through the frame holes, connecting them to the ESCs:
   - **RED**: Left
   - **BLUE**: Middle
   - **BLACK**: Right
4. Secure the wires to the arm using zip ties, ensuring no wires are damaged.

**5. Mounting the RTK Module**

*Tools & Materials:*

- RTK Module with mounting hardware
- Metric Hex Bit (M2)
- Pliers

*Steps:*

1. Attach the circular plate to the RTK module using the included screws.
2. Insert the carbon fiber tube into the circular plate clamp.
3. Secure the tube with an M2 screw.
4. Mount the RTK assembly to the frame’s front top rails, securing with screws.

**6. Mounting the WiFi Module and RC Receiver**

*Tools & Materials:*

- 3DR WiFi Module
- RC Receiver (TGY-IA6B)
- Double-sided tape
- Scissors (optional)

*Steps:*

1. Cut a small strip of double-sided tape.
2. Attach the tape to the RC receiver and mount it over the plus/minus connections at the back of the PDB.
3. Secure the WiFi module similarly using double-sided tape.

.. note::

    Images will be added to each step to provide visual guidance.

MORE TO BE ADDED
----------------
