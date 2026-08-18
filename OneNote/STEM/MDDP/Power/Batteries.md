---
onenote-id: 0-49a36ad4328f063932812c342ab8c41b!1-D084F068F621FF9!3684
---
Types
 
- Primary
	- Used once and discarded
	- Non-reversible electrochemical reaction
	- Polarise during use
		- Hydrogen accumulating at cathode and reducing effectiveness
		- Oxidising agent added to counteract
			- e.g. Manganese dioxide
- Secondary
	- **Rechargeable**
	- Reversible reaction
		- Regenerate chemical reactants

Rechargeable
 
- Arranged in electrochemical cells
- **Accumulator**
	- Accumulates and stores energy through reaction
- Charging
	- Positive active material oxidised (+electrons)
	- Negative material reduced (-electrons)
	- AC mains
		- Source voltage must be higher than battery to charge
			- Not high enough to damage it
- Depth of Discharge
	- 0% = fully charged
	- Can change over time or charge cycles
	- Generally handle more charge cycles with lower average DOD
	- Li-ion 80-90%
	- Lead-acid 50-60%
	- Flow batteries 100%

Boat
 
Use Classes:

- SLI
	- _Starting/Lighting/Ignition_
	- Not designed for deep discharging
		- Can reduce lifespan
- Deep Cycle
 
_"When any 12-volt lead-acid battery is discharged below 12.4 volts and is left sitting in that state, sulfation begins forming in the plates, which diminishes both capacity and lifespan. In applications like boats and RVs, that tend not to see continuous use, that makes it very important to keep battery voltage properly-maintained with a quality battery maintenance device."_
 
_"So what can you do to maximize the performance and lifespan of your marine and automotive batteries? Keep them fully-charged whenever possible."_
 
