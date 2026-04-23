# AITM Demo

An interactive, browser-based visualization of an **Adversary-in-the-Middle (AiTM)** phishing attack — built for a live classroom presentation on MFA bypass via Evilginx2-style session hijacking.

Watch a fake Microsoft login proxy capture credentials, intercept MFA, and steal the session cookie in 6 animated steps — ending with a full session replay.

## Run it

Open `index.html` directly in a browser, or serve locally:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Or deploy to Vercel / Netlify / GitHub Pages — it's a single static file.

## Controls

| Key | Action |
|---|---|
| `Space` / `→` / `Enter` | Next step |
| `←` | Previous step |
| `R` | Reset |
| `F` | Fullscreen |
| `Esc` | Dismiss HACKED overlay |

Click the URL bar in the victim's browser to toggle between the **real** `login.microsoftonline.com` and the **fake** `login.tcucyberclass.website` — the "would you get hacked?" hook.

## The 6 steps

1. Victim clicks the phishing link
2. Proxy relays the request to Microsoft
3. Credentials captured in transit
4. MFA prompt forwarded both ways
5. Session cookie stolen
6. Attacker replays → account pwned

## Closing line

> MFA verified identity. It did not verify origin.
> That is the AiTM vulnerability.
