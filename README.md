# rajimo-apps.github.io (the GitHub *user* site)

Only purpose: serve `/.well-known/assetlinks.json`, so Android opens Calenzo event
links (`https://rajimo-apps.github.io/calenzo/e/#…`) directly in the app.
App Links are verified at the root of the domain, which only the repository named
exactly `rajimo-apps.github.io` can serve; the Calenzo site itself stays in the
`calenzo` repository (`/calenzo/…`).

Upload to the repository `rajimo-apps.github.io`:
- `.well-known/assetlinks.json` (first fingerprint = Play App signing key, taken from the
  Play API generatedApks on 2026-10-26; second = upload key, for builds installed by hand)
- `.nojekyll` (empty file: without it GitHub Pages skips folders starting with '.')
- `README.md` (optional, this file)

Check after publishing: https://rajimo-apps.github.io/.well-known/assetlinks.json
