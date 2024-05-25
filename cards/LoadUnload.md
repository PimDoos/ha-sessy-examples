# Sessy Load / Unload view

## Requirements
- Sessy batterij (duh)
- [Sessy Integratie](https://github.com/PimDoos/ha-sessy)
- [Apexcharts LoveLace](https://github.com/RomRider/apexcharts-card)
- Home Assistant version 2022.7 or newer.


## Installation

1. Kopieer alle afbeeldingen "images/sessy naar je Home assistant systeem "/local/images/sessy".
2. Creeer nieuwe LoveLave views zoals hieronder getoond.
3. Vervang de sessy entities met jouw entitities in de lovelace yaml views

![Chart](cards/LoadUnload.png)
```
type: custom:apexcharts-card
graph_span: 24h
header:
  show: false
yaxis:
  - id: first
    opposite: true
    decimals: 0
    min: -100
    max: 100
    apex_config:
      tickAmount: 10
  - id: second
    decimals: 0
    min: -2200
    max: 2200
    apex_config:
      tickAmount: 10
series:
  - entity: sensor.sessy_xxxx_state_of_charge
    yaxis_id: first
    type: line
    name: Sessy Batterij Percentage
    min: 0
    max: 100
    group_by:
      func: last
      duration: 30min
  - entity: sensor.sessy_xxxx_power
    yaxis_id: second
    color: blue
    type: area
    name: Sessy Power
    min: -1700
    max: 1700
    group_by:
      func: last
      duration: 30min
```
