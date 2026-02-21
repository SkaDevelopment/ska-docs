# ⚙️Configuration

```lua title="Config.lua"
Config = {}

-- Density (0.0 to 1.0)
Config.pedFrequency = 0.0
Config.trafficFrequency = 0.0

-- 0.0 → No traffic / no peds
-- 0.1 – 0.5 → Reduced traffic / peds
-- 1.0 → Default GTA behavior


-- Global Behavior Flags
Config.DisablePolice = true
Config.DisableAmbulance = true
Config.DisableFiretrucks = true


-- Driving Behavior
Config.CruiseSpeed = 25.0 -- Speed in m/s
Config.DrivingStyle = 786603

-- 786603       Normal (Default)    Stops for lights, stays in lane, slows for turns, and avoids crashes. Very "legal."
-- 1074528293   Rushed              Will weave through traffic and overtake slow cars, but usually tries to avoid head-on crashes.
-- 2883621      Ignore Lights       Drives normally but completely ignores red lights and stop signs.
-- 6            Very Strict         Will not even overtake a parked car. It will wait forever if the path is blocked.
-- 524419       Semi-Aggressive     Good for "fast" traffic that still respects most rules but drives with urgency.
-- 16777216     Emergency           The style used by Police/Ambulance. They drive through anything to reach their goal.
```