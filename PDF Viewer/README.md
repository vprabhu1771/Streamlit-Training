```python
import streamlit as st

st.title("📄 PDF Viewer")

pdf_file = st.file_uploader("Upload a PDF", type=["pdf"])

if pdf_file:
    st.download_button("Download PDF", pdf_file, file_name="uploaded.pdf")
    st.write("Preview:")
    st.pdf(pdf_file)
```