# LCP

Safely copy and organize data from multiple recording units and/or devices in a project.

lcp creates a folder structure named `[date]_[location]/[unit]_[device]/[card number] in the target directory, copies all files from the source to every specified target simultaneously and finally checks if the files have been transferred completely.

## Usage

```
lcp [-f] [-a adjustment_in_days] [-l location_name] [-u unit_name] [-d device_name] [-o cardnumber_overwrite] source target [target2 …]
```

##### -a [signed integer]
Adjust the date used for the main folder. E.g. -1 uses yesterdays date, 1 copies stuff to tomorrow.

##### -d [string]
Specify the device used. E.g. Alexa, Sequoia, KitchenAid…

##### -f
Force lcp to skip the final transfer check.

##### -l [string]
Specify the location. Can also be used for project name. E.g. Düsseldorf, StudioA, Moms_Livingroom

##### -o [string]
Overwrite the card number. If nothing is specified, lcp will start with 001 and increment the card number if more files are copied with the same date/location/unit/device combination.

##### -u [string]
Specify the unit. E.g. ENG, Jib, Sound…

Location, Unit and Device are required. lcp will ask for them if they are not specified in arguments.

## Example

```
lcp -l Churyumov–Gerasimenko -u Philae -d SESAME -a -3 /Volumes/CF_CARD /Volumes/BackupDisk1 /Volumes/BackupDisk2 /Volumes/BackupDisk3
```

## License (MIT)

Copyright © 2016 Simon Schwär

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
