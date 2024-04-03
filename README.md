# ha-sessy-examples
Example automations for using Sessy with Home Assistant

## Sessy X-on the meter (XOM) automation
Controls Sessy to maintain value X on the grid meter.
- Load balancing across multiple Sessy's
- Except certain load via offset entities (e.g. EV charger)

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