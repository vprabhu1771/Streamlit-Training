```python
import streamlit as st

st.sidebar.title("Navigation")
page = st.sidebar.radio("Go to", ["Home", "About", "Contact"])

if page == "Home":
    st.title("🏠 Home Page")
    st.write("Welcome to the Streamlit multi-page example!")

elif page == "About":
    st.title("ℹ️ About")
    st.write("This is a simple app with multiple pages using sidebar navigation.")

elif page == "Contact":
    st.title("📞 Contact")
    st.write("Email: example@example.com")
```