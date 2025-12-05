# Pro JSON for Beckhoff TwinCAT

A JSON parsing and composing library for Beckhoff TwinCAT, ported and refactored from the CODESYS Pro JSON library.

## Origin & Credits

This library is a "fork" and port of the original work by **Tim Van Meppelen**, available at [CODESYS Forge](https://forge.codesys.com/lib/pro-json/home/Home/)

## Refactoring & Changes

- Replaced CODESYS-specific pointer logic (e.g., `StrLenA`, `StrFindA`) with standard IEC 61131-3 functions (`Tc2_Standard` and `Tc2_Utilities` libraries).
- Updated `JSONVAR.FB_Init` logic to correctly detect variable paths in the TwinCAT hierarchy (removing reliance on the *Application* keyword found in CODESYS).

## Notes

- Arrays must be indexed from 1.
- See `Notes` POU in the source for known limitations and version history.
- Ported on *TwinCAT 3.1: Build 4026.19*
