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
```

The restored plan can also be Balanced, High Performance, or another custom power plan.

## Requirements

- Windows 11 version 24H2 or later
- Windhawk
- The standard Windows Power Saver plan must be available

## Installation

1. Open Windhawk.
2. Select **Create a new mod**.
3. Replace the example code with the contents of `energy-saver-power-plan-link.wh.cpp`.
4. Select **Compile Mod**.
5. Enable the mod.

## Verification

Run this command in PowerShell:

```powershell
powercfg /getactivescheme
```

Enabling Energy Saver should activate Power Saver. Disabling Energy Saver should restore the previously active plan.

## License

Licensed under the MIT License.
