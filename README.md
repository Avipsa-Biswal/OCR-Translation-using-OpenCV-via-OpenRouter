### 📘 OCR + Translation using OpenCV (via OpenRouter: GPT-4o & Mistral)

This project demonstrates a complete pipeline for **Optical Character Recognition (OCR)** and **Translation** of text from images. It uses **OpenCV** and **Tesseract** for OCR, and leverages the **OpenRouter API** to access large language models from **OpenAI (GPT-4o)** and **Mistral (Mixtral)**. The user interface is built with **Gradio**.

---

## 🔧 Features

* 📸 Upload or capture an image
* 🧹 Preprocess image using **OpenCV**
* 🧠 Extract text using **Tesseract OCR**
* 🌐 Translate extracted text using **OpenRouter API**:

  * `openai/gpt-4o` for high-quality translation
  * `mistralai/mixtral-8x7b-instruct` for free-tier translation
* 🖼️ Display everything via an interactive **Gradio** UI

---

## 🧪 Dependencies

Install all required libraries:

```bash
pip install opencv-python pytesseract gradio pillow requests torchvision openai python-dotenv
```

Also install **Tesseract OCR**:

* Ubuntu: `sudo apt install tesseract-ocr`
* Windows: [Download here](https://tesseract-ocr.github.io/)

---

## 🧠 Workflow

1. **Image Preprocessing**: Resize, denoise, and optionally enhance the image.
2. **OCR**: Extract text using **Tesseract**.
3. **Translation**:

   * If you have OpenRouter credits: use `openai/gpt-4o`.
   * If not: fall back to free models like `mistralai/mixtral-8x7b-instruct`.
4. **Display**: Show original image, detected text, and translated output in the UI.

---

## 📁 Project Structure

```
OCR_+_Translation_using_OpenCV(via_OpenRouter_OpenAI_Client).ipynb
OCR_+_Translation_using_OpenCV(via_OpenRouter).ipynb
README.md
```

---

## 🔑 API Setup

You only need your **OpenRouter API key** to use this app.
No OpenAI key is required. You can use all supported models directly via OpenRouter.

---

## 🔁 Supported Models via OpenRouter

| Model                             | Description                       | Requires OpenAI Key | Requires OpenRouter Key | Free?               |
| --------------------------------- | --------------------------------- | ------------------- | ----------------------- | ------------------- |
| `openai/gpt-4o`                   | GPT-4 Omni (latest ChatGPT model) | ❌ No                | ✅ Yes                   | ⚠️ Requires credits(can be used directly upto a certain amount) |
| `mistralai/mixtral-8x7b-instruct` | Open-weight, high-quality LLM     | ❌ No                | ✅ Yes                   | ✅ Free              |

---

## ✅ Example Use Cases

* Translate handwritten classroom notes
* OCR + translate signs, menus, forms
* Aid multilingual understanding of documents

---

##  How to Run

Run the Jupyter Notebook:

```bash
OCR_+_Translation_using_OpenCV(via_OpenRouter_OpenAI_Client).ipynb
```
