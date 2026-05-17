# 📈 LSTM Stock Predictor

> A stock price forecasting web app powered by an LSTM neural network,
> built with Flask and TensorFlow that runs entirely on Google Colab.

Experimenting with Google Colab as a full-stack development environment,
where the entire UI (HTML, CSS, JS) is served directly from a Python notebook
via Flask and exposed publicly using ngrok — no local setup required.

<img src="https://github.com/John-Da/LSTM-Stock-Predictor-Using-Flask-Ngrok-In-Collab/blob/main/demo.png" alt="demo image" />

---

## ⚠️ Notice
*UI scripts (HTML, CSS, JS) are embedded directly inside the `.ipynb` notebook cells
and may not render correctly when viewed on GitHub.
Downloading the file and opening it locally or in Google Colab is recommended.*

---

## Features
- Predicts stock prices for the next 7, 14, or 30 days
- Uses LSTM (Long Short-Term Memory) neural network
- Interactive chart showing historical vs predicted prices
- Day-by-day forecast breakdown
- Supports any valid stock ticker (AAPL, TSLA, NVDA, etc.)

---

## Tech Stack
| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript, Chart.js |
| Backend | Python, Flask |
| Machine Learning | TensorFlow, Keras, LSTM |
| Data | yfinance (Yahoo Finance) |
| Deployment | Google Colab + ngrok |

---

## Project Structure
```
LSTM-Stock-Predictor/
├── templates/
│   └── index.html        # Frontend UI
├── static/
│   ├── style.css         # Dark theme styling
│   └── app.js            # Chart + API logic
├── LSTM_Stock_Predictor.ipynb   # Main Colab notebook
└── .gitignore
```

---

## Getting Started

### Run in Google Colab
1. Open the notebook in Google Colab
2. Mount your Google Drive
3. Add your ngrok token to `NGROK_TOKEN.txt`
4. Run all cells
5. Open the public ngrok URL
Then you will see the web page in a new tab. That's it.

### Requirements
```bash
!pip3 install -q pyngrok flask flask-bootstrap yfinance numpy pandas scikit-learn tensorflow
```

### For Ngrok, put the token to token.txt (or can change the name/variables later)
```bash
NGROK_TOKEN = "YOUR TOKEN FOR NGROK DASHBOARD"
```

---

## How It Works
1. Fetches 2 years of historical stock data from Yahoo Finance
2. Normalizes and prepares data using a 60-day lookback window
3. Trains an LSTM model on 80% of the data
4. Predicts future prices using a sliding window approach
5. Returns predictions to the frontend as JSON

---

## Disclaimer
> This project is for **educational purposes only**.
> Stock predictions are not financial advice.
> LSTM models cannot reliably predict real market movements.

---

## License
MIT
