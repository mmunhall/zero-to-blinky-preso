## Hardware

#### Resistors

* orange - orange - brown - gold: 330
* brown - black - orange - gold: 1k
* brown - black - orange - gold: 10k  

#### Pins

1. Pin 11: Output
2. Pin 6: Ground
3. Pin 1: 3.3 DC power (use to test)

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

    gpio.setup(11, gpio.DIR_OUT, write);

    function write(state) {
        gpio.write(11, state, function(err) {
            if (err) throw err;
            setTimeout(write, 1000, !state);
        });
    }

## Execute script (sudo required)

    sudo node blinky.js
