# Egocentric segmentation · Team updates

Live page: `https://YOUR-USERNAME.github.io/egocentric-updates/`

Only `data.json` needs editing. `index.html` holds the design; leave it as it is.

## Add a client update

Open `data.json` → pencil icon → find `"updates": [`.

**Same day already exists?** Add an item inside that date's `"items"` list.
**New day?** Paste a new date block right after `"updates": [` so the newest stays on top:

```json
{
  "date": "2026-10-22",
  "items": [
    {
      "topic": "Camera motion",
      "text": "Write the update here.",
      "images": []
    }
  ]
},
```

Optional fields for an item:

```json
"points": ["Sub-point one", "Sub-point two"],
"previous": ["Verb: wipes"],
"now": ["Verb: mops"],
"images": ["mop-example.jpg"]
```

Topics: `Segments`, `Objects`, `Bounding boxes`, `Verbs & actions`, `Locations`, `Camera motion`, `Other field`.

## Add a common mistake

Inside `"mistakes": [ ]`:

```json
{
  "topic": "Camera motion",
  "title": "Marking idle in camera motion",
  "details": "If the camera doesn't move, leave the field blank.",
  "wrong": ["Camera motion: idle"],
  "right": ["Camera motion: (blank)"],
  "images": []
}
```

## Update performance

Fill in `"period"` and the `"name"` / `"note"` of the five rows in `"top"` and `"bottom"`.

## Add an image

1. Open the `images` folder → **Add file → Upload files** → commit.
2. Put the exact file name in the entry's `"images"` list.

## Rules that prevent a broken page

- Every entry except the last one in a list ends with a comma.
- Text goes inside straight double quotes `"like this"`.
- If the page shows "couldn't load its content", open the file's **History** on GitHub and revert the last change, or paste the file into jsonlint.com to find the error.
- Changes appear on the live page within 1–2 minutes. Press Ctrl+F5 if you still see the old version.
