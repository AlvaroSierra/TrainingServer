# ILS (LOC only)
This plugin makes aircraft follow the ILS very precisely.

Command and data must be in the following form:
```
ILS <RWY threshold lat> <RWY threshold long> <RWY course (precision is required, get from charts)> <Airport altitude> <Glide slope>
```

It's recommended to use a rewriter with this plugin so, during a session, the data for the specific ILS does not need to be inputted manually.

## Limitations
- Don't use angles greater than 90 degrees
- Command will fail if already passed the localizer
- Once the command is sent, it cannot be overridden (not even with an interrupt)
- If the traffic is too high, it will not descend on the glide slope but this will not be notified

## Possible issues
Once the traffic reaches the threshold, it should delete itself automatically. This might sometimes fail.

## Example

Example commands:
```
ILS 40.47350560 -3.53618004 322 2000 3.0
```

Maintainer: Alvaro (519820)

