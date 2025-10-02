# 🎓 Student Grade Predictor

A **web-based application** that predicts the grade of a student based on their **Math**, **Reading**, and **Writing** scores. The predicted grade is displayed in a **color-coded card**, making it easy to visualize. This project is built using **Python**, **Flask**, and **scikit-learn**.

---

## 📝 Features

- **Grade Prediction**: Predicts grades (A, B, C, D, F) using Random Forest Classifier.
- **Color-coded Output**: Each grade is shown in a colored card (A → Green, F → Dark Red).
- **User-friendly Interface**: Simple HTML/CSS interface for input and results.
- **Reproducible ML Model**: Model saved with `joblib` and includes label encoder for grade mapping.

---
## 🗂 Folder Structure
StudentGradePredictor/
│
├── Models/
│ ├── student_grade_model_labelenc.pkl # Random Forest model with encoded grades
│ ├── student_grade_model.pkl # Random Forest model (optional)
│ └── label_encoder.pkl # Label encoder for grades
│
├── templates/
│ └── index.html # Main HTML page
│
├── static/
│ └── style.css # CSS styling for form & cards
│
├── app.py # Flask application
├── requirements.txt # Python dependencies
└── README.md # Project documentation

1. Technologies Used
- Python 3.x
- Flask
- scikit-learn
- pandas
- numpy
- joblib
- HTML, CSS


 **Installation Instructions:**
1. **Clone the repository:**
   ```bash```
   git init
   git clone <your-repo-link>

3. **Navigate to the project folder:**
    cd StudentGradePredictor

4. **Create and activate a virtual environment:**
    python -m venv venv
    # Windows
    venv\Scripts\activate
    
    # macOS/Linux
    source venv/bin/activate
5.  **Install dependencies:**
    pip install -r requirements.txt

3. **How to Run**  
1. Make sure the Models folder contains:
   - `student_grade_model_labelenc.pkl`
   - `label_encoder.pkl`
   - `student_grade_model.pkl` (optional)

2. **Start the Flask server:**
   ```bash```
   python app.py

3. **Open your browser and go to:**
   http://127.0.0.1:5000/
4. Enter Math, Reading, and Writing marks, then click "Predict Grade".
    
4. **How It Works (Brief Explanation)**  
- The Random Forest model is trained on sample student scores and corresponding grades.
- Grades are encoded using `LabelEncoder` to convert A, B, C, D, F into numbers for model training.
- When a user inputs new marks, the model predicts the encoded grade.
- The LabelEncoder converts the numeric prediction back to the letter grade.
- The result is displayed in a color-coded card on the webpage.




**Author / Contact**
**Author**: Bhoomika.V
**Email:** bhoomikav618@gmail.com




