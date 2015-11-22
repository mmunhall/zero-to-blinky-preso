## Create directory

    cd
    mkdir blinky
    cd blinky

## Intialize project

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
