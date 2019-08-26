Verify hardware:

https://docs.rust-embedded.org/discovery/03-setup/verify.html


Build Application:

https://docs.rust-embedded.org/discovery/05-led-roulette/index.html


Command to compile:

cargo build --target thumbv7em-none-eabihf

Open new terminal run these commands:

cd /tmp

openocd -f interface/stlink-v2.cfg -f target/stm32f3x.cfg

Open another new terminal and go to step01_rust_mcu_hello directory and run these commands:

arm-none-eabi-gdb -q target/thumbv7em-none-eabihf/debug/step01_rust_mcu_hello

It opens a gdb shell:

target remote :3333

load

Now debug it: https://docs.rust-embedded.org/discovery/05-led-roulette/debug-it.html

break main

continue




