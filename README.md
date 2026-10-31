# ARC-210 Radio Panel for DCS C-130J — October 30, 2026

**Last updated: October 30, 2026 at 9:38 PM MDT (America/Denver)**

I’m planning C-130J support for my [existing ARC-210 radio panel](https://github.com/dgdimick/ARC-210-DCS-Display). After comparing the panel, I plan to reuse the same faceplate, controls, display, PCBs, and printed parts. The work here will focus on the C-130J firmware, DCS-BIOS mappings, and menu system.

## Project status

This project is getting started. There is no C-130J firmware or tested C-130J compatibility available here yet, and I haven’t set a release date. I’ll check the module’s current ARC-210 functions and available DCS-BIOS data before deciding how much of the existing code can be reused.

## Shared hardware

The plan is to use the same **Teensy 4.1, 3.5-inch LCD display, buttons, switches, and encoders** as my A-10C II ARC-210 build. I’m treating this as a software adaptation of that panel; I haven’t identified a need for a separate PCB design.

- [Parts list and hardware choices](https://github.com/dgdimick/ARC-210-DCS-Display/blob/master/parts/README.md)
- [PCB files and manufacturing downloads](https://github.com/dgdimick/ARC-210-DCS-Display/tree/master/PCBs)
- [Final 17-part STL and 3MF print set](https://github.com/dgdimick/ARC-210-DCS-Display/blob/master/Supporting%20STL%27s/README.md#complete-17-part-print-set)
- [Assembly guide](https://github.com/dgdimick/ARC-210-DCS-Display/blob/master/Docs/Build%20Guide/README.md)

I have printed the complete 17-part set at 100% scale, and all parts passed test fitting for the existing hardware. That physical fit does not establish that the panel works with the C-130J software. The manufactured-board assembly and electrical testing remain part of the original project’s work.

## Things that need to be completed

**Last updated: October 30, 2026 at 9:38 PM MDT (America/Denver)**

1. **Compare operation:** Check the C-130J ARC-210 controls, display pages, startup behavior, and menu functions against my existing panel.
2. **DCS-BIOS mappings:** Identify the C-130J radio inputs and outputs, check which are available, and document any needed export changes.
3. **Firmware adaptation:** Reuse the existing display and control code where practical and add the C-130J mappings.
4. **Menu system:** Adapt and test the menu pages and display values against the aircraft.
5. **Bench-testing app:** Modify my debug app to provide C-130J ARC-210 test data and independent panel testing.
6. **Testing in DCS:** Test controls, display updates, power changes, reconnection, and the final menu system in the C-130J. Test the panel with the other USB devices connected and run an extended reliability test.
7. **Documentation:** Publish firmware loading, aircraft setup, DCS-BIOS requirements, and troubleshooting instructions. Link to the shared hardware documentation where it applies.

## DCS-BIOS

[My step-by-step DCS-BIOS guide](https://github.com/dgdimick/ARC-210-DCS-Display/blob/master/Docs/DCS-BIOS.md) covers installation and TekConnect, the app I use to manage my USB serial connections.

The guide’s patched `A-10C.lua` is for the A-10C ARC-210 project. **It does not configure the C-130J.** I’ll document any C-130J-specific module changes here once I have checked them.

## Bench testing

I use a [modified version of dcsBiosDebug](https://github.com/dgdimick/dcsBiosDebug/tree/arc210-working), based on [tldBear’s original app](https://github.com/tldBear/dcsBiosDebug), for the A-10C II ARC-210 panel. C-130J mappings and simulated data still need to be added; the existing A-10 shortcuts do not establish C-130J support.

## USB connections and test computer

- [My USB connections and powered hubs](https://github.com/dgdimick/ARC-210-DCS-Display/blob/master/Docs/USB-Connections-and-Powered-Hubs.md)
- [My SIMPIT and test computer](https://github.com/dgdimick/ARC-210-DCS-Display/blob/master/Docs/My-SIMPIT-and-Test-Computer.md) — my own setup, not minimum requirements.

## Related radio projects

- [ARC-210 for DCS A-10C II](https://github.com/dgdimick/ARC-210-DCS-Display)
- [ARC-164 UHF panel](https://github.com/dgdimick/ARC-164-DCS-Display)
- [ARC-186 COMM-VHF panel](https://github.com/dgdimick/ARC-186-DCS-Display)

## Questions and community builds

**Planning a build?** Tell me which panel you’re interested in—even if you haven’t started yet. You can ask questions or share ideas in [Issues](https://github.com/dgdimick/ARC-210-C-130J-DCS-Display/issues).

## PC Flights affiliation

I am not affiliated with [PC Flights](https://pcflights.com/). I chose their faceplate for my own cockpit build.

This is a hobby flight-simulation project. Verify the current files and instructions before building. Shared hardware, firmware, and printable files retain the licenses stated in their original repository.
