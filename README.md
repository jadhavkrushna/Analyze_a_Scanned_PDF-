# Analyze a Scanned PDF

This project demonstrates how to extract text and structured data from a scanned PDF document using Optical Character Recognition (OCR). It uses Python with libraries like PyMuPDF, Tesseract, OpenCV, and Pillow.

## Features

- Loads a scanned PDF.
- Converts PDF pages to images.
- Pre-processes images to improve OCR accuracy (grayscale, contrast, sharpness, filtering, thresholding).
- Extracts text from the images using Tesseract OCR.
- Extracts structured data (like names, dates, amounts) using regular expressions.
- Draws bounding boxes around detected words and key fields on the document image.

## Dependencies

- `tesseract-ocr`
- `pymupdf`
- `pytesseract`
- `opencv-python`
- `pillow`

## How to Run

1.  Install the required dependencies.
2.  Update the Tesseract path in the notebook if you are on Windows.
3.  Update the path to your scanned PDF file.
4.  Run the cells in the Jupyter Notebook sequentially.
