# SeenZone ✓✓

Drop in a WhatsApp chat and swipe through the receipts on your friendship: who texts first, who ghosts, who's up at 2am, and who's carrying it.

## How it works

- **One file.** The whole site is `index.html`. Fonts and libraries are embedded, so there is no build step and no dependencies to install.
- **Private by design.** Chats are read and analysed entirely in the browser. Nothing is uploaded or stored. `netlify.toml` sets a Content-Security-Policy with `connect-src 'none'`, so the browser blocks the page from making any network request at all.
- **Two voices.** Captions switch automatically between a global voice and a desi (Hinglish) voice based on the chat, or manually with the Auto / Global / Desi switch.

## Supported exports

- WhatsApp on Android (`.txt`) and iPhone (`.zip` or `_chat.txt`), exported **without media**.
- WhatsApp caps exports at 40,000 messages, dropping the oldest. The site says so on the cover card when an export hits the cap.

## Deploying

Connected to Netlify: every push to `main` redeploys automatically. Settings live in `netlify.toml` (publish directory is the repo root).

## Before going public

- Set `SITE_URL` near the top of the second `<script>` in `index.html` so call-outs carry the link.
- Replace `[add your contact email]` in the privacy policy.

## Credits

Fonts: Instrument Serif, Onest, Caveat, Permanent Marker, Patrick Hand (SIL Open Font License 1.1).
Libraries: JSZip 3.10.1 (MIT), html2canvas 1.4.1 (MIT).

Not affiliated with WhatsApp, Instagram or Meta Platforms, Inc.
