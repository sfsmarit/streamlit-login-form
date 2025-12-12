# streamlit-login-form

## Usage
Edit config.yaml and add users into usernames section;
```yaml
cookie:
    expiry_days: 1
    key: some_signature_key
    name: some_cookie_name
credentials:
    usernames:
        david:
            name: david
            password: admin
```
> Password will be hashed automatically when you run the app.

Place login form in your app;
```python
# main.py
import streamlit as st
from login_form import login

if not login():
    st.stop()
```

Run your app;
```bash
streamlit run main.py
```