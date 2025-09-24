# Sessy Battery Status view

## Requirements
- Sessy batterij (duh)
- [Sessy Integratie](https://github.com/PimDoos/ha-sessy)
- [Apexcharts LoveLace](https://github.com/RomRider/apexcharts-card)
- Home Assistant version 2022.7 or newer.

## Installation

1. Kopieer alle afbeeldingen "cards/images naar je Home assistant systeem "/local/images/sessy".
2. Creeer nieuwe LoveLave views zoals hieronder getoond.
3. Vervang de sessy entities met jouw entitities in de lovelace yaml views

![Chart](BatteryStatus.png)
```
elements:
  - entity: sensor.sessy_xxxx_state_of_charge
    image: /local/images/sessy/sessy-00.png
    state_image:
      '0': /local/images/sessy/sessy-00.png
      '1': /local/images/sessy/sessy-01.png
      '2': /local/images/sessy/sessy-02.png
      '3': /local/images/sessy/sessy-03.png
      '4': /local/images/sessy/sessy-04.png
      '5': /local/images/sessy/sessy-05.png
      '6': /local/images/sessy/sessy-06.png
      '7': /local/images/sessy/sessy-07.png
      '8': /local/images/sessy/sessy-08.png
      '9': /local/images/sessy/sessy-09.png
      '10': /local/images/sessy/sessy-10.png
      '11': /local/images/sessy/sessy-11.png
      '12': /local/images/sessy/sessy-12.png
      '13': /local/images/sessy/sessy-13.png
      '14': /local/images/sessy/sessy-14.png
      '15': /local/images/sessy/sessy-15.png
      '16': /local/images/sessy/sessy-16.png
      '17': /local/images/sessy/sessy-17.png
      '18': /local/images/sessy/sessy-18.png
      '19': /local/images/sessy/sessy-19.png
      '20': /local/images/sessy/sessy-20.png
      '21': /local/images/sessy/sessy-21.png
      '22': /local/images/sessy/sessy-22.png
      '23': /local/images/sessy/sessy-23.png
      '24': /local/images/sessy/sessy-24.png
      '25': /local/images/sessy/sessy-25.png
      '26': /local/images/sessy/sessy-26.png
      '27': /local/images/sessy/sessy-27.png
      '28': /local/images/sessy/sessy-28.png
      '29': /local/images/sessy/sessy-29.png
      '30': /local/images/sessy/sessy-30.png
      '31': /local/images/sessy/sessy-31.png
      '32': /local/images/sessy/sessy-32.png
      '33': /local/images/sessy/sessy-33.png
      '34': /local/images/sessy/sessy-34.png
      '35': /local/images/sessy/sessy-35.png
      '36': /local/images/sessy/sessy-36.png
      '37': /local/images/sessy/sessy-37.png
      '38': /local/images/sessy/sessy-38.png
      '39': /local/images/sessy/sessy-39.png
      '40': /local/images/sessy/sessy-40.png
      '41': /local/images/sessy/sessy-41.png
      '42': /local/images/sessy/sessy-42.png
      '43': /local/images/sessy/sessy-43.png
      '44': /local/images/sessy/sessy-44.png
      '45': /local/images/sessy/sessy-45.png
      '46': /local/images/sessy/sessy-46.png
      '47': /local/images/sessy/sessy-47.png
      '48': /local/images/sessy/sessy-48.png
      '49': /local/images/sessy/sessy-49.png
      '50': /local/images/sessy/sessy-50.png
      '51': /local/images/sessy/sessy-51.png
      '52': /local/images/sessy/sessy-52.png
      '53': /local/images/sessy/sessy-53.png
      '54': /local/images/sessy/sessy-54.png
      '55': /local/images/sessy/sessy-55.png
      '56': /local/images/sessy/sessy-56.png
      '57': /local/images/sessy/sessy-57.png
      '58': /local/images/sessy/sessy-58.png
      '59': /local/images/sessy/sessy-59.png
      '60': /local/images/sessy/sessy-60.png
      '61': /local/images/sessy/sessy-61.png
      '62': /local/images/sessy/sessy-62.png
      '63': /local/images/sessy/sessy-63.png
      '64': /local/images/sessy/sessy-64.png
      '65': /local/images/sessy/sessy-65.png
      '66': /local/images/sessy/sessy-66.png
      '67': /local/images/sessy/sessy-67.png
      '68': /local/images/sessy/sessy-68.png
      '69': /local/images/sessy/sessy-69.png
      '70': /local/images/sessy/sessy-70.png
      '71': /local/images/sessy/sessy-71.png
      '72': /local/images/sessy/sessy-72.png
      '73': /local/images/sessy/sessy-73.png
      '74': /local/images/sessy/sessy-74.png
      '75': /local/images/sessy/sessy-75.png
      '76': /local/images/sessy/sessy-76.png
      '77': /local/images/sessy/sessy-77.png
      '78': /local/images/sessy/sessy-78.png
      '79': /local/images/sessy/sessy-79.png
      '80': /local/images/sessy/sessy-80.png
      '81': /local/images/sessy/sessy-81.png
      '82': /local/images/sessy/sessy-82.png
      '83': /local/images/sessy/sessy-83.png
      '84': /local/images/sessy/sessy-84.png
      '85': /local/images/sessy/sessy-85.png
      '86': /local/images/sessy/sessy-86.png
      '87': /local/images/sessy/sessy-87.png
      '88': /local/images/sessy/sessy-88.png
      '89': /local/images/sessy/sessy-89.png
      '90': /local/images/sessy/sessy-90.png
      '91': /local/images/sessy/sessy-91.png
      '92': /local/images/sessy/sessy-92.png
      '93': /local/images/sessy/sessy-93.png
      '94': /local/images/sessy/sessy-94.png
      '95': /local/images/sessy/sessy-95.png
      '96': /local/images/sessy/sessy-96.png
      '97': /local/images/sessy/sessy-97.png
      '98': /local/images/sessy/sessy-98.png
      '99': /local/images/sessy/sessy-99.png
      '100': /local/images/sessy/sessy-100.png
    style:
      left: 50%
      top: 27%
      width: 80%
    type: image
  - entity: sensor.sessy_xxxx_state_of_charge
    style:
      left: 50%
      top: 40%
      font-size: 150%
    type: state-label
  - entity: sensor.sessy_xxxx_system_state
    style:
      left: 50%
      top: 57%
      font-size: 175%
      text-align: center
    type: state-label
    prefix: 'Status: '
  - entity: select.sessy_xxxx_power_strategy
    style:
      left: 50%
      top: 70%
      font-size: 175%
      text-align: center
    type: state-label
    prefix: 'Modus: '
  - type: conditional
    conditions:
      - entity: sensor.sessy_xxxx_charge_power
        state_not: '0'
    elements:
      - type: state-label
        prefix: 'Opladen met: '
        entity: sensor.sessy_xxxx_charge_power
        style:
          top: 83%
          left: 50%
          font-size: 175%
          text-align: center
  - type: conditional
    conditions:
      - entity: sensor.sessy_xxxx_discharge_power
        state_not: '0'
    elements:
      - type: state-label
        prefix: 'Ontladen met: '
        entity: sensor.sessy_xxxx_discharge_power
        style:
          top: 83%
          left: 50%
          font-size: 175%
          text-align: center
  - type: conditional
    conditions:
      - entity: sensor.sessy_xxxx_charge_power
        state_not: '0'
    elements:
      - type: image
        entity: sensor.sessy_xxxx_charge_power
        image: /local/images/sessy/sessy-charging.png
        style:
          left: 14.7%
          top: 40.7%
          width: 10%
  - type: conditional
    conditions:
      - entity: sensor.sessy_xxxx_discharge_power
        state_not: '0'
    elements:
      - type: image
        entity: sensor.sessy_xxxx_discharge_power
        image: /local/images/sessy/sessy-discharging.png
        style:
          left: 11.5%
          top: 44%
          width: 10%
title: Sessy batterij status
image: /local/images/sessy/blank.png
type: picture-elements
```

