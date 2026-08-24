# rainjinl.github.io

Rain Liu's personal site. Night-lake visual system shared with《篝火与彗星》:
`#10151B` ground / `#E9E2D4` ink / `#E58A45` ember / `#82D4BE` comet · Noto Serif SC + IBM Plex Mono.

## Deploy (first time)

```bash
cd /c/Rain/Projects/rainjinl.github.io
git init
git add .
git commit -m "Site skeleton"
```

Then on github.com: create a new **public** repo named exactly `RainJinL.github.io`, and:

```bash
git remote add origin https://github.com/RainJinL/RainJinL.github.io.git
git branch -M main
git push -u origin main
```

Site goes live at https://rainjinl.github.io within a few minutes
(Settings → Pages should show "Deploying from branch main" automatically).

## Update photos

Drop images into `photos/` and replace each placeholder in `index.html`:

```html
<div class="ph">PHOTO COMING</div>
<!-- becomes -->
<img src="photos/tsuchinshan_2024.jpg" alt="Comet Tsuchinshan–ATLAS over Beijing, Oct 2024">
```

Keep files under ~500 KB each (export ~1600px wide JPEG, quality 80).

## TODO

- [ ] Add real photos (6 slots marked PHOTO COMING)
- [ ] Rocky Worlds write-up — after the challenge closes
- [ ] Custom domain later: buy one, add `CNAME` file, done (GitHub Student Pack gives a free year)
