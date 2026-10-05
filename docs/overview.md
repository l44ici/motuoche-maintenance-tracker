# Overview

## What it is
A maintenance tracking app for motorcyclists. It tracks each component on the bike and flags when something needs a check, so riders know what to pay attention to before small issues become bigger ones.

This is not a diagnostic tool. It doesn't predict component lifespans or replace a professional mechanic. It's a simple tracker for routine maintenance.

## The problem
Riders have no easy way to know which parts of their bike need a look, so small issues get missed until they turn into bigger ones.

## What it does
- Tracks each component separately, including engine oil, brakes, tyres, spark plugs, and valve clearances
- Adapts to the bike's drive system (chain, belt, or shaft)
- Flags when something needs a check, based on distance ridden, time since the last service, and the manufacturer's recommended intervals
- Handles second-hand bikes by asking for the current odometer reading and any known service history at setup
- Sends a notification before things get bad, not after
- Lets riders log a check or service so the tracker resets
- Provides a simple parts catalogue so riders know what to buy
- Exports the full service history as a PDF
- Works offline, so it's usable in the garage with no Wi-Fi

## What it doesn't do
- Diagnose faults or predict component lifespans
- Cover every part on the bike (fuel pumps, sensors, and ignition leads are out of scope)
- Book mechanics or sell parts
- Track rides
- Support multiple bikes in V1 (planned for a future version)

Keeping the scope focused means building something that works really well, rather than something that tries to do everything.

## Objectives
Every feature connects back to at least one of these.

**1. Show what needs attention at a glance**
The main screen makes it immediately clear which components are fine and which need a look.
*Working when:* users understand what to do without any explanation.

**2. Send reminders before things become a problem**
Most people won't open the app daily, so notifications reach out when a component is getting close, not after it's overdue.
*Working when:* users act on notifications rather than dismissing them.

**3. Make logging quick**
If logging takes more than 30 seconds, people stop doing it.
*Working when:* checks are logged regularly, not just once at setup.

**4. Work reliably, including offline**
In the garage, on the road, anywhere, with or without a connection.
*Working when:* core features work with no internet.

## Target users
**Casual motorcyclist**
Rides for fun or to commute, with little to no mechanical knowledge. Wants to know when to take the bike to a shop. Needs almost no setup.

**Semi-serious rider**
Rides regularly and does their own basic servicing. Wants a clear record of what's been done and when.

Both share the same core need. If scope has to narrow, the casual motorcyclist comes first, since they have the least existing system to fall back on.
