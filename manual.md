# Vitezovi MiG-29 MFD Pilot Manual

Nov 6, 2026 · @Lukas

How to fly with the Vitezovi MiG-29 MFD add-on v1.7: one MFD with situational awareness, navigation, intercept, fuel, stores and RWR pages, on top of KRN MODS' MiG-29A(M) Cockpit Modernization.

## Before you fly

You need two things installed before the add-on: the DCS MiG-29A Fulcrum module and KRN MODS' "MiG-29A(M) Cockpit Modernization" V1.0.3, unzipped into `Saved Games\DCS\Mods\tech` as KRN describes.

Download KRN's mod from its release page: [MiG-29A(M) Cockpit Modernization on DCS User Files](https://files.digitalcombatsimulator.com/en/files/3350140/).

**Install**

1. Close DCS.
2. Unzip the add-on anywhere (not into the Mods folder) and double-click `INSTALL.bat`.
3. The installer finds KRN's mod, checks it is V1.0.3, keeps a copy of every KRN file it changes and installs the add-on. If it reports a problem, it has changed nothing.
4. In DCS: Options > Special > MIG-29AM, keep KRN's own MiG29 box ticked.

**Remove:** double-click `UNINSTALL.bat`. KRN's original files come back and KRN's mod works on its own.

**If the installer says KRN's files are not originals** (another KRN version, or the old all-in-one Vitezovi package): delete KRN's folder, unzip KRN's mod again, run `INSTALL.bat` again.

**Updating KRN's mod later:** uninstall the add-on first, update KRN, then install the add-on version made for that KRN version.

**Test missions** (installed to `Saved Games\DCS\Missions`):

- `MiG29_DL_Test_Flight.miz`: four MiG-29 slots at Kutaisi plus dynamic spawn.
- `MiG29_RWR_Test.miz`: air start with a full load, an SA-6 site and an armed Su-27, for the RWR and stores pages.

## Power and start-up

The MFD runs on the jet's DC power and has its own power button: the top-left rocker on the bezel, labelled PWR.

- **On:** press PWR once. It needs jet power (battery switch on, or a generator running).
- **Off:** hold PWR for 2 seconds. A "DISPLAY POWER OFF" bar fills while you hold; let go early and nothing happens.
- **Hot start and air start:** the MFD is already on.
- **Cold start:** the screen stays dark until the battery is on and you press PWR.

&#91;image: Holding PWR: the DISPLAY POWER OFF bar\]

1. Shown while you hold PWR; the bar fills over 2 seconds and the display switches off when it is full.
2. Let go before it is full and nothing happens.

**The start-up (about 16 seconds)**

1. Screen test: a short flash, then a test grid with grey steps.
2. Boot ROM: the display's own hardware check in small text.
3. Software boot log: each check ticks in with its boot clock, then a loading bar.
4. Squadron badge with the program version and a start-up bar.
5. BUILT-IN TEST checklist: every line goes from IN TEST to GO (white) or NO-GO (red). The right column shows real values: DC volts, your latitude and longitude (the nav alignment), datalink tracks, SPO-15, stations and the number of cartridges. Bottom-centre SKIP shows the result at once.
6. SELECT CARTRIDGE: see below. Then the MENU page.

NO-GO lines are information, not faults of the add-on: NAV / POSITION without a position, DATALINK RECEIVER without datalink packets (export off on a server, for example), GCI / BULLSEYE without a bullseye in the mission.

&#91;image: The BUILT-IN TEST checklist\]

1. Test mode and the add-on's version.
2. Check box: tick = GO, red cross = NO-GO, amber square = running now, empty = still waiting.
3. Result of each line.
4. A NO-GO line (here: no datalink packets yet).
5. The line being tested right now.
6. Your position from the nav alignment, latitude and longitude.
7. Summary: lines passed and failed.
8. SKIP: show the whole result at once.

**Choosing a cartridge**

The cartridges for the current map are listed as cards. The selected card is gold, with a preview of its route, points and drawings on the right and what it holds below (flight members, radio presets, waypoints, airfields, RSBN, drawings).

