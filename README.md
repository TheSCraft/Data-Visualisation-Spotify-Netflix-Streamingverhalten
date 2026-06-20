# Saisonale Stimmungsmuster im Spotify- und Netflix-Streamingverhalten

Dieses Projekt untersucht saisonale Muster im Streamingverhalten anhand von Spotify- und Netflix-Daten.  
Dabei wird analysiert, ob sich Musik- und Film-/Serienkonsum je nach Jahreszeit verändern und ob bestimmte Stimmungen, Genres oder Streaming-Volumina saisonale Trends zeigen.

## Projektidee

Die zentrale Fragestellung lautet:

**Gibt es saisonale Stimmungsmuster im Streamingverhalten von Spotify- und Netflix-Nutzern?**

Dazu werden unter anderem folgende Aspekte betrachtet:

- Entwicklung von Spotify-Merkmalen wie `valence`, `energy`, `danceability` und `acousticness`
- Vergleich von Sommer- und Wintermonaten
- Analyse von Netflix-Top-10-Daten über mehrere Jahre
- Visualisierung von Trends und saisonalen Unterschieden

## Repository-Struktur

```text
Data-Visualisation-Spotify-Netflix-Streamingverhalten/
│
├── Saisonale_Stimmungsmuster_im_Streaming.ipynb
├── Konzept.ipynb
│
├── Datensätze/
│   ├── all-weeks-global.xlsx
│   ├── netflix_movies_detailed_up_to_2025.xlsx
│   ├── netflix_tv_shows_detailed_up_to_2025.xlsx
│   ├── final.csv                  # muss manuell heruntergeladen werden
│   └── Spotify_Dataset_V3.csv      # muss manuell heruntergeladen werden
│
└── README.md
```


## Tutorial: Fehlende Spotify-Datensätze herunterladen

Da einige Spotify-Datensätze zu groß für GitHub sind, werden sie nicht direkt im Repository gespeichert.  
Damit das Notebook vollständig funktioniert, müssen diese Dateien manuell von Kaggle heruntergeladen und in den Ordner `Datensätze/` gelegt werden.

Das Notebook erwartet später folgende Dateien:

```text
Datensätze/final.csv
Datensätze/Spotify_Dataset_V3.csv
```

---

### 1. Benötigte Datensätze

Die fehlenden Spotify-Datensätze befinden sich auf Kaggle:

- [Top 200 Spotify Songs Dataset](https://www.kaggle.com/datasets/brunoalarcon123/top-200-spotify-songs-dataset)
- [Spotify 200 Dataset](https://www.kaggle.com/datasets/yelexa/spotify200/data)

---

### 2. Datensätze manuell herunterladen

1. Öffne den ersten Kaggle-Link:

   [Top 200 Spotify Songs Dataset](https://www.kaggle.com/datasets/brunoalarcon123/top-200-spotify-songs-dataset)

2. Klicke auf **Download**.

3. Entpacke die heruntergeladene ZIP-Datei.

4. Suche die benötigte CSV-Datei.

5. Lege sie in den Ordner:

   ```text
   Datensätze/
   ```

6. Benenne die Datei so um, falls sie anders heißt:

   ```text
   final.csv
   ```

---

7. Öffne danach den zweiten Kaggle-Link:

   [Spotify 200 Dataset](https://www.kaggle.com/datasets/yelexa/spotify200/data)

8. Lade auch diesen Datensatz herunter.

9. Entpacke die ZIP-Datei.

10. Lege die benötigte CSV-Datei ebenfalls in den Ordner:

   ```text
   Datensätze/
   ```

11. Benenne die Datei bei Bedarf so um:

   ```text
   Spotify_Dataset_V3.csv
   ```

---

### 3. Richtige Ordnerstruktur prüfen

Nach dem Herunterladen sollte der Ordner `Datensätze/` ungefähr so aussehen:

```text
Datensätze/
├── all-weeks-global.xlsx
├── netflix_movies_detailed_up_to_2025.xlsx
├── netflix_tv_shows_detailed_up_to_2025.xlsx
├── final.csv
└── Spotify_Dataset_V3.csv
```

Wichtig ist vor allem, dass diese beiden Dateien vorhanden sind:

```text
Datensätze/final.csv
Datensätze/Spotify_Dataset_V3.csv
```

Wenn eine der beiden Dateien fehlt oder anders heißt, kann das Notebook nicht vollständig ausgeführt werden.

---

### 4. Alternative: Download über die Kaggle API

Falls die Kaggle API eingerichtet ist, können die Datensätze auch direkt über das Terminal heruntergeladen werden.

Zuerst muss die Kaggle API installiert werden:

```bash
pip install kaggle
```

Danach können die Datensätze heruntergeladen werden:

```bash
kaggle datasets download -d brunoalarcon123/top-200-spotify-songs-dataset -p Datensätze --unzip
kaggle datasets download -d yelexa/spotify200 -p Datensätze --unzip
```

Anschließend muss geprüft werden, ob die Dateien korrekt heißen:

```text
Datensätze/final.csv
Datensätze/Spotify_Dataset_V3.csv
```

Falls die Dateien anders benannt wurden, müssen sie entsprechend umbenannt werden.

---

### 5. Notebook ausführen

Wenn alle Datensätze vorhanden sind, kann das Hauptnotebook geöffnet und ausgeführt werden:

```text
Saisonale_Stimmungsmuster_im_Streaming.ipynb
```

Das Notebook lädt die Daten aus dem Ordner `Datensätze/`, bereitet sie auf und erstellt anschließend die Visualisierungen zur Analyse saisonaler Streamingmuster.

