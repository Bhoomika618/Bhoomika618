## Student Grade Predictor

Predict a student's final letter grade — A, B, C, D, E, or F — from their Math, Reading, and Writing scores using a Random Forest Classifier. This Flask web app takes the three marks as input and displays the predicted grade in a color-coded result card.

---

## Folder Structure

```text
Student Grade Predictor/
├── Models/
│   ├── random_forest_model.pkl          # Trained RandomForestClassifier (example filename)
│   └── label_encoder.pkl                # Fitted LabelEncoder for grades A–F (example filename)
├── static/
│   └── style.css                        # App styles (color-coded result card)
├── templates/
│   └── index.html                       # Main template (form + result card)
├── app.py                               # Flask application
├── requirements.txt                     # Python dependencies
└── README.md                            # This file
```

---

## Features

- **Grade prediction (A–F)**: Predicts a letter grade from three numeric inputs: Math, Reading, Writing.
- **Color-coded result card**: Displays the predicted grade in a visually distinct colored card for quick recognition.
- **Lightweight web UI**: Simple form-based interface with instant server-side prediction.
- **Production-friendly model loading**: Uses serialized `.pkl` artifacts for fast startup.

---

## Technologies Used

- **Backend**: Flask (Python)
- **ML**: scikit-learn (RandomForestClassifier), LabelEncoder
- **Utilities**: joblib or pickle for model serialization, numpy/pandas (commonly used for training)
- **Frontend**: HTML (Jinja2 templates), CSS

---

## Installation

Prerequisites:
- **Python 3.8+** and **pip** installed

1) Clone the repository and change directory:

```bash
git clone <your-repo-url>.git
cd student-grade-predictor
```

2) Create and activate a virtual environment (Linux/macOS):

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

3) Install dependencies:

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

## Running the App Locally

Option A — run via Python:

```bash
python app.py
```

Option B — run via Flask CLI:

```bash
export FLASK_APP=app.py        # set on Linux/macOS
# setx FLASK_APP app.py        # on Windows (PowerShell)
flask run --host 0.0.0.0 --port 5000
```

The app will be available at `http://127.0.0.1:5000/` (or your configured host/port).

---

## Usage

1) Open the app in a browser.
2) Enter **Math**, **Reading**, and **Writing** marks (typically 0–100).
3) Submit the form to get a predicted letter grade.
4) The **result card** will show the predicted grade with a distinctive color.

---

## How It Works

- **Model**: A `RandomForestClassifier` is trained to map numeric scores (Math, Reading, Writing) to a letter grade. During training, the target labels (A–F) are encoded into integers using scikit-learn's `LabelEncoder`.
- **Serialization**: The trained classifier and the fitted `LabelEncoder` are saved to `.pkl` files (e.g., `random_forest_model.pkl`, `label_encoder.pkl`).
- **Inference**: On form submission, the app reads the three inputs, constructs a feature vector, and calls `model.predict(...)`. The predicted integer label is then converted back to its original letter grade with `label_encoder.inverse_transform(...)`.
- **UI**: The resulting grade is rendered in a color-coded card to make the outcome easily scannable at a glance.

---

## Notes / Important Information

- **Required files in `Models/`**:
  - A trained Random Forest model saved as a `.pkl` file (example: `random_forest_model.pkl`).
  - A fitted `LabelEncoder` saved as a `.pkl` file (example: `label_encoder.pkl`).
- **Filenames must match your `app.py`**: If your artifact names differ, update the corresponding load paths in `app.py`.
- **Version compatibility**: Pickled models are sensitive to library versions. Ensure the scikit-learn version used at inference is compatible with the version used during training.
- **Input validation**: The UI expects numeric scores. If you add stricter validation (e.g., 0–100 bounds), ensure both client and server validate consistently.

---

## Author

Your Name

# 💫 About Me:
I'm a student


## 🌐 Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/https://www.linkedin.com/in/bhoomika-v-6194a0352/) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:bhoomikav618@gmail.com) 

# 💻 Tech Stack:
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=flat-square&logo=css3&logoColor=white) ![C](https://img.shields.io/badge/c-%2300599C.svg?style=flat-square&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=flat-square&logo=c%2B%2B&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=flat-square&logo=openjdk&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=flat-square&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=flat-square&logo=javascript&logoColor=%23F7DF1E) ![Python](https://img.shields.io/badge/python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=flat-square&logo=php&logoColor=white) ![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=flat-square&logo=firebase) ![React](https://img.shields.io/badge/react-%2320232a.svg?style=flat-square&logo=react&logoColor=%2361DAFB) ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=flat-square&logo=mysql&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=flat-square&logo=Matplotlib&logoColor=black) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=flat-square&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat-square&logo=pandas&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat-square&logo=scikit-learn&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=flat-square&logo=github&logoColor=white)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Bhoomika618&theme=vue-dark&hide_border=false&include_all_commits=true&count_private=true)<br/>
![](https://nirzak-streak-stats.vercel.app/?user=Bhoomika618&theme=vue-dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Bhoomika618&theme=vue-dark&hide_border=false&include_all_commits=true&count_private=true&layout=compact)

---
[![](https://visitcount.itsvg.in/api?id=Bhoomika618&icon=0&color=0)](https://visitcount.itsvg.in)