| Button | Does |
| --- | --- |
| Left 2 UP / left 3 DOWN | Select a cartridge |
| Bottom centre LOAD | Load the selected cartridge |
| Right 1 MSN | Use the mission plan instead |
| Right 5 NONE | No flight plan |

&#91;image: SELECT CARTRIDGE\]

1. Your aligned position.
2. The cartridges for this map, one card each, with points, flight members and GEO when it has drawings.
3. The selected cartridge: gold, with the pointer.
4. Preview of its route (white), points (blue) and drawings (pink).
5. More cartridges below; UP and DOWN scroll to them.
6. What it holds: flight members, radio presets, waypoints / airfields / RSBN, drawings.
7. UP (L2).
8. DOWN (L3).
9. LOAD (bottom centre): load the selected cartridge.
10. MSN (R1): use the mission plan.
11. NONE (R5): no flight plan.

You can change cartridges later on the NAV page (right 1 LOAD).

**Power cuts**

- Under 1.5 seconds: the screen goes dark and comes back on the same page.
- Longer (engines and battery off for a rearm, for example): the MFD switches off. With PWR still on, it runs the full start-up again as soon as power returns.

## The bezel

&#91;embedded content: MFD bezel · the five controls that never change\]

Everything else changes with the page: read the label printed beside a button before you press it. Buttons with no label do nothing on that page.

## MENU and moving between pages

The MENU page (squadron badge, fuel and datalink status at the bottom) is the hub: every page is one button away, and the bottom-centre button brings you back to it from anywhere.

&#91;image: The MENU page in the cockpit\]

1. PWR rocker: press = on, hold 2 s = off.
2. Left page buttons (SA, PIC, NAV, HSI, COM/NAV).
3. Right page buttons (FPAS, SMS, FLT, RWR, OPT).
4. Page title.
5. Status line: fuel and datalink state.
6. MENU (bottom centre): back to this page from anywhere.
7. Brightness rocker.
8. SYM rocker (symbol brightness).
9. D/N switch: day / night colours.

| Left | Page | Right | Page |
| --- | --- | --- | --- |
| 1 | SA | 1 | FPAS (fuel and engines) |
| 2 | NAV | 2 | SMS (stores) |
| 3 | HSI | 3 | FLT (your flight) |
| 4 | COM/NAV | 4 | RWR |

- **Bottom centre (MENU):** to the MENU from any page. Pressed on the MENU, it takes you back to the page you came from.
- **UFCP NAV button:** straight to the NAV page; again = back.
- **SA page right 2 PIC:** the PICTURE page.
- **MISSILE LAUNCH and BINGO FUEL** alerts show on every page.

## SA page

The SA page is a heading-up picture around your jet in the style of the F-15 SIT page: datalink contacts, ground threats, your route, markpoints and the cartridge's drawings, optionally over DCS's own charts.

&#91;image: SA page with INTC running\]

1. H1–H5: range and declutter buttons.
2. INTC heading tape (only while INTC runs).
3. Your bullseye position.
4. Range scale.
5. Active steerpoint: TO, bearing and range.
6. Your jet.
7. Cursor box on a contact.
8. SA-11 threat ring.
9. Route waypoints.
10. INTC meeting point (X).
11. INTC readouts: heading, time and range to the meeting point.
12. Bearing and range from you to the cursor.

| Button | Does |
| --- | --- |
| Left 1 FPL | Flight plan route on / off |
| Left 2 DCTR / CNTR | Move your jet low on the screen to see further ahead, and back |
| Left 3 / 4 RNG + / - | Range 20, 40, 80, 160, 320 km |
| Left 5 NEXT | Cursor to the nearest contact, then the next one |
| Top H1 to H5 | Cursor to the nearest to 5th nearest hostile |
| Right 1 GEO | Cartridge drawings shown (white) / hidden (grey); no label = none |
| Right 2 PIC | PICTURE page |
| Right 3 INTC | Intercept steering on / off (green while on) |
| Bottom 1 MARK / 2 DEL | Drop a markpoint / delete the newest |
| Bottom 4 EXP / NORM | Expanded view around the cursor's contact |
| Bottom 5 MAP | Moving map on / off (when enabled in Options) |

