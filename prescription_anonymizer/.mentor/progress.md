# Interview Prep Progress Bank (v3)

Q1 | High | Defense | B0 | | streak:0 | last: | due:s1 | In War Story 1, what caused over 90 benign clinical lines to be blacked out, and how did the Sobel gradient ratio test fix it?
Q2 | High | Defense | B0 | | streak:0 | last: | due:s1 | In War Story 2, why did OpenCV barcode detector miss the right-hand barcode on Aryan March 26, and how does the sliding window fix it?
Q3 | High | Defense | B0 | | streak:0 | last: | due:s1 | In War Story 3, what three separate bugs exposed the patient name on Aryan March 25, and how did symmetric midpoint clamping resolve it?
Q4 | High | Defense | B0 | | streak:0 | last: | due:s1 | In War Story 4, why did the microservice crash with OOM on 512MB cloud tiers, and how does the display-list painting and 100 DPI bake architecture resolve it?
Q5 | High | Decision | B1 | | streak:0 | last: | due:s1 | In src/raster_checker.py, why not classify a document as SCANNED_RASTER purely based on image presence (image_count > 0)?
Q6 | High | Numbers | B1 | | streak:0 | last: | due:s1 | What are the exact thresholds for character and image counts that trigger SCANNED_RASTER, and why is there both a page-level and doc-level check?
Q7 | High | Mechanism | B1 | | streak:0 | last: | due:s1 | If an empty CAD blueprint or vector clinic drawing is uploaded with char_count=0 and image_count=0, which route does it take and why?
Q8 | Medium | Trace | B1 | | streak:0 | last: | due:s1 | Trace Apollo Digital PDF (char_count=2412, image_count=1) through inspect_pdf_structure and state the exact output dictionary.
Q9 | Medium | Bug | B1 | | streak:0 | last: | due:s1 | Look at inspect_pdf_structure with char_count < 20 changed to char_count < 200. What silent failure occurs on short digital intake slips?
Q10 | Medium | LiveMod | B1 | | streak:0 | last: | due:s1 | If the examiner asks you to support scanned PDFs containing hidden OCR text layers without re-running Tesseract, what line in src/raster_checker.py do you modify?
Q11 | High | Decision | B2 | | streak:0 | last: | due:s1 | Why must vector redaction use page.apply_redactions() with garbage=4 rather than painting black rectangles via page.draw_rect()?
Q12 | High | Numbers | B2 | | streak:0 | last: | due:s1 | Why is the whitelist IoU overlap threshold set to 0.85, and what breaks if set to 0.40 vs 0.95?
Q13 | High | Mechanism | B2 | | streak:0 | last: | due:s1 | What happens if PII is redacted from page text but the PDF metadata dictionary is left untouched?
Q14 | Medium | Trace | B2 | | streak:0 | last: | due:s1 | Trace a candidate box touching a whitelisted drug by 0.15 IoU through the boundary clamping formulas in src/vector_redactor.py.
Q15 | Medium | Bug | B2 | | streak:0 | last: | due:s1 | Look at redact_vector_pdf with doc.save garbage=4 omitted. What forensic vulnerability is left in the output PDF?
Q16 | Medium | LiveMod | B2 | | streak:0 | last: | due:s1 | If an examiner asks you to make redactions transparent red boxes for auditing instead of black boxes, which exact function call do you edit?
Q17 | High | Decision | B3 | | streak:0 | last: | due:s1 | Why do we use tile-based LAB CLAHE instead of standard global Otsu thresholding for camera clicks?
Q18 | High | Numbers | B3 | | streak:0 | last: | due:s1 | In visual line reconstruction, what do the magic numbers 0.45 overlap and 0.35 vertical center drift control?
Q19 | High | Mechanism | B3 | | streak:0 | last: | due:s1 | Why does visual line reconstruction update a running mean vertical center rather than using a static horizontal ruler?
Q20 | Medium | Trace | B3 | | streak:0 | last: | due:s1 | Trace a word token at y_mid=114.2 against an existing line at running center 113.8 through reconstruct_visual_lines.
Q21 | Medium | Bug | B3 | | streak:0 | last: | due:s1 | What happens if reconstruct_visual_lines appends words to a line without recomputing l_mid as a running average?
Q22 | Medium | LiveMod | B3 | | streak:0 | last: | due:s1 | If camera scans come in with 15-degree paper rotations, which threshold in reconstruct_visual_lines breaks first?
Q23 | High | Decision | B4 | | streak:0 | last: | due:s1 | Why does the system use morphological line erasure rather than relying on Tesseract OCR to read handwritten cursive patient names?
Q24 | High | Numbers | B4 | | streak:0 | last: | due:s1 | Why are the morphological ruler kernels set to (25, 1) and (1, 25), and why is ink density gated between 0.012 and 0.65?
Q25 | High | Mechanism | B4 | | streak:0 | last: | due:s1 | Why wrap detected cursive ink with cv2.boundingRect rather than blacking out the entire printed form box?
Q26 | Medium | Trace | B4 | | streak:0 | last: | due:s1 | Trace an empty form box with printed border lines through detect_handwritten_fill_in_zone and explain why 0 ink pixels remain.
Q27 | Medium | Bug | B4 | | streak:0 | last: | due:s1 | What silent bug happens if the upper ink ratio bound 0.65 is increased to 0.95 in detect_handwritten_fill_in_zone?
Q28 | Medium | LiveMod | B4 | | streak:0 | last: | due:s1 | If a hospital form uses dotted underline guides instead of solid lines, how do the morphological rulers need to be adapted?
Q29 | High | Decision | B5 | | streak:0 | last: | due:s1 | Why does OpenCV BarcodeDetector silently fail on 30MP phone photos unless sliced into sliding window tiles?
Q30 | High | Numbers | B5 | | streak:0 | last: | due:s1 | Why is the Sobel gradient polarity ratio threshold set to 2.2, and what breaks if it is lowered to 1.2?
Q31 | High | Mechanism | B5 | | streak:0 | last: | due:s1 | How does Sobel gradient polarity physically distinguish a 1D barcode from a paragraph of dense English text?
Q32 | Medium | Trace | B5 | | streak:0 | last: | due:s1 | Trace an overlapping barcode detected in both tile 1 and tile 2 through the IoU > 0.40 deduplication gate.
Q33 | Medium | Bug | B5 | | streak:0 | last: | due:s1 | What happens if sliding tile stride is increased from 0.20 to 0.45 in detect_barcodes_sliding_window?
Q34 | Medium | LiveMod | B5 | | streak:0 | last: | due:s1 | If prescriptions contain QR codes in addition to 1D barcodes, how does the detector route them differently?
Q35 | High | Decision | B6 | | streak:0 | last: | due:s1 | Did you hardcode patient names in your NER engine, and why strip parsers from spaCy en_core_web_sm?
Q36 | High | Numbers | B6 | | streak:0 | last: | due:s1 | How many universal pharmacological suffixes protect medications, and why is minimum entity length set to 4 chars?
Q37 | High | Mechanism | B6 | | streak:0 | last: | due:s1 | What happens when an aggressive NER model mistakes brand-name antibiotic Augmentin for a person name?
Q38 | Medium | Trace | B6 | | streak:0 | last: | due:s1 | Trace the sentence 'Patient Rahul Sharma prescribed Pantoprazole 40mg' through find_entities.
Q39 | Medium | Bug | B6 | | streak:0 | last: | due:s1 | What catastrophic clinical failure occurs if is_whitelisted() check is omitted from the NER loop?
Q40 | Medium | LiveMod | B6 | | streak:0 | last: | due:s1 | If the engine is deployed in a German hospital, what environment variable controls whether multi-lingual models are loaded?
Q41 | High | Decision | B8 | | streak:0 | last: | due:s1 | Explain the 'Sticker vs Photocopy' architecture: why does draw_rect use 0 MB, and why is the 100 DPI bake necessary?
Q42 | High | Numbers | B8 | | streak:0 | last: | due:s1 | Why bake at 100 DPI instead of 300 DPI, and why set MALLOC_ARENA_MAX=2?
Q43 | High | Mechanism | B8 | | streak:0 | last: | due:s1 | Why isn't Python's gc.collect() sufficient to prevent cloud memory crashes on Render?
Q44 | Medium | Trace | B8 | | streak:0 | last: | due:s1 | Trace resident memory (RSS) from upload (30MP) through OCR, vector painting, flattening bake, and malloc_trim(0).
Q45 | Medium | Bug | B8 | | streak:0 | last: | due:s1 | What security vulnerability exists if the flattening bake is skipped and the PDF is saved with draw_rect only?
Q46 | Medium | LiveMod | B8 | | streak:0 | last: | due:s1 | If your cloud container is upgraded to 8GB RAM, what code change restores native 600 DPI print quality?
