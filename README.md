# ✈️ Flight Fare Prediction

A machine learning project that predicts domestic flight ticket prices based on factors like airline, route, departure time, number of stops, and journey date.

---

## 📌 Problem Statement

Flight prices vary significantly based on booking time, airline, route, and travel duration. This project builds a regression model to predict flight fares using historical data, helping travellers make cost-effective booking decisions.

---

## 📁 Repository Structure

```
Flight-Fare-Prediction/
│
├── Flight Price Final.ipynb   # Main notebook: EDA, feature engineering, model training
├── Data_Train.xlsx            # Training dataset
├── Test_set.xlsx              # Test dataset
├── Flight_Fare.csv            # Processed/exported fare data
└── README.md
```

---

## 📊 Dataset

The dataset includes the following features:

| Feature          | Description                                      |
|------------------|--------------------------------------------------|
| `Airline`        | Name of the airline                              |
| `Date_of_Journey`| Date of the flight                               |
| `Source`         | Departure city                                   |
| `Destination`    | Arrival city                                     |
| `Route`          | Flight route (via stops)                         |
| `Dep_Time`       | Departure time                                   |
| `Arrival_Time`   | Arrival time                                     |
| `Duration`       | Total flight duration                            |
| `Total_Stops`    | Number of stops (non-stop, 1 stop, etc.)        |
| `Additional_Info`| Extra details (meals, baggage, etc.)            |
| `Price`          | **Target variable** — ticket price in INR        |

---

## 🔧 Workflow

**1. Data Preprocessing**
- Handled missing values
- Parsed datetime columns (`Date_of_Journey`, `Dep_Time`, `Arrival_Time`, `Duration`) into numeric features (day, month, hour, minute)
- Dropped irrelevant columns post-extraction

**2. Exploratory Data Analysis (EDA)**
- Distribution of prices across airlines and routes
- Impact of stops and journey duration on fare
- Correlation heatmaps and feature distributions

**3. Feature Engineering**
- Extracted `Journey_Day`, `Journey_Month`, `Dep_Hour`, `Dep_Min`, `Arrival_Hour`, `Arrival_Min`, `Duration_Hours`, `Duration_Mins`
- Applied Label Encoding and One-Hot Encoding to categorical variables

**4. Model Training**
- Train-test split applied on the training dataset
- Model(s) trained: `[e.g., Random Forest Regressor, XGBoost — fill in based on your notebook]`
- Hyperparameter tuning: `[e.g., RandomizedSearchCV / GridSearchCV — fill in if used]`

**5. Model Evaluation**

| Metric | Score |
|--------|-------|
| R² Score | `[fill in]` |
| MAE | `[fill in]` |
| RMSE | `[fill in]` |

> ⚠️ **Note:** Replace the placeholders above with your actual results from the notebook.

---

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Environment:** Jupyter Notebook
- **Libraries:**
  - `pandas`, `numpy` — data manipulation
  - `matplotlib`, `seaborn` — visualization
  - `scikit-learn` — machine learning models & preprocessing

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/jagadishv2001/Flight-Fare-Prediction.git
cd Flight-Fare-Prediction
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
```

### 3. Run the notebook

```bash
jupyter notebook "Flight Price Final.ipynb"
```

---

## 📈 Results

The final model was evaluated on the test set and achieved an R² score of `[fill in]`, indicating that it explains `[X]%` of the variance in flight prices.

---

## 🔮 Future Improvements

- Add more recent flight data for better generalization
- Deploy as a web app using Flask or Streamlit
- Incorporate real-time pricing data via APIs
- Experiment with ensemble methods or neural networks for higher accuracy

---

## 👤 Author

**Jagadish V**
- GitHub: [@jagadishv2001](https://github.com/jagadishv2001)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
