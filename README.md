# ELITESYNC-SOC-AIELITESYNC SOC AI – Autonomous Threat Intelligence & Fraud Guard

SOA ITER Campus Security Demo

A lightweight, browser‑based Security Operations Center (SOC) built with React + Vite that showcases real‑time threat detection, explainable AI forensics, and automated SOAR playbooks—all running entirely offline. The UI is fully re‑branded for the ELITESYNC team and the SOA ITER campus, with a friendly, human‑style tone.

🎯 What the demo does
✅ Feature	💡 Why it matters
Live telemetry stream – continuous generation of benign and malicious events (configurable speed).	Simulates real‑world traffic without needing external data sources.
Dynamic DEFCON badge – changes color & pulse based on critical alerts.	Gives an at‑a‑glance risk indicator.
Interactive Threat Map – campus‑specific location (Bhubaneswar) with live pulse markers.	Visualizes where attacks originate.
Three custom attack scenarios – Web3 drainer, SIM‑swap, Zero‑Day SQLi.	Demonstrates modern threat vectors.
XAI‑powered audit modal – explains why each event was flagged, with a “Built by the ELITESYNC hackathon crew 🛠️” footer.	Makes AI decisions transparent to analysts.
SOAR automation – one‑click mitigation actions (block IP, quarantine device, revoke credentials).	Shows how playbooks can be executed instantly.
Copilot assistant – chat‑style XAI explanations and recommendations.	Bridges the gap between automation and human insight.
Human‑like UI copy – informal greetings, emojis, and author attribution.	Reduces the “AI‑generated” feel and makes the demo more relatable.
Zero external dependencies – runs locally with npm run preview; no API keys required.	Perfect for hackathons, labs, or quick demos.
🚀 Quick Start (Windows)
powershell
# 1️⃣ Clone (or copy) the repo
cd C:\path\to\your\workspace
# 2️⃣ Install dependencies (once)
npm install
# 3️⃣ Build (optional, just for production output)
npm run build
# 4️⃣ Start the live preview server
npm run preview -- --port 3000 --host   # falls back to 3001 if 3000 is busy
# 5️⃣ Open in a browser
http://localhost:3000/

The preview server will automatically pick an open port (e.g., 3001) and expose both a local and network URL.

📂 Repository Layout (high‑level)
src/
 ├─ components/          # React UI pieces (Navbar, ThreatMap, AuditReportModal, …)
 ├─ services/            # Telemetry generator, SOAR engine, LLM helpers
 ├─ types/               # TypeScript interfaces for events/metrics
 └─ App.tsx              # Main app bootstrap & routing
public/
 └─ elitesync-logo.jpg   # Project logo (used throughout UI)
package.json
vite.config.ts
README.md                # (this file)
🛠️ Extending the Demo
Add more attack scenarios – edit services/telemetryStream.ts and push them to the UI selector.
Persist data – integrate a lightweight SQLite DB or browser IndexedDB for historic forensics.
Deploy to the cloud – containerize with Docker (docker build . -t elitesync-soc) and run on any host.
🙏 Acknowledgements
Team ELITESYNC – built for the 2026 hackathon at SOA ITER.
Open‑source libraries – lucide-react, vite, react, and the Antigravity framework.
📄 License

The project is released under the MIT License – feel free to fork, remix, and use it in your own demos.
