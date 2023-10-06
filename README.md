# Experimenty s jednocipy a elektronikou

## Articles

### [Unbricking Seeed Studio Xiao BLE / Arduino Nano 33 BLE](/unbrick_xiao_ble/)

As the Xiao BLE devel board is only having native USB used also for the programming it's quite easy to brick a whole module. The same applies for the Adruino Nano 33 BLE. The only way how to unbrick it is using debug pins SWDIO/SWDCLK.

[Whole article](/unbrick_xiao_ble/)

### [Repositories](https://github.com/kiiv-cz)

* [Atmel experiments](https://github.com/kiiv-cz/atmel_projects) Atmel studio, experiments with CCL, RTC, events (Tiny416/212, Atmega4809, AVR128DB48, ...)
* https://github.com/kiiv-cz/MicroBitRadio_mbedos Mbed OS occupies RADIO ISR (for BLE), so here I'm using another thread to handle events without ISR. TODO: redirect events through SW interrupts if the faster communication is needed.

### [Logitronik 02 manual CZ (pdf)](/logitronik_02.pdf)

