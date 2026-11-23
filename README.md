# GroupDNA-WhatsApp-Analyzer
# GroupDNA: WhatsApp Group Chat Analyzer

**GroupDNA** is a Python data analytics project that parses raw WhatsApp `.txt` chat exports and generates a visual report of group dynamics, activity rhythms, vocabulary, and member personality archetypes.

## Key Features
- **Custom Edge-Case Parser:** Reads raw chat logs line-by-line, separating timestamps, senders, and messages while filtering out system alerts, `<Media omitted>` entries, deleted messages, and blank lines.
- **Group Overview & Peak Activity:** Calculates message volume per member, percentage shares, busiest single date, and busiest hourly window using `datetime`.
- **NumPy Activity Heatmap:** Builds a `6 × 24` matrix tracking hourly activity per member and renders a text-art heatmap using block shading (`░`, `▒`, `█`).
- **Vocabulary & Behavioral Metrics:** Extracts top 10 group words (after lowercasing, punctuation stripping, and stopword removal), conversation starters after 4+ hour silences, average reply speeds, and longest silent streaks.
- **Personality Archetype Engine:** Assigns quantitative roles (*The Spammer, The Group Mom, The Night Owl, The Storyteller, The Drama Queen, The Ghost*).

## Technical Constraints
Built strictly using **Python fundamentals and NumPy** (`strings`, `lists`, `dicts`, `sets`, `tuples`, `loops`, `datetime`, and `numpy` arrays). High-level shortcut libraries (`pandas`, `matplotlib`, `re`, `collections.Counter`) were intentionally prohibited.

## How to Run
1. Open the `.ipynb` notebook in **Google Colab** or **Jupyter Notebook**.
2. Upload `hostel_bois.txt` to the session directory (`/content/hostel_bois.txt`).
3. Run all cells from top to bottom to generate the full report.
