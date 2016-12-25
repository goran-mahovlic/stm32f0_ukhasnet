# README

### Pre-requisites
#### Hardware
First options:
* STM32F103C8T6 developed board (bluepill)
* RFM69HW/W on a Breakout board
* USB/Serial for Debuging
* STlink or Black magic probe

#### Software
* arm-none-eabi-gcc (on OSX you can use homebrew and https://github.com/ARMmbed/homebrew-formulae)
* stlink (https://github.com/texane/stlink)

### Install
1. git clone https://github.com/goran-mahovlic/stm32f0_ukhasnet.git
2. cd stm32f0_ukhasnet
3. mv src/settings-example.h src/settings.h   <<  edit your settings to suit your node
4. git submodule init
5. git submodule update
6. cd libopencm3/
7. make
8. cd..
9. cd src/
10. sh build.sh
11. cd..
12. sh flash.sh

## Board connections

| Port  | Function      | Description                       |
| ----- | ------------- | --------------------------------- |
| `PB6` | `(USART1_TX)` | TTL serial output `(38400,8,N,1)` |
| `PA4` | `(SPI_SS)`    | SPI SS (also know as CSS)         |
| `PA7` | `(SPI_MOSI)`  | SPI MOSI                          |
| `PA6` | `(SPI_MISO)`  | SPI MISO                          |
| `PA5` | `(SPI_SCK)`   | SPI SCK                           |
| `PA9` | `(LED)`       | LED                               |
|`PC13` | `(LED)`       | onboard LED                       |
  
