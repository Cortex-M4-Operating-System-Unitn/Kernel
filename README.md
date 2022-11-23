# PiOS Kernel

## Project structure

- The kernel source code lives in the [kernel](kernel) folder.
- The [test_app](test_app) contains an application to run tests on qemu.
- The [build](build) folder is used to build PiOS as a static library (more on that in the next section).

## Building the kernel

Pios is provided as a static library, issue the following commands to build it (assuming you are currently in the root directory of the project):
```
$ cd build
$ cargo build --release
$ cp target/thumbv7em-none-eabi/release/libpios.a ..
$ cd ..
```

In the root directory you should now have a `libpios.a` file.

## Testing

All unit and integration tests are run on a qemu virtual machine. 