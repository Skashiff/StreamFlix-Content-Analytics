# StreamFlix Data Dictionary

## subscribers

| Column | Meaning |
|---|---|
| subscriber_id | Unique subscriber key |
| signup_date | Subscription signup date |
| country | Subscriber country |
| region | Subscriber region |
| age | Subscriber age |
| gender | Female / Male / Non-binary / Undisclosed |
| plan_type | Basic with Ads / Standard / Premium |
| monthly_price_usd | Monthly subscription price in USD |
| household_size | Household size |
| primary_device | Subscriber's primary device |
| payment_method | Payment method |
| tenure_months | Tenure as of 1 June 2026 |
| is_active | Current active-status flag |
| churn_date | Churn date; blank when active |

## titles

| Column | Meaning |
|---|---|
| title_id | Unique title key |
| title_name | Title name |
| type | Movie / TV Show |
| primary_genre | Primary genre |
| country | Content origin country |
| language | Primary language |
| release_year | Release year |
| date_added | Date added to StreamFlix |
| maturity_rating | Content maturity rating |
| seasons | Number of seasons; 0 for movies |
| content_duration_min | Content duration in minutes |
| is_original | StreamFlix Original flag |
| license_type | Original / Exclusive License / Non-Exclusive License / Co-Production |
| director | Director |
| cast | Cast |
| quality_score | Quality score, 0–100 |
| popularity_score | Source popularity score |
| license_cost_usd | Licence/content investment cost in USD |
| license_expiry | Licence expiry date; blank for Originals |
| total_watch_hours | Catalogue-level watch hours |
| total_plays | Catalogue-level total plays |

## watch_history

| Column | Meaning |
|---|---|
| watch_id | Unique viewing-session key |
| subscriber_id | Subscriber foreign key |
| title_id | Title foreign key |
| watch_date | Viewing date |
| device | Device used for the session |
| region | Session region |
| content_duration_min | Content duration in minutes |
| watch_duration_min | Minutes watched |
| completion_pct | Percentage of content watched |
| completed | Completion flag |

## ratings

| Column | Meaning |
|---|---|
| rating_id | Unique rating key |
| subscriber_id | Subscriber foreign key |
| title_id | Title foreign key |
| rating | Rating from 1 to 5 |
| rating_date | Rating date |

## reviews

| Column | Meaning |
|---|---|
| review_id | Unique review key |
| subscriber_id | Subscriber foreign key |
| title_id | Title foreign key |
| review_text | Review text |
| sentiment | Positive / Neutral / Negative |
| helpful_votes | Helpful-vote count |
| review_date | Review date |

## watchlist

| Column | Meaning |
|---|---|
| watchlist_id | Unique watchlist-event key |
| subscriber_id | Subscriber foreign key |
| title_id | Title foreign key |
| added_date | Date title was saved |
| watched | Whether the saved title was later watched |
