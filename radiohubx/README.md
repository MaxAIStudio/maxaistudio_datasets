# RadioHubX Dataset (Public)

This folder hosts public dataset bundles used by RadioHubX.

## Bundles

- `stations_lite.db.gz`: smaller bundle for default app startup (Top-N filtered)
- `stations_lite_all.db.gz`: larger full bundle (more stations)

## Metadata files

- `latest.json`: metadata for `stations_lite.db.gz`
- `latest_all.json`: metadata for `stations_lite_all.db.gz`

Each metadata file contains:

- `version`: dataset version label (date-based)
- `updated_at_utc`: UTC timestamp when metadata was generated
- `file`: target dataset filename
- `sha256`: SHA-256 checksum of that dataset file
- `size`: file size in bytes
- `source`: upstream data source

## Raw URLs

- `https://raw.githubusercontent.com/MaxAIStudio/maxaistudio_datasets/main/radiohubx/stations_lite.db.gz`
- `https://raw.githubusercontent.com/MaxAIStudio/maxaistudio_datasets/main/radiohubx/latest.json`
- `https://raw.githubusercontent.com/MaxAIStudio/maxaistudio_datasets/main/radiohubx/stations_lite_all.db.gz`
- `https://raw.githubusercontent.com/MaxAIStudio/maxaistudio_datasets/main/radiohubx/latest_all.json`

## Recommended app strategy

- Default mode: check `latest.json`, download/use `stations_lite.db.gz`
- More-stations mode: check `latest_all.json`, download/use `stations_lite_all.db.gz`
- Validate file integrity with `sha256` before replacing local DB

## Data source

- Radio Browser: `https://www.radio-browser.info/`

## Notes

- For station logo display, dataset should include `favicon`.
- For playback reliability, dataset should include `url_resolved` and `url`.