[Optima Batteries - Marine & Car Batteries](https://www.optimabatteries.com/en-us/experience/2020/06/what-difference-between-marine-battery-and-car-battery)
 
![Exported image](../../../../img/OneNote/Batteries%20image%201ebcb5e3bdb214c4.png)

C Rate
 
- Standard current rate for to full charge or discharge battery in 1 hour
- Charge or discharge current divided by battery's capacity to store electrical charge
 
- 500 mAh battery
	- Discharge rate of 5 A
		- $\left(5000   m A\right)/\left(500   m A h\right) = 10 \left(  h\right)^{- 1}$

$\left(5000   m A\right)/\left(500   m A h\right) = 10 \left(  h\right)^{- 1}$  

- Current and capacity in C-rate multiplied by voltage
	- C-rate becomes ratio of power to capacity
	- 100 kWh battery
		- Charging at 120 kW
			- $\left(120   k W\right)/\left(100   k W h\right) = 1 . 2 \left(  h\right)^{- 1}$
		- Discharging at 451 kW
			- $\left(451   k W\right)/\left(100   k W h\right) = 4 . 51 \left(  h\right)^{- 1}$

$\left(120   k W\right)/\left(100   k W h\right) = 1 . 2 \left(  h\right)^{- 1}$ $\left(451   k W\right)/\left(100   k W h\right) = 4 . 51 \left(  h\right)^{- 1}$  

- Higher C-rate
	- Must account for increased heating
	- Attractive to users
		- Quicker charge
		- Higher output current
	- Monitoring chargers
		- Terminal voltage
		- Temperature
	- Only some battery types

Chargers
 
# Simple

- Constant or pulsed DC
- Don't alter output based on time or charge on battery
- Typically take longer
	- Using lower charge current
- Batteries still weakened or damaged from over-charging if left too long

# Fast

- Control circuity within battery or external charger
	- Split across both

# Three-stage

- Bulk absorption
	- High charging current and constant
		- Limited by charger
- Stage 2
	- Battery outgassing voltage
		- 2.22 V per cell
	- Voltage held constant
		- Delivered current declines
- Stage 3
	- Current less than 0.005C
	- Constant 2.25 V across cell
	- Small charging current
		- Maintain high battery charge
		- Compensate for self-discharge

# Intelligent

- Responds to condition of battery
- Smart batteries
	- Internal protection
	- Supervision
	- Management circuitry
- Dumb batteries
	- No control circuitry
- May monitor
	- Voltage
	- Temperature
	- Time under charge
- Ni-Cd/NiMH
	- Voltage across battery increases slowly during charging
	- Once full voltage decreases
		- Indicates fully charged
	- ΔV/Delta V/Delta peak
		- Can be small in high capacity batteries
			- Hard to notice

Cell Types
 
# Wet

- _Flooded cell_
- _Vented cell_
	- Produced gases escape into air
- Liquid electrolyte
- Precursor to dry cell
	- Learning tool
- Primary or secondary applications
- Used in
	- Car batteries
	- Industry
		- Switchgear
		- UPS
			- Gel Cells
- Lead-acid
- Nickel-cadmium

# Dry

- Paste electrolyte
- Operate in any orientation
	- Not going to spill
	- Portable equipment
- Zinc-carbon

# Molten salt

Capacity
 
- Charge it can deliver at the rated voltage
	- More electrode material = more capacity

Operation
 
- Typically, released energy is the difference in cohesive or bond energies
	- Metals, oxides or molecules
	- E.g. Zn or Li
		- High energy metals
		- Not stabilised by d-electron bonding
		- Unlike transition metals
- Redox reaction only occurs when current drawn
- Voltaic cells
	- Two half cells
		- Connected in series by electrolyte
			- Containing metal cations
		- Cathode
			- Negative electrode
			- To which anions migrate
			- Cations reduced
				- e- added
		- Anode
			- Positive electrode
			- To which cations migrate
			- Metal atoms oxidized
				- e- removed
		- Sometimes two different electrolytes with separate to stop mixing
		- Each has emf
			- Volts
			- Electromotive force
			- Relative to [standard](https://en.wikipedia.org/wiki/Standard_hydrogen_electrode)
			- Net emf is difference in half-cell emfs
				- Difference between the reduction potentials of the half-reactions
		- Terminal voltage
			- $\Delta V_{b a t}$
			- Open-circuit voltage
				- When not charging or discharging
				- Emf of the cell
			- Smaller when discharging due to internal resistance

$\Delta V_{b a t}$

Lifespan
 
# Self-discharge

- Disposables lose 8-20% a year
	- _Self-discharge rate_
- Non-current producing side-reactions
	- Even with no load
	- Can reduce by cooling

# Corrosion

- Metals can corrode

# Physical Component Changes

- Active materials change chemical composition on charge/discharge
	- May be lost due to physical changes in volume
- Electrolyte migrates away from the electrodes

# (Dis)Charge Speed

- Faster charging takes higher current
	- Higher heat
	- Faster degradation

# Overcharging

# Memory Effect

- NiCd cells if used in a repetitive manner may show decreased capacity

# Environmental Conditions

- Lead-acid car batteries
	- Vibration
	- Shock
	- Temperature range
	- Sulfation of lead plates
	- SLI batteries can have thin lead plates
		- Maximise current
		- Thicker plates = longer life
	- Deep-cycle batteries
		- Golf carts
		- Thicker plates

# Storage

- Store at low temperature
	- Slows side reactions
	- Extends alkaline by 5%
- To reach max voltage
	- Must be at room temperature
	- Alkaline battery at 250mA at 0 C  
		- Half as efficient as at 20 C  
            

Wikipedia
 
[Battery Storage Power Station](https://en.wikipedia.org/wiki/Battery_storage_power_station)  
[Electric Vehicle Battery](https://en.wikipedia.org/wiki/Electric_vehicle_battery)  
[Flow Battery](https://en.wikipedia.org/wiki/Flow_battery)
 
Links
 
[Battery University](https://batteryuniversity.com/learn/archive/whats_the_best_battery)
  
Need
 
[Strathclyde - Fuel Cell Construction and Performance Characterisation](http://www.esru.strath.ac.uk/EandE/Web_sites/99-00/bio_fuel_cells/groupproject/library/constructionefficiency/text.htm)

[All About Circuits: EV Batteries](https://www.allaboutcircuits.com/technical-articles/introduction-to-electric-vehicle-battery-systems/)

[Epectec - Cell formats](https://www.epectec.com/batteries/prismatic-pouch-packs.html)  
[Batt Uni - Cell formats](https://batteryuniversity.com/learn/article/types_of_battery_cells)  
[18650 shop](https://18650.uk/shop/18650-batteries/)