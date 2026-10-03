# POKER ROOM 40BB

6-max No-Limit Texas Hold'em browser app for GitHub Pages.

Live site: https://ryuya-matsubara.github.io/poker2/

- Starting stack: 40BB
- SB 0.5BB / BB 1BB / BB ante 1BB
- Preflop actions match the public MTT 40BB sizing profile: unopened `Fold / Limp / Open to 2.3BB` (SB opens to 3.5BB); facing an open `Fold / Call / 3-bet` where 3-bet is 3x IP or 4x OOP, capped at 9BB IP / 10BB OOP; facing a 3-bet `Fold / Call / 4-bet all-in`; facing the all-in `Fold / Call`.
- Multiway pots, side pots, ties and postflop play are supported.
- 1BB = ¥1,000 for display, matching the original `poker` app.

## Preflop strategy data

The app uses the public `MTT_40_GTO.json` range set from [`jensbaagaard/poker-practice`](https://github.com/jensbaagaard/poker-practice). That project documents the range data as MIT/free to use.

The public dataset is 6-max MTT, 40BB, ante 1BB with mixed frequencies. The app now uses its native sizing profile: **2.3BB open (SB 3.5BB), 3-bet 3x IP / 4x OOP with 9BB/10BB caps, and 4-bet all-in**.

Multiway/unsupported histories and postflop decisions use fallback heuristics and are not claimed to be GTO.

Source data:
- https://github.com/jensbaagaard/poker-practice/blob/main/data/openSourcePokerData/MTT_40_GTO.json
- https://github.com/jensbaagaard/poker-practice/blob/main/data/openSourcePokerData/README.md
