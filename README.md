# Battery CAN Analyzer V11

Offline **BMS / CAN engineering toolkit** — single-page web app for signal decoding, DBC editing, battery pack design, simulation, and guided learning.

100% client-side. No backend. Works after first load even without internet (with service worker).

---

## Features

| Area | Modules |
|------|---------|
| **Study** | Learn (22 topics), CAN Editor, DBC Editor, Battery Maker, Pack Builder |
| **Engineering** | Simulator, Bus Master, Protocol Viz, TPDO Map, Recipe Editor, V11 Lab |
| **Project** | Project Hub, Test Manager, imports/exports (CSV, Excel, JSON, DBC, logs) |
| **Protocols** | CAN, CANopen, UART, RS-485, Modbus, SMBus, I²C, SPI, LIN, Ethernet/DoIP |

### Accounts (client-side gate)

| Role | User ID | Password | Access |
|------|---------|----------|--------|
| **Admin** | `Aravindjogi` | `Tinju@2001` | Full toolkit |
| **Study** | `9381329751` | `Tinju@2001` | Learn + CAN/DBC editors + Battery Maker + Pack Builder |

> Credentials live only in browser JS for local/demo use. Change them before any public deployment if needed.

---

## Quick start (local)

1. Download or clone this repository.
2. Open `index.html` in Chrome / Edge / Firefox  
   **or** serve the folder (recommended for PWA / service worker):

```bash
# Python
python -m http.server 8080

# Node
npx serve .
```

3. Visit `http://localhost:8080`

---

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `BatteryCANAnalyzer-V11`).
2. Push this folder as the repo root:

```bash
cd BatteryCANAnalyzer-V11
git init
git add .
git commit -m "Initial commit: Battery CAN Analyzer V11"
git branch -M main
git remote add origin https://github.com/<YOUR_USER>/<YOUR_REPO>.git
git push -u origin main
```

3. On GitHub: **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)`**.
4. After a minute, open:  
   `https://<YOUR_USER>.github.io/<YOUR_REPO>/`

### Optional: GitHub Actions (static)

If you prefer Actions, add `.github/workflows/pages.yml` with a static HTML deploy workflow. The app needs no build step.

---

## Project structure

```
BatteryCANAnalyzer-V11/
├── index.html          # Full application (single file UI + logic)
├── manifest.json       # PWA manifest
├── sw.js               # Offline service worker
├── icons/              # App icons (optional; add PNG 192 & 512)
├── .gitignore
└── README.md
```

---

## Icons (optional)

For a complete PWA install experience, add:

- `icons/icon-192.png` (192×192)
- `icons/icon-512.png` (512×512)

You can generate these from any ⚡ / battery icon. The app runs fine without them.

---

## Notes

- All decoding, DBC, formulas, and UI run in the browser.
- Session role is stored in `sessionStorage` (`bca-auth`, `bca-role`).
- Preferred protocol is stored in `localStorage` (`bca-protocol`).
- For public demos, replace or remove default passwords in `index.html` (search `ADMIN_ID` / `AUTH_ID`).

---

## License

Use freely for education and engineering projects. Attribution appreciated: **BMS V11 @Tinju**.
