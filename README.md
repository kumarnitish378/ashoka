# Ashoka

Ashoka is a Rover-only autopilot firmware derived from
[ArduPilot](https://ardupilot.org), the open-source autopilot project.
It's been trimmed down to just the Rover vehicle and its shared
dependencies (the other vehicle firmwares - Copter, Plane, Sub,
AntennaTracker, Blimp - and all git submodules have been removed/flattened),
plus custom driver work for a Hi-Link HLK-LD2451 24GHz mmWave radar and a
Webots-based simulation rig for developing and testing it.

See [`docs/HLK-LD2451/`](docs/HLK-LD2451/) for the radar driver, its SITL
simulators, and the Webots test setup.

## Building

Same as upstream ArduPilot's SITL workflow:

```bash
./waf configure --board sitl
./waf rover
```

See `BUILD.md` for platform-specific build instructions (inherited from
upstream and still accurate for this fork).

## License

Ashoka is licensed, like ArduPilot, under the GNU General Public License,
version 3 - see [`COPYING.txt`](COPYING.txt) for the full text.
