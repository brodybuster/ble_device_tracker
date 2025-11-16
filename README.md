Home Assistant Blueprint that utilizes Virtual Devices (for persistant virtual device trackers)and ESPresence to provide a GPS based device tracking entity.

Blueprint utilizes an "exit node" through which all tracked devices need to pass through before being marked away. This avoids false not_home states when a bluetooth device goes down for longer than the away_timeout. 

A typical BLE to Device Tracker automation will mark a device not_home once ESPresence no longer detects a device, despite the fact the device may not have left home, ie due to dead battery, etc.

Blueprint leverages an input toggle and helper timer to determine of a device is actual not_home. 
