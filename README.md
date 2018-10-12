# AVR-Toolbox

A repo containing tips and tricks for AVR development

## MacOS installation

### Removing CrossPack-AVR

CrossPack-AVR seems pretty cool from the outside with its convenient installer but is really outdated. The bundled `avrdude` and `avr-libc` are several versions behind the latest release. Plus, USB communication doesn't seem to work really well. Here's how to uninstall it:

1) Open `Terminal` then enter `cd /usr/local/`
2) List every CrossPack folder with `ls | grep CrossPack`
3) For each folder named `CrossPack-AVR-*`
    1) `cd <folder-name>`
    2) `./uninstall`
    3) Follow on-screen instructions

### Installing [Homebrew](https://brew.sh) (`brew`)

`brew` is the unofficial package manager for MacOS. We will use it to install the latest version of the avr toolchain.

1) Install `brew` by pasting the following command in the terminal : `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
2) Follow on screen instructions

### Installing the AVR Toolchain

In `Terminal`, run the following commands:
1) `brew tap osx-cross/avr`
2) `brew install avr-binutils avr-gcc avr-gdb avrdude`
3) Let cook in the oven at 350°F for 30 minutes _(step 2. will take some time and will make your mac heat up a bit)_
4) Verify installation with `avrdude --version` and `avr-gcc --version`