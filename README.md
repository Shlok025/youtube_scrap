# YouTube Music Data Scraper

## Overview
The **YouTube Music Data Scraper** is a Python-based project designed to extract and analyze data from popular **YouTube music channels** such as **T-Series, Times Music, Zee Music Company, and Sony Music India**. It fetches key video details, including views, likes, comments, and engagement metrics, which can be further processed for insights.

## Features

### **Scraping Capabilities**
- **Fetch Video Metadata:** Extracts video titles, upload dates, views, likes, and comments.
- **Channel Statistics:** Retrieves subscriber count, total channel views, and video uploads.
- **Data Cleaning:** Removes duplicates and emojis from video titles for better readability.
- **CSV Export:** Saves the cleaned data into a structured CSV file (`Cleaned_Music_Channel.csv`).

### **Data Processing**
- **Deduplication:** Ensures that duplicate entries in video titles are removed.
- **Emoji Removal:** Cleans the dataset by eliminating unnecessary symbols.
- **Formatted Output:** Stores structured data for further analysis or visualization.

## **Data Cleaning Process**
To ensure high-quality data, the following cleaning steps are applied:
1. **Remove Emojis:** Uses regex to filter out emojis from the `Title` column.
2. **Drop Duplicates:** Ensures that duplicate video titles are removed.
3. **Standardize Text Format:** Converts titles to a uniform format.
4. **Handle Missing Values:** Checks for and processes missing data fields.
5. **Validate Data Types:** Ensures numerical columns (views, likes, comments) have correct data types.
6. **Save Cleaned Data:** Exports the final processed dataset to `csv/Cleaned_Music_Channel.csv`.

## **Data Details**
The extracted data is saved in `Cleaned_Music_Channel.csv`, containing the following key columns:

- **Channel Name:** Name of the YouTube music channel.
- **Title:** Song title (processed for duplicates and emojis).
- **Date Released:** The release date of the song.
- **Views:** Total number of views per song.
- **Likes:** Number of likes received per song.
- **Comments:** Number of comments per song.

## **Requirements**
To run this scraper, ensure the following:
- **Python 3.x** installed on your system.
- Install required dependencies using:
  ```sh
  pip install google-api-python-client pandas numpy
  ```
- **YouTube API Key:** Obtain a valid API key from [Google Cloud Console](https://console.cloud.google.com/) and store it in an `.env` file.

## **Setup Instructions**
1. Clone this repository:
   ```sh
   git clone https://github.com/your-username/YT-Music-Scraper.git
   ```
2. Navigate to the project directory:
   ```sh
   cd youtube_scrap
   ```
3. Add your YouTube API key in a `.env` file:
   ```sh
   YOUTUBE_API_KEY=your_api_key_here
   ```
4. Run the scraper:
   ```sh
   python multipleScrapper.py
   ```
5. Processed data will be saved in `csv/Cleaned_Music_Channel.csv`.
6. Data cleaning, including duplicate removal and emoji filtering, is applied before final export.

## **Usage**
This scraper is useful for:
- **Data Analysts:** Extracting insights from YouTube music video performance.
- **Content Creators:** Understanding audience engagement trends.
- **Music Industry Professionals:** Monitoring the popularity of songs across different channels.

## **Power BI Dashboard**
In addition to data scraping, I have created a **YouTube Music Channel Analysis Dashboard** using **Power BI**, located in the `powerbi` folder. This dashboard provides interactive visualizations for analyzing YouTube music channel performance.

## **Contribution**
Contributions are welcome! If you have suggestions for improvement or encounter any issues, feel free to open an issue or submit a pull request.

## **License**
This project is licensed under the **MIT License**.

