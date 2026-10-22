# RTK Overview

Real-time kinematic (RTK) positioning combines GNSS observations from a reference receiver and a rover. The reference data are sent to the rover, commonly as RTCM messages over a radio or IP-based link. The rover uses the shared observations and its own measurements to estimate a relative baseline and, when conditions and the algorithm allow, resolve carrier-phase ambiguities.

## End-to-end checks

1. Confirm the base coordinates and reference point are correct and expressed in the expected datum and epoch.
2. Confirm the base is generating the required correction messages and that the transport carries them without truncation or excessive delay.
3. Confirm the rover is receiving and decoding those messages and that constellation, signal, and message support are compatible at both ends.
4. Check antenna installation, sky visibility, multipath, interference, and measurement quality.
5. Interpret solution status together with correction age, satellite geometry, baseline length, and the receiver's documented quality indicators.

A displayed fixed status is not a universal guarantee of accuracy. Performance depends on equipment, configuration, environment, baseline, correction quality, and validation method. Use the applicable receiver documentation and project acceptance criteria for numerical limits.

## RTCM references

RTCM publishes GNSS differential-service standards. The standards themselves may require access or purchase; this note does not reproduce their message definitions.

- [RTCM published standards](https://www.rtcm.org/rtcm-standards)
- [IGS RINEX working group](https://www.igs.org/wg/rinex/)

