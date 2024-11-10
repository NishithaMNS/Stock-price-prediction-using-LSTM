# Stock Price Prediction using LSTM

This is a web application built using **Flask** and **Keras** to predict stock prices using the **LSTM (Long Short-Term Memory)** deep learning model. The model is trained on historical stock price data to predict future stock prices, and the application visualizes the results through interactive **Plotly** charts.

### Features
- **Upload CSV**: Upload a CSV file containing historical stock price data.
- **LSTM Model**: The app uses an LSTM model to predict future stock prices.
- **Visualization**: Interactive plots to visualize the stock prices, training/validation loss, and prediction errors.
- **Regression Metrics**: Calculates and displays regression metrics like MSE, RMSE, MAE, R², and more.

---

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Regression Metrics](#regression-metrics)
- [Contributing](#contributing)
---

## Installation

### 1. Clone the Repository
First, clone this repository to your local machine.

```bash
git clone https://github.com/your-username/stock-price-prediction-lstm.git
cd stock-price-prediction-lstm
```

### 2. Set Up a Virtual Environment (Optional but recommended)
It is recommended to set up a virtual environment to manage dependencies.

```bash
python -m venv venv
```

### 3. Activate the Virtual Environment
For **Windows**:

```bash
venv\Scripts\activate
```

For **macOS/Linux**:

```bash
source venv/bin/activate
```

### 4. Install Dependencies
Install the required dependencies by running:

```bash
pip install -r requirements.txt
```

**requirements.txt** includes:
- Flask
- Keras
- TensorFlow
- scikit-learn
- pandas
- numpy
- Plotly
- matplotlib
- pyttsx3 (for speech-to-text functionality)
---

## Usage

### 1. Run the Application
To start the application, use the following command:

```bash
python app.py
```

The Flask server will start, and you can access the app at `http://127.0.0.1:5000/` in your web browser.

### 2. Upload CSV File
Upload a CSV file containing historical stock data (with columns such as `Date` and `Open` price). The application will process the data and predict future stock prices.

### 3. Interactive Graphs and Metrics
After the model processes the data, you will be presented with several interactive plots that display:
- Raw stock prices vs. predicted prices.
- Loss curves for training and validation.
- Distribution of prediction errors.

Regression metrics like **MSE**, **RMSE**, **MAE**, **R²**, and **EVS** are displayed to assess the model's performance.

### 4. Predict Future Prices
The app predicts the stock price for the next day based on the trained LSTM model.

---

## File Structure

```
stock-price-prediction-lstm/
│
├── app.py                # Main Flask app file
├── templates/
│   ├── index.html        # Homepage for uploading CSV
│   └── results.html      # Results page with charts and metrics
├── static/
│   └── styles.css        # Custom CSS styles (if any)
└── README.md             # Project documentation
```

---

## Regression Metrics

The model evaluates its performance using several key regression metrics:
- **Mean Squared Error (MSE)**: Measures the average squared difference between predicted and actual values.
- **Root Mean Squared Error (RMSE)**: The square root of the MSE, providing the error in the same units as the target variable.
- **Mean Absolute Error (MAE)**: The average of the absolute differences between predicted and actual values.
- **R² Score**: A measure of how well the model explains the variance in the data (ranges from 0 to 1, where 1 is perfect).
- **Explained Variance Score (EVS)**: Measures the proportion of variance explained by the model.
- **Median Absolute Error (MedAE)**: The median of absolute differences between predicted and actual values.

---

## Contributing

1. Fork this repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Create a pull request.

---
