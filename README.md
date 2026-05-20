# defnotallc.github.io

This repository powers `https://defnotallc.github.io/` — the shared
developer site that hosts infrastructure files (e.g. `app-ads.txt`)
which must live at the host root for verification by ad networks and
app stores.

This is **not** an app site. Each app has its own repository and, where
relevant, its own GitHub Pages project site. See the table below.

## Repository layout

```
.
├── app-ads.txt           Shared across all DefNotA apps; one section per app.
├── index.html            Minimal landing page listing DefNotA's apps.
└── apps/
    └── <app-slug>/       Per-app notes, metadata, and links.
        └── README.md
```

## Why one shared `app-ads.txt`?

The IAB Tech Lab `app-ads.txt` specification requires a **single file
at the developer website's host root**. All apps under this developer
account share that single file. Each app's authorized seller lines are
grouped under a clearly labeled comment section so future apps can be
appended cleanly.

## Apps

| App | Bundle ID | Source repo | Public site |
|---|---|---|---|
| Western Dance Studio | `com.defnota.WesternDanceStudio` | [WesternDanceStudio](https://github.com/defnotallc/WesternDanceStudio) (private) | [western-dance-studio](https://defnotallc.github.io/western-dance-studio/) |

When adding a new app:

1. Add a section to `app-ads.txt` with `# --- <App Name> (<bundle.id>) ---`.
2. Add a row to the table above.
3. Create `apps/<app-slug>/README.md` with the app-specific metadata.
4. Add a link entry to `index.html`.
