import streamlit as st
from datetime import datetime, date
from prayer_times import PrayerTimes
import base64

# إعداد الموقع
location = {"latitude": 36.75, "longitude": 3.06, "timezone": +1}
pt = PrayerTimes(location)
today = date.today()
prayer_times = pt.get_times(today)

# إعداد الصفحة
st.set_page_config(page_title="تطبيق الأذان", layout="centered")

# خلفية
def set_bg(image_file):
    with open(image_file, "rb") as image:
        encoded = base64.b64encode(image.read()).decode()
    page_bg = f"""
    <style>
    .stApp {{
        background-image: url("data:image/jpg;base64,{encoded}");
        background-size: cover;
        background-repeat: no-repeat;
        background-attachment: fixed;
    }}
    </style>
    """
    st.markdown(page_bg, unsafe_allow_html=True)

set_bg("background.jpg")

st.markdown("<h1 style='text-align: center; color: white;'>🕌 مواقيت الصلاة - الجزائر</h1>", unsafe_allow_html=True)

# أوقات الصلاة
for name, t in prayer_times.items():
    st.markdown(f"<h4 style='color:white;'>{name.capitalize()}: {t.strftime('%H:%M')}</h4>", unsafe_allow_html=True)

# تشغيل صوت الأذان
st.markdown("---")
st.markdown("### 🔊 تشغيل الأذان:")

audio_file = open("athan.mp3", "rb")
audio_bytes = audio_file.read()
st.audio(audio_bytes, format='audio/mp3')

# الصلاة القادمة
now = datetime.now().time()
next_prayer = None
for name, t in prayer_times.items():
    if now < t:
        next_prayer = (name, t)
        break

if next_prayer:
    name, t = next_prayer
    st.markdown(f"<h3 style='color:yellow;'>🕰️ الصلاة القادمة: {name.capitalize()} في {t.strftime('%H:%M')}</h3>", unsafe_allow_html=True)
else:
    st.markdown(f"<h3 style='color:yellow;'>🕰️ الصلاة القادمة: Fajr في {prayer_times['Fajr'].strftime('%H:%M')} (غدًا)</h3>", unsafe_allow_html=True)
