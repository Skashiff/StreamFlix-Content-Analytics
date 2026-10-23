# Data

The StreamFlix source and cleaned CSV files are intentionally **not committed** to this public portfolio repository.

The project analyses **979,000 records across six interconnected tables**:

| Dataset | Rows | Purpose |
|---|---:|---|
| subscribers | 15,000 | Subscriber profile, plan, geography, tenure and churn status |
| titles | 9,000 | Catalogue metadata, genre, format, Originals/licensing and cost |
| watch_history | 650,000 | Viewing sessions, watch duration and completion |
| ratings | 130,000 | 1–5 star title ratings |
| reviews | 110,000 | Review text and sentiment |
| watchlist | 65,000 | Saved titles and watched conversion |

## Expected local structure

```text
data/
├── raw/
│   ├── subscribers.csv
│   ├── titles.csv
│   ├── watch_history.csv
│   ├── ratings.csv
│   ├── reviews.csv
│   └── watchlist.csv
└── cleaned/
    ├── subscribers_clean.csv
    ├── titles_clean.csv
    ├── watch_history_clean.csv
    ├── ratings_clean.csv
    ├── reviews_clean.csv
    └── watchlist_clean.csv
```

The Phase 1 notebook treats raw files as read-only, validates quality, and exports cleaned copies for downstream analysis.
