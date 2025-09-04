```python
import streamlit as st
from PIL import Image, ImageOps

st.title("Image Upload & Processing 🖼️")

uploaded_file = st.file_uploader("Upload an image", type=["jpg", "png", "jpeg"])

if uploaded_file:
    img = Image.open(uploaded_file)
    st.image(img, caption="Original", use_container_width=True)

    if st.button("Convert to Grayscale"):
        gray = ImageOps.grayscale(img)
        st.image(gray, caption="Grayscale", use_container_width=True)

```