# TuneBuddy

**Song recommendations from an artist and a track name, with Spotify posters.**

![Python](https://img.shields.io/badge/python-3.x-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/app-Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

TuneBuddy is a lightweight Python song recommender. Enter a song and it suggests similar ones, ranked with **TF-IDF vectorization** and **cosine similarity**, and shows each song's poster fetched from the **Spotify API**.


## Features

- Recommends songs from an artist and song name
- Ranks candidates with TF-IDF vectors and cosine similarity
- Shows song posters fetched from Spotify
- Simple Streamlit interface, small and easy to set up

## How it works

1. Song text data is converted into **TF-IDF** vectors, which weight terms that are distinctive for a song.
2. **Cosine similarity** measures how close each song's vector is to the one you entered.
3. The closest songs are returned as recommendations, and `spotify_poster.py` fetches a poster for each from Spotify.

## Quick start

```bash
git clone https://github.com/JamshaidBasit01/TuneBuddy.git
cd TuneBuddy

python -m venv venv
source venv/bin/activate      # Linux / macOS
venv\Scripts\activate         # Windows

pip install -r requirements.txt
```

### Add your Spotify credentials

The poster feature needs a free Spotify developer app:

1. Go to the [Spotify for Developers dashboard](https://developer.spotify.com/dashboard) and create an app.
2. Copy its **Client ID** and **Client Secret**.
3. Create a file named `.env` in the project folder:

```env
client_id=YOUR_SPOTIFY_CLIENT_ID
client_secret=YOUR_SPOTIFY_CLIENT_SECRET
```

Keep `.env` private: it is listed in `.gitignore`, so it is never committed.

### Run

```bash
streamlit run main.py
```

Then enter a song name to get recommendations.

## Project structure

```text
TuneBuddy/
  main.py             Streamlit app and the recommendation logic
  spotify_poster.py   Fetches song posters from the Spotify API
  requirements.txt    Python dependencies
  d3.png              Demo screenshot
  LICENSE             MIT License
```

## Tech

Python, Streamlit, TF-IDF, cosine similarity, Spotify API


## License

MIT, see [LICENSE](LICENSE).

---

[GitHub](https://github.com/JamshaidBasit01) · [LinkedIn](https://www.linkedin.com/in/jamshaid-basit-227b35219/)