**Reading it**

- Colours: green friendly, red hostile, yellow unknown, cyan your flight. Lines from contacts show where they are heading.
- Top left: your bearing and range from the bullseye. Top right: range scale and the active steerpoint (TO ...). An amber NO DL or DL OFF appears there only when the datalink is missing.
- Bottom right: the datablock of the contact under the cursor (bearing / range from you and from the bullseye, altitude, type).
- Red rings are ground threats seen over the datalink.

**Cursor:** move it with the jet's radar cursor (TDC) slew controls, or jump to contacts with NEXT and H1 to H5.

**EXP:** zooms around the contact or SAM under the cursor (else the cursor point, else your jet) and follows a contact you picked. RNG + / - inside EXP zooms only the expanded view; NORM brings back your normal range, and the next EXP comes back at the zoom you used last.

**Declutter (SYM rocker, bottom left):** left click less, right click more, five steps: 1 FULL, 2 SHORT labels, 3 ALT only, 4 CLEAN (no labels, no route), 5 MIN (contacts and threats only).

**Markpoints:** MARK (or the UFCP MRK button) drops one at the cursor, or under the jet when the cursor is off. Up to 5. They appear on FPAS as places to go home to.

**Moving map:** tick Moving map in Options (see the last section). Charts exist for Caucasus, Syria, Persian Gulf, Sinai, Iraq, Afghanistan, Nevada, Mariana Islands, Marianas WWII, South Atlantic, Germany Cold War and Kola.

## PICTURE and INTC

Both are advisory and live only on the MFD: they read what the jet and the datalink already know and never touch the autopilot, HUD, radar or weapons.

**PICTURE (SA page right 2)**

The contacts grouped into formations, up to five groups, nearest first. Each row shows the group, BULLS (from the bullseye) or BRAA (from you), altitude, size and type, and aspect: HOT, FLANK, BEAM or DRAG with its direction. The selected group's call is written out (for example "BULLS 045/62, 8000, HOT, HOSTILE, 2 SHIP F-16.") above a small north-up plot.

&#91;image: PICTURE page\]

1. Group count and the call format.
2. SHOW filter in use.
3. Group table.
4. Selected group (boxed).
5. The call written out, ready to read on the radio.
6. Plot of the groups.
7. Plot range.
8. GRP buttons (R1–R5): pick a group.
9. CALL (L2).
10. INTC (L4): intercept the selected group.
11. SA (L5).
12. RNG+ (B1).
13. AUTO (B4).
14. SHOW / ALL (B5).

| Button | Does |
| --- | --- |
| Right 1 to 5 | Select a group |
| Left 2 CALL BULL / BRAA | Call format, and the plot's centre: bullseye or your jet |
| Left 4 INTC | Start intercept steering on that group, back to SA |
| Left 5 SA | Back to SA with the cursor on that group |
| Bottom 1 / 2 | Plot range + / - (25 to 400 km) |
| Bottom 4 AUTO | Plot range that fits all groups |
| Bottom 5 SHOW | Hostile / friendly / all (hostile red, friendly green) |

**INTC intercept steering (SA page right 3)**

Starts on the contact under the cursor, else the nearest hostile (or from PICTURE left 4). Press INTC again to stop.

- **Heading tape** at the very top: put the green diamond under the centre mark to fly the collision course (CC). Amber at the end of the tape = more than 20 degrees to turn.
- **On the scope:** a yellow X where you will meet, dashed lines from you and from the target to it, a white ring on the target (amber = track lost).
- **Bottom right** (in place of the cursor datablock): target and aspect, CC and time to X, bearing / range / altitude, closure, and fuel at X (amber or red against your FPAS bingo).
- **TAIL CHASE:** the target is faster and running, so there is no collision course; the diamond points at the target.

## NAV page

NAV steers you along the cartridge's route: put the green diamond on the centre mark and you fly the command heading (CMD) that keeps you on the planned leg.

&#91;image: NAV page\]

