# orange pi zero hx711

## source

```txt
https://opi-gpio.readthedocs.io/en/latest/api-documentation.html
```

## install

``` bash
git clone https://github.com/tatobari/hx711py

git clone  https://github.com/Jeremie-C/OrangePi.GPIO

cd /OrangePi.GPIO

sudo pip install OrangePi.GPIO

# copy hx711.py and example.py to ~/OrangePi.GPIO
cp ../hx711py/example.py example/
cp ../hx711py/hx711.py example/

```

## adapt this this for orange pi zero

- replace < line with the > line. 
- Think on the tab wide it is python

```bash
example.py

< hx = HX711(5, 6)
> hx = HX711(7, 3)

hx711.py
< import RPi.GPIO as GPIO
> import OPi.GPIO as GPIO
< GPIO.setmode(GPIO.BCM)

> GPIO.setboard(GPIO.ZERO)
> GPIO.setmode(GPIO.BOARD)
```

## cable connect on the opi zero double connector

```txt
opi zero ####################### hx711
PIN 1 Vcc 3,3 V ---------------- PIN 1 VCC
PIN 9 GND ---------------------- PIN 4 GND
PIN 3 SCK ---------------------- PIN 2 SCK
PIN 7 DT  ---------------------- PIN 3 DT
```
