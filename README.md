# Adarsh · आदर्श

UPSC Mains topper answer copies, organized by paper and sub-topic.

## What it is

A personal vault of model answers from UPSC toppers. Six papers (GS1–4, Essay, Math Optional). Each paper has sub-topics from the standard UPSC Mains syllabus. Each sub-topic contains questions, and each question can have multiple toppers' answers (scanned handwritten copies as images).

## How to use

1. Open the app — `index.html` works standalone, no backend needed for v1.
2. Tap the **+** floating button (bottom-right) to add a topper answer.
3. Fill in: paper, sub-topic, question, marks/year, topper name, AIR rank, marks got, image URLs (one per line).
4. Image URLs should point to scanned answer images — host them anywhere (GitHub raw URLs, Cloudinary, Imgur, your Supabase Storage).
5. Browse by paper → sub-topic → question → topper's answer.

## v1 features

- ✓ 6 papers with standard UPSC syllabus seeded as sub-topics
- ✓ Add/view answer with metadata (topper, rank, year, marks got, pages)
- ✓ Image lightbox (tap any image to zoom)
- ✓ Save / bookmark answers
- ✓ Recent (last 30 viewed)
- ✓ Toppers index (browse by topper)
- ✓ Search across question text, topper name, year, topic
- ✓ Light Anthropic-inspired theme

## v2 (when ready)

- Cloud sync via Supabase (same Gmail as your other apps)
- Image upload via GitHub OAuth (commits to a `study/answers/` folder in this repo)
- Bulk import from JSON
- Filter by year, marks, rank range
- Notes per answer (what makes it good)
- Share specific answers via deep link

## Deploy

Same workflow as your other apps:

```bash
git init
git add .
git commit -m "Adarsh v1"
git remote add personal https://github.com/sauravanandb2w/adarsh.git
git push -u personal main
```

Then Netlify → Import from GitHub → Deploy.

## Data structure

Each answer is stored as:

```js
{
  id: "ans-1717..." ,
  paper: "gs2",            // gs1 | gs2 | gs3 | gs4 | essay | math
  topic: "Pressure Groups & RPA",
  question: "Critically examine...",
  marks: "15",
  year: "2022",
  topper: "Shruti Sharma",
  rank: "1",
  got: "13",
  pages: "2",
  images: ["https://.../p1.jpg", "https://.../p2.jpg"],
  notes: "Strong intro · 3 examples · clean diagram",
  createdAt: 1717760000000
}
```

Currently in `localStorage`. Will migrate to Supabase in v2.
