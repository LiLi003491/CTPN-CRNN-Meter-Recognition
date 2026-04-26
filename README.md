# Digital Meter OCR: CTPN + CRNN Implementation

This project implements a high-precision OCR system specifically designed for **industrial digital meter displays**. By combining **CTPN** for text detection and **CRNN** for character recognition, the system can accurately extract data from LED/LCD panels.

---

## 🌟 Key Features
* **Specialized Detection**: Optimized for Seven-Segment Displays and LED digital panels.
* **Robust Pipeline**: Leverages **CTPN** (Connectionist Text Proposal Network) for precise localization and **CRNN** (Convolutional Recurrent Neural Network) for sequence recognition.
* **Industrial Applicability**: High accuracy even in low-light, high-glare, or blurry industrial environments.
* **End-to-End Inference**: Automated workflow from raw image input to structured digital data output.

---

## 📊 Experimental Results
The model demonstrates excellent performance on real-world meter data, accurately identifying multi-line parameters and single-line status displays.

### Sample 1: Multi-line Meter Data
The CTPN model identifies multiple rows of digital readings, and CRNN recognizes the values with high confidence.
![Multi-line Meter](t5.jpg)

### Sample 2: Single-line Industrial Display
Precise detection and recognition of characters on industrial LED panels.
![Single-line Display](t2.jpg)

---

## 🛠 Tech Stack
* **Text Detection**: CTPN (Connectionist Text Proposal Network)
* **Text Recognition**: CRNN (CNN + Bi-LSTM + CTC Loss)
* **Image Processing**: OpenCV, NumPy
* **Deep Learning Framework**: PyTorch / TensorFlow (Please specify your framework)

---

## 🚀 Quick Start

### 1. Installation
```bash
git clone [https://github.com/YourUsername/YourRepoName.git](https://github.com/YourUsername/YourRepoName.git)
cd YourRepoName
pip install -r requirements.txt

···

## 🚀 How to Run (Inference)

Follow these steps to run the OCR recognition on your own images:

1. **Prepare your environment**: Make sure you have installed all dependencies and downloaded the pre-trained weights.
2. **Place images**: Put the meter images you want to recognize into the `test_images/` folder.
3. **Execute the script**: Run the following command in your terminal:

```bash
# Run OCR on a single image
python predict.py --input ./test_images/t5.jpg

# (Optional) If you want to save the results to a specific folder
python predict.py --input ./test_images/t2.jpg --output ./results/
