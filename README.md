# SMS Spam Detection

This project implements a machine learning model to classify SMS messages as either spam or ham (non-spam). It uses a Naive Bayes classifier trained on real-world SMS data and includes a Streamlit web app for user interaction.

---

## Features

- Classifies SMS messages into spam or ham
- Uses TF-IDF vectorization and Multinomial Naive Bayes
- Supports CSV file upload and batch predictions
- Web interface built with Streamlit
- Downloadable results with predictions

---

## Project Structure

```
├── app.py                     # Streamlit web app
├── sms_model.py              # Model training script
├── spam_model.pkl            # Trained model (saved using joblib)
├── vectorizer.pkl            # TF-IDF vectorizer
├── sms_sample.csv            # Sample input file
├── sms_sample_larger.csv     # Larger test file (20 rows)
└── README.md                 # Project documentation
```

---

## Technologies Used

- Python 3
- Pandas
- Scikit-learn
- Joblib
- Streamlit

---

## How to Run

### Local Environment

1. Clone the repository:
   ```
   git clone https://github.com/your-username/sms-spam-detection.git
   cd sms-spam-detection
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Train the model:
   ```
   python sms_model.py
   ```

4. Run the web app:
   ```
   streamlit run app.py
   ```

---

### Google Colab (Optional)

1. Upload all files to Colab (including `app.py`, `sms_model.py`, and dataset).
2. Install required packages:
   ```python
   !pip install streamlit pyngrok joblib
   ```

3. Run the app using ngrok:
   ```python
   from pyngrok import ngrok
   get_ipython().system_raw('streamlit run app.py &')
   print(ngrok.connect(8501))
   ```

---

## Input Format

Upload a CSV file containing a column named `message`, like this:

```csv
message
Congratulations! You've won a prize
Hey, how are you?
Your loan is approved. Call now.
```

---

## Output Format

The result will include:

- The original message
- A label indicating whether it's Spam or Ham

You can download the result as a CSV from the app.

---

## License

This project is released for educational and non-commercial use only.

---

## Author

Submitted as part of a Machine Learning Internship Project.
