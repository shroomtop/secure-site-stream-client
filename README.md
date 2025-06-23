# secure-site-stream-client

> **Front-end Client for Secure, Zero-Code-Leak Video Streaming of Private Web Apps**  
> **by Shroomtop420™**

---

## What is this?

`secure-site-stream-client` is a **single-file HTML5 web client** that lets users securely interact with a private website via an encrypted real-time video stream.  
- **Users see only a live, interactive video feed.**  
- **No site code, DOM, or logic is ever sent to the browser.**  
- **All mouse/keyboard input is relayed securely to the backend server.**  
- **Zero attack surface from the client side—no “View Source,” no code leaks, no XSS or injection risk.**

---

## Key Features

- ⚡️ **Glassmorphic, PWA-ready UI**: Modern, mobile-optimized, and installable.
- 🔒 **No code ever delivered**: Only pixels are shown. All logic runs server-side.
- 📡 **WebRTC + Socket.io signaling**: Real-time, low-latency, peer-to-peer connection.
- 🖱 **Full input capture**: Mouse and keyboard input routed to backend, just like a remote desktop.
- 🗄 **IndexedDB stub**: Ready for audit logs or session persistence.
- 🪟 **Fullscreen & mobile support**: UX is maximized for all devices.
- 📝 **MIT Licensed**: Free to use, modify, and extend.

---

## How It Works

1. **User opens this HTML file in their browser.**
2. **Clicks “Connect”** – a WebRTC connection is established to your secure backend.
3. **The backend runs a real browser (e.g. browserless/chrome + puppeteer-stream)**, rendering your private web app.
4. **A live video feed is streamed to the client.**
5. **All mouse and keyboard events are relayed to the backend**, allowing full interaction.
6. **No source code, HTML, CSS, JS, or sensitive assets are ever sent to the user device.**

---

## Architecture

```text
User Browser (HTML5 Client)
   │  (WebRTC + Socket.io)
   ▼
Reverse Proxy (Nginx, Caddy)
   │
App Server (Headless Chrome + Video Pipeline)
   │
Private Web App (never public)