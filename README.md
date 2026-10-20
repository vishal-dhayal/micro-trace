# MicroTrace — Forensic Hair Analysis Prototype

## Run locally
1. Extract the ZIP.
2. Open the `MicroTrace_Forensic` folder in VS Code.
3. Open `index.html` with Live Server (recommended), or open it in a modern browser.
4. Open an evidence record to see its microscopy image and metadata. Choose **View evidence** or **View report** from the register; saved reports can be previewed and downloaded as PDF.

## Included files
- `index.html` — application interface and views
- `styles.css` — dark forensic/microscopy-inspired theme
- `app.js` — evidence register, image upload, exploratory image processing, report preview, PDF and JSON exports
- `assets/microscopy_reference_1.jpg`, `assets/microscopy_reference_2.jpg` — illustrative microscopy-style reference images

## Scope and limitations
- Seven preloaded records are included with distinct evidence IDs and specimen descriptions. Two use provided illustrative microscopy-style reference images; the remaining records use generated illustrative images.
- Reference images and example measurements are for interface demonstration/training, not verified human/animal specimens or laboratory findings. They should not be represented as real case evidence.
- PDF reports can be downloaded from the Reports view or evidence detail. Reports summarize saved analysis values and clearly state limitations.
- Image thresholding and connected-region measurements are exploratory outputs; they do not guarantee hair shaft detection or biological object segmentation.
- This prototype does not implement validated automatic medulla segmentation, cuticle classification, or human-versus-animal/species classification.
- Medullary index is not calculated unless the example path explicitly supports an illustrative value; real uploaded images default to not measurable because there is no validated medulla segmentation engine.
- Comparison currently compares basic image statistics, not validated hair morphology or source identity.
- Browser localStorage is not secure evidence storage and does not constitute a validated chain-of-custody audit trail.
- Do not use this prototype as the basis for forensic conclusions. Validate image algorithms against independently labelled reference samples before making forensic classification claims.
