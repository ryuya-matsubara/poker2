# POKER ROOM 40BB

6-max No-Limit Texas Hold'em browser app for GitHub Pages.

Live site: https://ryuya-matsubara.github.io/poker2/

- Starting stack: 40BB
- SB 0.5BB / BB 1BB / BB ante 1BB
- Preflop action abstraction: unopened `Fold / Limp 1BB / Open to 2.5BB / All-in`; facing 2.5BB `Fold / Call / Raise to 7.5BB / All-in`; facing 7.5BB `Fold / Call / All-in`; facing all-in `Fold / Call`.
- Multiway pots, side pots, ties and postflop play are supported.
- 1BB = ¥1,000 for display, matching the original `poker` app.

## Preflop strategy data

The app uses the public `MTT_40_GTO.json` range set from [`jensbaagaard/poker-practice`](https://github.com/jensbaagaard/poker-practice). That project documents the range data as MIT/free to use.

The public dataset is 6-max MTT, 40BB, ante 1BB with mixed frequencies. Its native sizing profile is **2.3BB open (SB 3.5BB), 3-bet 3x IP / 4x OOP, 4-bet all-in**. This app intentionally enforces the requested **2.5BB open / 7.5BB raise** abstraction, so the imported frequencies are the closest public 40BB/ante reference, not an exact Nash equilibrium for this altered sizing tree.

Multiway/unsupported histories and postflop decisions use fallback heuristics and are not claimed to be GTO.

Source data:
- https://github.com/jensbaagaard/poker-practice/blob/main/data/openSourcePokerData/MTT_40_GTO.json
- https://github.com/jensbaagaard/poker-practice/blob/main/data/openSourcePokerData/README.md
