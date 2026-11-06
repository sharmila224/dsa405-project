# Data sources
- backblaze_extract.csv — One daily snapshot from Backblaze Drive Stats, Q1 2026,
  reduced to columns: date, serial_number, model, capacity_bytes, failure,
  smart_5_raw, smart_187_raw, smart_188_raw, smart_197_raw, smart_198_raw.
  Downloaded from https://www.backblaze.com/cloud-storage/resources/hard-drive-test-data
  on 2026-09-30. Extract derived once, then never modified.

## Source 2: Wikipedia drive specifications
- Articles: en.wikipedia.org/wiki/Seagate_Technology, /Seagate_Barracuda, /Western_Digital,
  /Ultrastar, /HGST, /Toshiba
- Access: requests + BeautifulSoup, honest User-Agent, 1 req/sec, cached to data/raw/wiki_*.html
- Collected: November 2026
- License: CC BY-SA (Wikipedia); attribution given
