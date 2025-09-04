```python
import streamlit as st

st.title("Simple Chatbot 🤖")

if "messages" not in st.session_state:
    st.session_state.messages = []

user_input = st.text_input("You:")

if st.button("Send") and user_input.strip():
    # Append user message
    st.session_state.messages.append(("You", user_input))
    # Fake response (replace with OpenAI API call)
    bot_reply = f"Echo: {user_input}"
    st.session_state.messages.append(("Bot", bot_reply))

for sender, msg in st.session_state.messages:
    st.write(f"**{sender}:** {msg}")
```