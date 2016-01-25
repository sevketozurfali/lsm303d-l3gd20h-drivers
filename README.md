LSM303D / L3GD20H I2C Drivers
=============================

Raspberry Pi Installation
-------------------------

Compile the drivers and install the device tree overlay to the
`/boot/overlays` folder:

```
  sudo make
  cd board
  sudo make install
```

Insert the drivers:

```
  sudo insmod lsm303d/lsm303d.ko
  sudo insmod l3gd20h/l3gd20h.ko
```

Conversion Tables
-----------------

Accelerometer (g) | mg/LSB | Magnetometer (gauss) | mgauss/LSB | Gyroscope (dps) | mdps/LSB
------------------|--------|----------------------|------------|-----------------|---------
2                 | 0.061  | 2                    | 0.080      | 245             | 8.75
4                 | 0.122  | 4                    | 0.160      | 500             | 17.50
6                 | 0.183  | 8                    | 0.320      | 2000            | 70.00
8                 | 0.244  | 12                   | 0.479      |                 |
16                | 0.732  |                      |            |                 |

Resources
---------

- [L3GD20H
  Datasheet](https://www.pololu.com/file/download/L3GD20H.pdf?file_id=0J731)
- [LSM303D
  Datasheet](https://www.pololu.com/file/download/LSM303D.pdf?file_id=0J703)
- [Raspberry Pi Device
  Tree](https://www.raspberrypi.org/documentation/configuration/device-tree.md)
