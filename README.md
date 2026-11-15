# SignalTrace

**Connectivity diagnostics made understandable.** SignalTrace is a standalone browser application for people troubleshooting unreliable home internet connections.

## Try it

Visit[ https://adanikamal.github.io/SignalTrace/](https://signal-trace-khaki.vercel.app/).

## What it does

- Displays a blue/red speedometer for download and upload transfer estimates.
- Sends five cache-busted HTTP requests to the hosted SignalTrace page and reports response durations and success count.
- Attempts 1 MB download and 256 KB upload transfers through Cloudflare's public speed-test endpoints (browser/network restrictions may prevent measurements).
- Collects reported symptoms and troubleshooting steps, then prepares a support-ready report.
- Supports copying, downloading as TXT, and printing or saving as PDF.

No npm, Node.js, backend, database, or build process is needed. The app is contained in `index.html`.

## Publish with GitHub Pages

Go to **Settings → Pages → Build and deployment**, select **Deploy from a branch**, then choose **main** and **/(root)** and save.

## Measurement limitations

HTTP request duration is not ICMP ping, and HTTP request failures are not packet loss. The short transfer tests are approximate, not a substitute for full multi-sample speed tests. Measurements depend on Cloudflare's endpoint accessibility and the tested route. Browser online status is only an indicator. User reports are unverified and SignalTrace does not confirm ISP outages.

Testing contacts Cloudflare, which can receive connection data including IP address. No customer account or backend storage is used.

## Version history

| Version | Changes |
|---|---|
| v1.0 | Single-file release: speedometer, browser HTTP and short transfer checks, symptom questionnaire, recommendations, support-report export. |

**SignalTrace · 2026**
