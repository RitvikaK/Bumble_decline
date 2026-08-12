# 🐝 Bumble Strategic Analysis

## Why is Bumble losing users?

Bumble became one of the most recognisable dating platforms globally. However, despite its strong brand presence, user growth and revenue have weakened in recent years.

This project analyses **~49,000 user reviews and discussions** to identify the underlying drivers behind declining user satisfaction and uncover the product issues affecting retention.

The key question:

> **What are users actually unhappy about, and what can Bumble do to improve the experience?**

---

## Project Overview

This project analyses Bumble user feedback to understand the biggest challenges from the customer's perspective.

Rather than analysing sentiment alone, reviews were classified into business-relevant themes to identify:

- The biggest sources of dissatisfaction
- How user complaints changed over time
- Which product areas most affected trust and perceived value

---

## Data & Methodology

### Data Sources

The analysis combines:

- Bumble-related Reddit discussions
- Scraped app-store reviews
- Public app review datasets

### Approach

A hybrid analytics approach was used:

- Python for data collection and processing
- A manually developed classification framework to categorise user issues
- Anthropic API-assisted contextual classification for Reddit discussions
- Google Sheets pivot analysis to identify trends and relationships

User feedback was classified across:

- **Dimensions** — broad business themes
- **Category 1** — main user issue
- **Category 2** — specific pain point

For more detail, see the full [methodology](./methodology).

---

# Key Findings

## 1. Account issues eroded platform trust

Account-related problems generated the highest negative sentiment among high-volume categories.

The biggest drivers were:

- Login and verification failures
- Unjustified bans and suspensions
- Account access issues

These issues were frequently linked with poor support experiences, suggesting unresolved user friction.

---

## 2. Premium monetisation reduced perceived value

Forced subscription was the largest complaint category.

Users frequently associated monetisation with:

- Frustration
- Poor value for money
- Feeling pressured to pay

This suggests premium features were increasingly viewed as restrictions rather than meaningful improvements.

---

## 3. Match quality weakened Bumble's core proposition

Match quality became an increasingly significant source of dissatisfaction.

Key drivers included:

- No matches
- Poor quality matches
- Low-effort interactions

When users do not see meaningful outcomes, confidence in the overall platform experience declines.

---

# Results

The final strategic analysis and visualisations can be found in:

[Results](./results)

---

# Tools Used

### Programming & Data Processing
- Python
- Pandas

### AI & NLP
- Anthropic API
- Text classification techniques

### Analysis & Visualisation
- Google Sheets
- Pivot tables
- Flourish

---

# LinkedIn Project

View the full strategic analysis and presentation:

[Add LinkedIn link]

---

# Disclaimer

This project was conducted independently using publicly available user feedback data.

The analysis represents reported user experiences and sentiment, rather than internal Bumble data.
