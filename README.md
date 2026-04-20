# Adhyapakh Notes

A Jekyll-powered portal for purchasing and downloading lecture notes from the YouTube channel [Ranji Raj](https://www.youtube.com/@RanjiRaj18).

## Subjects Available

| Subject | Price |
|---|---|
| Artificial Intelligence | ₹200 |
| Data Mining & Business Intelligence | ₹100 |
| Simulation Notes | ₹250 |
| Cloud Computing | ₹200 |
| Wireless Technology | ₹200 |

## How It Works

1. Students browse the subject catalog on the homepage
2. On a subject page, they scan the UPI QR code or tap the **Pay via UPI** button
3. After payment, they download the PDF directly

> **Note:** The payment integration is currently a work in progress (WIP).

## Project Structure

```
_config.yml          # Jekyll configuration
_subjects/           # Subject markdown files (front matter defines price, PDF path, etc.)
_layouts/            # Page templates (default, subject)
_includes/           # Reusable partials (nav)
assets/
  css/style.css      # Site styles
  pdfs/              # PDF files for download
index.html           # Homepage
```

## Local Development

```bash
# Install dependencies
gem install jekyll webrick

# Serve locally
jekyll serve --port 4000
```

Then open http://localhost:4000.

## Adding / Updating a Subject

Create a new file in `_subjects/` (e.g. `_subjects/new-subject.md`):

```yaml
---
title: New Subject
description: Brief description of the notes.
price: 200
icon: "📘"
pdf_file: /assets/pdfs/new-subject.pdf
topics:
  - Topic 1
  - Topic 2
---
```

Place the corresponding PDF in `assets/pdfs/`.

## License

All rights reserved. Notes are for personal use only and may not be redistributed.

## Co-Authors

- [u778589_lhgroup](https://github.com/u778589_lhgroup)
