# RINEX

RINEX (Receiver Independent Exchange Format) is a text-based exchange format used for GNSS data. It allows observation and navigation data from different receiver brands to be handled by compatible processing software, subject to the signals and fields actually present in each file.

RINEX versions evolve. The IGS RINEX working group currently publishes the RINEX 4.02 format document and describes RINEX 3.05 as the last RINEX 3 version supported for ongoing IGS development. Older receiver or processing workflows may still require another version, so select a version supported by both the source data and downstream software.

## File review checklist

- Check the version declaration and file type before parsing.
- Read the header for marker, receiver, antenna, approximate position, observation types, time information, and interval where present.
- Verify the observation section contains the expected epochs, constellations, signals, and measurements.
- Treat missing observations as missing data; do not synthesize values without marking them as derived.
- Validate converted files with an independent RINEX-aware tool when the result is used for engineering or survey decisions.

## References

- [IGS RINEX working group and format versions](https://www.igs.org/wg/rinex/)
- [RINEX 4.02 format document](https://files.igs.org/pub/data/format/rinex_4.02.pdf)

