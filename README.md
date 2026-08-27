# Battery CAN Analyzer V11.1

Offline **BMS / CAN engineering toolkit** — single-page web app for signal decoding, DBC editing, battery pack design, simulation, guided learning, live Web Serial CAN, and more.

100% client-side. No backend. Works after first load even without internet (service worker caches app + icons).

---

## What's new in V11.1

| Feature | Description |
|---------|-------------|
| **Command palette** | `Ctrl+K` / `⌘K` — jump to any module |
| **Full offline cache** | Service worker caches HTML, manifest, icons, SW |
| **Credential manager** | Change Study/Admin IDs & passwords (localStorage) |
| **Cell heatmap** | Voltage/temp color grid + imbalance stats |
| **Fault injection** | OV/UV/OT/bus-off/contactor/isolation scenarios |
| **Web Serial CAN** | SLCAN TX/RX for CANable / candleLight-class adapters |
| **Pack templates** | 16S NMC, 48V LFP, 400V traction, ESS presets |
| **DBC multiplex** | Parses `SG_ name M` / `SG_ name m0` multiplexor signals |

---

## Quick start

1. Unzip this folder.
2. **Best:** serve it (needed for offline PWA + Web Serial):

```bash
cd BatteryCANAnalyzer-V11
python -m http.server 8080
```

3. Open **http://localhost:8080** in Chrome or Edge.

You can also double-click `index.html`, but Web Serial and service worker work best via localhost.

### Login (defaults)

| Role | User ID | Password |
|------|---------|----------|
| Admin | `Aravindjogi` | `Tinju@2001` |
| Study | `9381329751` | `Tinju@2001` |

Change via the **🔑** button after login.

---

## License

MIT — see `LICENSE`. Copyright (c) 2026 BMS V11 @Tinju
