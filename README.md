# 🥗 MacroSnap — AI Nutrition Buddy

**MacroSnap** is a Streamlit-powered AI nutrition buddy built with **Google Gemini 2.5 Flash** (Chat + Vision) and **Twilio WhatsApp API**.

Users can onboard with their name and WhatsApp number, chat with the AI nutrition buddy by typing questions or uploading meal photos to get instant calorie and macro estimates, and send a complete daily summary directly to their WhatsApp phone.

---

## 🌟 Features

- **Multi-Modal Meal Tracking:** Ask text questions or attach meal photos (`.jpg`, `.jpeg`, `.png`) for instant Gemini vision-based calorie and macro decoding.
- **AI Persona & Safety:** Guided nutrition buddy persona powered by Gemini system instructions to keep conversation focused strictly on food, meals, and fitness.
- **WhatsApp Integration:** One-click instant summary sent to WhatsApp via Twilio Content Template Messaging API.
- **Session State Management:** Connection-cached Gemini and Twilio client sessions for reliable real-time chatting.

---

## 🛠️ Built With

- [Python 3.9+](https://www.python.org/)
- [Streamlit](https://streamlit.io/)
- [Google GenAI SDK (`google-genai`)](https://github.com/google-gemini/deprecations)
- [Twilio Python SDK](https://www.twilio.com/docs/libraries/python)

---

## 🚀 Quick Start (Local Setup)

### 1. Clone the repository
```bash
git clone https://github.com/tarunk8060/macrosnap.git
cd macrosnap
```

### 2. Create and activate a virtual environment
```bash
# Windows
py -m venv venv
.\venv\Scripts\Activate.ps1

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure API Keys & Secrets
Copy `.streamlit/secrets.toml.example` to `.streamlit/secrets.toml`:

```bash
cp .streamlit/secrets.toml.example .streamlit/secrets.toml
```

Fill in your actual keys in `.streamlit/secrets.toml`:
```toml
GEMINI_API_KEY = "your-gemini-api-key"
TWILIO_ACCOUNT_SID = "your-twilio-account-sid"
TWILIO_AUTH_TOKEN = "your-twilio-auth-token"
TWILIO_WHATSAPP_FROM = "whatsapp:+14155238886"
TWILIO_CONTENT_SID = "your-content-template-sid"
```

### 5. Run the application
```bash
streamlit run app.py
```

---

## ☁️ Deployment on Streamlit Community Cloud

1. Push this project to GitHub.
2. Go to [share.streamlit.io](https://share.streamlit.io/) and log in with GitHub.
3. Click **New app**, select repository `tarunk8060/macrosnap`, branch `main`, and main file `app.py`.
4. In **Settings → Secrets**, paste the contents of your `.streamlit/secrets.toml`.
5. Click **Deploy**!
