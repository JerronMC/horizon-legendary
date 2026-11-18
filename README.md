# Horizon Mod Hub (fan made, by Jerron)

Static site for GitHub Pages. Upload every file in this zip to the repo root (keep `.nojekyll`).
Settings > Pages > Deploy from branch > main / root.

## Files you may edit
- `config.js`: Launch settings (Horizon Android v1.0.1 package, APK link) and registry links.
- `mods-data.js`: snapshot of playhorizon.dev/mods (164 projects, Nov 2026). One mod per line.

## Notes on v2
- `extras.js` and `extras.css` hold the v2 features (they load after `app.js`).
- `config.js` `server`: optional counter URL returning `{online,total}` for worldwide numbers. Empty = this device only.
- `config.js` `download`: official download link template; check it matches playhorizon.dev.
- Ratings, comments, accounts and security warnings are stored in each visitor's browser. Real cross-user behaviour needs a backend.

## Old launch button (removed in v2)
Opens Horizon Android with `package` from `config.js` (`com.goydevv.horizon`, inferred from the app's file provider).
If it does not open the app, find the real package name (adb: `pm list packages | grep -i horizon`) and fix it.

## Notes
- Registry mods are listed with credit; "View" opens the mod's page on playhorizon.dev. Nothing is re-hosted.
- Icons load from horizon-rust.github.io/horizon-mods/icons (the registry's own icons).
- Accounts, posts and settings are saved in each visitor's browser only (IndexedDB).
