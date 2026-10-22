# GNSS Observations

GNSS processing uses measurements made by a receiver from satellite signals. The most common observation families are code pseudorange, carrier phase, and Doppler. A receiver may also report signal strength or carrier-to-noise density, lock indicators, and tracking quality; these are useful diagnostics but are not interchangeable with the three primary measurements.

## Pseudorange

Code tracking estimates signal travel time using a ranging code. The resulting range-like measurement includes receiver and satellite clock offsets and propagation and hardware effects. It is therefore not, by itself, a direct geometric distance.

## Carrier phase

Carrier-phase tracking measures the phase of the received carrier. It supports high-precision positioning, but the integer number of carrier cycles between satellite and receiver is initially unknown and must be resolved or otherwise estimated by the positioning method.

## Doppler

Doppler observations describe the received signal's frequency shift and are useful for estimating range rate and receiver velocity. Sign conventions depend on the data format and implementation; check the relevant format specification before interpreting a sign.

## Practical interpretation

- Preserve the observation epoch and time system when comparing or combining measurements.
- Check units, signal identifiers, lock status, and cycle-slip indicators before drawing conclusions.
- Do not interpret a signal-strength value as a direct measure of position accuracy.
- Receiver-specific raw message names and fields must be verified in the matching interface manual.

## References

- [IGS RINEX formats](https://www.igs.org/wg/rinex/)
- [RINEX 4.02 format document](https://files.igs.org/pub/data/format/rinex_4.02.pdf)

