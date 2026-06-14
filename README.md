# ha-sessy-examples
Example automations for using Sessy with Home Assistant


## Sessy X-range the meter (XOM) automation
Extended version of the earlier blueprint (below) made by Tazzios.


## Features
- Dynamic load balancing across multiple batteries  
- SOC-based inclusion/exclusion for optimal battery health  
- Optional offsets for other power consumers (e.g., EV chargers)    
- Keep SOC`s within x% of each other option to ensure equal usage over time or Rotates by priority template.  
- Set grid target range, create a deadband.
- Setpoint template, Do you not want to follow the grid and do something custom?   
- Minimum and maximum power option.
- Smooth transitions, minimum and maximum different in setpoint changes.
- Smooth transitions, Smoothing factor above adjustable level.
- Smooth transitions, seperate smoothing factor when passing zero.
- Start condition, Set a start condition before the script is allowed to run
- Stop action, When the start condition is not met do something else instead. 

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FPimDoos%2Fha-sessy-examples%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fsessy%2Fsessy-+x-range+om.yaml)
 
[Documentation: settings overview](https://github.com/Tazzios/ha-marstek/blob/main/blueprints/Documentation.md)

## Sessy X-on the meter (XOM) automation
Controls Sessy to maintain value X on the grid meter.
- Load balancing across multiple Sessy's
- Except certain load via offset entities (e.g. EV charger)
- Some attention points:
  - Make sure you don't have any helper entities with `_power_strategy`, `_power_setpoint`, `_state_of_charge` or `_system_state` in the name
  - `Update Interval` needs to be slower than the grid connection sensor update interval.
  - `Smoothing` default of 100 to 1000 is a good starting point. This is the maximum step adjustment. When your sensor updates more frequent you should lower the smoothing value. A large value may result in instable control 
  - Your net grid consumption sensor needs to have the unit Watt or kW

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FPimDoos%2Fha-sessy-examples%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fsessy%2Fsessy-xom.yaml)


## Sessy Full charge script
Charges Sessy to the specified amount, then activates a certain strategy.
- Supports multiple Sessy's
- Script ends when all Sessy's report full, above set percentage, or after timeout passes.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FPimDoos%2Fha-sessy-examples%2Fblob%2Fmain%2Fblueprints%2Fscript%2Fsessy%2Fsessy-full-charge.yaml)

## Sessy Dynamic Schedule with ApexCharts
Display the power schedule and energy prices for the dynamic strategy within Home Assistant using ApexCharts. 

[![Dynamic schedule in a graph](cards/DynamicSchedule.png)](cards/DynamicSchedule.md)

[Learn More](cards/DynamicSchedule.md)
