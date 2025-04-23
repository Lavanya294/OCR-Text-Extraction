# OCR-Text-Extraction
  
This project implements a complete pipeline for image processing and text extraction using **OpenCV**, **Tesseract OCR**, and **Python**. It includes advanced preprocessing techniques like noise removal, sharpening, resizing, and text recognition—along with targeted data extraction such as **dates** and **MRP (Maximum Retail Price)**.



## Features

- **Image Display & Processing**
  - Display using Matplotlib
  - Inversion, binarization, grayscale, resizing, and sharpening

- **Noise Removal**
  - Dilation, erosion, morphological transformations, and median blurring

- **OCR Text Extraction**
  - Extract text from processed images using Tesseract OCR

- **Date & MRP Extraction**
  - Identify expiration/manufacture dates and MRP from text using Regex



## Requirements

Ensure the following Python libraries are installed:

```bash
pip install opencv-python matplotlib numpy pytesseract
```

### Additional Setup:
Install **Tesseract OCR** and configure the path:

- [Download Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- Update the path in the code:
```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```



## Project Workflow

1. **Load Input Image**  
2. **Invert Colors** – `cv2.bitwise_not`  
3. **Grayscale Conversion**  
4. **Binarization** – Thresholding  
5. **Noise Removal** – Dilation, erosion, blurring  
6. **Resize & Sharpen** – For better OCR results  
7. **Text Extraction** – Using Tesseract OCR  
8. **Date & MRP Extraction** – With regular expressions



## Code Structure

- `display()`: View image states  
- `noise_removal()`: Clean image  
- `resize_image()`: Resize for better OCR  
- `sharpen_image()`: Enhance details  
- Tesseract: Extract raw text  
- Regex: Find expiration dates and MRP values



## How to Run

```bash
git clone https://github.com/Lavanya294/ocr-text-extraction.git
cd ocr-text-extraction
pip install opencv-python matplotlib numpy pytesseract
python script_name.py
```

Make sure to update the path to Tesseract executable in the script.



## Sample Output

**Extracted Text:**
```
Manufactured on: 05-05-2022  
Expires on: 05-05-2024  
MRP: Rs. 249.50
```

**Processed Output:**
```
Expiration Date: 05/2024  
MRP: 249.5
```



## Output Files

- `inverted.png`  
- `gray.png`  
- `im_bw.png`  
- `noise.png`  
- `resized.png`  
- `sharpened.png`



## Future Enhancements

- Add deskewing for rotated images  
- Support for multiple languages  
- Improve regex patterns for complex formats  



## License

This project is open-source under the **MIT License**.



## Author
Lavanya Gupta
