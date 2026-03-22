# RadioHubX Dataset (Public)

This folder hosts the public dataset files used by the RadioHubX app.

## Files

- `stations_lite.db.gz`: compressed SQLite dataset for app download
- `latest.json`: dataset metadata (version, checksum, file size)

## Raw URLs

- `https://raw.githubusercontent.com/MaxAIStudio/maxaistudio_datasets/main/radiohubx/stations_lite.db.gz`
- `https://raw.githubusercontent.com/MaxAIStudio/maxaistudio_datasets/main/radiohubx/latest.json`

## latest.json fields

- `version`: dataset version label (date-based)
- `updated_at_utc`: UTC timestamp when metadata was generated
- `file`: dataset filename
- `sha256`: SHA-256 checksum of `stations_lite.db.gz`
- `size`: file size in bytes
- `source`: upstream data source

## Data source

- Radio Browser: `https://www.radio-browser.info/`

## Notes

- The app should download `latest.json` first, then compare version/checksum.
- For logo display in app station list, ensure dataset includes `favicon` field.
- For playback reliability, ensure dataset includes `url_resolved` and `url`.
