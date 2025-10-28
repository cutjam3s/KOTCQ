# Session Notes - Knight of the Cursed Queen

Date: 2025-10-28

## What we changed today
- KOTCQ.html
  - Safer storage load with normalization to avoid corrupt localStorage crashes
  - One-time listener guard + null-safe bindings
  - Better a11y for errors: role=alert, assertive live region

- KOTCQ-cursed-queen.html (new)
  - Implemented cursed state via external Set so chess.js moves don’t drop it
  - Restored board colors; pieces ignore pointer events for reliable clicking
  - Post-move queen rule: any queen that captured becomes cursed knight (incl. promotions)
  - Guards when the game is over (no new selections/moves)
  - Responsive board sizing with CSS var; keyboard support (Enter/Space) and ARIA labels

## How to run
- Open KOTCQ-cursed-queen.html locally or via GitHub Pages:
  - https://<username>.github.io/<repo>/KOTCQ-cursed-queen.html

## Ideas for tomorrow
- Add Reset/New Game and a "Restart as Cursed Knights" control
- Visual check indicator (king highlight) and move history panel
- Option to toggle variant rules on/off at runtime
- Shareable game state (FEN in URL) and simple mobile UI polish
- Light test harness for rule transitions and edge cases
