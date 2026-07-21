# Energy Saver Power Plan Link

A Windhawk mod that links the Windows 11 **Energy Saver** toggle with the classic **Power Saver** power plan.

## How it works

When Energy Saver is enabled, the mod:

- Saves the currently active Windows power plan.
- Switches to the standard Power Saver plan.

When Energy Saver is disabled, the mod:

- Restores the previously active power plan.
- Restores it only if Power Saver is still active.

If the user manually selects another power plan while Energy Saver is enabled, that manual selection is preserved.

## Example

```text
Ultimate Performance
        ↓
Enable Energy Saver
        ↓
Power Saver
        ↓
Disable Energy Saver
        ↓
Ultimate Performance
