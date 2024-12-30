Assembly Guide for Redding Drone Show Drones
============================================

This guide provides detailed instructions for assembling drones for internal use at Redding Drone.

.. note::
   Most of this guide follows alongside PX4's own guide on building the S500 frame. For unclear instructions, refer to their guide here: https://docs.px4.io/main/en/frames_multicopter/holybro_s500_v2_pixhawk4.html

Parts List
----------

Core Components:
^^^^^^^^^^^^^^^^

- F9P RTK Module: High-precision GPS for positioning
- Pixhawk 6C Mini Flight Controller: Main control system for the drone
- 5000mAh 4C LiPo Battery: Powers the entire drone
- 3DR WiFi Module: Provides wireless communication for drone control
- TGY-IA6B Radio Receiver: Receives control inputs from the remote
- S500 Drone Frame / Motor Kit

.. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/WIFI.png
   :width: 400
   :alt: Basic Hardware Overview

Additional Hardware:
^^^^^^^^^^^^^^^^^^^^

- Metric Screwdrivers: M2.5, M2

Wiring Configuration
--------------------

- F9P RTK Module → GPS 1 on Pixhawk
- PM02 Power Module → POWER on Pixhawk
- 3DR WiFi Module → TELEM 1 on Pixhawk
- TGY-IA6B Radio Receiver → PPM/SBUS RC on Pixhawk
  - Yellow wire: Signal (top pin)
  - Black wire: Ground (bottom pin)
- ESCs → I/O PWM OUT

.. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/ReceiverWiring.png
   :width: 400
   :alt: Receiver Wiring Example

Assembly Steps
--------------

1. Landing Gear Installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: https://docs.px4.io/main/assets/s500_fig1.NawTu5yB.jpg
   :width: 250
   :alt: S500 Landing Gear

**Tools & Materials:**

- Metric Hex Bit (2.5mm)
- 2x Landing Gear
- 2x Vertical Pole

**Steps:**

1. Unscrew the clamp on the Landing Gear.
2. Insert the Vertical Pole into the Landing Gear.
3. Align the flat base so that the Vertical Pole is symmetrical with the Landing Gear.
4. Tighten the clamp on the Landing Gear.

.. image:: https://docs.px4.io/main/assets/s500_fig2.DUocALWg.jpg
   :width: 250
   :alt: S500 assembled landing gear

2. Solder Battery Adapter to Frame PDB
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Tools & Materials:**

- Pliers/scissors (to cut wires)
- Wire Strippers
- Soldering Station
- Solder
- PM02 V3 Power Module

**Steps:**

1. Cut the male end of the power module (close to the connector to not waste wire).

   .. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/cutPower.png
      :width: 250
      :alt: Cut diagram for PM02D

   .. warning::
      Make sure the battery is disconnected

2. Separate the two connections, stripping off ~1.5cm of shielding on each.
3. Pre-tin the tips of both ends.
4. Pre-solder a generous amount on each pad (+ & -).
5. Solder connections appropriately (Red to + | Black to -).

   .. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/SolderPoints.jpg
      :width: 250
      :alt: Already Soldered Ends on PDB

3. Attaching Landing Gear to Frame PDB
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Tools & Materials:**

- M3*8 Screws (8x Black)
- Metric Hex Bit (2.5mm)
- 2x Assembled Landing Gear

**Steps:**

1. Place the landing gear on the frame's PDB (Power Distribution Board).

   .. image:: https://docs.px4.io/main/assets/s500_fig3.5YUW7iL9.jpg
      :width: 250
      :alt: S500 landing gear placement and screw holes

2. Secure the gear using M3X8 screws, threading them through the PDB into the gear's attachment points. Repeat for all 8 screws (4 for each landing leg).

   .. note::
      Cross-tighten the screws one by one to reduce the chance of stripping and ensure even tolerance.

   .. image:: https://docs.px4.io/main/assets/s500_fig4.C5K72HQ9.jpg
      :width: 250
      :alt: S500 landing gear attached to frame

4. Attaching the Arms to the Frame
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Tools & Materials:**

- M2.5*6 Screws (8x)
- Metric Hex Bit (M2)
- PDB Board with Landing Gear attached
- 4x Drone Arms

**Steps:**

1. Place each arm on the frame, aligning the screw holes.
2. Secure each arm with 2 M2 screws through the PDB into the arm's threads.
3. Route the ESC wires through the center of the arm to the board.

