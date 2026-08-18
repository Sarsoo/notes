---
onenote-id: 0-e70271a3b92c01612da9a768f8aec752!1-D084F068F621FF9!3684
---
$N_{c e l l s} = \left(\left(V_{b a t}\right)/\left(V_{c e l l}\right)\right) \cdot \left(\left(I_{b a t}\right)/\left(I_{c e l l}\right)\right)$

[Determine How Many Cells In A Battery Pack](https://www.batteriesinaflash.com/blog/determine-many-cells-battery-pack/)  
[BU-302: Series and Parallel Battery Configurations](https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations)  
[BU-304b: Making Lithium-ion Safe](https://batteryuniversity.com/learn/article/bu_304b_making_lithium_ion_safe)

_Adding cells in parallel will increase the available amperage(capacity). Adding cells in series will increase the voltage(power to push the capacity)_
 
_When in series they add to increase the voltage but the current is the same in each cell._
 \> From \<[https://www.quora.com/How-many-cells-make-one-battery](https://www.quora.com/How-many-cells-make-one-battery)\>  

- Voltage fixed by chemistry
	- Storage measured in Ah not Wh
- Discharge current measured by C-rate

_If you are charging lithium-ion or LiPo batteries in series, you need to make sure to use special circuitry known as a "balancer" to ensure the voltages among the cells stays even. Some chargers, like_ _this one__, have balancers to allow for safe charging._
 \> From \<[https://learn.sparkfun.com/tutorials/what-is-a-battery/all](https://learn.sparkfun.com/tutorials/what-is-a-battery/all)\>  

# Series

Increase voltage
 
# Parallel

Increase capacity

- Also C-rate
- All the cells should have the same nominal voltage and same charge level
- If there are any voltage differences, a short circuit could occur causing overheating and possibly fire.

![2000 mAh z 2000 mAh z 2000 mAh 2000 mAh O](../../../../../img/OneNote/Configuration%20image%202125974091a97d97.png) ![Batteries in parallel](../../../../../img/OneNote/Configuration%20image%204ba28952c5b24c71.png) ![Batteries in series and parallel](../../../../../img/OneNote/Configuration%20image%2048c21bfa709b6a0e.png)

_In large battery packs, especially lithium-ion, you often see the configuration listed using 'S' and 'P' for series and parallel. The configuration for the circuit above is 2S2P_

_A cell that develops high resistance or opens is less critical in a parallel circuit than in a series configuration, but a failing cell will reduce the total load capability. It’s like an engine only firing on three cylinders instead of on all four. An electrical short, on the other hand, is more serious as the faulty cell drains energy from the other cells, causing a fire hazard. Most so-called electrical shorts are mild and manifest themselves as elevated self-discharge._
 
_A total short can occur through reverse polarization or dendrite growth. Large packs often include a fuse that disconnects the failing cell from the parallel circuit if it were to short._
 \> From \<[https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations](https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations)\>  

_With Li-ion, the parallel strings are always made first; the completed parallel units are then placed in series._
 \> From \<[https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations](https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations)\>  

_Cell matching is a challenge when replacing a faulty cell in an aging pack. A new cell has a higher capacity than the others, causing an imbalance. Welded construction adds to the complexity of the repair, and this is why battery packs are commonly replaced as a unit._
 
_High-voltage batteries in electric vehicles, in which a full replacement would be prohibitive, divide the pack into modules, each consisting of a specific number of cells. If one cell fails, only the affected module is replaced. A slight imbalance might occur if the new module is fitted with new cells_
 \> From \<[https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations](https://batteryuniversity.com/learn/article/serial_and_parallel_battery_configurations)\>  

|   |   |   |   |
|---|---|---|---|
|**Nominal cell voltage**|**Typical end-of-discharge**|**Max charge voltage**|**Notes**|
|3.6V|2.8–3.0V|4.2V|Classic nominal voltage of cobalt-based Li-ion battery|
|3.7V|2.8–3.0V|4.2V|Marketing advantage. Achieved by low internal resistance|
|3.8V|2.8–3.0V|4.35V|Surface coating and electrolyte additives. Charger must have correct full-charge voltage for added capacity|
|3.85V|2.8–3.0V|4.4V|Surface coating and electrolyte additives. Charger must have correct full-charge voltage for added capacity|
 \> From \<[https://batteryuniversity.com/learn/article/confusion_with_voltages](https://batteryuniversity.com/learn/article/confusion_with_voltages)\>  
       
18650 Cell
 
- Tesla S85 EV has over 7,000 cells
 
- Nominal Voltage: 3.6V
- Nominal Capacity: 2,850 mAh
- Minimum Discharge Voltage: 3V
- Maximum Discharge current: 1C
- Charging Voltage: 4.2V (maximum)
- Charging current: 0.5C
- Charging Time: 3 hours (approx)
- Charging Method: CC and CV
- Cell Weight: 48g (approx)
- Cell Dimension: 18.4mm (dia) and 65mm (height) \> From \<[https://components101.com/batteries/18650-lithium-cell](https://components101.com/batteries/18650-lithium-cell)\>  
 \> From \<[https://components101.com/batteries/18650-lithium-cell](https://components101.com/batteries/18650-lithium-cell)\>  

|   |   |   |   |
|---|---|---|---|
|**Make and model**|**Cell type**|**Cost per kWh**|**Specific energy**|
|Tesla S 85, 90kWh (2015)*|18650|$260/kWh|250Wh/kg|
|Tesla 48kWh Gen III|18650|$260/kWh|250Wh/kg|
|Best practices DoE/AABC)|pouch/prismatic|$350/kWh|150–180Wh/kg|
|Nissan Leaf, 30kWh (2016)*|pouch/prismatic|$455/kWh|80–96Wh/kg|
|BMW i3|pouch/prismatic|N/A|120Wh/kg|

***** In 2015/16 Tesla S 85 increased the battery from 85kWh to 90kWh; Nissan Leaf from 25kWh to 30kWh.
 \> From \<[https://batteryuniversity.com/learn/article/building_a_lithium_ion_pack](https://batteryuniversity.com/learn/article/building_a_lithium_ion_pack)\>