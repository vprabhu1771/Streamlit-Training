```python
import streamlit as st
from transformers import pipeline

st.title("Sentiment Analyzer 📝")

classifier = pipeline("sentiment-analysis")

text = st.text_area("Enter text here:")

if st.button("Analyze"):
    if text.strip():
        result = classifier(text)[0]
        st.write(f"**Label:** {result['label']}")
        st.write(f"**Score:** {result['score']:.2f}")
```