5. Mounting the Motors to the Arms
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Tools & Materials:**

- M3*7 Screws (16x Silver)
- Metric Hex Bit (M2.5)
- 4x Motors
- 4x Zip Ties

**Steps:**

1. Identify motor placement (e.g., black motors on the back arms, white on the front).
2. Secure each motor to the corresponding arm using 4 M3 screws.
3. Route the motor wires through the frame holes, wiring only the black motors as follows:
   - RED: Left
   - BLACK: Middle
   - BLUE: Right

   .. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/DroneArmBlack%20Bg.png
      :width: 250
      :alt: Black Motor Wiring

4. Wire the white motors as follows:
   - RED: Left
   - BLUE: Middle
   - BLACK: Right

   .. image:: https://raw.githubusercontent.com/BillyDaBones/Redding-Drone/main/docs/source/assets/DroneArmWhite%20Bg.png
      :width: 250
      :alt: White Motor Wiring

   .. warning::
      Wiring configuration is *VITAL* to be done correctly. Take care to ensure the correct order of wires.

5. Secure the wires to the arm using zip ties, ensuring no wires are damaged.

6. Battery Mount Installation
-------------------------

**Tools & Materials:**

- Phillips Head Screwdriver
- Hex M2 Bit
- Battery Mount Components:
  - 4x Rubber Couplings
  - 4x Plastic Adapters
  - 2x Carbon Adapters
  - 1x Adapter Plate
  - 4x Phillips Screws
  - 2x Carbon Tubes
  - 2x Mounting Attachments
      .. image:: https://docs.px4.io/main/assets/s500_fig31.n6bm_ztm.jpg
         :width: 250
         :alt: required parts for assembly

**Steps:**

1. Prepare the Rubber Couplings:
   - Insert one rubber coupling into each plastic adapter (4 total)
   
   .. note::
      Ensure the rubber couplings are fully seated in the plastic adapters for proper grip.
   .. image:: https://docs.px4.io/main/assets/s500_fig33.Dcf0oGtL.png
      :width: 250
      :alt: arranged parts for assembly

2. Assemble the Main Plate:
   - Place the carbon adapters on either side of the adapter plate
   - Insert Phillips screws through the adapter plate
   - Secure the screws into the carbon adapters
   - Ensure connections are tight but not over-tightened
      .. image:: https://docs.px4.io/main/assets/s500_fig35.CwQe4_cB.jpg
         :width: 250
         :alt: Plate attachment for carbon rod adapters 

1. Prepare the Carbon Tubes:
   - Take the rubber/plastic adapter assemblies from step 1
   - Place two adapters onto each carbon tube
   - Space them evenly for balanced support
   
2. Final Assembly:
   - Mount the completed assembly to the bottom PDB Board
   - Use the two outer attachment points for securing
   - Verify the mount is level and secure
      .. image:: https://docs.px4.io/main/assets/s500_fig34.DgCxhyz9.jpg
         :width: 250
         :alt: fully assembled batttery mount
   
   .. note::
      The battery mount clips should be utilizing the outer row of holes on the PDB

.. image:: https://docs.px4.io/main/assets/s500_fig36.C6Fs6qVj.jpg
   :width: 250
   :alt: Battery Mount Assembly

7. Mounting the RTK Module
^^^^^^^^^^^^^^^^^^^^^^^^^^

**Tools & Materials:**

- RTK Module with mounting hardware
- Metric Hex Bit (M2)
- Pliers

**Steps:**

1. Attach the circular plate to the RTK module using the included screws.
2. Insert the carbon fiber tube into the circular plate clamp.
3. Secure the tube with an M2 screw.
4. Mount the RTK assembly to the frame's front top rails, securing with screws.

8. Mounting the WiFi Module and RC Receiver
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

**Tools & Materials:**

- 3DR WiFi Module
- RC Receiver (TGY-IA6B)
- Double-sided tape
- Scissors (optional)

**Steps:**

1. Cut a small strip of double-sided tape.
2. Attach the tape to the RC receiver and mount it over the plus/minus connections at the back of the PDB.
3. Secure the WiFi module similarly using double-sided tape.

.. note::
   Images will be added to each step to provide visual guidance.

More to be Added
----------------

This guide is a work in progress. Additional steps and details will be added in future updates.