# GroupDNA — WhatsApp Group Chat Analyzer

**"Spotify Wrapped, but for your friend group."**  
A Python behavioural analytics and text-mining tool built for The Unlox Academy Week 1 Minor Project that decodes raw WhatsApp `.txt` chat exports into a terminal-style personality and activity report—using **only Python fundamentals, `datetime`, and `NumPy`**.

## Output Report (`hostel_bois.txt`)

![GroupDNA Report](Screenshot%202026-11-24%20233002.png)

## Features Built
1. **WhatsApp Chat Parser:** Reads raw `.txt` exports line by line and handles 5 real-world edge cases without regex—empty lines, multi-line continuations, system notifications, `<Media omitted>` stubs, and deleted messages.
2. **Group Overview & Per-Person Stats:** Calculates total messages, date range, duration in days, ranked per-person message counts/percentages, and average words per message.
3. **Most Active Day & Hour:** Identifies the single busiest calendar day and the peak messaging hour across the chat period.
4. **NumPy Activity Heatmap:** Builds a `(participants × 24)` NumPy matrix of hourly activity and renders a 4-level block-character heatmap (`.`, `░`, `▒`, `█`).
5. **Top Words & Vocabulary:** Normalizes text to lowercase, strips punctuation, removes common stop words, and plots horizontal bar charts for the group's Top 10 words plus Top 5 words per person.
6. **Response Speed & Silent Streaks:** Uses `datetime` arithmetic to find fastest/slowest average reply times and each member's longest consecutive silent streak.
7. **Personality Archetype Engine:** Scores every participant across 8 core archetypes (`The Spammer`, `The Group Mom`, `The Night Owl`, `The Storyteller`, `The Drama Queen`, `The Ghost`, `The Comedian`, `The Question Master`) plus a custom 9th archetype (`The Early Bird`) with exclusive assignment and tie-breaking.
8. **Formatted Terminal Report:** Combines all analytics into one aligned, screenshot-ready console report.

## Technical Constraints Followed
- **Used:** Core Python (strings, lists, dicts, sets, tuples, loops, conditionals, functions, f-strings, `sorted()`), `open()`, `datetime` (`strptime`, `timedelta`), and `NumPy`.
- **Forbidden & Avoided:** `pandas`, `matplotlib`/`seaborn`/`plotly`, `collections.Counter`, `collections.defaultdict`, `re` (regex), and any pre-built WhatsApp or ML library.

## How to Run
1. Open `GroupDNA_ParthSharma_PARTH1939160.ipynb` in Google Colab or Jupyter Notebook.
2. Place `hostel_bois.txt` in the same folder (or upload it to `/content/` in Google Colab).
3. Run all cells from top to bottom (`Runtime -> Run all`).
