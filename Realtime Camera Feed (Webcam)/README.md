```python
import streamlit as st

st.title("📷 Webcam Capture")

picture = st.camera_input("Take a picture")

if picture:
    st.image(picture, caption="Captured Image", use_container_width=True)
```