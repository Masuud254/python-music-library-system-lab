# Music Library System

A `Song` class built in Python that models individual songs while tracking global library statistics — total song count, unique artists, unique genres, and per-genre/per-artist counts.

## Description

Each `Song` instance stores its own `name`, `artist`, and `genre`. On creation, the class automatically updates shared, class-level data:

- `count` — total number of songs created
- `genres` — list of unique genres seen so far
- `artists` — list of unique artists seen so far
- `genre_count` — dictionary mapping each genre to how many songs belong to it
- `artist_count` — dictionary mapping each artist to how many songs they have

## Installation

```bash
git clone https://github.com/Masuud254/python-music-library-system-lab.git
cd python-music-library-system-lab
pipenv install
pipenv shell
```

## Usage

```python
from song import Song

Song("99 Problems", "Jay Z", "Rap")
Song("Halo", "Beyonce", "Pop")

print(Song.count)         # 2
print(Song.genres)        # ["Rap", "Pop"]
print(Song.artist_count)  # {"Jay Z": 1, "Beyonce": 1}
```

## Running Tests

```bash
pytest lib/testing/song_test.py -v
```

All 6 tests pass.

## Authors

Masuud254

## License

See `LICENSE.md` in this repository.