# gentoo-utils

### timezone.eselect
This is an eselect module that sets the timezone via `/etc/timezone`.
Sample usage:
To list available timezones form `/usr/share/zoneinfo`
```sh
$ eselect timezone list
Directory: /usr/share/zoneinfo
  [1]   Africa/
  [2]   America/
  [3]   Antarctica/
  [4]   Arctic/
  [5]   Asia/
  [6]   Atlantic/
  // collapsed //
  [61]  W-SU
  [62]  Zulu
```
and timezones from a directory within `/usr/share/zoneinfo`:
```sh
$ eselect timezone list 6
Available timezone selections:
Directory: /usr/share/zoneinfo/Atlantic
  [6-1] Azores
  [6-2] Bermuda
  [6-3] Canary
  [6-4] Cape_Verde
  [6-5] Faeroe
  [6-6] Faroe
  [6-7] Jan_Mayen
  [6-8] Madeira
  [6-9] Reykjavik
  [6-10]South_Georgia
  [6-11]Stanley
  [6-12]St_Helena
```
And to set a timezone:
```sh
# eselect timezone set 6-9
Configuring pkg...

 * Updating /etc/localtime with /usr/share/zoneinfo/Atlantic/Reykjavik
```
String literal also works: `eselect timezone set Atlantic/Reykjavik`
