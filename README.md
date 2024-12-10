# 2010s to 2020s Billboard Hot 100 Songs Trend Analysis


## Overview

This project looks at the Spotify audio features and lyrics of the songs *Billboard Hot 100* year end charts from the years of 2010 to 2023. 

Audio features are analyzed for trends using STL decomposition, vector autoregressive models, and Granger Causality tests.

Lyrics were processed through an TF-IDF vectorizer and used Latent Semantic Analysis with K-means to extract major themes from songs for each year.

This project was inspired by the critiques received by Katy Perry's album *143* on how it sounded like an attempt to rehash her 2010s success. This prompted the question: what exactly defines the 2010s sound? And how has popular music changed since?

A full report breaking down all aspects of the project and findings can be found [here](report/songs_analysis_report.pdf).

## Data Source 
The song names, artists, and year are collected through using the [`billboard.py API`](https://github.com/guoguo12/billboard-charts?tab=readme-ov-file).

Since Spotify API has rolled back their audio features access, the following three Kaggle datasets were used to compile the audio features and lyrics for the songs obtained.

- [🎹960K Spotify Songs With Lyrics data🎵](https://www.kaggle.com/datasets/bwandowando/spotify-songs-with-attributes-and-lyrics/data)
- [Billboard Hot weekly charts](https://www.kaggle.com/datasets/thedevastator/billboard-hot-100-audio-features)
- [Billboard Hot-100[2000-2023] data with features](https://www.kaggle.com/datasets/suparnabiswas/billboard-hot-1002000-2023-data-with-features)

Any missing lyrics were then further collected using [`lyricgenius`](https://lyricsgenius.readthedocs.io/en/master/) with the Genius API.

All data collection, merging, cleaning, and major preprocessing is carried out in [`data_collection.ipynb`](data/data_collection.ipynb).

## Code and Packages Used

In addition to above, the project is carried out in Python (ver 3.10) set up via Jupyter Notebooks with the following packages used:
- `pandas`
- `numpy`
- `statsmodel`
- `scikit`
- `matplotlib`

All libraries and modules used are listed in the first cell for every `ipynb` file. 


