# 🎬 Movie Recommender System

This is a **Content-Based Movie Recommendation System** built using Python, Pandas, Scikit-learn, and Streamlit (or Flask) for the web interface. It suggests similar movies based on user-selected titles using cosine similarity on feature vectors.

---

## 📌 Features

- Suggests top similar movies based on a selected movie
- Uses TMDb 5000 Movies Dataset
- Pre-computed similarity matrix for fast recommendations
- Web interface for easy access
- Deployment-ready structure (Heroku/Render-compatible)

---

## 📁 Project Structure

movies-recommender-system/
│
├── app.py # Main app file (Streamlit or Flask)
├── movies.pkl # Movie metadata
├── movies_dict.pkl # Dictionary format of movie metadata
├── similarity.pkl # Precomputed similarity matrix (very large)
├── requirements.txt # Dependencies list
├── Procfile # For Heroku deployment
├── setup.sh # Deployment setup script
├── .gitignore # Ignore unnecessary files
└── README.md # This file



---

## 🧠 How it Works

1. **Data Preprocessing:** Loaded and cleaned TMDb data.
2. **Feature Extraction:** Combined genres, keywords, cast, and crew into a single text field.
3. **Vectorization:** Used `CountVectorizer` to convert text into vectors.
4. **Similarity Computation:** Used cosine similarity to compute similarity scores.
5. **Recommendation Logic:** Sorted and returned top 5–10 similar movies based on scores.

---

## 🚀 Deployment

You can deploy this app on platforms like:

- [Heroku](https://www.heroku.com/)
- [Render](https://render.com/)
- [Streamlit Cloud](https://streamlit.io/cloud)

Make sure to include:
- `requirements.txt`
- `Procfile` (for Heroku)
- `setup.sh` (optional)

---

## ⚠️ Note on Large Files

The `similarity.pkl` file is **over 100 MB**, which exceeds GitHub's upload limit.

To use it:

1. Download it from this link (replace with your own hosted link):  
   👉 [Download similarity.pkl](https://drive.google.com/drive/folders/10o4-ZXzSK1_lSCaadch4AayIvj2DLPCp?usp=drive_link)

2. Place it in the project directory before running `app.py`.

Alternatively, you can use **Git LFS** to track large files.

---

## 🛠 Installation & Running Locally

```bash
# Clone the repo
git clone https://github.com/yourusername/movies-recommender-system.git
cd movies-recommender-system

# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py