1. Name of the loaded plan.
2. Current steerpoint.
3. Bearing and range to it.
4. Direction and cross-track error.
5. Steering diamond (CMD): fly it to the centre.
6. Centre mark.
7. Commanded heading.
8. Route list.
9. Time-on-target line.
10. SEQ AUTO: steerpoints step on by themselves.

| Left | Does | Right | Does |
| --- | --- | --- | --- |
| 1 PREV | Previous steerpoint | 1 LOAD | Choose a cartridge, MSN or OFF |
| 2 NEXT | Next steerpoint | 2 TOT | Set a time on target (UFCP keypad) |
| 3 AUTO / MAN | Automatic or manual sequencing | 3 PT | Move the TOT cursor along the route |
| 4 DIR | Fly direct from where you are | 4 CLR | Remove the TOT under the cursor |
| 5 RTE | Pick the route to fly | 5 RSBN / TOT | Swap the bottom block |

Bottom 1 ADD and bottom 2 DEL add and remove typed-in waypoints.

**Top block:** the selected steerpoint and its note, bearing and range, time to go and ETA, the leg course (DTK) or DIR, cross-track error and the steering bar. Off the leg, CMD brings you back onto it at up to 45 degrees. All bearings are true (T) and match the SA page, HSI and UFCP.

**Route list:** the cartridge's whole route plus its airfields, with bearing and distance from the jet and the ETA along the route.

**Which steerpoint is active:** whatever you used last wins between PREV / NEXT, the UFCP STP switch and the jet's NAV panel WP-A/D buttons. In AUTO the next point is taken when you are within 3 km or have passed abeam.

**Time on target**

1. Right 3 PT moves the cursor (<) to the point.
2. Right 2 TOT, then type the time on the UFCP keypad as HHMMSS (or HHMM, then ENT). Mission time, as on the cockpit clock.
3. Set as many TOTs as you like; each leg between two TOTs gets its own speed.
4. Fly the cyan caret (your ground speed) into the green box (speed needed). The THEN line shows the next leg's speed.

Fuel at the TOT point and at the last steerpoint turns amber when it is below bingo or reserve. Ground speed needs about 2 seconds after opening the page.

**Member routes (RTE, left 5)**

One cartridge can hold every flight member's route: in DCS's DTC editor, start a point's note with member numbers ("1 IP", "12 TGT", "1234 RV"; untagged = everyone).

- Left 1 to 4: member 1 to 4's route.
- Right 1 to 5: add or remove that point by hand; the number in \[ \] is its place in the route.
- Bottom 1 / 2 page, bottom 4 CLR, bottom 5 ALL, left 5 DONE.

Changing the route clears TOTs and typed-in waypoints.

**Typed-in waypoints**

- Bottom 1 ADD = latitude / longitude entry; ADD again = MGRS; a third time = cancel. CLR deletes the last digit.
- Lat / long: 13 digits DDMMmm DDDMMmm, for example 4155850415172 = N 41 55.85 E 041 51.72. N/S and E/W come from where the jet is.
- MGRS: easting and northing in the jet's own 100 km square (shown on the line), 10 digits, or 4 / 6 / 8 digits then ENT.
- The point goes in after the selected steerpoint and is flown to directly. Bottom 2 DEL removes it.

**RSBN view (right 5):** the cartridge's RSBN 1 to 3 and the nearest map stations with bearing and range, NO RX beyond the radio horizon, and the jet's RSBN channel in green.

## HSI, COM/NAV, FPAS, SMS, FLT and RWR

**HSI (MENU left 3):** a NATO-style HSI with heading bug, course and TACAN.

- Left 1 HDG, 2 CRS, 3 TCN: type the value on the UFCP keypad; ENT applies, CLR deletes.
- Left 4: course to the active steerpoint. Left 5: heading bug to your present heading.
- Right 1 TCN OFF: switches the TACAN pointer off again (shown while a channel is set).

&#91;image: HSI page\]

1. Steerpoint bearing and range.
2. TACAN state (OFF here).
3. Heading readout.
4. Heading bug.
5. Course arrow and deviation bar.
6. Steerpoint bearing pointer (green).
7. HDG and CRS readouts.
8. HDG (L1): set the heading bug.
9. CRS (L2): set the course.
10. TCN (L3): TACAN on / off.
11. STP (L4): set the course to the steerpoint.
12. SYNC (L5): put the bug on your current heading.

