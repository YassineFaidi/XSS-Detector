# 🛡️ XSS Detector - Deep Learning Approach

Welcome to the **XSS Detector** project!  
This repository provides a deep learning-based solution for detecting Cross-Site Scripting (XSS) payloads in input data.

---

## 📂 Project Structure

```
XSSDetector/
├── XSS_dataset.csv          # Dataset containing (id, sentence, label)
├── tokenizer.pickle         # Tokenizer used to preprocess input text
├── xss_detector_model.h5    # Trained deep learning model (BiLSTM)
├── train_xss_detector.ipynb # Jupyter Notebook to train the model
├── test_xss_detector.ipynb  # Jupyter Notebook to test the model
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/YassineFaidi/XSS-Detector.git
cd XSSDetector
```

### 2. Install Requirements

This project uses **TensorFlow**, **scikit-learn**, and **NumPy**.  
Install the necessary libraries using:

```bash
pip install tensorflow scikit-learn numpy
```

(You can also open the `.ipynb` files directly in **Google Colab**.)

---

## 🛠️ How to Train

- Open the `train_xss_detector.ipynb` notebook.
- Run all the cells to:
  - Load and preprocess the dataset.
  - Build and train a BiLSTM-based deep learning model.
  - Save the trained model and tokenizer.

The model will be saved as `xss_detector_model.h5` and the tokenizer as `tokenizer.pickle`.

---

## 🔍 How to Test

- Open the `test_xss_detector.ipynb` notebook.
- Run the cells to:
  - Load the saved model and tokenizer.
  - Predict whether input sentences are **safe** or **contain XSS attacks**.

You can test predefined examples or enter your own custom input sentences!

---

## 📊 Dataset Description

The dataset (`XSS_dataset.csv`) consists of three columns:
- `id`: unique identifier for each sample
- `sentence`: the input string (could be safe HTML or malicious XSS)
- `label`: 
  - `0` → Safe
  - `1` → XSS Attack

Example rows:

| id | sentence | label |
|----|----------|-------|
| 0 | `<li><a href="/wiki/File:Socrates.png"...` | 0 |
| 1 | `<tt onmouseover="alert(1)">test</tt>` | 1 |
| 2 | `</span> <span class="reference-text">...` | 0 |

---

## ✨ Future Improvements
- Fine-tune using pre-trained models like **BERT**.
- Extend dataset with more advanced or obfuscated XSS payloads.
- Deploy the model into a real-time web firewall system.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Contributing

Pull requests are welcome!  
If you find a bug or have suggestions, please open an issue first.

---

## 💬 Contact

For any questions, feel free to reach out via [email@example.com]!

---