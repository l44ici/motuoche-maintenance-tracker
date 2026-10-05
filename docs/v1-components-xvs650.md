# Components: Yamaha XVS650

## The bike
Yamaha XVS650 (V-Star 650) Custom. Shaft drive, carburetted, air-cooled. This is the confirmed bike for V1, and this table is the data the app ships with. Every interval is verified against the factory owner's manual periodic maintenance chart (pages 6-2 to 6-4).

This format also serves as the template for adding other bikes later.

## Maintenance schedule

| Component | Trigger type | Interval | Notes |
|---|---|---|---|
| Engine oil | Distance or time | 6,000 km or 6 months | Base service interval |
| Oil filter element | Every Nth service | Every 2nd oil change | |
| Spark plugs | Distance or time | Check and clean each service, replace as needed | |
| Air filter | Condition modified | Each service, sooner if wet or dusty | |
| Fuel line | Distance or time | 6,000 km or 6 months | Dealer |
| Valve clearance | Distance or time | 6,000 km or 6 months (check) | Dealer, special tools |
| Final gear (shaft) oil | Distance or time | Initial 1,000 km, then 24,000 km or 24 months | |
| Front fork (oil and seals) | Inspect at service | Each service | Dealer. Check for leaks, no scheduled oil change |
| Front / rear brakes | Inspect at service | Each service | Dealer |
| Brake fluid seals | Time only | Every 2 years | Odometer never triggers |
| Brake hoses | Time only | Every 4 years | Odometer never triggers |
| Wheel bearings, tyres, wheels | Inspect at service | Each service | |
| Brake rotors | Inspect at service | Each service | Checked with brakes |
| Steering / swingarm bearings | Distance or time | Re-grease every 24,000 km or 24 months | |
| Carburettor sync and idle | Inspect at service | Each service | Per-model item |

Items needing special tools are flagged as dealer jobs rather than DIY reminders.

The manual has two interval columns (6,000 km / 6 months and 12,000 km / 12 months). This table uses the 6,000 km cycle, with some items like the oil filter falling on the 12,000 km cycle.

## Why model profiles override defaults
The XVS650 has no chain and no coolant, and its shaft oil interval is about five times longer than the old generic default. A model profile replaces the generic drive-type and cooling defaults entirely rather than layering on top of them.

Generic chain and belt defaults are kept for future multi-bike support but aren't needed for V1.

## Out of scope
Not tracked in V1. These either need specialist diagnosis, vary too much between models, or fall outside core maintenance.

- Fuel pump
- Sensors and electronics
- Ignition leads
- Clutch (mechanical check, not a core wear item)
- Chassis fasteners (no measurable interval to track)
- Sidestand and sidestand switch (low failure risk)
