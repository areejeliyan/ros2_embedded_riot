ROS 2 embedded prototype on Riot:
---------------------------------

### Building:
```bash
cd examples/hello-world/
make BOARD=stm32f4discovery
```

### Building + flashing:
```bash
cd examples/hello-world/
make flash BOARD=stm32f4discovery
```

### Debugging:
Launch the server:
```bash
cd examples/hello-world
st-util -v
```
Launch the client
```bash
cd examples/hello-world
arm-none-eabi-gdb -tui bin/stm32f4discovery/hello-world.elf -ex 'target remote localhost:4242'
```
