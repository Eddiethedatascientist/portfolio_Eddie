# Eddie Nguyen — Portfolio (v6)

Static site: `index.html` + `assets/`. Open `index.html` in a browser to preview; edit it with Notepad or VS Code.

## What changed in v5
- Engagement (Ambassador, VSAF) and Media show the **first 3 items** as cards with a cover photo.
  If there are more than 3, a **"View all N ↓"** button expands the rest ("Show less ↑" collapses).
- Clicking a card opens a detail window: full description, role/date, a link button, and all photos with captions.
  Clicking a photo enlarges it.
- Media has filters (All / Video / Posts & social / Blogs & campaigns).
- The first 3 items are the teaser, so **put your strongest items first** in each list.

## Where to edit (in `index.html`, block `const DEFAULT`, search with Ctrl+F)
Each event (`ambassador:`, `vsaf:`) and media item (`media:`) accepts:

```js
{title:"Tên sự kiện", date:"October 2025", role:"Vai trò",
 outcome:"Mô tả ngắn hiện trên thẻ (3 dòng).",
 long:"Mô tả đầy đủ hiện khi bấm vào (tùy chọn, xuống dòng được).",
 link:"https://www.instagram.com/p/...", linkLabel:"View Instagram post ↗",
 images:["assets/a-1.jpg", {src:"assets/a-2.jpg", caption:"Chú thích ảnh"}]},
```
- The first image in `images` is the card cover. Without images the card shows a coloured tile.
- `link` must start with `https://` or `assets/`. `linkLabel`, `long` and captions are optional.
- Media items use `type:"video"`, `"social"` or `"written"` and `description:` instead of `outcome:`/`date`/`role`.
- Projects: same `images`, plus `code:"https://github.com/..."` and `case:"..."`.
- Do not use straight double quotes `"` inside text; keep commas and brackets.

## Before publishing
1. `LINKS` (top of `<script>`): github, linkedin, email. Empty = button hidden.
2. Files in `assets/`: `hero-1.jpg` … `hero-5.jpg`, `portrait.jpg`, `Eddie_Nguyen_CV.pdf`, and your evidence photos.
3. Check GPA 4.93/5 and 92 ECTS against your transcript.
4. GitHub Pages: upload the folder contents, then Settings → Pages → Deploy from branch → main / root.

## v6 additions
- Footer social icons (Facebook, LinkedIn, Instagram, Email). All links are DEFAULTS: edit the `LINKS` block at the top of `<script>`
  (`facebook`, `linkedin`, `instagram`, `github`, `email`, `cv`). Set a value to `""` to hide that icon/button.
- VSAF list now starts with "Get Together 2026" (Event Lead, ongoing). Add photos, description (`long`) and links to it in the `vsaf:` list.
