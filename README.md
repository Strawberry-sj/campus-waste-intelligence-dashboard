# Campus Waste Intelligence Dashboard

A browser-based prototype for campus waste monitoring, segregation analytics, audit approvals, waste-batch tracking, and a simulated smart-weighing workflow. Prepared as a demo project for Sociothon 2026.

> **Demo notice:** The dashboard currently uses generated sample data. Do not present the sample figures as real campus measurements. Audit records and settings are saved in the current browser only.

## Features

- Campus-wide and location-specific dashboard
- 7-, 14-, and 28-day reporting windows
- Waste stream breakdown for food, paper, plastic, metal/glass, and other waste
- Segregation leaderboard and hotspot alerts
- Seven-day forecast and a basic historical backtest
- Audit entry with optional photo evidence
- Pending, approved, and rejected audit workflow
- Waste-balance ledger for collected, recycled, composted, rejected, disposed, and unreconciled waste
- Batch creation, dispatch and facility receipt tracking
- Browser-side hash-chain verification
- Segregation-improvement scenario calculator
- Smart-weighing calibration simulation and optional Web Serial connection

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. For best compatibility—especially for Web Serial—serve it from `localhost` using a local development server and use Chrome or Edge.

No build step or package installation is required for the current prototype.

## Publish with GitHub Pages

1. Create a repository on GitHub, for example `campus-waste-intelligence-dashboard`.
2. Upload `index.html` and `README.md` to the repository's root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select the `main` branch and `/(root)` folder, then save.
6. Wait for the deployment to finish. GitHub will show the published site URL in the Pages settings.

## Important limitations

- **Sample data:** Historical records are generated in the browser and are not verified campus measurements.
- **Local-only storage:** `localStorage` is tied to the browser and device. Different users do not share records.
- **No real authentication:** Supervisor names are entered into the interface but are not authenticated accounts.
- **Client-side integrity checks:** Hash checks can detect some changes in the current browser data, but are not a secure, server-signed audit trail.
- **Photo evidence:** Evidence images are stored in browser-local records, not uploaded to a central service.
- **Forecast assumptions:** The forecast and backtest are simple illustrative methods, not validated operational predictions.
- **Environmental and financial estimates:** Conversion factors are placeholders and must be replaced with credible, cited local sources before making claims.
- **Scale integration:** Serial support depends on compatible hardware, browser support, permissions, and the scale's output format. The simulation is not real weighing evidence.
- **QR dependency:** QR rendering currently uses a third-party JavaScript library loaded from a CDN, so QR generation requires internet access to that CDN.

## Suggested next steps for a real deployment

1. Replace generated data with actual, timestamped weighbridge/bin-audit records.
2. Add a backend API and shared database.
3. Add secure sign-in and role-based permissions for auditors and supervisors.
4. Upload evidence photos to controlled cloud storage.
5. Record facility receipts and recycling/composting certificates against each batch.
6. Add audit history, exportable CSV reports, and server-side tamper-evident logs.
7. Validate forecast accuracy and publish the sources for environmental and financial factors.

## Technology

- HTML, CSS, and vanilla JavaScript
- SVG-based dashboard charts
- Browser `localStorage`
- Web Crypto API for client-side hash checks
- Optional Web Serial API
- Third-party QR-code library loaded from CDN

## License

No license is specified yet. Add a license file if you want to grant others explicit permission to reuse or modify this project.
