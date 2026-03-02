# EgyID
# EgyID — Egyptian ID Front-Side Detection + OCR Pipeline (Colab)

A multi-stage computer vision pipeline that detects key fields on Egyptian ID **front-side** images and extracts the **14-digit national ID number** into structured JSON. Built and executed in **Google Colab** using **Ultralytics YOLOv8** for detection and **EasyOCR** for OCR.

> Current milestone: front-side ID number extraction is working end-to-end.  
> Result in the current run: **13/22** front images produced a valid 14-digit ID.

---

## What this project does

### Inputs
- Front-side Egyptian ID images (dataset exported from Roboflow in YOLO format)

### Outputs
- Cropped field images (from detections)
- OCR CSV outputs
- Final structured JSON (front only for now)

Example output (Layer 6):
```json
[
  { "doc_id": "ID177", "front": { "id_number": "30603103722043" }, "back": null },
  { "doc_id": "ID178", "front": { "id_number": "30801031235728" }, "back": null }
]
