# Interview Prep Progress

## Block 1: Document Structure Ingestion & Format Router (`src/raster_checker.py`)
- [ ] Q1 (High) [Decision]: An evaluator asks: "Why don't you just check if a PDF contains any embedded images? If `image_count > 0`, route it to OCR; otherwise, treat it as digital vector." Why does this naive logic fail catastrophically on real hospital prescriptions?
- [ ] Q2 (High) [Math-And-Constant]: In `src/raster_checker.py`, what are the exact thresholds for character count and image count that trigger the `SCANNED_RASTER` route, and why do we check both per-page and whole-document?
- [ ] Q3 (Medium) [Bug-Injection]: Suppose someone uploads an empty clinic vector template or blueprint with zero selectable text and zero embedded images (`char_count = 0`, `image_count = 0`). What does the router do, and what bug would happen if it defaulted to raster?