**COM/NAV (MENU left 4):** the R-862 channel and frequency, the 20 presets (channels 0 to 19), RSBN / ILS / ADF / GCI channels and the nearest RSBN / PRMG stations. Read only: the MiG-29 keeps its own preset frequencies.

&#91;image: COM/NAV page\]

1. Radio channel and frequency.
2. Preset table.
3. Current channel (amber).
4. RSBN, ILS, ADF and GCI settings.
5. Nearest stations.

**FPAS (MENU right 1):** fuel and engines.

- Time and range to 500 kg, best range and endurance (estimates), engine RPM and EGT.
- Left 1 BINGO: type kg on the UFCP keypad, ENT. Below bingo, a BINGO FUEL alert shows on every page.
- Left 2 HOME: cycles through the plan's airfields and your markpoints, with fuel needed to get there and fuel on arrival. With no airfield in the cartridge and no markpoint it shows HOME -- (common on air starts): drop a markpoint over your base, or load a cartridge that has your home airfield.

&#91;image: FPAS page\]

1. Total fuel.
2. RPM and EGT.
3. At the current setting: time to 500 kg and range.
4. Best range.
5. Best endurance.
6. Bingo and home figures.
7. BINGO (L1).
8. HOME (L2).

**SMS (MENU right 2):** what hangs on each station, gun rounds, chaff and flares. Amber = selected station.

&#91;image: SMS page\]

1. Station list.
2. Selected station (amber).
3. Gun rounds, chaff and flares.
4. Summary of the load.

**FLT (MENU right 3):** your flight's positions, radar and jammer status, alive or lost.

- Left 1 ADD lists friendly aircraft (players first); pick up to 5 with the right buttons. Left 2 removes the selected member.
- Members are remembered between flights.
- Fuel and weapons of other jets are not available outside single player, so FLT shows radar / jammer / alive instead.

&#91;image: FLT page\]

1. Flight members on the right buttons.
2. Status of the selected member.
3. ADD (L1).
4. REM (L2).

**RWR (MENU right 4):** the SPO-15 picture on the MFD. It shows exactly what the SPO-15 shows: sector lamps, type letters and signal strength. It does not name the radar or aircraft that is painting you.

- The main threat sits in its direction, nearer the centre the stronger it is, with its SPO-15 type letter (P Z H N F S).
- Amber = main threat, red ring = locked on you, flashing ring and banner = missile launch.
- Other threats show their direction on the outer ring.

&#91;image: RWR page\]

1. SPO-15 state and how many sectors are lit (SPO-15 OFF or CLEAR when there is nothing).
2. Chaff and flares left.
3. Scope with your jet in the middle.
4. Main threat: its SPO-15 type letter in its sector, nearer the centre the stronger it is; red ring = locked on you.
5. Other lit sectors on the outer ring. They carry a type letter only when one other type lamp is lit, otherwise "?".
6. Main threat line: type letter, sector direction, power level (out of 15) and LOCK or LAUNCH.
7. All type lamps that are lit.
8. Directions of the other lit sectors (above or below for the main threat shows under these when the SPO-15 lights it).

## UFCP buttons and the STP switch

Three UFCP keys belong to the add-on (their labels are changed on the panel) and the keypad types values for the MFD pages.

| UFCP control | Does |
| --- | --- |
| MRK | Markpoint at the SA cursor, or under the jet |
| DIR (was DVR) | Fly direct to the selected steerpoint from here |
| NAV (was FLT/MENU) | NAV page; again = back |
| Keypad, ENT, CLR | Values for HSI, BINGO, TOT and typed-in waypoints |
| STP switch | With a cartridge loaded: step through its steerpoints |

With a cartridge loaded the UFCP shows the add-on's steerpoint: line 1 "STP P3", line 2 its true bearing and distance, the same numbers as the SA and NAV pages. With MSN the STP switch stays KRN's own (mission route).

## Data cartridges, drawings and the DTC Planner

