# SIO2BSD
SIO emulation by Drac030 (http://drac030.krap.pl/). This is my fork of TheMontezuma's 1.19 SIO2BSD code (https://github.com/TheMontezuma/SIO2BSD).

# Description
Atari 8 bit Floppy (SIO) emulation.

At the moment, I've not really changed TheMontezuma's 1.19 code that much (no new functionality).

# Options

```
$ ./sio2bsd -h

SIO2BSD 1.1.21, (c) 2017 by KMK/DLT/NJC

sio2bsd [opts] [-f] drive [-f] drive ...

Where 'opts' are:
-m        - use COMMAND line
-l        - extended log messages
-s fname  - serial device ("/dev/rfcomm0" by default)
-b n      - set turbo to 19200*n (n<8)
-d n      - additional delay required for Bluetooth communication
-p fname  - printer file
-t        - enable ATASCII->ASCII translation for printer
-u        - accept uppercase characters only in PCLink dirs
-8        - block PERCOM commands

-f drive  - first 3 sectors of new formatted DD disk have full size in ATR

and 'drive' can be one of the following:

ATR file  - the image file will be mounted for sector I/O
directory - the directory will be mounted as PCLink drive
-         - none, this drive will remain unassinged

Number of drives (ATR or PCLink) is limited to 16.

Options enbled by -b 0 (custom turbo speed):
-i n      - set HSINDEX to n
-q hz     - set accurate POKEY frequency to hz
            "pal" set 1773447.0 Hz
            "ntsc" set 1789790.0 Hz
            "ntscf" set 1789772.5 Hz as of FREDDY NTSC machines
            by default average PAL/NTSC frequency (1781618.500 Hz) is using
-c x      - set POKEY nonlinearity constant to x (7.186100 is being used by default)

-h        - help
-?        - help
```

# Links
* http://drac030.krap.pl/
* https://github.com/TheMontezuma/SIO2BSD
* http://ushomeautomation.com/Projects/Atari/sio2pi.html

# License
GPL 2