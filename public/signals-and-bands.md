# GNSS Signal Names and Frequency Bands

GNSS signal names identify a constellation-specific signal or service. A band label such as L1, L2, E1, B1I, or B1C is not always enough to identify the exact observation: the constellation, signal component, code, tracking mode, and receiver output convention may also matter.

## Reading receiver output

- Keep constellation identifiers separate from satellite PRNs and signal identifiers.
- Do not assume that a signal ID has the same frequency mapping across NMEA versions, receiver vendors, or proprietary messages.
- When decoding RINEX, use the observation-code definitions for the declared RINEX version.
- When decoding receiver-specific output, use that receiver's protocol manual and firmware-specific mapping.
- A receiver's ability to track a signal does not establish support for a correction service broadcast on that signal, nor does it establish licensing or regional availability.

For exact carrier frequencies and signal definitions, consult the relevant constellation's current interface specification. For GPS interface references, the U.S. Coast Guard Navigation Center maintains the official technical-reference index.

## References

- [U.S. Coast Guard Navigation Center: GPS technical references](https://navcen.uscg.gov/gps-technical-references)
- [IGS RINEX working group](https://www.igs.org/wg/rinex/)

