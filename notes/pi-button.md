## Hardware

#### Resistors

* orange - orange - brown - gold: 330
* brown - black - orange - gold: 1k
* brown - black - orange - gold: 10k  

#### Pins

1. Pin 1: 3.3 DC power
2. Pin 12: Input
3. Pin 6: Ground

## Create directory

    cd
    mkdir blinky
    cd blinky

## Initialize project

    npm init

## Install dependency

    npm install rpi-gpio --save-dev

-or-

    npm link rpi-gpio

## Create empty script

    touch index.js

## Write code
    var gpio = require('rpi-gpio');

    gpio.setup(12, gpio.DIR_IN, read);

    function write(state) {
        gpio.read(12, function(err, val) {
            if (err) throw err;
            console.log("Button pressed: " + val);
            setTimeout(read, 250);
        });
    }

## Execute script (sudo required)

    sudo node blinky.js
