# Controller Tester

Code for manually testing each of the components connected to the equipment controller. 

The Arduino serial port configuration is:
9600 baud 8N1

# Arduino Port-to-Equipment Mapping
The ports on the Arduino for controlling the equipment relays are mapped as follows:

| Benchtop Equipment | Arduino Pin |
| -------------------|-------------|
| Main Incubator     | A1          | 
| UV Transilluminator| A2          |
| Overhead Lighting  | D2          |
| Shaker             | D3          |
| Electrophoresis    | D4          |
| Centrifuge         | D5          |
| WL Transilluminator| D6          |
| Shaker Incubator   | D7          |


When the test script is initialized, the equipment relays have the following state:

| Benchtop Equipment | Initial State|
| -------------------|--------------|
| Main Incubator     | On           | 
| UV Transilluminator| Off          |
| Overhead Lighting  | On           |
| Shaker             | Off          |
| Electrophoresis    | Off          |
| Centrifuge         | Off          |
| WL Transilluminator| Off          |
| Shaker Incubator   | On           |


The keyboard commands to turn each of the equipment relays on and off are as follows:

| Benchtop Equipment | On  | Off |
| -------------------|-----|-----|
| Main Incubator     | 'E' | 'F' | 
| UV Transilluminator| '1' | '0' |
| Overhead Lighting  | '4' | '3' |
| Shaker             | '7' | '8' |
| Electrophoresis    | '9' | 'A' |
| Centrifuge         | '5' | '6' |
| WL Transilluminator| 'B' | 'C' |
| Shaker Incubator   | 'G' | 'H' |


The `Enter` Key (or newline character) does not need to be pressed for a command to take effect,
however, if using the Arduino IDE for serial port communication, the `Enter` Key needs to be
pressed for a command to be sent.
When a command has been received by the Arduino, it will be echoed on the terminal to indicate
receipt of the command.
