# 🚀 SmartOCR

**SmartOCR** is a comprehensive OCR project designed to compare and analyze the performance of **PaddleOCR** and **TrOCR**. It extracts text from images, visualizes bounding boxes, and merges outputs from both OCR engines for an in-depth comparison.

---

## 🎯 Features

- **Text Extraction** using **PaddleOCR** and **TrOCR**  
- **Merged Output** for combined analysis  
- **Visualization** with color-coded bounding boxes  
- **Export** OCR results to **CSV** and **JSON**  
- **Comparison** of OCR accuracy and coverage  

| Color | OCR Engine |
|-------|------------|
| 🔴 Red | PaddleOCR |
| 🔵 Blue | TrOCR |

---

## 🗂️ Project Structure

```text
SmartOCR/
│
├─ PaddleOCR + Results/
│   ├─ 01-paddle-detector.ipynb
│   └─ results/                 # Bounding boxes, extracted text, JSON/CSV
│
├─ TrOCR + Results/
│   ├─ 02-trocr-detector.ipynb
│   └─ trocr_results/           # TrOCR outputs (CSV/JSON)
│
├─ Comparison/
│   ├─ Comparison_Visuals.ipynb
│   └─ ocr_combined/            # Merged blocks and visualizations
│
├─ dataset/
│   └─ ocr-testing-images/      # Input images
│
└─ requirements.txt
```
 ## ⚡ Quick Start
1️⃣ Clone the repository
```bash
git clone https://github.com/jawad-ahmad1/SmartOCR.git
cd SmartOCR
```
2️⃣ Install dependencies
```bash
pip install -r requirements + instrucitons.txt
```
3️⃣ Run notebooks in order
| Notebook                   | Description                         |
| -------------------------- | ----------------------------------- |
| `01-paddle-detector.ipynb` | Extract text using PaddleOCR        |
| `02-trocr-detector.ipynb`  | Extract text using TrOCR            |
| `Comparison_Visuals.ipynb` | Merge outputs and visualize results |

## 📌 Notes & Findings
TrOCR Performance
TrOCR can be less reliable, especially on small datasets or models that have been fine-tuned on limited data.

Visualization Convention

🔴 Red = PaddleOCR

🔵 Blue = TrOCR

LayoutLM / DocTR Integration
Integration was attempted but omitted due to environment constraints and compatibility issues.

Merged Analysis
Combining outputs from both OCR engines provides a clearer comparison of detected text and bounding boxes.

Bounding Box Observations
PaddleOCR tends to detect more precise boxes for printed text, while TrOCR may sometimes produce one large bounding box around the whole image.

## 🛠️ How It Works

PaddleOCR detects text blocks in images and outputs bounding boxes, text, and confidence scores.

TrOCR extracts text, optionally providing bounding boxes.

Comparison Notebook merges both outputs into a single data structure with source labels (paddle or trocr).

Visualization draws bounding boxes on the original image for a color-coded comparison.

Exports combined results to CSV and JSON for further analysis.

## 📌 License

This project is released under the MIT License, free to use, modify, and distribute.


Made with ❤️ by Jawad Ahmad


