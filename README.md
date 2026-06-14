🐾 Dog vs Cat Image Classification using SVM

Python Streamlit Scikit-Learn License

A Machine Learning web application that classifies images as either a Dog 🐶 or Cat 🐱 using a Support Vector Machine (SVM). Built with Python, Streamlit, and Scikit-learn, this project demonstrates image preprocessing, machine learning model training, evaluation, and deployment through an interactive dashboard.

✨ Features
Feature	Description
🧠 SVM Classifier	RBF-kernel SVM with probability calibration
⚙️ Image Preprocessing	Grayscale conversion, 64×64 resizing, normalization
🔍 Live Prediction	Upload an image and get instant classification
📊 Interactive Dashboard	User-friendly Streamlit interface
📈 Evaluation Metrics	Accuracy, Precision, Recall, F1-Score
📉 Visualizations	Confusion Matrix and performance charts
💾 Model Persistence	Save and load trained models using Pickle
⬇️ Export Support	Download model and metrics report
📂 Project Structure
Dog_Cat_Classification/
│
├── app.py
├── train_model.py
├── model.pkl
├── metrics.json
├── requirements.txt
├── README.md
│
├── dataset/
│   ├── cats/
│   └── dogs/
│
├── images/
└── assets/
🚀 Getting Started
1️⃣ Clone the Repository
git clone https://github.com/yourusername/dog-cat-classification.git
cd dog-cat-classification
2️⃣ Create Virtual Environment
python -m venv venv
Windows
venv\Scripts\activate
Linux / macOS
source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Add Dataset
Place cat and dog images inside:

dataset/
├── cats/
└── dogs/
Dataset Source:

https://www.kaggle.com/c/dogs-vs-cats/data

5️⃣ Train the Model
python train_model.py
Generated files:

model.pkl
metrics.json
6️⃣ Run the Application
streamlit run app.py
Open:

http://localhost:8501
🔬 Machine Learning Pipeline
Raw Image
    ↓
Grayscale Conversion
    ↓
Resize (64×64)
    ↓
Flatten
    ↓
StandardScaler
    ↓
SVM Classifier
    ↓
Prediction
🧠 Support Vector Machine (SVM)
The model uses an RBF (Radial Basis Function) Kernel to classify images.

Hyperparameters
SVC(
    kernel="rbf",
    C=10,
    gamma="scale",
    probability=True
)
Why SVM?
Effective for binary classification
Works well with high-dimensional data
Generates robust decision boundaries
Provides confidence scores through probability calibration
🖼️ Image Preprocessing
Steps Performed
Read image using OpenCV
Convert RGB image to Grayscale
Resize image to 64×64
Flatten into 4096-dimensional vector
Normalize using StandardScaler
Feed into trained SVM model
📊 Technologies Used
Technology	Purpose
Python	Core Programming Language
Streamlit	Web Application
Scikit-Learn	Machine Learning
OpenCV	Image Processing
NumPy	Numerical Computation
Pandas	Data Handling
Matplotlib	Visualization
Seaborn	Heatmaps & Charts
Pillow	Image Loading
📈 Expected Performance
Dataset Size	Accuracy
200 Images/Class	~68%
500 Images/Class	~74%
1000 Images/Class	~80%
Performance improves as training data increases.

🚀 Future Improvements
CNN-Based Classification
Transfer Learning (ResNet50, VGG16)
HOG Feature Extraction
Hyperparameter Tuning
Real-Time Webcam Prediction
Docker Deployment
FastAPI Integration
MLflow Model Tracking
📜 License
This project is licensed under the MIT License.

🙌 Acknowledgements
Kaggle Dogs vs Cats Dataset
Scikit-Learn Documentation
Streamlit Community
OpenCV Documentation
