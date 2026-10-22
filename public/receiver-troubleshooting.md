# GNSS Receiver Troubleshooting Workflow

Use a controlled sequence so that each test narrows the fault domain. Record the receiver model, firmware, antenna, cable, power source, configuration, test location, and time before changing settings.

## No satellites or weak tracking

1. Check receiver power, startup state, port selection, baud rate, and whether expected output messages are enabled.
2. Inspect antenna placement, sky visibility, connector condition, cable continuity, and any splitter or inline device.
3. Verify antenna power requirements against the receiver hardware documentation. Do not apply an assumed voltage.
4. Compare with a known-good antenna and cable in the same location, changing one component at a time.
5. Review per-satellite signal strength, elevation, constellation, and signal identifiers. A single aggregate satellite count can hide a signal-specific issue.

## Poor or unstable positioning

1. Check satellite geometry, obstruction, multipath, and possible RF interference.
2. For RTK, verify base coordinates, correction message availability, rover reception, correction age, and compatibility.
3. Compare solution status with raw observations and independent reference data; do not rely on one status flag alone.
4. Save representative logs before changing configuration. Keep the original and modified configurations distinct.

## Escalation data

Provide a short time-bounded log, exact model and firmware, configuration export, antenna and cable details, approximate location/environment, expected behavior, observed behavior, and the steps already tested. Redact serial numbers, credentials, customer names, and precise locations unless they are essential and explicitly approved for sharing.

