# Analyze a Scanned PDF

This project demonstrates how to extract text and structured data from a scanned PDF document using Optical Character Recognition (OCR). It uses Python with libraries like PyMuPDF, Tesseract, OpenCV, and Pillow.

## Features

- Loads a scanned PDF.
- Converts PDF pages to images.
- Pre-processes images to improve OCR accuracy (grayscale, contrast, sharpness, filtering, thresholding).
- Extracts text from the images using Tesseract OCR.
- Extracts structured data (like names, dates, amounts) using regular expressions.
- Draws bounding boxes around detected words and key fields on the document image.

## Requirements

- Python 3.x
- Tesseract OCR engine
- The following Python packages:
  - `pymupdf`
  - `pytesseract`
  - `opencv-python`
  - `pillow`
  - `numpy`
  - `jupyter`

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/jadhavkrushna/Analyze_a_Scanned_PDF-.git
    cd Analyze_a_Scanned_PDF-
    ```

2.  **Install Tesseract:**
    - **Windows:** Download and install Tesseract from the [official repository](https://github.com/UB-Mannheim/tesseract/wiki). Make sure to add the installation path to your system's `PATH` environment variable or update the path in the notebook:
      ```python
      pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
      ```
    - **macOS:**
      ```bash
      brew install tesseract
      ```
    - **Linux (Ubuntu/Debian):**
      ```bash
      sudo apt install tesseract-ocr
      ```

3.  **Install Python dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: You may need to create a `requirements.txt` file or install packages directly as shown in the notebook)*

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```

5.  **Open and run the notebook:**
    - Open the `Analyze_a_Scanned_PDF_project.ipynb` file in Jupyter.
    - Update the `pdf_document_path` variable to the location of your scanned PDF file.
    - Run the cells sequentially.

## Input

A scanned PDF file. The project is configured to work with a sample mortgage document, but it can be adapted for other scanned documents. You will need to provide the path to your PDF file in the notebook.

Example:
```python
pdf_document_path = r"c:\Users\adminpc\Downloads\sample_mortgage_document.pdf"
```

## Output Sample

The project produces several outputs:

1.  **Extracted Text:** A raw string of text extracted from the document.
2.  **Structured Data (JSON):** Key information extracted from the document in JSON format.
    ```json
    {
        "document_title": "Mortgage",
        "borrower_names": [
            "Ro Leading",
            "Mercia Fill",
            ...
        ],
        "lender_name": null,
        "loan_amount": null,
        "property_address": null,
        "document_dates": []
    }
    ```
3.  **Image with Bounding Boxes:** An image of the document page with bounding boxes drawn around detected words and key fields.
