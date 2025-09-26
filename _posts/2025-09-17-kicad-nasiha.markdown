---
layout: post
title:  Designing PCBs with KiCad
date:   2018-07-05 15:01:34 +0300
image:  nasi/cover.png
tags:   Home kicad
author: Nasiha
---
##  What is KiCad?
KiCad is a free and open-source software suite for Electronic Design Automation (EDA), used for designing electronic circuit schematics and printed circuit boards (PCBs). It is a powerful tool for professionals and hobbyists and runs on Windows, macOS, and Linux. It simplifies the complex process of going from an idea to a physical circuit board by breaking it down into a logical, step-by-step workflow.

![]({{ site.baseurl }}/images/nasi/kicad-logo.png)
*Kicad logo*

### Core features:
KiCad's integrated environment offers a comprehensive suite of tools for the entire electronic design process:
* **Schematic editor:** Use a vast library of existing components or create your own custom symbols to build a circuit diagram. Features include hierarchical schematics for complex designs and an electrical rules checker (ERC).
  
* **Integrated simulation:** Verify your circuit's behavior with the built-in SPICE simulator before committing to a physical layout.
  
* **PCB layout editor:** Design the physical layout of your circuit board, from simple two-sided boards to complex, modern designs with up to 32 copper layers. It includes advanced features like a push-and-shove interactive router and customizable design rule checking (DRC).
  
* **Footprint and symbol editors:** Create custom component footprints and schematic symbols to add to your personal libraries.
  
* **3D viewer:** Inspect your PCB design in a 3D environment to check for mechanical fit and visualize the finished product.
  
* **Manufacturing file generation:** Generate standard manufacturing files, such as Gerber files, bills of materials (BOM), and artwork, to send to a PCB fabrication house.


## The KiCad Workflow Explained

The design process is divided into a few key stages within the KiCad software suite.

### Step 1: Create the Project

A project file (`.kicad_pro`) keeps all your design files organized in a single folder.

1.  From the KiCad Project Manager, go to **File > New Project**.
2.  Give your project a name and save it to a new, dedicated folder.

### Step 2: Draw the Schematic (Schematic Editor)

This is where you define the electrical connections of your circuit using a virtual blueprint.

1.  **Open the editor:** Double-click the `.kicad_sch` file in the project manager.
2.  **Add components (symbols):** Press `A` to add components like resistors and LEDs from the library.
3.  **Wire components:** Use the `W` hotkey to draw wires that connect the component pins.
4.  **Run Electrical Rules Check (ERC):** This tool checks your schematic for common errors like unconnected pins.

Below it is shown a shematic diagram of an inverting amplifier
    
![]({{ site.baseurl }}/images/nasi/schematic.png)
*Schematic*

### Step 3: Assign Footprints

After verifying your schematic, you must link each virtual symbol to a physical footprint.

1.  **Open the Footprint Assignment Tool:** Go to **Tools > Assign Footprints** from the Schematic Editor.
2.  **Match symbols:** Link each symbol to a corresponding footprint from KiCad's extensive library.

### Step 4: Lay out the PCB (PCB Editor)

This is where you design the physical board's shape and place the components.

1.  **Open the editor:** Click the **Run Pcbnew** icon from the project manager.
2.  **Import components:** Select **Tools > Update PCB from Schematic** (`F8`) to bring your components and their connection information into the layout editor.
3.  **Define board shape:** Switch to the `Edge.Cuts` layer and draw the outline of your PCB.
4.  **Position components:** Arrange the footprints on the board to optimize the layout, minimizing long connections.

here a pcb layout of  an inverting amplifier is shown:

![]({{ site.baseurl }}/images/nasi/PCBlayout.png)
*Layout*

### Step 5: Route the Traces

Routing is the process of creating the physical copper tracks on the board.

1.  **Use the routing tool:** Select the **Route Tracks** tool (`X`) to draw the copper traces that will connect your components.
2.  **Switch layers:** Press `V` to insert a via and switch to another layer, allowing traces to cross.

### Step 6: Perform Design Rules Check (DRC)

This is a critical final check to ensure your board is manufacturable.

1.  **Launch the DRC:** Go to `Inspect` > `Design Rules Checker`.
2.  **Run the check:** Enable "Refill all zones" and "Test for parity with schematic," then click **Run DRC**.
3.  **Fix errors:** Double-click on any errors in the report to find and correct them.
4.  **View in 3D:** Use `View` > `3D Viewer` to see a virtual model of your completed board.

![]({{ site.baseurl }}/images/nasi/3Dview.png)
*Schematic*

### Step 7: Generate Fabrication Files

The final step is to generate the standard files a PCB manufacturer needs to build your board.

1.  **Generate Gerbers:** Go to **File > Fabrication Outputs > Gerbers** to generate the files for each layer of your board.
2.  **Generate drill files:** In the same menu, go to **Drill Files** to create the files for drilling the holes.
3.  **Package files:** Compress all the output files into a zip file to send to the manufacturer.

---

## Why Use KiCad?

*   **Completely Free & Open-Source:** No cost or restrictive licenses.
*   **Professional-Grade:** Supports complex multi-layer boards and includes advanced features.
*   **Multi-Platform:** Runs on Windows, macOS, and Linux.
*   **Active Community:** Backed by a large community of users and developers, with excellent documentation and support.
Think of KiCad as a digital version of a drafting table for electronics. It provides a complete design environment for:
*   **Schematic Capture:** Drawing your circuit using symbols to represent components.

---


