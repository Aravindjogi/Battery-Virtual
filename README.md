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

## Features (full)

| Area | Modules |
|------|---------|
| **Study** | Learn (22 topics), CAN Editor, DBC Editor, Battery Maker, Pack Builder |
| **Engineering** | Simulator, Bus Master, Protocol Viz, TPDO Map, Recipe Editor, V11 Lab |
| **V11.1** | Command palette, Heatmap, Faults, Web Serial CAN, Templates, Creds |
| **Project** | Project Hub, Test Manager, imports/exports (CSV, Excel, JSON, DBC, logs) |
| **Protocols** | CAN, CANopen, UART, RS-485, Modbus, SMBus, I²C, SPI, LIN, Ethernet/DoIP |

### Accounts (client-side gate)

| Role | Default User ID | Default Password | Access |
|------|-----------------|------------------|--------|
| **Admin** | `Aravindjogi` | `Tinju@2001` | Full toolkit |
| **Study** | `9381329751` | `Tinju@2001` | Learn + CAN/DBC + Battery Maker + Pack Builder + heatmap/templates |

> Change credentials via the 🔑 button (stored in localStorage). Change them before any public deployment.

---

## Quick start (local)

1. Open `index.html` in Chrome / Edge / Firefox  
   **or** serve the folder (required for PWA + Web Serial):

```bash
python -m http.server 8080
# or: npx serve .
```

2. Visit `http://localhost:8080`

### Web Serial CAN

- Use **Chrome or Edge** on desktop.
- Page must be **localhost** or **HTTPS**.
- Adapter must speak **SLCAN / Lawicel ASCII** over USB-CDC (e.g. CANable, candleLight).
- Connect → select bitrate → **Open channel** → TX frames as `3E0#0A1082FFA4C00064`.

---

## Deploy to GitHub Pages

```bash
cd BatteryCANAnalyzer-V11
git init
git add .
git commit -m "Battery CAN Analyzer V11.1"
git branch -M main
git remote add origin https://github.com/<YOUR_USER>/<YOUR_REPO>.git
git push -u origin main
```

GitHub → **Settings → Pages → Deploy from branch → main / root**.

---

## Project structure

```
BatteryCANAnalyzer-V11/
├── index.html          # Full application + V11.1 suite
├── manifest.json       # PWA manifest
├── sw.js               # Offline service worker (v11-2 cache)
├── icons/              # icon-192.png, icon-512.png
├── .gitignore
├── LICENSE
└── README.md
```

---

## License

MIT — see `LICENSE`. Copyright (c) 2026 BMS V11 @Tinju
