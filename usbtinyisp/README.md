# Prepare ISP programmer

Connect attiny85 to socket and usbtiny v2.0

Set jumper in USB PWR

## Check connection with lsusb
~~~
$ lsusb
...
Bus 001 Device 007: ID 1781:0c9f Multiple Vendors USBtiny
...
~~~

![usbtiny](<isp.jpg>)

## Check ISP programmer

~~~
$ sudo avrdude -c usbtiny -p t85

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.00s

avrdude: Device signature = 0x1e930b (probably t85)

avrdude: safemode: Fuses OK (E:FF, H:DF, L:62)

avrdude done.  Thank you.
~~~

