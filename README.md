# ESPHome VL6180X

ESPHome external component for the VL6180X time-of-flight distance and ambient light sensor.

Based on the `vl6180x` component by [@NonaSuomy](https://github.com/NonaSuomy) and
[@k-korn](https://github.com/k-korn), from
[NonaSuomy/esphome, branch `vl6180x-pololu-scaler`](https://github.com/NonaSuomy/esphome/tree/vl6180x-pololu-scaler/esphome/components/vl6180x)
at commit `89944f7`.

## Usage

```yaml
external_components:
  - source: github://mikulik86/esphome-vl6180x@main
    components: [ vl6180x ]

sensor:
  - platform: vl6180x
    address: 0x29
    update_interval: 1s
    distance:
      name: "Distance"
      scaler: 1 # 1, 2 or 3
```

See [`components/vl6180x/vl6180x_sensor.yml`](components/vl6180x/vl6180x_sensor.yml) for a longer example.

## License

Like ESPHome, which this component comes from: the C++ code is published under the GPLv3 and the
Python code under the MIT license. See [LICENSE](LICENSE).
