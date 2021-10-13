## Embedded Virtual Machine Drivers

The `embvm-drivers` organization contains device driver implementations that are designed to work with the [Embedded VM framework](https://github.com/embvm) (`embvm`). They are kept in a separate organization to avoid cluttering the primary repository set.

## New Driver Development

If you are developing a driver for the `embvm` framework, start with our [driver-repository-template](https://github.com/embvm-drivers/driver-repository-template).

## State

Many of the drivers shown here are either proofs-of-concept or under active development. We do not recommend relying on them for development at this time. However, they may serve as useful examples for your own portable driver development efforts.

- [ST-VL53L1X](https://github.com/embvm-drivers/ST-VL53L1X) (Time of Flight sensor)
  - Functional, can be configured for all supported ranging modes and reads samples in an asynchronous manner. Will be redesigned to avoid asynchronous callback hell.
- [sensirion-sps-30](https://github.com/embvm-drivers/sensirion-sps-30) (particulate matter sensor)
  - Under development
- [aardvark](https://github.com/embvm-drivers/aardvark) (USB-to-I2C/SPI/GPIO)
  - I2C is supported and used by example projects
  - GPIO is supported and used by example projects
  - SPI is implemented but not tested
- [two-tone-oled](https://github.com/embvm-drivers/two-tone-oled) (OLED driver, currently targeting SSD1306)
  - functional, used by embvm examples
  - driver will be refactored to remove drawing functionality that should instead be kept in a standalone library
  - driver will be redesigned to avoid asynchronous callback hell, reduce the number of transfers to be queued on intiailizlation, and to imrpove system memory usage (primarily by reducing transfers)
  
