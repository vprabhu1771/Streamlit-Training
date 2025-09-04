```python
import streamlit as st
import yfinance as yf
import datetime

st.title("📈 Stock Price Viewer")

ticker = st.text_input("Enter stock ticker (e.g. AAPL, TSLA):", "AAPL")
start = st.date_input("Start date", datetime.date(2022, 1, 1))
end = st.date_input("End date", datetime.date.today())

if st.button("Get Data"):
    data = yf.download(ticker, start, end)
    st.line_chart(data["Close"])
    st.dataframe(data.tail())
```