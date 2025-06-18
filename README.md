# 🖼️ OCR + Translation using ResNet & Mistral (via OpenRouter)

This project extracts text from images using OCR (Tesseract), enhances the image with a ResNet model for better clarity, and translates the extracted text using the `mistralai/mistral-7b-instruct:free` model from OpenRouter.

---

## 📦 Requirements

Install the dependencies in a Google Colab notebook or your local environment:

```bash
!pip install gradio opencv-python-headless pytesseract torch torchvision requests python-dotenv
````

---

## 🔑 API Key Setup

You need an OpenRouter API key.

1. Go to [OpenRouter](https://openrouter.ai) and log in.
2. Generate an API key.
3. Store the key in an environment variable:

```python
import os
os.environ["OPENROUTER_API_KEY"] = "your_openrouter_api_key_here"
```

---

## 🧠 Pipeline Breakdown

### 1. Image Preprocessing

* Grayscale conversion
* Thresholding using Otsu's method
* Denoising using OpenCV

### 2. ResNet Enhancement

* Uses pretrained `resnet18` from `torchvision`
* Normalizes and resizes the image to feed into ResNet
* Extracts features (for future use, e.g., semantic enhancements)

### 3. OCR Extraction

* Uses Tesseract to extract text from the preprocessed image.

### 4. Translation

* Translates extracted text using OpenRouter’s API with the `mistralai/mistral-7b-instruct:free` model.

---

## 🚀 Running the App

Just run the notebook cells or use `gradio` to launch the UI:

```python
if __name__ == "__main__":
    demo.launch()
```

---

## 📁 File Structure

```
OCR_Translation/
│
├── ocr_translation_resnet_openrouter.ipynb
---

## 📌 Notes

* Make sure Tesseract is installed and available (Colab already has it).

```

---
