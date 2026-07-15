# Kris's Plugin Marketplace

A Claude plugin marketplace that distributes **DPI Demand Finder** with update support. Unlike sharing a loose `.plugin` file, installing from here means recipients get notified (and can update) whenever a new version is pushed.

## Publish it (one time)

1. Create a new GitHub repo (public, or private if your group has access to it).
2. Put these files at the repo root and push:
   ```
   git init
   git add .
   git commit -m "DPI Demand Finder marketplace v1.0.0"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```

## Share it with your group

Send them two commands:
```
/plugin marketplace add <your-username>/<repo>
/plugin install dpi-demand-finder@kris-dpi-marketplace
```
(Cowork desktop users: add the marketplace from the Marketplace screen using the same repo, then install DPI Demand Finder.)

## Ship an update

1. Edit the plugin under `plugins/dpi-demand-finder/`.
2. Bump the `version` in `plugins/dpi-demand-finder/.claude-plugin/plugin.json` (e.g. `0.1.0` → `0.2.0`). **This is what tells everyone an update exists** — if you don't bump it, no update is delivered.
3. Optionally bump `version` in `.claude-plugin/marketplace.json` too.
4. Commit and push.

On each recipient's next launch, Claude checks this repo, sees the new version, and notifies them; they run `/reload-plugins` (or it loads next start). Their in-progress work is never interrupted mid-session.

## Layout

```
.claude-plugin/marketplace.json      ← lists the plugin (this is what makes it a marketplace)
plugins/dpi-demand-finder/           ← the actual plugin (self-contained)
```

The marketplace points at the plugin with a local path (`./plugins/dpi-demand-finder`), so this one repo is fully self-contained — no second repo or GitHub username baked in.
