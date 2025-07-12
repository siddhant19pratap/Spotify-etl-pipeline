# 🎧 Spotify Data Engineering Pipeline

This project is an end-to-end **data pipeline** that extracts playlist data from the **Spotify API**, processes it using Python, and stores structured datasets in **AWS S3**. It leverages `Spotipy`, `pandas`, and `AWS Lambda` for a lightweight, serverless solution.

---

## 📌 Features

- Extracts track, album, and artist metadata from Spotify playlists
- Cleans and transforms the data using Pandas
- Stores output in S3 as CSV files (songs, albums, artists)
- Modular Python scripts for `extract`, `transform`, `load`
- AWS Lambda-compatible — with Zip packaging and layer support

---

## ⚙️ Tech Stack

- **Language**: Python 3.x  
- **Libraries**: [Spotipy](https://spotipy.readthedocs.io/), Pandas  
- **Cloud**: AWS Lambda, AWS S3  
- **Other**: IAM Roles, Serverless Packaging, Jupyter (for local testing)

---

## 📁 Project Structure

```
spotify-etl-pipeline/
├── spotify_api_data_extract.py              # Extraction logic using Spotipy
├── spotify_transformation_load_function.py  # Cleans and uploads data to S3
├── Spotify Data Pipeline Project.ipynb      # End-to-end pipeline demonstration
├── spotipy_layer/                           # Custom Spotipy layer (zipped for Lambda)
└── README.md
```

---

## 🧪 Sample Output

Each run generates the following CSV files:

- `spotify_songs.csv`
- `spotify_albums.csv`
- `spotify_artists.csv`

Stored in S3 with timestamped folders like:  
`spotify-pipeline-output/YYYY-MM-DD/`

---

## 🚀 How to Run

### ✅ Local Setup

1. Clone the repo  
   ```bash
   git clone https://github.com/siddhant19pratap/spotify-etl-pipeline.git
   ```

2. Install dependencies  
   ```bash
   pip install spotipy pandas boto3
   ```

3. Run notebook or `spotify_api_data_extract.py` to test extraction

---

## ☁️ AWS Lambda Deployment

1. Zip `spotipy_layer` and upload as Lambda layer  
2. Deploy main transformation function using the AWS Console  
3. Add your Spotify and AWS credentials in environment variables or securely via Secrets Manager

---

## 🔐 Requirements

- Spotify Developer Account + API Key
- AWS Account with Lambda and S3 access
- Proper IAM Role attached to Lambda

---

## 📊 Example Use Case

Ideal for anyone looking to build **data engineering portfolios** or **Spotify listening dashboards**, or automate ingestion of audio metadata.

---

## 📬 Author

Made with 💚 by [Siddhant Pratap Singh](https://github.com/siddhant19pratap)

---

## 📜 License

This project is open-source and available under the MIT License.
