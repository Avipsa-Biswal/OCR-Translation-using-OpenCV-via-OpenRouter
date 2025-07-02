# 📘 OCR + Translation using OpenCV (via OpenRouter)

This project demonstrates a pipeline for **Optical Character Recognition (OCR)** and **Translation** of text from images. It uses **OpenCV** and **Tesseract** for OCR and leverages an external API (via **OpenRouter**) for language translation. The application is wrapped in an interactive UI using **Gradio**.

## 🔧 Features

* 📸 Upload or capture an image
* 🔍 Image preprocessing with **OpenCV**
* 🧠 Text extraction using **Tesseract OCR**
* 🌐 Text translation via **OpenRouter API**
* 🖼️ User interface with **Gradio**

## 🧪 Dependencies

Install all required packages :

```bash
pip install opencv-python pytesseract gradio pillow requests torchvision
```

Also ensure **Tesseract OCR** is installed on your system:

* Ubuntu: `sudo apt install tesseract-ocr`
* Windows: [Download here](https://tesseract-ocr.github.io/)

## 🧠 Workflow

1. **Image Preprocessing**: Resize, denoise, and optionally use **ResNet** to enhance image quality.
2. **OCR Extraction**: Extract text from the processed image.
3. **Translation**: Send the extracted text to OpenRouter for translation.
4. **Display**: Show original image, detected text, and translated output.

## 📁 Project Structure

```
OCR_+_Translation_using_OpenCV(via_OpenRouter).ipynb
README.md
```

## 🔑 API Note

Make sure to set up your **OpenRouter API key** before running the app. It should be passed in the headers for translation requests.

## ✅ Example Use Case

* Translate handwritten or printed documents.
* Translate menus, signs, or product labels from images.

## 🚀 Run the App

```python
!gradio app.py  # or run the notebook cells directly
```
