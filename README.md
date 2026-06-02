# Text Recognition Using OCR

This project is a simple Optical Character Recognition (OCR) system that extracts readable text from an image using Python, OpenCV, and Tesseract OCR.

The project was completed as part of the DecodeLabs Artificial Intelligence Internship.

## Project Overview

The goal of this project is to build a basic AI text recognition pipeline. The program loads an image, preprocesses it to improve text clarity, applies OCR using Tesseract, and displays the extracted text.

The pipeline follows these steps:

1. Load a sample image
2. Display the original image
3. Resize the image if needed
4. Convert the image to grayscale
5. Apply Gaussian blur
6. Apply adaptive thresholding
7. Extract text using pytesseract
8. Display the final OCR result
9. Check OCR confidence
10. Save the extracted text to a file

## What is OCR?

OCR stands for Optical Character Recognition. It is a technology that allows computers to read and extract text from images, scanned documents, receipts, screenshots, and printed pages.

## Technologies Used

* Python
* Jupyter Notebook
* OpenCV
* pytesseract
* Tesseract OCR
* Matplotlib
* Pandas

## Project Files

```text
AI_Text_Recognition_OCR_p4.ipynb
```
Main notebook containing the full OCR pipeline.


```text
ocr_extracted_text.txt
```
Output file containing the extracted text from the image.


## How the Project Works

First, the image is loaded using OpenCV. If the image is too large, it is resized to make the OCR process faster and more stable.

Then, the image is converted to grayscale because OCR works better when unnecessary color information is removed.

After that, Gaussian blur is applied to reduce noise, and adaptive thresholding is used to make the text stand out clearly from the background.

Finally, Tesseract OCR is used to extract text from the processed image. The extracted text is displayed in the notebook and can also be saved into a text file.

## OCR Confidence Check

The project also includes a confidence check using `pytesseract.image_to_data()`. This helps evaluate how confident the OCR model is about the detected words.

This step makes the output more reliable because it does not only extract text, but also gives an idea of how accurate the recognition is.

## Installation

Install the required Python libraries:

```bash
pip install opencv-python pytesseract matplotlib pandas
```

For Linux or Ubuntu, install Tesseract OCR:

```bash
sudo apt update
sudo apt install tesseract-ocr
```

If needed, set the Tesseract path inside the notebook:

```python
pytesseract.pytesseract.tesseract_cmd = "/usr/bin/tesseract"
```

## How to Run

1. Open the notebook in Jupyter Notebook.
2. Place your image file in the same folder as the notebook.
3. Change the image file name in the `image_path` variable.
4. Run the notebook cells from top to bottom.
5. View the extracted text and confidence results.

Example:

```python
image_path = "OCR_Test_Image.png"
```

## Example Output

The system displays:

* The original image
* The grayscale image
* The blurred image
* The thresholded image
* The extracted text
* The OCR confidence score

## What I Learned

Through this project, I learned how OCR systems work and how image preprocessing affects text recognition accuracy. I also learned how to use OpenCV to prepare images before applying Tesseract OCR.

This project helped me understand that AI results depend heavily on input quality. A clear image with good lighting and readable text gives much better OCR results than a blurry or noisy image.

## Conclusion

This project successfully demonstrates a basic OCR pipeline using Python. It extracts text from images, improves recognition through preprocessing, and evaluates the result using confidence scores.

Although the system works well on clear printed text, it may struggle with blurry images, handwriting, poor lighting, or complex backgrounds. Future improvements could include automatic parameter selection, deskewing tilted images, and testing the system on different types of documents.

