# Status System

## Statuses
Statuses are calculated from real data, never guessed. If any component is overdue, the whole bike is treated as needing attention.

| Status | Meaning |
|---|---|
| OK | All good. No action needed. |
| Due soon | Getting close. Worth a check. |
| Overdue | Needs attention now. |
| Unverified | No known service history. Treated the same as Overdue, since it's safer to assume a check is needed. |

The rider can also mark a component with one of two manual states:

| State | Meaning |
|---|---|
| Flagged | Rider spotted something and is inspecting it. |
| Under service | Bike is currently being serviced. |

## How status is calculated
Status is worked out from three things:
- Distance ridden since the last check
- Time since the last check
- The manufacturer's recommended interval for that component on that model

The app takes whichever signal is most urgent.

## Trigger types
Every component has a trigger type that decides when it's due. This is the core of the notification engine.

- **Distance or time** (most common): fires on whichever comes first. Example: engine oil every 6,000 km or 6 months.
- **Time only**: fires on a calendar interval and ignores the odometer. Example: brake fluid seals every 2 years.
- **Every Nth service**: fires on a count of completed services. Example: oil filter every second oil change.
- **Inspect at service**: rides along with the next scheduled service. Example: tyres and brakes at each service.
- **Condition modified**: a base interval that shortens under certain conditions. Example: air filter serviced sooner in wet or dusty riding.

## Setup flow
Setup is a short multi-step flow rather than one long form, following the same low-friction principle as logging.

### Step 1: Bike and riding basics
Confirms the bike, current odometer reading, and ride frequency (low, average, or high use). Also records the setup date, used as the baseline for new bikes with no prior history.

### Step 2: New or second-hand
- **New bike:** all components start from a clean baseline. One extra question: whether the first oil change (if done) included a filter change, so the oil filter's service count starts from a known point.
- **Second-hand bike:** the rider is asked whether they know the service history. If not, every component is marked unverified and setup skips to Step 4. If yes, they continue to Step 3.

### Step 3: Service history (second-hand only)
Each item is a quick yes/skip choice. Nothing is required, and anything skipped is marked unverified.
- **Last full service date**, used by Inspect at service components
- **Last replacement dates for brake fluid seals and brake hoses**, asked separately since they're time-only
- **Last known date and odometer** for distance-or-time components, asked once as a combined entry

### Step 4: Enable notifications
A plain-language prompt to turn on notifications, with a short explanation of why.

## Ride frequency
Chosen at setup. Adjusts how early a component moves to Due soon:

| Ride frequency | Due soon at |
|---|---|
| High | 80% of interval |
| Average | 90% of interval |
| Low | 95% of interval |

## Riding conditions
Wet or dusty riding shortens the air filter's interval. Since conditions vary trip to trip, this is captured when logging a check, not at setup.
