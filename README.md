# HopDrop

Share notes and files between devices, right in the browser. No install, no accounts, no uploads.

**Live:** https://badmetevils.github.io/hopdrop/

## How it works

1. Open HopDrop on one device and tap **Start a room**. You get a 5-digit code and a QR code.
2. On other devices, tap **Join a room** and type the code, or scan the QR.
3. Send notes and drop files. Everyone in the room gets them.

Notes and files travel directly between devices over WebRTC. The public [PeerJS](https://peerjs.com) broker is only used to introduce devices to each other by room code.

## Good to know

- The device that started the room relays to everyone else; the room closes when it leaves.
- Received files are held in memory until downloaded, so very large files (over ~1 GB on phones) may fail.
- Some strict networks (corporate VPNs, some mobile carriers) block direct connections. Same Wi-Fi works best.

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.
