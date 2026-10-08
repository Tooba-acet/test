# Cyber Escape Room

An information security escape room for ACET Solutions, led by Tooba (Security Awareness Training Lead).

- Full game: `index.html` (about 15–20 minutes)
- Tester: `test/index.html` (three easy questions)

Players open the link, enter their name and email, and play. No sign-in is needed.

## Where scores go

GitHub Pages only hosts the pages. Each finished game is sent to a Power Automate flow, which adds a row to the **Scores** table in `Cyber Escape Room Scores.xlsx` in OneDrive. The flow returns the rows, without email addresses, so the game can show the leaderboard.

The flow URL is set in `index.html` and `test/index.html` on the line:

    const SCORES_API = "PASTE_FLOW_URL_HERE";

Requires a Power Automate Premium licence (the "When an HTTP request is received" trigger is a Premium connector).
