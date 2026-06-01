# of-advanced-sort

An OmniFocus plug-in that sorts tasks in a perspective by urgency and priority tag, then writes estimated-minute durations so OmniFocus can order them correctly.

## What it does

1. Opens a named perspective (default: `Today`) and collects all tasks.
2. Sorts them into four urgency buckets — Overdue, Due Today (available), Planned, Due Today (not yet available) — then within each bucket by priority tag (`1️⃣ First`, `2️⃣ Next`, `3️⃣ Later`) and flag status.
3. Writes sequential `estimatedMinutes` values (10, 20, 30 …) so OmniFocus sorts the list in the intended order.
4. Sequential-task siblings are kept together and inherit the best priority tag in the group.

A dry-run mode previews the proposed order without writing any changes.

## Configuration

Open the script and edit the constants at the top:

| Variable | Default | Description |
|---|---|---|
| `PERSPECTIVE` | `"Today"` | Name of the perspective to sort |
| `DRY_RUN` | `false` | `true` = preview only, no writes |
| `STEP_MINUTES` | `10` | Minute increment between tasks |

## Installation

1. Download `of-advanced-sort.omnifocusjs`.
2. Double-click the file — OmniFocus will prompt you to install it.
3. Run it from the Plug-Ins menu or assign a keyboard shortcut in OmniFocus settings.

## Requirements

OmniFocus 3 or later (macOS or iOS with Automation support).

## License

MIT — see [LICENSE](LICENSE).
