# 📊 Project Title: *Advanced House Prices Prediction*

## 🏠 Overview

This project predicts house prices using the Ames Housing dataset, showcasing a complete machine learning workflow:

- 🧹 **Data Cleaning & Feature Engineering:** Raw data is preprocessed and transformed for optimal model performance.
- 🤖 **Model Training:** A linear regression model is trained on the engineered features. Users can also train custom regression models directly within the Streamlit app using their own data.
- 🚀 **Deployment:** The Streamlit web app provides an interactive UI for predictions, custom model training, and basic analysis of results.
- 📊 **Analysis:** The app displays key evaluation metrics (MAE, MSE) and visualizations to help interpret model performance.

The pipeline is designed for reproducibility and flexibility in advanced regression tasks.

```
├── 📂 data/                # Datasets and description
│   ├── 📄 train.csv        # Training data
│   ├── 📄 test.csv         # Test data
│   ├── 📄 new_train.csv    # Cleaned/engineered train data
│   ├── 📄 new_test.csv     # Cleaned/engineered test data
│   ├── 📄 sample_submission.csv
│   └── 📄 data_description.txt
│
├── 📂 models/              # Trained model(s) and data schemas
│   ├── 📦 linear_regression_model.pkl
│   └── 📄 schemas.py       # Pydantic schemas for input features and predictions
│
├── 📂 configs/             # App configuration, mostly for the streamlit app
│   └── ⚙️ config.py
│
├── 📂 views/               # Streamlit app logic
│   ├── 🏡 house_price.py   # Main house price prediction UI
│   └── 🛠️ custom_app.py    # Custom regression UI
│
├── 📓 data_cleaning_and_feature_engineering.ipynb   # Notebook for data cleaning & feature engineering
├── 🚀 main.py                                       # Streamlit entry point
├── 📦 requirements.txt     # Python dependencies
├── 🐳 Dockerfile           # Containerization
├── 🖥️ start.sh             # Shell script to launch app with docker
└── 📘 README.md            # This file
```

---

## 🔧 Setup and Installation Instructions
### 🅰️ Option 1: Create and activate a virtual environment

#### 🐧 Linux/macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

#### 🪟 Windows

```bat
python -m venv .venv
.\.venv\Scripts\activate
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

### 🅱️ Option 2: Run with Docker

Build and start the app using Docker:

```bash
docker build -t streamlit_app .
docker run --rm -p 8501:8501 streamlit_app
```

Or use the provided shell script:

```bash
bash start.sh
```

## 🛠️ Step-by-Step Guide

### 1️⃣ Data Cleaning & Feature Engineering
- Open and run `Data_Cleaning_and_Feature_Engineering_Final_Version.ipynb` to preprocess and engineer features from the raw data.
- Follow up to train a Linear Regression Model on this difficult case.

### 2️⃣ Train Model (if needed)
- Use scripts or notebook to train and save models in `models/` (default model provided).

### 3️⃣ Launch the Streamlit App
- Run the following command or using docker:
    ```bash
    streamlit run main.py
    ```
- Use the sidebar to select between house price prediction and custom regression modules.
- Train your own model on your own data using the custom regression module.

---

## 📊 Results

- **Predictions:** 🏡 View predicted house prices in the Streamlit app UI.
- **Model:** 🤖 The trained linear regression model is stored in `models/linear_regression_model.pkl`.
- **Data:** 🗂️ Cleaned datasets are in `data/new_train.csv` and `data/new_test.csv`.
- **Notebook:** 📓 All preprocessing and feature engineering steps are documented in the notebook.
- **Evaluation Metrics:**  
    - *📉 Mean Absolute Error (MAE):* Measures the average absolute difference between predicted and actual prices. Lower values indicate better accuracy.
    - *📈 Mean Squared Error (MSE):* Measures the average squared difference between predicted and actual prices. It penalizes larger errors more than MAE.  
        **Notebook Result:** 711,102,117.35 MSE

For more details, see comments in code and notebook sections.

## 🚀 Showcase

### 👤 Getting Started with Your GitHub Profile

1. 📦 **Create a Profile Repository:**  
    Follow the official [GitHub instructions](https://docs.github.com/en/get-started/start-your-journey/setting-up-your-profile#step-1-create-a-new-repository-for-your-profile-readme) to set up your profile README. This helps you showcase your skills and projects right on your GitHub homepage.

2. 📝 **Master Markdown:**  
    Get familiar with Markdown formatting using the [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/). You can also use Markdown extensions or even embed HTML for advanced customization.

3. 🎨 **Generate a Profile Template:**  
    Try the [GitHub Profile README Generator](https://rahuldkjain.github.io/gh-profile-readme-generator/) to quickly create a stylish profile. Be sure to select programming languages and skills you have experience with or have tried before.

> 💡 **Pro Tip:** Add emojis 🎉, badges 🏅, and custom sections 🧩 to make your profile stand out! Use LLMs 🤖 to enhance your content and showcase your skills.

### 🌟 How to Showcase Your Project on GitHub

1. 🏁 Visit [`https://github.com/{your_github_username}?tab=repositories`](https://github.com/{your_github_username}?tab=repositories) (replace `{your_github_username}` with your actual username).
2. 🟢 Click the green **New** button in the top right to start a new repository.
3. 📝 Enter a descriptive repository name and details.
4. 🗂️ In the **Add .gitignore** section, select the Python template to automatically exclude unnecessary files.
5. 💻 After creation, follow the provided instructions to clone your repository locally and 🚀 push your project files.

> 💡 **Tip:** Add a clear README and relevant tags to make your project easy to discover!
6. Now you can start creating your code.

### 💡 Tips & Tricks

- 🖼️ **Add Screenshots:** Include images or GIFs of your app in action to make your README visually appealing.
- 📚 **Document Clearly:** Use concise instructions and highlight unique features.
- 🏷️ **Use Tags:** Add relevant topics/tags to improve discoverability.
- 🔗 **Link Resources:** Reference notebooks, datasets, or external documentation for deeper insights.
- 📝 **Update Regularly:** Keep your README and project files up to date as your project evolves.