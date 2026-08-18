---
onenote-id: 0-bfb991204ba9054d0b25c6a58cce8647!1-D084F068F621FF9!3684
---
To Remember
 
- Fuses for dodgy cells
- Balancer when charging to be equal across cells

PTC  
Positive Temperature Coefficient Switches  
CID  
Charge Interrupt Devices
 
- Can be left out in larger cells
	- The PTC and CID work as expected to switch of the cell on excessive current and internal cell pressure; however the shutdown occurs in cascade format. While some cells may go offline early, the load current causes excess current on the remaining cells. Such overload condition could lead to a thermal runaway before the remaining safety devices activate.
		- \> From \<[https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations](https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations)\>  
            

\> From \<[https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations](https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations)\>  

![Metal outer jacket Terminal contact Vent hole Scor...](../../../../../img/OneNote/Safety%20image%209026364efe672953.png)  

**Figure 1: Typical safety mechanism of the 18650 cell cap.**  
PTC (blue) increases resistance by heat to reduce electrical current. The effect is reversible.  
CID consists of a top disk (orange) that breaks under pressure and permanently disconnects the current flow.

The current interrupt device (CID) is a fuse-type device that cuts off the electrical circuit permanently when triggered by excessive cell pressure, high temperature, or high voltage, depending on design. In Figure 1, the CID operates by pressure. When the internal pressure increases to about 1,000kPa, the scored top disk (orange) breaks, separates from the metallic foil (brown) and disconnects the current flow. This also allows gas to vent.
 \> From \<[https://batteryuniversity.com/learn/article/safety_circuits_for_modern_batteries](https://batteryuniversity.com/learn/article/safety_circuits_for_modern_batteries)\>  

Further layers of safeguards can include solid-state switches in a circuit that is attached to the battery pack to measure current and voltage and disconnect the circuit if the values are too high. Protection circuits for Li-ion packs are mandatory. (See [BU-304b: Making Lithium-ion Safe](https://batteryuniversity.com/index.php/learn/article/bu_304b_making_lithium_ion_safe).)
 \> From \<[https://batteryuniversity.com/learn/article/safety_circuits_for_modern_batteries](https://batteryuniversity.com/learn/article/safety_circuits_for_modern_batteries)\>  

Intrinsically Safe
 
**1. Types of Hazardous Materials present**  
Class I        Flammable gases, vapours or liquids in petroleum refineries, utility gas plants  
Class II       Combustible dust in grain elevators, coal preparations plants  
Class III      Ignitable fibres and flyings in textile mills, wood processing creating sawdust, etc.  
   
**2. Likelihood of Hazardous Materials present**  
Division I        Hazardous materials can exist in ignitable concentrations  
Division II       Hazardous materials will not likely exist in ignitable concentrations  
   
**3. Potency of Hazardous Material** (Groups from A to G)  
A hazardous material is given a designation of: Acetylene (A), hydrogen (B), ethylene (C), propane, gasoline, etc. (D), metal dust (E), coal dust  (F) and grain dust (G).  
   
**4. Temperature Codes** (from T1 to T6)  
The explosion danger of gases or combustible dust is affected by surface temperature. T1 is a hot 450ºC (842ºF); T6 is a moderate 85ºC (185ºF). All other temperatures fall in between.
 \> From \<[https://batteryuniversity.com/learn/article/safety_circuits_for_modern_batteries](https://batteryuniversity.com/learn/article/safety_circuits_for_modern_batteries)\>  

Failures
 
There are two basic types of battery failures. One occurs at a predictable interval-per-million and is connected with a design flaw involving the electrode, separator, electrolyte or processes. These defects often involve a recall to correct a discovered flaw. The more difficult failures are random events that do not point to a design flaw. It may be a stress event like charging at sub-freezing temperature, vibration, or a fluke incident that is comparable to being hit by a meteor.  
 \> From \<[https://batteryuniversity.com/learn/article/safety_concerns_with_li_ion](https://batteryuniversity.com/learn/article/safety_concerns_with_li_ion)\>   
- A mild short will only cause elevated self-discharge and the heat build-up is minimal because the discharging power is very low
	- If enough microscopic metallic particles converge on one spot, a sizable current begins to flow between the electrodes of the cell, and the spot heats up and weakens
	- Heat buildup damages the insulation layer in a cell and cause an electrical short
 
- The temperature can quickly reach 500 C (932 F), at which point the cell catches fire or it explodes. This thermal runaway that occurs is known as “venting with flame.” “Rapid disassembly” is the preferred term by the battery industry.

Cooling
 
Large batteries for power applications are cooled. Some use a rod system to bring the heat to the outside, others deploy forced air or use liquid cooling. Liquid cooling is superior and although more expensive, EV batteries gravitate towards this form of cooling
 \> From \<[https://batteryuniversity.com/learn/article/building_a_lithium_ion_pack](https://batteryuniversity.com/learn/article/building_a_lithium_ion_pack)\>  

UN Transportation Testing (UN/DOT 38.3)
 
T1 – **Altitude Simulation**: Low pressure simulates unpressurized cargo hold at 15,000 meters.  
T2 – **Thermal Test**: Temperature extreme by keeping batteries for 6h at -40°C and then +75°C.  
T3 – **Vibration**: Simulates vibration during transportation at 7Hz to 200Hz for up to 3 hours.  
T4 – **Shock**: Simulates vibration during transportation at given G-forces relating to battery size.  
T5 – **External Short Circuit**: Short circuit with \<0.1Ω at 50°C. Case cannot exceed 170°C.  
T6 – **Impact**: \>20mm cylindrical cells are impact tested; \<20mm cell types are crush tested.  
T7 – **Overcharge**: Charge at twice the recommended current for 24 hours (secondary batteries only)  
T8 – **Forced Discharge**: Same as T7, forced discharge with primary and secondary cells.
 \> From \<[https://batteryuniversity.com/learn/article/building_a_lithium_ion_pack](https://batteryuniversity.com/learn/article/building_a_lithium_ion_pack)\>  

[IEC-62133 Required Safety](https://www.intertek.com/energy-storage/battery-safety/iec-62133/)

[Washington Uni - Lithium Battery Safety](https://www.ehs.washington.edu/system/files/resources/lithium-battery-safety.pdf)  
[Batt uni - BMS](https://batteryuniversity.com/learn/article/how_to_monitor_a_battery?__cf_chl_jschl_tk__=4685dca1ed5d604fe4e7ab13e253e52481563a7c-1609081551-0-AY3KyIfMzWp-rjki3VrQtV3ZNqfY0mhbYai-rTzIVnCjvNNUhWgCh6RJE450-Ttqal6J082sPJDMTdDVTBlPabeHU01JU4hTzvq5BNx-2V8y61985TywTXNZRlWKQ4g1GK5DgSvqI8QmT8Rbaj0PxiTq2OKUHJiS7zadYTNFN460lUVDX8f8tfZTZIR8IC1gpA9mF76kM0QJ8WV7J-Y4Sfsjv4ga1vaL6EmpuECZFv-1zfqeZ66xoUDtNm4vW9x97x9MX4KflmzUr7Xk2E41XfmoNVFLYxYxfcGWsrniA4ldIY3w-NogKvfp-36vXjFGTTnQICScZv6ERsJ9jq_9NOkkyJdoNYIwS-dYFFrxNcMS)  
[Batt uni - smart battery](https://batteryuniversity.com/index.php/learn/article/inner_workings_of_a_smart_battery)  
[Batt uni - SOC](https://batteryuniversity.com/index.php/learn/article/how_to_measure_state_of_charge)  
[Electropaedia - BMS](https://www.mpoweruk.com/bms.htm)