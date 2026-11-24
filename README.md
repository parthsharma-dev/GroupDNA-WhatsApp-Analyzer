# GroupDNA — WhatsApp Group Chat Analyzer

**"Spotify Wrapped, but for your friend group."**  
A Python behavioural analytics and text-mining tool built for The Unlox Academy Week 1 Minor Project that decodes raw WhatsApp `.txt` chat exports into a terminal-style personality and activity report—using **only Python fundamentals, `datetime`, and `NumPy`**.

## Sample Output (`hostel_bois.txt`)
![GroupDNA Report](groupdna_report.png)

## Features Built
1. **Robust WhatsApp Chat Parser:** Handles 5 real-world export edge cases without regex—empty lines, multi-line message continuations, system notifications, `<Media omitted>` stubs, and deleted messages.
2. **Group Overview & Per-Person Stats:** Computes total messages, date span, ranked member activity percentages, and average words per message.
3. **Peak Activity Detection:** Identifies the single busiest calendar date and peak messaging hour across the chat period.
4. **NumPy Activity Heatmap:** Builds a `(participants × 24)` NumPy matrix of hourly activity and renders a 4-level block-character heatmap (`.`, `░`, `▒`, `█`).
5. **Vocabulary & Top Words:** Normalizes text, strips punctuation, filters stop words, and renders horizontal bar charts for the group's Top 10 words plus Top 5 words per member.
6. **Response Speed & Silent Streaks:** Uses `datetime` arithmetic to find the fastest/slowest repliers and each member's longest consecutive silent streak.
7. **Personality Archetype Engine:** Evaluates 8 core archetypes (`The Spammer`, `The Group Mom`, `The Night Owl`, `The Storyteller`, `The Drama Queen`, `The Ghost`, `The Comedian`, `The Question Master`) plus a custom 9th archetype (`The Early Bird`) with exclusive assignment and tie-breaking.
8. **Formatted Terminal Report:** Combines all analytics into a clean, aligned, screenshot-ready console report.

## Technical Constraints Followed
- **Used:** Core Python (strings, lists, dicts, sets, tuples, loops, conditionals, functions, f-strings), `open()`, `datetime` (`strptime`, `timedelta`), and `NumPy`.
- **Forbidden & Avoided:** `pandas`, `matplotlib`/`seaborn`/`plotly`, `collections.Counter`, `collections.defaultdict`, `re` (regex), and external WhatsApp/NLP libraries.

## How to Run
1. Clone this repository or open `GroupDNA_Parth_PARTH1939160.ipynb` in Google Colab.
2. Place `hostel_bois.txt` in the same working directory (or upload it to `/content/` in Colab).
3. Run all cells from top to bottom (`Runtime -> Run all`).
