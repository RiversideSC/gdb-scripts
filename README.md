# folder structure
## armv8m
Scripts for armv8m register value friendly display.
### Example output - MPU
```
start mpu register print

MPU Control Register
-- 0xe000ed94:	0x00000005
  |- 1 privileged default enable
  |- 0 hardfault nmi enable
  |- 1 enable

MPU Type Register
-- 0xe000ed90:	0x00000800
  |- 8 regions

MPU Memory Attribute Indirection Register 0
0xe000edc0:	0x00000444
MPU Memory Attribute Indirection Register 1
0xe000edc4:	0x00000000
  |- 7    | 6    | 5    | 4    | 3    | 2    | 1    | 0    |
  |- 0x00 | 0x00 | 0x00 | 0x00 | 0x00 | 0x00 | 0x04 | 0x44 |

MPU Memory Region Base Address Register
--|- region | address     | not shareable | outer shareable | inner shareable | R/W privileged only | R/W any privilege | Read only privileged only | Read only any privilege | execute not permitted |
  |-  0     | 0x00000000  | 1             | 0               | 0               | 0                   | 0                 | 1                         | 0                       | 0                     |
  |-  1     | 0x20000000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 1                     |
  |-  2     | 0x40140000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 1                     |
  |-  3     | 0x00000000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 0                     |
  |-  4     | 0x00000000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 0                     |
  |-  5     | 0x00000000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 0                     |
  |-  6     | 0x00000000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 0                     |
  |-  7     | 0x00000000  | 1             | 0               | 0               | 1                   | 0                 | 0                         | 0                       | 0                     |

MPU Memory Region Limit Address Register
--|- region | limit address | execution only permitted if read permitted | execution from a privileged mode is not permitted | attr index | region enabled |
  |-  0     | 0x0fffffff    | 1                                          | 0                                                 | 0          | 1              |
  |-  1     | 0x2fffffff    | 1                                          | 0                                                 | 0          | 1              |
  |-  2     | 0x40143fff    | 1                                          | 0                                                 | 0          | 1              |
  |-  3     | 0x0000001f    | 1                                          | 0                                                 | 0          | 0              |
  |-  4     | 0x0000001f    | 1                                          | 0                                                 | 0          | 0              |
  |-  5     | 0x0000001f    | 1                                          | 0                                                 | 0          | 0              |
  |-  6     | 0x0000001f    | 1                                          | 0                                                 | 0          | 0              |
  |-  7     | 0x0000001f    | 1                                          | 0                                                 | 0          | 0              |
```
## tf-m
Scripts for trusted-firmware-m important variable/object display.
