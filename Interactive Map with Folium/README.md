```
pip install folium
```

```
pip install streamlit_folium
```

```python
import streamlit as st
import folium
from streamlit_folium import st_folium

st.title("Interactive Map 🌍")

m = folium.Map(location=[20.5937, 78.9629], zoom_start=5)

folium.Marker([28.6139, 77.2090], popup="Delhi").add_to(m)
folium.Marker([19.0760, 72.8777], popup="Mumbai").add_to(m)

st_data = st_folium(m, width=700, height=500)
```
