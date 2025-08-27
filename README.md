<div align="center">
	<h1>Endgame Custom Firmware</h1>
    <a href="https://github.com/Gael-Lopes-Da-Silva/endgame-firmware">https://github.com/Gael-Lopes-Da-Silva/endgame-firmware</a>
</div>

## Description

This is my custom vial firmware for my build of the Endgame keyboard.

I changed the layout to fix a key selection issue and added the HOLD_ON_OTHER_KEY_PRESS option in the config. See more about this option in the qmk documentation.

## Usage

It really depends on your micro controller. Generally, what you will want to do is, to boot in the micro controller bootloader. This will let you access it's storage. Then copy and paste the uf2 file in it and it should close.

But again, it really depends on the micro controller used and it may be different for yours (I use a RP2040-zero for my build).

## Build From Source

Start by cloning the vial-qmk repository.

```shell
git clone https://github.com/vial-kb/vial-qmk
```

After that, clone this repository into the `keyboards` folder in the vial-qmk folder.

```shell
cd vial-qmk/keyboards
git clone https://github.com/Gael-Lopes-Da-Silva/endgame-firmware endgame
```

Then compile it as following.

```shell
make endgame:default
# or
make endgame:default:flash
```

You will find the build in the `.build` folder.
