# Auto-levelling

* Preheat everything

```
M851 Z0; reset Z offset to 0
M500; save to EEPROM
G28; auto-home sensor
G1 X110 Y110; bring nozzle to centre
```

* Move nozzle down to A4-paper height

```
G92 Z0; tell printer 'this is now Z0'
```

* Response is something like `Recv: Bed X: 110.00 Y: 110.00 Z: 2.02`. Subtract the Z-value from 0 for the next line

```
M851 Z-2.02; define offset
M500; save to EEPROM
```
