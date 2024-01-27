# Midea fan-coil (and clones) ESPHome

The Midea fan-coil with PQE ports and clones like [Concept]([https://www.airwell.com/en/](https://gepesz.hu/shop/list.php?menu=151)) can be managed using the Modbus protocol. This project contains configuration file(s) which can be placed on an ESPHome enabled device to communicatie using modbus with the heat pump.

<span style="color: red;">**See below for a ready-made ESPHome compatible heatpump controller!!**</span>

![MKG C magasoldalfali fan-coil](https://github.com/Yocee84/Midea-fan-coil-ESPHome/assets/25384303/fbb1c6ea-7d2e-437e-84d8-ef4f1cf0a02c)

## Disclaimer

The information provided for the heat pump is intended for informational purposes only. Its use is entirely at your own risk. We do not take any responsibility for any damage or loss caused by the use of information taken from this project. We strongly recommend that you consult with a professional HVAC technician before making any changes to your heat pump configuration or installation. By using the information from this project, you acknowledge that you understand and accept these terms and conditions.

## Connect a ESPHome board to the Fan-coil

Connecting a device to the fan-coil is not that difficult, but keep the disclaimer in mind. Before you start, disconnect the power from the indoor and the outdoor unit. Never ever open up the Fan-coil with the power switched on!!

A modbus device has two wires, A+ and B- and optional a ground/earth connection. The modbus device needs to be connected to the Fan-Coil P+ Q- ports.



Detach the front panel of the indoor unit. Remove the motherboard. Check the output of the PQE port. If it is not connected, change it to the XYE port.

Connect the B- wire to P and A+ wire to Q.

![v400c](https://github.com/Yocee84/Midea-fan-coil-ESPHome/assets/25384303/19c5e2d6-1955-43c0-a6c0-93d7af01596e)


When all is connected, place the back panel of the display back and put back the front panel of the indoor unit.

## Configuration

Place the content of the file [heatpump.yaml](heatpump.yaml) in your ESPHome device and change the `uart` and `modbus_controller` settings to your needs. The `substitutions` section can be used to change the entities name as they apear in Home Assistant. In the [homeassistant](homeassistant) directory I placed and example dashboard and some example automations.



## ESPHome Midea Fan-Coil Controller

## Recommend hardwares
ESP32 CAN RS-485 IOT Engineer Control Module Development Board (flow pin configuration needed)

https://www.lilygo.cc/products/t-can485?_pos=2&_psq=can&_ss=e&_v=1.0

![can](https://github.com/Yocee84/Midea-fan-coil-ESPHome/assets/25384303/f0896d90-d77a-4e7c-b378-1d2515739950)


TTL Turn To RS485 Module Hardware Automatic Flow Control Module Serial UART Level Mutual Conversion Power Supply Module 3.3V 5V
https://www.aliexpress.us/item/3256801435432059.html?spm=a2g0o.productlist.main.27.ec3f80ac9IUXPE&algo_pvid=0b522372-88c7-4f9f-abeb-51e34648b090&algo_exp_id=0b522372-88c7-4f9f-abeb-51e34648b090-13&pdp_npi=4%40dis%21USD%210.89%210.89%21%21%210.89%210.89%21%40210318c317063686265568100e4c4f%2112000016846569467%21sea%21US%21179588603%21&curPageLogUid=1w8lmMdR0LFo&utparam-url=scene%3Asearch%7Cquery_from%3A
![modbus module for esp](https://github.com/Yocee84/Midea-fan-coil-ESPHome/assets/25384303/0999f556-3c4e-4fd8-bbf7-0336394146b1)

You also need an esp32 panel for this panel. I use the ESP32 CAM module because I like it. If you would also use an external antenna, don't forget to order one or solder the motherboard resistor!

![esp32cam](https://github.com/Yocee84/Midea-fan-coil-ESPHome/assets/25384303/21a3f0a5-2018-467a-915a-648a37cdd79c)


https://www.aliexpress.us/item/3256806113048872.html?spm=a2g0o.productlist.main.1.4f0f3f77mU2rK9&algo_pvid=f52fcef5-90a0-47e2-accd-f82f7b8fed2d&aem_p4p_detail=202401270720294150456483594760001656668&algo_exp_id=f52fcef5-90a0-47e2-accd-f82f7b8fed2d-0&pdp_npi=4%40dis%21USD%2113.97%214.59%21%21%2199.83%2132.75%21%40210307c117063688290714222eac11%2112000036671494991%21sea%21US%21179588603%21&curPageLogUid=ZKY13LM54o7m&utparam-url=scene%3Asearch%7Cquery_from%3A&search_p4p_id=202401270720294150456483594760001656668_1

![modbus module for esp](https://github.com/Yocee84/Midea-fan-coil-ESPHome/assets/25384303/641a1ecb-0852-434d-b7da-dbb5fcab5a29)




