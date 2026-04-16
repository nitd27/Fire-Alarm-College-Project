# 🔥 Fire-Alarm-College-Project

> ⚠️ **This is a work-in-progress. Tasks are tracked below.**

An advanced fire detection system built with Arduino — engineered for **college-level standards**, not school demonstrations. This is a complete architectural upgrade over the [original Fire-Alarm project](https://github.com/nitd27/Fire-Alarm), moving from naive polling logic to a production-minded embedded design with interrupt-driven detection, a finite state machine, non-blocking timing, debouncing, and analog intensity sensing.

---

## What Makes This College-Level

| Feature | School Version | This Version |
|---|---|---|
| Detection method | Constant polling with `delay()` | Hardware interrupts (INT0) |
| Timing | Blocking `delay()` calls | Non-blocking `millis()` |
| Sensor data | Binary (fire / no fire) | Analog intensity (0–100%) |
| False positive handling | None | 3-read debounce confirmation |
| System logic | Flat if/else | Finite state machine |
| Extensibility | Hard to add features | Modular, ready for LCD/GSM/SD |

---

## Progress Tracker

### ✅ Done
- [x] Repo created
- [x] Draft README written
- [x] Architecture planned (ISR + FSM + millis + debounce + analog)
- [x] Reference to original project linked

### 🔧 Core Implementation
- [ ] Write upgraded `.ino` with interrupt-driven detection on D2
- [ ] Implement finite state machine (`IDLE → CONFIRMING → ALERTING → COOLDOWN`)
- [ ] Replace all `delay()` with `millis()` non-blocking timers
- [ ] Add analog read on A0 for intensity percentage
- [ ] Implement 3-read debounce before alarm triggers
- [ ] Test and tune `INTENSITY_THRESH`, `ALERT_DURATION`, `COOLDOWN_PERIOD` constants

### 🔌 Hardware
- [ ] Update circuit diagram (sensor DO → D2, AO → A0)
- [ ] Verify breadboard wiring matches new pin assignments
- [ ] Photograph or GIF the working circuit

### 📄 Documentation
- [ ] Finalize README with full circuit table
- [ ] Add Serial Monitor output screenshots
- [ ] Write brief explanation of each upgrade (for viva/presentation)
- [ ] Add wiring diagram image

### 🚀 Stretch Goals (if time allows)
- [ ] LCD display showing live state + intensity
- [ ] GSM/SIM800L SMS alert on fire confirmation
- [ ] SD card logging with timestamps
- [ ] Multiple sensor zones (sector-based detection)

---

## Components Required

- Arduino UNO
- IR Flame Sensor (with both DO and AO pins)
- Buzzer
- Jumper wires + Breadboard
- 5V regulated power supply

---

## Related

- 🔗 Previous version: [Fire-Alarm (school project)](https://github.com/nitd27/Fire-Alarm)
