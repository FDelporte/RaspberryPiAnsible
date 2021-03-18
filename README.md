# Raspberry Pi Ansible scripts

A few ansible scripts to configure a new Raspberry Pi.

## Prerequisites

1. Prepare an SD card with the [Raspberry Pi Imager tool](https://www.raspberrypi.org/software/) 
   and select **"Raspberry Pi OS (32-bit)"**. This is a "minimal" desktop version, and we will 
   install all extra tools needed with one of the provided scripts in this repository.
   * When you want to create a **"kiosk mode" JavaFX application** which only shows the JavaFX application, 
    and no other desktop please select **"Raspberry Pi OS (32-bit)" > "Raspberry Pi OS Lite (32-bit)"**.

![Screenshot of the Raspberry Pi Imager tool](docs/imager.png)

2. When the SD card is ready, put it in your Raspberry Pi, power it and follow the on-screen 
   step-by-step to select your language, configure Wifi, install updates, etc.
   
## Use Ansible to install additional tools

There are two possible approaches to use Ansible to install extra tools.

### Run the Ansible scripts on another PC 

3. In the terminal, run `sudo raspi-config`, go to ???, and enable SSH.

4. On your PC, execute one of the provided scripts with
    `?`.
   
### Run the Ansible scripts on the Raspberry Pi itself

3. Open a terminal and run the following commands to install the Ansible tool and download this project.

```
$ sudo apt update
$ sudo apt install -y ansible sshpass
$ git clone https://github.com/FDelporte/RaspberryPiAnsible.git
$ cd RaspberryPiAnsible
```

4. You are now inside this project and can execute one of the provided scripts with 
   `???`.

## Run the ansible scripts

This project provides multiple scripts, depending on the work you want to do. Run one or more
of these scripts.

| Script            | Java      | JavaFX    | Maven     | VSC       | Extra                 |
| :---              | :---:     | :---:     | :---:     | :---:     | :---                  |
| javafx.yml        | Yes       | Yes       | Yes       | Yes       |                       |
| javafx-kiosk.yml  | Yes       | Yes       | Yes       | -         | X11 for kiosk mode    |



