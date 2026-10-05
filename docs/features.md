# Features

## V1
Each feature connects to at least one objective in [overview.md](overview.md).

| Feature | Priority | Description |
|---|---|---|
| Components Dashboard | High | The main screen. Shows every tracked component's status at a glance, sorted by urgency. |
| Push Notifications | High | Alerts when a component is due soon or overdue, delivered even when the app isn't open. |
| Service Log | High | A record of every check and service with date, distance, and notes. Append-only, so nothing gets lost. |
| Offline Mode | Medium | The app works fully without an internet connection. |
| Generic Parts Catalogue | Medium | A simple reference of common parts per component category, including what to look for. |
| PDF Export | Low | A downloadable summary of the full service history, useful for mechanics, insurers, or selling the bike. |

## Moved to V2

### Multiple bike profiles
Valuable, but not needed to prove the core idea works.

### AI Mechanic Assistant
The dashboard tells a rider what needs attention, but not what it means for someone with no mechanical background: whether it's urgent, or what to say to a mechanic.

The assistant answers plain-language questions using the rider's real component data from the status engine (for example, "What should I check before my long ride?").

**It does:**
- Answer natural-language questions about current component status
- Explain due-soon and overdue items in plain terms for casual riders
- Use only the rider's real tracked data, never inventing service history

**It doesn't:**
- Replace the rule-based status engine. Statuses are still calculated deterministically, not by the AI
- Diagnose faults beyond the tracked data
- Book mechanics or make purchase decisions

Moved to V2 because the core rule-based tracking is the priority for V1.