A cartridge is a MiG-29 `.dtc` file in `Saved Games\DCS\DTC`, made in DCS's own DTC editor or in the Vitezovi DTC Planner. Only cartridges for the current map are listed.

- **One cartridge for both worlds:** its 3 waypoints, 3 airfields and 3 RSBN channels drive the jet's own navigation; its route (any length) drives the NAV and SA pages.
- **Member tags:** start a point's note with member numbers ("1 IP", "12 TGT"); see Member routes on the NAV page. Notes hold 7 characters.
- **Examples installed:** VITEZOVI GCI NETWORK (intercept and escort routes for four members, ranges, FLOT and orbit tracks), VITEZOVI FLIGHT 40 (member routes), VITEZOVI ROUTE 20 (a 20-point route).

**Drawings (.geo.txt)**

An optional file with the same name next to the cartridge (`DTC\<name>.dtc` + `DTC\<name>.geo.txt`) adds drawings to the SA page. The DTC Planner's DRAWINGS tab writes it; Notepad works too, one drawing per line, latitude / longitude in decimal degrees, radius in km, # = comment.

| Line | Draws |
| --- | --- |
| `RING SA-11 35 42.9000 42.9000` | Red ring with name and radius (confirmed threat) |
| `RING? SA-8? 12 42.5500 42.3500` | Pink dashed ring (suspected threat) |
| `FLOT MAIN RIDGE 43.55 40.10 / 43.58 40.55` | Cyan dashed line |
| `BORDER GEO-RUS 42.85 41.0 / 42.7 41.6` | Grey dash-dot-dot line |
| `AREA CAP SOUTH 41.95 42.3 / 41.95 42.9 / 41.75 42.9` | Cyan dashed outline with its name |

SA page right 1 GEO shows or hides them; threats seen over the datalink stay. "LOADED \<name> +GEO" confirms a cartridge with drawings.

**The DTC Planner** is the single `Vitezovi DTC Planner.html` file in the package: double-click it, it works offline with every map built in. Plan the route and drawings, then SAVE writes the `.dtc` and `.geo.txt` to Downloads; move them to `Saved Games\DCS\DTC`.

## Options, settings and troubleshooting

**Options** (DCS Options > Special > MIG-29AM > "MiG-29 WW MFD"). They are read when a mission loads, so restart the mission after changing them. Keep KRN's own MiG29 box ticked: it switches the whole cockpit mod on.

| Option | Off / on means |
| --- | --- |
| Datalink | Off: SA shows only your own radar, FLT is off, the export does not scan the mission's units (saves CPU) |
| RWR page | Off: no RWR page and no launch alerts |
| Launch warnings | Off: launches show as a normal lock, no banner |
| Moving map | On: DCS's charts behind the SA page, MAP button to hide them in flight |

**Brightness:** top-right rocker, left click brighter, right click darker. D/N switch bottom right: left click day, right click night (separate levels).

**Settings file** (text size, keypad mapping, ranges, power and start-up): `Saved Games\DCS\Mods\tech\MiG-29A(M) Cockpit Modernization - KRN MODS V1.0.3\Cockpit\Scripts\DL\dl_config.lua`. For example `boot_skip = true` keeps the power button but skips the start-up screens; `power_mode = "always"` keeps the MFD always on.

**Troubleshooting**

| Symptom | Cause and fix |
| --- | --- |
| MFD stays dark on a cold start | Battery on, then press PWR (top-left rocker) |
| NO DL on the SA page | No datalink packets: the server switches off export of world objects, or the Datalink option is off. Only your own radar is shown |
| No cartridges listed | Cartridges are listed per map; the file must be a MiG-29 `.dtc` in `Saved Games\DCS\DTC` |
| No moving map | Tick Moving map in Options and restart the mission; some maps have no charts |
| Installer reports KRN files not original | Delete KRN's folder, unzip KRN's mod again, run `INSTALL.bat` |
| Anything else | Logs in `Saved Games\DCS\Logs\mig29dl_*.log`; send them with your report |

The SA datalink is a simulation built from the unit list DCS exports (sensor ranges, radar horizon, terrain): DCS has no real Link 16 for the MiG-29.
