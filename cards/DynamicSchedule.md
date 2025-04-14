# Sessy Dynamic Schedule with ApexCharts


Since ha-sessy 0.6.0 and Sessy firmware 1.6.5, Sessy's dynamic schedule and energy prices are visible within Home Assistant.

With the [ApexCharts custom card](https://github.com/RomRider/apexcharts-card?tab=readme-ov-file#installation) you can show this data in a graph.

![Dynamic schedule in a graph](DynamicSchedule.png)

# Card configuration
**Note**: Replace 'sessy_XXXX' in the examples below with the name of your own Sessy.

## Today
```yaml
type: custom:apexcharts-card
header:
  show: true
  title: Today
  show_states: true
  colorize_states: true
now:
  show: true
span:
  start: day
yaxis:
  - id: power
    decimals: 0
    opposite: true
  - id: price
    decimals: 2
series:
  - entity: sensor.sessy_XXXX_power_schedule
    yaxis_id: power
    name: Power Schedule
    type: column
    show:
      in_header: raw
    data_generator: |
      let hours = [];
      for(var i = 0; i < 24; i++){ hours.push(i); }
      let date = new Date().getTime();
      let dateindex = new Date(date).toISOString().split("T")[0];
      return hours.map((hour, index) => {
        let date = new Date(dateindex).setHours(hour,0,0);
        return [date, entity.attributes[dateindex][index]];
      });
  - entity: sensor.sessy_XXXX_energy_price
    yaxis_id: price
    name: Energy Price
    curve: stepline
    show:
      in_header: raw
    float_precision: 5
    data_generator: |
      let hours = [];
      for(var i = 0; i < 24; i++){ hours.push(i); }
      let date = new Date().getTime();
      let dateindex = new Date(date).toISOString().split("T")[0];
      return hours.map((hour, index) => {
        let date = new Date(dateindex).setHours(hour,0,0);
        return [date, entity.attributes[dateindex][index]];
      });
```

## Tomorrow
```yaml
type: custom:apexcharts-card
header:
  show: true
  title: Tomorrow
  show_states: false
span:
  start: day
  offset: +1d
yaxis:
  - id: power
    decimals: 0
    opposite: true
  - id: price
    decimals: 2
series:
  - entity: sensor.sessy_XXXX_power_schedule
    yaxis_id: power
    name: Power Schedule
    type: column
    data_generator: |
      let hours = [];
      for(var i = 0; i < 24; i++){ hours.push(i); }
      let date = new Date().getTime() + 86400000;
      let dateindex = new Date(date).toISOString().split("T")[0];
      return hours.map((hour, index) => {
        let date = new Date(dateindex).setHours(hour,0,0);
        return [date, entity.attributes[dateindex][index]];
      });
  - entity: sensor.sessy_XXXX_energy_price
    yaxis_id: price
    name: Energy Price
    curve: stepline
    float_precision: 5
    data_generator: |
      let hours = [];
      for(var i = 0; i < 24; i++){ hours.push(i); }
      let date = new Date().getTime() + 86400000;
      let dateindex = new Date(date).toISOString().split("T")[0];
      return hours.map((hour, index) => {
        let date = new Date(dateindex).setHours(hour,0,0);
        return [date, entity.attributes[dateindex][index]];
      });
```
