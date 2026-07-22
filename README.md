# Energy Saver Power Plan Link

A Windhawk tool mod that links the Windows 11 **Energy Saver** toggle with the
classic **Power Saver** power plan.

The mod runs in a dedicated Windhawk process instead of being injected into
`explorer.exe`.

## How it works

When Energy Saver is enabled, the mod:

- Saves the currently active Windows power plan.
- Switches to the standard Power Saver plan.

When Energy Saver is disabled, the mod:

- Restores the previously active power plan.
- Restores it only if Power Saver is still active.

If the user manually selects another power plan while Energy Saver is enabled,
that manual selection is preserved.

Disabling the mod also restores the previous power plan when appropriate.

## Example

```text
Balanced
    ↓
Enable Energy Saver
    ↓
Power Saver
    ↓
Disable Energy Saver
    ↓
Balanced
```

The restored plan can also be High Performance, Ultimate Performance, or another
custom power plan.

## Requirements

- Windows 11 version 24H2 or later
- Windhawk
- The standard Windows Power Saver plan must be available

> On some Modern Standby systems, the classic Power Saver plan might be hidden
> or unavailable. In that case, Windows can't switch to Power Saver and the mod
> leaves the current power plan unchanged.

## Verification

Run this command in PowerShell:

```powershell
powercfg /getactivescheme
```

Enabling Energy Saver should activate Power Saver. Disabling Energy Saver should
restore the previously active plan.

## License

Licensed under the MIT License.
