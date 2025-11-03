# Prediction-Model-for-Pakistani-Legal-Judgments-Using-Deep-Learning-Techniques
An AI-powered legal judgment prediction model trained on Pakistani criminal case data using transformer architectures (BART, T5, GPT-2, OPT-125M). It predicts potential charges, fines, and legal sections based on crime scenarios and witness statements to assist legal professionals.

### Habib University — School of Science and Engineering

**Authors:** Hussain Mustansir, Muhammad Anas, Muhammad Ansab Chaudhary, Abdul Samad, Sandesh Kumar

---

## 📘 Overview

This project presents a **deep learning–based prediction system** designed to generate potential **criminal case judgments** under Pakistani law. By training transformer models on **real legal judgments** from the Supreme Court and High Courts of Pakistan, the model predicts **legal sections, fines, and punishments** based on a given crime scenario and witness statements.

The goal is to support **lawyers, citizens, and judicial professionals** by offering AI-driven insights into legal case outcomes, promoting the digitization and efficiency of Pakistan’s judicial system.

---

## ⚖️ Research Objective

To determine whether **deep learning models can predict legal judgments** for criminal cases in Pakistan by analyzing crime scenarios, witness statements, and historical court decisions.

---

## 🧩 Methodology

### 1. **Data Collection**

* **Sources:**

  * Supreme Court, Lahore High Court, Sindh High Court, and Peshawar High Court online databases.
  * Supplementary datasets from [Kaggle](https://www.kaggle.com/datasets/shahsayesha/supreme-court-of-pakistan-judgment).
* **Dataset Size:** 1,004 verified criminal case judgments (2007–2024).
* **Tools Used for Cleaning:** BeautifulSoup, Tesseract, Pandas, and Llama3.2-8b for content extraction.

### 2. **Models Used**

| Model                 | Architecture    | Purpose                               |
| --------------------- | --------------- | ------------------------------------- |
| **BART**              | Encoder–Decoder | Best performer in judgment prediction |
| **T5-Base**           | Encoder–Decoder | High-quality text generation          |
| **DistilGPT-2**       | Decoder-only    | Lightweight baseline                  |
| **Facebook OPT-125M** | Decoder-only    | Comparison model                      |

* Implemented using **Hugging Face Transformers**
* Training monitored using **Weights & Biases (W&B)**

### 3. **Evaluation Metric**

* **ROUGE-1 Score** used to measure text similarity between generated and real judgments.
* BART achieved the **highest score (>0.40)**.

---

## 🚀 Results

* **BART and T5-Base** generated coherent and contextually relevant judgments.
* Correctly identified **Pakistan Penal Code (PPC) sections** such as *302(b)* (murder cases).
* Achieved approximately **80% prediction accuracy** for sentences and fines.
* Model training took ~1 hour per model on a **T4 GPU**.

---

## ⚙️ Installation and Usage

### Prerequisites

* Python 3.10+
* GPU (recommended)
* Hugging Face Transformers
* PyTorch
* Weights & Biases (optional)

### Setup

```bash
# Clone the repository
git clone https://github.com/ansabchaudhary/legal-judgment-prediction.git
cd legal-judgment-prediction

# Install dependencies
pip install -r requirements.txt
```

### Run Training

```bash
python train_model.py --model bart --epochs 3 --batch_size 4
```

### Generate Judgment

```bash
python predict.py --input "Mr. X was robbed by Mr. Y at gunpoint..."
```

---

## 📊 Example Output

**Input:**

> “Mr. X was robbed by Mr. Y at gunpoint. Mr. Y took Mr. X’s laptop and cash…”

**Predicted Judgment (BART):**

> “The accused is convicted under section 392 PPC for robbery and sentenced to 7 years imprisonment and a fine of Rs. 50,000.”

---

## 🔬 Limitations

* Dataset limited to 1,004 criminal cases.
* Performance may degrade on rare or complex crimes.
* Model cannot replicate human ethical or emotional judgment.

---

## 🔮 Future Work

* Expand dataset to include more diverse and rare cases.
* Incorporate **contextual metadata** (judge opinions, prior precedents).
* Explore **multilingual legal prediction** and **Llama 3.x fine-tuning** for enhanced accuracy.
* Deploy as a **web-based legal assistance tool** for Pakistan’s judicial system.

---

## 🧠 Tech Stack

* **Python**
* **Hugging Face Transformers**
* **PyTorch**
* **Weights & Biases (W&B)**
* **BeautifulSoup / Tesseract / Pandas**
* **Groq API (for experimentation)**

---

## 📚 References

* Supreme Court & High Court Online Portals
* [Pakistan Penal Code (1860)](https://www.pakistani.org/pakistan/legislation/1860/actXLVof1860.html)
* [Kaggle Judgment Dataset](https://www.kaggle.com/datasets/shahsayesha/supreme-court-of-pakistan-judgment)
* [Groq LLaMA API](https://groq.com/)
* [Weights & Biases](https://wandb.ai/)

---

## 👥 Contributors

| Name                         | Email                                                                   | Affiliation      |
| ---------------------------- | ----------------------------------------------------------------------- | ---------------- |
| Hussain Mustansir            | [hm08436@st.habib.edu.pk](mailto:hm08436@st.habib.edu.pk)               | Habib University |
| Muhammad Anas                | [ma08458@st.habib.edu.pk](mailto:ma08458@st.habib.edu.pk)               | Habib University |
| **Muhammad Ansab Chaudhary** | [mc08077@st.habib.edu.pk](mailto:mc08077@st.habib.edu.pk)               | Habib University |
| Abdul Samad                  | [abdul.samad@sse.habib.edu.pk](mailto:abdul.samad@sse.habib.edu.pk)     | Habib University |
| Sandesh Kumar                | [sandesh.kumar@sse.habib.edu.pk](mailto:sandesh.kumar@sse.habib.edu.pk) | Habib University |

---

## 🏛️ License

This project is open-source and available under the **MIT License**.

---

Would you like me to make it slightly shorter and more **GitHub-optimized** (with emojis and sections condensed), or keep it as a **formal academic-style README** like above?
