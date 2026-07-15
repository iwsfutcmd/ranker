# 🥇🥈🥉 ranker

Paste a list of items (one per line), answer head-to-head questions, get a
full ranking. A single HTML file with no dependencies.

**Use it:** https://iwsfutcmd.github.io/ranker/

## How it works

- Uses interleaved merge sort, so a ranking of *n* items takes at most
  ~*n*·log₂(*n*) questions — within ~10% of the information-theoretic minimum.
  Assumes preferences are transitive with no ties.
- Questions are drawn from a randomly chosen in-progress merge, and sides are
  randomized, so consecutive questions rarely repeat items.
- Progress auto-saves to `localStorage`; a 💾▶ button appears on the start
  page if there's a session to resume.
- 📤 exports progress as plain text: newline-delimited items, with `---`
  lines separating groups that are already ranked. Paste an export back into
  the start page to resume from it (or to add new items below a `---` under a
  finished ranking).
- ↩ undoes any answer, all the way back to the first question.
- Keyboard: ← / → pick the left/right item, Backspace undoes.
- The UI is Unicode symbols only (English hints live in hover tooltips).

## License

MIT
