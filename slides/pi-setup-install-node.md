##  Pi Setup - Install Node

    curl -sLS https://apt.adafruit.com/add | sudo bash
    sudo apt-get install node
    node -v

note:
- We'll use Node to interact with the GPIO pins.
- Using the package manager will give us old versions of Node and npm that don't work with the rpi-gpio library required to interact with GPIO.
- Adafruit has a package repository with current versions of Node.
- Add Adafruit's package repo to our sources list, then apt-get install node.
    - Installs node 0.12.?.
